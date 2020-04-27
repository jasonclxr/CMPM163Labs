# Lab 4
Spring 2020 CMPM 163 @ UCSC

video: https://drive.google.com/file/d/184yG4qSRO9Nhrtv8kSy1QKaGp5ju85BM/view?usp=sharing

Cube 1: The "first" cube is the one in the center! This one just has a texture on it with the norm map layered over it.

Cube 2: The "second" cube is the one on the right! This one just has the texture to use as comparison towards the center one.

Cube 3: This cube is the one on the top with a different texture slapped on it.

Cube 4: The cube on the top is using the shader to put a texture on it.

Cube 5: The final and hardest cube is the one on the bottom. I created a new vec2 variable that used the modulus of the
	current x and y by 0.25, and multiplied them by 2.0. This allowed me to create a 2x2 grid!

Problem 24 Q/A
	What is the formula given a u value of the uv coordinate (a value between 0 and 1), 
	I get the x value of the pixel to sample from in this 8x8 texture?
		
		function convert(u) {
			return max(floor(8*u - 1), 0);
		}
	What is the formula given a v value of the uv coordinate (a value between 0 and 1), 
	I get the y value of the pixel to sample from in this 8x8 texture?
		function convert(v) {
			return max(floor(8 * (1 - v) - 1), 0);
		}

	What color is sampled from the texture at the uv coordinate (0.375, 0.25)? 
	(sample from the image based on the number your formula gives you i.e. (1, 0) is blue)
		x = 8*u, x = 8*0.375 - 1, x = 2
		y = 8 * (1 - v), y = 8*(1 - 0.25), y = 8*0.75 - 1, y = 5.
		
		Therefore our coordinate is (3, 6), and the color is gray.