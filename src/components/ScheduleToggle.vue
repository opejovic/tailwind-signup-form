<template>
	<div class="absolute top-0 inset-x-0">
		<div class="bg-gray-400 mx-auto w-48 flex items-center tracking-wide text-gray-800 rounded-lg">
			<button @click="select('monthly')" class="focus:outline-none uppercase text-xs font-semibold py-1 text-center w-1/2 rounded-lg" :class="classes('monthly')">Monthly</button>
			<button @click="select('yearly')" class="focus:outline-none uppercase text-xs font-semibold py-1 text-center w-1/2 rounded-lg" :class="classes('yearly')">Yearly</button>
		</div>
	</div>
</template>

<script>
	export default {
		props: {
			value: {
				type: String,
			},
		},

		computed: {
			selected() {
				return 'bg-purple-700 shadow text-white';
			},

			notSelected() {
				return 'hover:bg-gray-500 opacity-75 hover:opacity-100 hover:shadow';
			},
		},

		methods: {
			select(schedule) {
				this.$emit('input', schedule);
			},

			classes(period) {
				return this.value === period ? this.selected : this.notSelected;
			},
		},
	}
</script>

<style lang="scss" scoped>

</style>