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
		<Button size="sm" class="bg-gradient-to-br from-fuchsia-500 to-sky-600">Get started</Button>
		<NavHamburger />
	</div>

	<NavUl class="order-1 ">
		<NavLi href="/" active={true} class="text-white">Home</NavLi>
		<NavLi href="/about" class="text-white">About</NavLi>
		<NavLi href="/docs/components/navbar" class="text-white">F.A.Q.</NavLi>
		<NavLi href="/contact" class="text-white">Contact</NavLi>
	</NavUl>
</Navbar>
