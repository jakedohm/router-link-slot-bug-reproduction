<template>
  <div id="app">
    <div id="nav">
      <router-link
        v-slot="{ isActive }"
        :class="[isActive ? 'bg-red' : 'bg-blue']"
        active-class="underline"
        to="/"
        >Home</router-link
      >
      |
      <router-link
        v-slot="{ isActive }"
        :class="[isActive ? 'bg-red' : 'bg-blue']"
        active-class="underline"
        to="/about"
        >About</router-link
      >
    </div>
    <router-view />
  </div>
</template>

<style>
#nav {
  padding: 20px;
}
a {
  color: white;
  padding: 10px 20px;
  border-radius: 5px;
  text-decoration: none;
}

.bg-red {
  background: red;
}

.bg-blue {
  background: blue;
}

.underline {
  text-decoration: underline;
}
</style>
