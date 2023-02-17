<template>
  <div class="home">
    <HelloWorld msg="Das ist ein Attribut, hier kann man Text reinschreiben"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>
