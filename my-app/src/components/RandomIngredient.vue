<template>
  <div>
    <h2>Zufällige Zutat</h2>
    <random-element :items="ingredients" :buttonLabel="'Zufalls-Zutat erzeugen'"></random-element>
  </div>
</template>

<script>
import RandomElement from "@/components/RandomElement";
export default {
  name: "RandomIngredient",
  components: {RandomElement},
  data: () => {
    return {
      ingredients: [
          'Salz',
          'Pfeffer',
          'Wasser',
          'Schnittlauch',
          'Petersilie',
          'Tofu',
          'Kuhmilch',
          'Ziegenmilch',
          'Essig',
      ]
    }
  }
}
</script>

<style scoped>

</style>