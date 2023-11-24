<script>
	import { Card } from 'flowbite-svelte';
</script>

<section class=" text-white">
	<div class="container max-w-xl p-6 py-12 mx-auto space-y-24 lg:px-8 lg:max-w-7xl">
		<div>
			<h2 class="text-3xl font-bold tracki text-center sm:text-5xl dark:text-gray-50">
				Aliquip definiebas ad est
			</h2>
			<p class="max-w-3xl mx-auto mt-4 text-xl text-center dark:text-gray-400">
				Quando cetero his ne, eum admodum sapientem ut.
			</p>
		</div>
		<div class="grid lg:gap-8 lg:grid-cols-2 lg:items-center">
			<div>
				<h3 class="text-2xl font-bold tracki sm:text-3xl dark:text-gray-50">
					Ad vix debet docendi
				</h3>
				<p class="mt-3 text-lg dark:text-gray-400">
					Ne dicta praesent ocurreret has, diam theophrastus at pro. Eos etiam regione ut, persius
					eripuit quo id. Sit te euismod tacimates.
				</p>
				<div class="mt-12 space-y-12">
					<Card href="/cards">
						<h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
							Noteworthy technology acquisitions 2021
						</h5>
						<p class="font-normal text-gray-700 dark:text-gray-400 leading-tight">
							Here are the biggest enterprise technology acquisitions of 2021 so far, in reverse
							chronological order.
						</p>
					</Card>
				</div>
			</div>
			<div aria-hidden="true" class="mt-10 lg:mt-0">
				<img
					src="https://source.unsplash.com/random/360x480"
					alt=""
					class="mx-auto rounded-lg shadow-lg dark:bg-gray-500"
				/>
			</div>
		</div>
		<div>
			<div class="grid lg:gap-8 lg:grid-cols-2 lg:items-center">
				<div class="lg:col-start-2">
					<h3 class="text-2xl font-bold tracki sm:text-3xl dark:text-gray-50">
						Eam nibh gloriatur ex
					</h3>
					<p class="mt-3 text-lg dark:text-gray-400">
						Per odio fabellas consulatu cu. Utroque detracto mel ea, quo te latine theophrastus. Ea
						his tale nibh dissentias, mei exerci tamquam euripidis cu.
					</p>
					<div class="mt-12 space-y-12">
						<Card href="/cards">
							<h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
								Noteworthy technology acquisitions 2021
							</h5>
							<p class="font-normal text-gray-700 dark:text-gray-400 leading-tight">
								Here are the biggest enterprise technology acquisitions of 2021 so far, in reverse
								chronological order.
							</p>
						</Card>
					</div>
				</div>
				<div class="mt-10 lg:mt-0 lg:col-start-1 lg:row-start-1">
					<img
						src="https://source.unsplash.com/random/361x481"
						alt=""
						class="mx-auto rounded-lg shadow-lg dark:bg-gray-500"
					/>
				</div>
			</div>
		</div>
	</div>
</section>
