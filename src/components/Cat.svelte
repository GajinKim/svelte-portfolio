<style lang="scss">
$color-black: black;
$color-white: whitesmoke;
$size: 170px; // (Fully responsive)

// Cat
.cat {
	position: relative;
	height: $size;
	width: $size * 1.13;
}

// Ears
.ear {
	position: absolute;
	top: -30%;
	height: 60%;
	width: 25%;
	background: $color-white;
	
	// Ear hair
	&::before,
	&::after {
		content: '';
		position: absolute;
		bottom: 24%;
		height: 10%;
		width: 5%;
		border-radius: 50%;
		background: $color-black;
	}
	
	&::after {
		transform-origin: 50% 100%;
	}
}

.ear--left {
	left: -7%;
	border-radius: 70% 30% 0% 0% / 100% 100% 0% 0%;
	transform: rotate(-15deg);
	
	&::before,
	&::after {
		right: 10%;
	}
	
	&::after {
		transform: rotate(-45deg);
	}
}

.ear--right {
	right: -7%;
	border-radius: 30% 70% 0% 0% / 100% 100% 0% 0%;
	transform: rotate(15deg);
	
	&::before,
	&::after {
		left: 10%;
	}
	
	&::after {
		transform: rotate(45deg);
	}
}

// Face
.face {
	position: absolute;
	height: 100%;
	width: 100%;
	background: $color-black;
	border-radius: 50%;
}

// Eyes
.eye {
	position: absolute;
	top: 35%;
	height: 30%;
	width: 31%;
	background: $color-white;
	border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
	
	// Eyelids
	&::after {
		content: '';
		position: absolute;
		top: 0;
		left: 0;
		height: 0;
		width: 100%;
		border-radius: 0 0 50% 50% / 0 0 40% 40%;
		background: $color-black;
		animation: blink 4s infinite ease-in;
	}
	
	@keyframes blink {
		0% { height: 0; }
		90% { height: 0; }
		92.5% { height: 100%; }
		95% { height: 0; }
		97.5% { height: 100%; }
		100% { height: 0; }
	}
	
	// Tips of the eyes
	&::before {
		content: '';
		position: absolute;
		top: 60%;
		height: 10%;
		width: 15%;
		background: $color-white;
		border-radius: 50%;
	}
}

.eye--left {
	left: 0;
	
	&::before {
		right: -5%;
	}
}

.eye--right {
	right: 0;
	
	&::before {
		left: -5%;
	}
}

// Pupils
.eye-pupil {
	position: absolute;
	top: 25%;
	height: 50%;
	width: 20%;
	background: $color-black;
	border-radius: 50%;

    // on mobile phones use default animation since no mouse cursor
    @media (pointer:none), (pointer:coarse) {
        animation: look-around 4s infinite;
        
        @keyframes look-around {
            0% { transform: translate(0) }
            5% { transform: translate(50%, -25%) }
            10% { transform: translate(50%, -25%) }
            15% { transform: translate(-100%, -25%) }
            20% { transform: translate(-100%, -25%) }
            25% { transform: translate(0, 0) }
            100% { transform: translate(0, 0) }
        }
    }

	.eye--left & {
		right: 30%;
	}
	
	.eye--right & {
		left: 30%;
	}
	
	// Glare on the pupil
	&::after {
		content: '';
		position: absolute;
		top: 30%;
		right: -5%;
		height: 20%;
		width: 35%;
		border-radius: 50%;
		background: $color-white;
	}
}

// Muzzle
.muzzle {
	position: absolute;
	top: 60%;
	left: 50%;
	height: 6%;
	width: 10%;
	background: $color-white;
	transform: translateX(-50%);
	border-radius: 50% 50% 50% 50% / 30% 30% 70% 70%;
}


</style>

<script>
import { onMount } from 'svelte';

onMount(() => {
	document.addEventListener('mousemove', (event) => {
		const eyes = document.querySelectorAll('.eye-pupil');

		// Calculate the center point between the eyes
		const eye1Rect = eyes[0].getBoundingClientRect();
		const eye2Rect = eyes[1].getBoundingClientRect();
		const centerX = (eye1Rect.left + eye2Rect.right) / 2;
		const centerY = (eye1Rect.top + eye2Rect.bottom) / 2;

		eyes.forEach(eye => {
			const { width, height } = eye.getBoundingClientRect();
			const mouseX = event.clientX;
			const mouseY = event.clientY;
			const deltaX = mouseX - centerX;
			const deltaY = mouseY - centerY;
			const angle = Math.atan2(deltaY, deltaX);

			// Adjust the max movement as needed
			const maxMovement = Math.min(width, height) / 0.8;
			const distance = Math.min(maxMovement, Math.hypot(deltaX, deltaY));

			const eyeX = distance * Math.cos(angle);
			const eyeY = distance * Math.sin(angle);
			eye.style.transform = `translate(${eyeX}px, ${eyeY}px)`;
		});
	});
});
</script>

<div class="cat">
	<div class="ear ear--left"></div>
	<div class="ear ear--right"></div>
	<div class="face">
		<div class="eye eye--left">
			<div class="eye-pupil"></div>
		</div>
		<div class="eye eye--right">
			<div class="eye-pupil"></div>
		</div>
		<div class="muzzle"></div>
	</div>
</div>