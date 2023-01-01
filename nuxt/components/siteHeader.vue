<template>
  <header>
    
    <div>
      <div class="icon vt-logo" />
      <span style="margin-left: 1em; transform: translateY(15%);">VueTube</span>
    </div>

    <div style="float: right; transform: translateY(-100%);">
      <NuxtLink v-for="link, l, in links" :key="l" :to="link.to" target="_blank" class="links">
        <div class="icon" style="margin-left: 1em;" :style="`background-image: url('${link.icon}')`"></div>
        <span style="margin-left: 0.25em;">{{ link.name }}</span>
      </NuxtLink>
    </div>

  </header>
</template>

<style scoped>
header {
  border-bottom: 1px solid rgba(255,255,255,0.25);
  padding: 0.5em 2em;
}
header > div {
  display: flex;
}

.vt-logo {
  background-image: url('/logos/nobg-white.svg');
  filter: invert(0);
  width: 25px;
  height: 25px;
}

.links {
  display: flex;
  text-decoration: none;
}
.links > div, .links > span {
  transition-duration: 0.5s;
  filter: invert(0.5);
}
.links:hover div { filter: invert(1); }
.links:hover span { filter: invert(0) }
</style>

<script>
export default {
  data() {
    return {
      links: [
        { name: "GitHub", icon: "/icons/github.svg", to: "https://github.com/VueTubeApp/VueTube" },
        { name: "Discord", icon: "/icons/discord.svg", to: "https://github.com/VueTubeApp/VueTube" },
      ]
    }
  }
}
</script>