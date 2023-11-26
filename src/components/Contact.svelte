<script>
	import { Label, Input, InputAddon, ButtonGroup, Select, Textarea } from 'flowbite-svelte';
	import { UserCircleSolid, EnvelopeSolid } from 'flowbite-svelte-icons';
	import emailjs from '@emailjs/browser';

	let selected;

	let countries = [
		{ value: 'ml', name: 'male' },
		{ value: 'fl', name: 'female' },
		{ value: 'ot', name: 'other' }
	];

	let textareaprops = {
		id: 'message',
		name: 'message',
		label: 'Your message',
		rows: 4,
		placeholder: 'Leave a message...'
	};

	function sendEmail(e) {
		emailjs.sendForm('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', e.target, 'YOUR_PUBLIC_KEY').then(
			(result) => {
				console.log('SUCCESS!', result.text);
			},
			(error) => {
				console.log('FAILED...', error.text);
			}
		);
	}
</script>

<section class="py-6 text-white">
	<div class="grid max-w-6xl grid-cols-1 px-6 mx-auto lg:px-8 md:grid-cols-2 md:divide-x">
		<div class="py-6 md:py-0 md:px-6">
			<h1 class="text-4xl font-bold">Get in touch</h1>
			<p class="pt-2 pb-4">Fill in the form to start a conversation</p>
			<div class="space-y-4">
				<p class="flex items-center">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
						fill="currentColor"
						class="w-5 h-5 mr-2 sm:mr-6"
					>
						<path
							fill-rule="evenodd"
							d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z"
							clip-rule="evenodd"
						></path>
					</svg>
					<span>Fake address, 9999 City</span>
				</p>
				<p class="flex items-center">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
						fill="currentColor"
						class="w-5 h-5 mr-2 sm:mr-6"
					>
						<path
							d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z"
						></path>
					</svg>
					<span>123456789</span>
				</p>
				<p class="flex items-center">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 20 20"
						fill="currentColor"
						class="w-5 h-5 mr-2 sm:mr-6"
					>
						<path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"></path>
						<path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"></path>
					</svg>
					<span>contact@business.com</span>
				</p>
			</div>
		</div>
		<form
			on:submit|preventDefault={sendEmail}
			class="flex flex-col py-6 space-y-6 md:py-0 md:px-6 items-center"
		>
			<Label htmlFor="fname" class="block text-white">Full Name</Label>
			<ButtonGroup class="w-full">
				<InputAddon>
					<UserCircleSolid class="w-4 h-4 text-gray-500 dark:text-gray-400" />
				</InputAddon>
				<Input id="fname" name="fname" placeholder="Full name" required />
			</ButtonGroup>

			<Label class="text-white w-full">
				Gender
				<Select class="mt-6" items={countries} bind:value={selected} name="gender" />
			</Label>
			<div class="mb-6 w-full">
				<Label for="input-group-1" class="block mb-6 text-white">Your Email</Label>
				<Input id="email" type="email" name="email" placeholder="name@flowbite.com" required>
					<EnvelopeSolid slot="left" class="w-5 h-5 text-gray-500 dark:text-gray-400" />
				</Input>
			</div>
			<Textarea {...textareaprops} />

			<button type="submit" value="Send">Submit</button>
		</form>
	</div>
</section>

<style>
	button {
		text-decoration: none;
		position: relative;
		border: none;
		font-size: 14px;
		font-family: inherit;
		color: #fff;
		width: 9em;
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
