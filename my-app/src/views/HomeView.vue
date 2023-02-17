<template>
  <div class="home">
    <HelloWorld msg="Das ist ein Property, die kann dann in der HelloWorld-Komponente dargestellt werden"/>
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
