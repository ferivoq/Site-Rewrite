<template>
  <div>
    <div class="warning" v-if="unavailable">VueTube isn't available for your current platform</div>
    <button :disabled="unavailable">
      <div class="icon" style="margin-right: 0.5em;" :style="`background-image: url('/icons/${icon}.svg')`"></div>
      Download for {{ platform }}
    </button>
  </div>
  
</template>

<style scoped>
.warning {
  margin-bottom: 25px;
}

button {
  background-color: #182E3F;
  display: flex;
  margin-bottom: 1em;
}
button:hover {
  background-color: #2b5270;
}
</style>

<script>
export default {
  data() {
    return {
      platform: "Android",
      icon: "android",
      unavailable: false,
    }
  },
  mounted() {


    if (this.$device.isWindows) {
      this.platform = "Windows";
      this.icon = "windows";
      this.unavailable = true;
    }


    if (this.$device.isIos) {
      this.platform = "iOS";
      this.icon = "apple";
    }


    if (this.$device.isMacOS) {
      this.platform = "Mac";
      this.icon = "apple";
      this.unavailable = true;
    }


  }
}
</script>
