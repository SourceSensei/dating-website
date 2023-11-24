<script>
	import { AccordionItem, Accordion, Button } from 'flowbite-svelte';
	const items = Array(3);

	const open_all = () => items.forEach((_, i) => (items[i] = true));
	const close_all = () => items.forEach((_, i) => (items[i] = false));
</script>

<section class="text-white">
	<div class="container flex flex-col justify-center p-4 mx-auto md:p-8">
		<p class="p-2 text-sm font-medium tracki text-center uppercase">How it works</p>
		<h2 class="mb-12 text-4xl font-bold leadi text-center sm:text-5xl">
			Frequently Asked Questions
		</h2>
		<div>
			<Button on:click={open_all} class="bg-gradient-to-br from-fuchsia-500 to-sky-600 shadow-md">Open all</Button>
			<Button on:click={close_all} class="bg-gradient-to-br from-fuchsia-500 to-sky-600 shadow-md">Close all</Button>
			<Accordion multiple class="bg-gradient-to-br from-fuchsia-500 to-sky-600">
				<AccordionItem bind:open={items[0]}>
					<span slot="header" class="text-white">My Header 1</span>
					<p class="mb-2 text-white">
						Lorem ipsum dolor sit amet, consectetur adipisicing elit. Illo ab necessitatibus sint
						explicabo ...
					</p>
					<p class="text-white">
						Check out this guide to learn how to <a
							href="/"
							target="_blank"
							rel="noreferrer"
							class="text-blue-600 dark:text-blue-500 hover:underline"
						>
							get started
						</a>
						and start developing websites even faster with components on top of Tailwind CSS.
					</p>
				</AccordionItem>
				<AccordionItem bind:open={items[1]}>
					<div slot="header" class="text-white">My Header 2</div>
					<p class="mb-2 text-white">
						Lorem ipsum dolor sit amet, consectetur adipisicing elit. Illo ab necessitatibus sint
						explicabo ...
					</p>
					<p class="mb-2 text-white">
						Lorem ipsum dolor sit amet, consectetur adipisicing elit. Illo ab necessitatibus sint
						explicabo ...
					</p>
					<p class="mb-2 text-white">Learn more about these technologies:</p>
				</AccordionItem>
				<AccordionItem bind:open={items[2]}>
					<div slot="header" class="text-white">My Header 3</div>
					<p class=" text-white">Something more</p>
				</AccordionItem>
			</Accordion>
		</div>
	</div>
</section>
