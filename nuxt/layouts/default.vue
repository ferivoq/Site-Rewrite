<template>
  <div>
    <siteHeader />
    <slot />
  </div>
</template>

<style>
* {
  font-family: Arial, Helvetica, sans-serif;
  color: white;
}

html, body {
  background-color: #1A1A1A;
  margin: 0;
  padding: 0;
}

.icon {
  width: 20px;
  height: 20px;
  background-repeat: no-repeat;
  filter: invert(1);
}
</style>