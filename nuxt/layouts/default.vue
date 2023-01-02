<template>
  <div>
    <siteHeader />
    <slot />
  </div>
</template>

<style>
:root {
  --grey: #999;
}

* {
  font-family: Arial, Helvetica, sans-serif;
  color: white;
}

html, body {
  background-color: #1A1A1A;
  margin: 0;
  padding: 0;
}

button {
  border-radius: 15em;
  outline: 0;
  border: none;
  padding: 0.5em 1em;
  box-shadow: 0 5px 1em rgba(0, 0, 0, 0.25);
  transition-duration: 0.5s;
  cursor: pointer;
}

.icon {
  width: 20px;
  height: 20px;
  background-repeat: no-repeat;
  filter: invert(1);
  vertical-align: center;
}
</style>