<template>
	<div>
		<!-- picker -->
		<schedule-toggle v-model="schedule" @input="switchperiod($event)"></schedule-toggle>
		
		<!-- plans -->
		<plan-card plan="Starter" monthly="19" yearly="190" :schedule="schedule" :selected="isSelected('Starter')" @select="select($event)">
			<ul slot="features" class="text-sm">
				<li>10000 files / month</li>
				<li>Unlimited imagination, and fun</li>
				<li>Analytics, teams, and more…</li>
			</ul>
		</plan-card>
		<plan-card plan="Advanced"  monthly="29" yearly="290" :schedule="schedule" :selected="isSelected('Advanced')" @select="select($event)">
			<ul slot="features" class="text-sm">
				<li>20000 files / month</li>
				<li>Unlimited imagination, and fun</li>
				<li>Analytics, teams, and more…</li>
			</ul>
		</plan-card>
		<plan-card plan="Premium" monthly="39" yearly="390" :schedule="schedule" :selected="isSelected('Premium')" @select="select($event)">
			<ul slot="features" class="text-sm">
				<li>30000 files / month</li>
				<li>Unlimited imagination, and fun</li>
				<li>Analytics, teams, and more…</li>
			</ul>
		</plan-card>

	</div>
</template>

<script>
	import PlanCard from './PlanCard.vue';
	import ScheduleToggle from './ScheduleToggle.vue';

	export default {
		components: { PlanCard, ScheduleToggle },

		data() {
			return {
				schedule: 'monthly',
				selectedPlan: 'Starter',
			}
		},

		computed: {

		},

		methods: {
			isSelected(plan) {
				return this.selectedPlan === plan;
			},

			select(plan) {
				this.$emit('select', plan);
				return this.selectedPlan = plan;
			},

			switchperiod(e) {
				this.$emit('period', e);
			},
		},
	}
</script>

<style lang="scss" scoped>

</style>