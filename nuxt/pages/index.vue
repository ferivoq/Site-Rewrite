<template>
  <center>
    
    <div class="icon vt-logo" />
    <h1 style="font-size: 3em; margin-top: 0.5em;">VueTube</h1>

    <dlbtn />
    <NuxtLink to="/downloads" style="text-decoration: none;"><a style="color: var(--grey)">More downloads</a></NuxtLink>

  </center>
</template>

<style scoped>
.vt-logo {
  background-image: url('/logos/full.svg');
  filter: invert(0);
  border-radius: 15em;
  width: 150px;
  height: 150px;
  margin-top: 10vh;
}
</style>