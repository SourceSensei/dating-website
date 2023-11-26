<script>
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, Button, Input } from 'flowbite-svelte';
</script>

<Navbar class="bg-gradient-to-br from-fuchsia-500/75 to-sky-500/75 ">
	<NavBrand href="/">
		<span class="self-center whitespace-nowrap text-xl font-semibold text-white">
			Sitting Smiles
		</span>
	</NavBrand>

	<div class="flex md:order-2">
		<button>Get Started</button>
		<NavHamburger />
	</div>

	<NavUl class="order-1 ">
		<NavLi href="/" active={true} class="text-white">Home</NavLi>
		<NavLi href="/about" class="text-white">About</NavLi>
		<NavLi href="/docs/components/navbar" class="text-white">F.A.Q.</NavLi>
		<NavLi href="/contact" class="text-white">Contact</NavLi>
	</NavUl>
</Navbar>

<style>
	button {
		text-decoration: none;
		position: relative;
		border: none;
		font-size: 14px;
		font-family: inherit;
		color: #fff;
		width: 7em;
		height: 3em;
		line-height: 1.25em;
		text-align: center;
		background: linear-gradient(90deg, #03a9f4, #f441a5, #ffeb3b, #03a9f4);
		background-size: 300%;
		border-radius: 15px;
		box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;
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
		border-radius: 15px;
		transition: 1s;
	}

	button:hover::before {
		filter: blur(20px);
	}

	button:active {
		background: linear-gradient(32deg, #03a9f4, #f441a5, #ffeb3b, #03a9f4);
	}
</style>
