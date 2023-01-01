<template>
  <button>
    <div class="icon" style="margin-right: 0.5em;" :style="`background-image: url('/icons/${icon}.svg')`"></div>
    {{ buttonText }}
  </button>
</template>

<style scoped>
button {
  background-color: #182E3F;
  display: flex;
}
button:hover {
  background-color: #2b5270;
}
</style>

<script>
export default {
  data() {
    return {
      buttonText: "Download for Android",
      icon: "android"
    }
  }
}
</script>