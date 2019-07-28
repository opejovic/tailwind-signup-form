<template>
	<button @click="$emit('select', plan)" :class="clicked" class="border text-left focus:outline-none focus:opacity-100 focus:bg-gray-400 block w-full border-gray-400 rounded px-6 py-4 text-gray-800 items-center mb-2">
		<div class="flex -mx-4 items-center">
			<!-- check circle - need to make it dynamic -->
			<div class="absolute left-0" v-if="selected">
				<img class="w-8" src="../assets/checkcircle.svg" alt="">
			</div>
			<div class="w-2/5 px-4">
				<h2 class="text-xl" v-text="plan"></h2>
				<div>
					<span class="text-3xl font-bold">${{ isMonthly ? monthly : yearly }}</span>
					<span class="mx-1">/</span>
					<span>{{ isMonthly ? 'month' : 'year' }}</span>
				</div>
			</div>
			<div class="w-3/5">
				<slot name="features"></slot>
			</div>
		</div>
	</button>
</template>

<script>
	export default {
		props: [
			'plan', 
			'monthly',
			'yearly',
			'selected',
			'schedule'
		],

		data() {
			return {
			
			}
		},

		computed: {
			clicked() {
				return this.selected ? 'border-purple-300 bg-gray-400 opacity-100' : 'hover:bg-gray-400 opacity-75 hover:opacity-100'; 
			},

			isMonthly() {
				return this.schedule === 'monthly'; 
			},
		},
	}
</script>

<style lang="scss" scoped>

</style>