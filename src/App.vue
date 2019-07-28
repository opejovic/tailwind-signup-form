<template>
	<div id="app" class="min-h-screen bg-gray-300">
		<div class="container mx-auto px-6">
			<header class="flex items-center justify-between py-6">
				<div class="flex items-baseline">
					<img class="w-16" src="./assets/logo.svg" alt="">
					<p class="pl-1 font-bold text-3xl tracking-tighter text-purple-900">imaginary.</p>
				</div>
				<div>
					<a href="#" class="text-purple-900 text-sm font-normal no-underline hover:text-indigo-400">Log In</a>
				</div>
			</header>
			<div>
				<h1 class="text-purple-900 text-center text-2xl font-light py-10">Start your imaginary journey today:</h1>
				<!-- -mx-6 here is because of the padding we are adding to each of the two columns. -->
				<div class="flex flex-wrap -mx-6">
					<!-- Left side -->
					<div class="w-1/2 px-4 pt-10 relative">
						<!-- picker -->
						<div class="absolute top-0 inset-x-0">
							<div class="bg-gray-400 mx-auto w-48 flex items-center tracking-wide text-gray-800 rounded-lg">
								<button class="uppercase text-xs font-semibold py-1 text-center w-1/2 bg-purple-700 shadow rounded-lg text-white">Monthly</button>
								<button class="uppercase text-xs font-semibold py-1 text-center w-1/2 hover:bg-gray-500 rounded-lg opacity-75 hover:opacity-100 hover:shadow">Yearly</button>
							</div>
						</div>
						<!-- plans -->
						<div class="border border-gray-400 rounded px-6 py-4 text-gray-800 items-center hover:bg-gray-400 opacity-75 hover:opacity-100 relative">
							
							
							<div class="flex -mx-4 items-center">
								<div class="w-2/5 px-4">
									<h2 class="text-xl">Starter</h2>
									<div>
										<span class="text-3xl font-bold">$19</span>
										<span class="mx-1">/</span>
										<span>month</span>
									</div>
								</div>
								<div class="w-3/5">
									<ul class="text-sm">
										<li>10,000 dreams / month</li>
										<li>Unlimited imagination, and fun</li>
										<li>Analytics, teams, and more…</li>
									</ul>
								</div>
							</div>
						</div>
						<div class="border border-purple-300 bg-gray-400 rounded px-6 py-4 text-gray-800 items-center mt-2 hover:bg-gray-400 overflow-hide">
							<div class="flex -mx-4 items-center">
								<div class="absolute left-0 -ml-1">
									<img class="w-10" src="./assets/checkcircle.svg" alt="">
								</div>
								<div class="w-2/5 px-4">
									<h2 class="text-xl">Advanced</h2>
									<div>
										<span class="text-3xl font-bold">$29</span>
										<span class="mx-1">/</span>
										<span>month</span>
									</div>
								</div>
								<div class="w-3/5">
									<ul class="text-sm">
										<li>50,000 dreams / month</li>
										<li>Unlimited imagination, and fun</li>
										<li>Analytics, teams, and more…</li>
									</ul>
								</div>
							</div>
						</div>

						<div class="border border-gray-400 rounded px-6 py-4 text-gray-800 items-center mt-2 hover:bg-gray-400 opacity-75 hover:opacity-100">
							<div class="flex -mx-4 items-center">
								<div class="w-2/5 px-4">
									<h2 class="text-xl">Premium</h2>
									<div>
										<span class="text-3xl font-bold">$39</span>
										<span class="mx-1">/</span>
										<span>month</span>
									</div>
								</div>
								<div class="w-3/5">
									<ul class="text-sm">
										<li>250,000 dreams / month</li>
										<li>Unlimited imagination, and fun</li>
										<li>Analytics, teams, and more…</li>
									</ul>
								</div>
							</div>
						</div>
					</div>

					<!-- Right side -->
					<div class="w-1/2 px-4 pt-10">
						<form class="">
							<input class="w-full mb-2 bg-transparent bg-gray-400 border border-gray-400 focus:bg-gray-500 px-4 py-4 rounded text-center outline-none text-xl text-gray-800" type="text" placeholder="Your Name">
							<input class="w-full mb-2 bg-transparent bg-gray-400 border border-gray-400 focus:bg-gray-500 px-4 py-4 rounded text-center outline-none text-xl text-gray-800" type="email" placeholder="Your Email">
							<input class="w-full mb-2 bg-transparent bg-gray-400 border border-gray-400 focus:bg-gray-500 px-4 py-4 rounded text-center outline-none text-xl text-gray-800" type="password" placeholder="Setup Your Password">
							<input class="w-full mb-2 bg-transparent bg-gray-400 border border-gray-400 focus:bg-gray-500 px-4 py-4 rounded text-center outline-none text-xl text-gray-800" type="text" placeholder="Card number">
							<button type="submit" class="text-white font-medium text-sm shadow uppercase bg-purple-900 block w-full py-4 rounded border-b-2 border-purple-700 hover:bg-purple-700 hover:border-purple-800 outline-none mb-4">Create my account</button>
							<p class="text-xs text-center text-gray-700">Includes a 10 days trial before billing begins.</p>
						</form>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
  name: 'app',

}
</script>

<style>
	@tailwind base;
	@tailwind components;
	@tailwind utilities;
</style>
