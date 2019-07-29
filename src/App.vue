<template>
  <div id="app" class="min-h-screen bg-gray-300 backg">
    <div class="container mx-auto px-6">
      <header class="flex items-center justify-between py-6">
        <button type="button">
          <a href="#" class="flex items-baseline">
            <img class="w-16" src="./assets/logo.svg" alt="Imaginary" />
            <p class="pl-1 font-bold text-3xl tracking-tighter text-purple-900">
              imaginary.
            </p>
          </a>
        </button>
        <div>
          <a
            href="#"
            class="border-b-2 hover:border-purple-600 text-purple-900 text-sm font-normal leading-loose"
            >Log In</a
          >
        </div>
      </header>
      <div class="pb-12">
        <h1 class="text-purple-900 text-center text-2xl font-light py-10">
          Start your imaginary journey today:
        </h1>
        <!-- -mx-6 here is because of the padding we are adding to each of the two columns. -->
        <div class="lg:flex flex-wrap -mx-6">
          <!-- Left side -->
          <div class="md:w-full lg:w-1/2 px-4 pt-10 relative">
            <plan-selector
              :schedule="schedule"
              @change-schedule="schedule = $event"
              @select="selectedPlan = $event"
              :selected-plan="selectedPlan"
            ></plan-selector>
          </div>

          <!-- Right side -->
          <div class="md:w-full lg:w-1/2 px-4 lg:pt-10">
            <p class="lg:hidden mt-5 mb-3 text-gray-700 text-xl text-center">
              Your Information
            </p>
            <form>
              <input
                class="w-full mb-2 bg-transparent bg-gray-400 border border-gray-400 focus:bg-gray-500 px-4 py-4 rounded text-center outline-none text-xl text-gray-800"
                type="text"
                placeholder="Your Name"
              />
              <input
                class="w-full mb-2 bg-transparent bg-gray-400 border border-gray-400 focus:bg-gray-500 px-4 py-4 rounded text-center outline-none text-xl text-gray-800"
                type="email"
                placeholder="Your Email"
              />
              <input
                class="w-full mb-2 bg-transparent bg-gray-400 border border-gray-400 focus:bg-gray-500 px-4 py-4 rounded text-center outline-none text-xl text-gray-800"
                type="password"
                placeholder="Setup Your Password"
              />
              <input
                class="w-full mb-2 bg-transparent bg-gray-400 border border-gray-400 focus:bg-gray-500 px-4 py-4 rounded text-center outline-none text-xl text-gray-800"
                type="text"
                placeholder="Card number"
              />
              <button
                type="submit"
                class="text-white font-medium text-sm shadow uppercase bg-purple-900 block w-full py-4 rounded border-b-2 border-purple-700 hover:bg-purple-700 hover:border-purple-800 outline-none mb-4"
              >
                Create my account
              </button>
              <p class="text-xs text-center text-gray-700">
                Includes a 10 days trial before billing begins.
              </p>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import PlanSelector from "./components/PlanSelector.vue";

  export default {
    components: { PlanSelector },
    name: "app",

    data() {
      return {
        schedule: "monthly",
        selectedPlan: "Basic"
      };
    }
  };
</script>

<style>
  @tailwind base;
  @tailwind components;
  @tailwind utilities;

  .backg {
	background-image: url(./assets/curve.svg);
	background-position-x: center;
    background-position-y: bottom;
    background-size: 5153px 200px;
    background-repeat-x: no-repeat;
    background-repeat-y: no-repeat;
    background-attachment: fixed;
    background-origin: initial;
    background-clip: initial;
    /* background-color: rgb(12, 24, 36); */
  }
</style>
