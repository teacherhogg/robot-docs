<template>
  <div class="grid grid-cols-1 md:grid-cols-2 gap-2 auto-cols-min">
    <!-- component -->
    <div
      v-for="feature in features"
      :key="feature.id"
    >
      <div class="max-w-sm rounded-sm border border-gray-200 bg-white shadow-lg">
        <div class="text-right p-4 bg-gray-300">
          <span class="text-xs text-gray-800 tracking-widest uppercase">{{ feature.label }}</span>
        </div>
        <div class="flex items-center relative mb-10">
          <div class="border-t border-gray-200 z-20 w-full"></div>
          <img
            :src="feature.icon"
            v-bind:class="feature.classes"
            class="rounded-full z-30 p-2 inline-block absolute mx-8 w-12 h-12"
          />
        </div>
        <div class="px-8 pb-4">
          <h4 class="text-gray-500 text-sm font-light">{{ feature.subtitle }}</h4>
          <h2 class="text-gray-800 text-xl font-bold">{{ feature.title }}</h2>
          <p
            v-for="desc in feature.description"
            :key="desc"
            class="text-gray-600 text-xs"
            v-html="desc"
          >
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['features'],
  data () {
    return {
      value: null
    }
  },
  methods: {
    closeModal: function () {
      console.log("Close Modal h?");
    },
  }
}
</script>

<style scoped>
</style>