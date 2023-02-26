<template>
  <div class="home">
    <!--HelloWorld msg="Das ist ein Property, die kann dann in der HelloWorld-Komponente dargestellt werden"/-->
    <random-ingredient></random-ingredient>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import RandomIngredient from "@/components/RandomIngredient";

export default {
  name: 'HomeView',
  components: {
    // HelloWorld,
    RandomIngredient
  }
}
</script>
