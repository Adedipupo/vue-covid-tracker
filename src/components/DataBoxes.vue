<template>
  <div class="grid md:grid-cols-2 gap-4">
    <div class="shadow-md bg-blue-100 p-10 text-center rounded">
      <div class="h3 text-3xl text-blue-900 font-bold mb-4">
        Cases
      </div>
      <div class="text-2xl mb-4">
        <span class="font-bold">New :</span>
        {{ stats.NewConfirmed }}
      </div>
      <div class="text-2xl mb-4">
        <span class="font-bold">Total :</span>
        {{ stats.TotalConfirmed }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "DataBoxes",
  props: ["stats"],
};
</script>
