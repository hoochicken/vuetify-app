<template>
  <nav>
    <router-link to="/">Home</router-link>
    |
    <router-link to="/about">About</router-link>
  </nav>
  <v-row class="text-center">
    <v-col cols="12">
      <h1 class="display-2 font-weight-bold mb-3">
        Randomizer
      </h1>
      <v-img
          :src="require('./assets/elves.png')"
          class="my-3"
          contain
          height="200"
      />
    </v-col>
  </v-row>
  <router-view/>
  <v-row>
    <v-col class="text-right">
      Thanks to&nbsp;<a href="https://hotpot.ai/art-generator" target="_blank">hotpot.ai/art-generator</a>&nbsp;;-)
    </v-col>
  </v-row>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  max-width: 800px;
  margin: 0 auto;
}

p {
  margin-bottom: 30px;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
