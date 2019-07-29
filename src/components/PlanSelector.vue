<template>
  <div>
    <!-- picker -->
    <schedule-toggle :value="schedule" @input="$emit('change-schedule', $event)"></schedule-toggle>

    <!-- plans -->
    <plan-card
      plan="Basic"
      monthly="19"
      yearly="190"
      :schedule="schedule"
      :selected="isSelected('Basic')"
      @select="select($event)"
    >
      <ul slot="features" class="text-sm">
        <li>10000 files / month</li>
        <li>Unlimited imagination, and fun</li>
        <li>Analytics, teams, and more…</li>
      </ul>
    </plan-card>
    <plan-card
      plan="Advanced"
      monthly="29"
      yearly="290"
      :schedule="schedule"
      :selected="isSelected('Advanced')"
      @select="select($event)"
    >
      <ul slot="features" class="text-sm">
        <li>20000 files / month</li>
        <li>Unlimited imagination, and fun</li>
        <li>Analytics, teams, and more…</li>
      </ul>
    </plan-card>
    <plan-card
      plan="Premium"
      monthly="39"
      yearly="390"
      :schedule="schedule"
      :selected="isSelected('Premium')"
      @select="select($event)"
    >
      <ul slot="features" class="text-sm">
        <li>30000 files / month</li>
        <li>Unlimited imagination, and fun</li>
        <li>Analytics, teams, and more…</li>
      </ul>
    </plan-card>
  </div>
</template>

<script>
  import PlanCard from "./PlanCard.vue";
  import ScheduleToggle from "./ScheduleToggle.vue";

  export default {
	components: { PlanCard, ScheduleToggle },
	props: ['schedule', 'selectedPlan'],

    methods: {
      isSelected(plan) {
        return this.selectedPlan === plan;
      },

      select(plan) {
        this.$emit("select", plan);
      },
    }
  };
</script>