<section class=" text-white custom-hero">
	<div
		class="container mx-auto flex flex-col items-center px-4 py-16 text-center md:py-32 md:px-10 lg:px-32 xl:max-w-3xl custom-div-content-hero"
	>
		<h1 class="text-4xl font-bold leadi sm:text-5xl">
			Welcome to our
			<span class="dark:text-violet-400">amazing</span> website
		</h1>
		<p class="px-8 mt-8 mb-12 text-lg">
			Cupiditate minima voluptate temporibus quia? Architecto beatae esse ab amet vero eaque
			explicabo!
		</p>
		<div class="flex flex-wrap justify-center">
			<button> Find Out More </button>
		</div>
	</div>
</section>

<style>
	.custom-hero {
		position: relative;
		background-image: url('../../src/images/hero-image-2.jpg');
		background-repeat: no-repeat;
		background-size: cover;
		background-position: center;
		height: 100vh;
	}

	.custom-hero::before {
		content: '';
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		background: linear-gradient(90deg, #03a9f4, #f441a5, #ffeb3b, #03a9f4);
		background-size: 400%;
		opacity: 0.6;
		z-index: 1;
	}

	.custom-div-content-hero {
		position: absolute;
		top: 50%;
		left: 70%;
		transform: translate(-50%, -50%);
		z-index: 2;
	}

	.custom-div-content-hero {
		position: absolute;
		top: 50%;
		left: 70%;
		transform: translate(-50%, -50%);
	}

	button {
		text-decoration: none;
		position: relative;
		border: none;
		font-size: 14px;
		font-family: inherit;
		color: #fff;
		width: 9em;
		height: 3em;
		line-height: 2em;
		text-align: center;
		background: linear-gradient(90deg, #03a9f4, #f441a5, #ffeb3b, #03a9f4);
		background-size: 300%;
		border-radius: 30px;
		z-index: 1;
	}

	button:hover {
		animation: ani 8s linear infinite;
		border: none;
	}

	@keyframes ani {
		0% {
			background-position: 0%;
		}

		100% {
			background-position: 400%;
		}
	}

	button:before {
		content: '';
		position: absolute;
		top: -5px;
		left: -5px;
		right: -5px;
		bottom: -5px;
		z-index: -1;
		background: linear-gradient(90deg, #03a9f4, #f441a5, #ffeb3b, #03a9f4);
		background-size: 400%;
		border-radius: 35px;
		transition: 1s;
	}

	button:hover::before {
		filter: blur(20px);
	}

	button:active {
		background: linear-gradient(32deg, #03a9f4, #f441a5, #ffeb3b, #03a9f4);
	}
</style>
