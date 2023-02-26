<template>
  <div>
    <span v-if="false">items: {{ items }}</span>
    <p>{{ item }}</p>
    <v-btn class="v-btn--rounded v-btn--border" color="blue-grey" v-on:click="getRandomItemFromList()">
      {{ buttonLabel }}
    </v-btn>
  </div>
</template>

<script>
export default {
  name: "RandomElement",
  props: ['items', 'buttonLabel'],
  data: () => {
    return {
        item: ''
    }
  },
  methods: {
    getRandomItemFromList() {
      let randomKey = this.getRandomNumber(this.items.length -1);
      this.item = this.items[randomKey]
    },
    getRandomNumber(maxNumber) {
      return Math.floor(Math.random() * maxNumber);
    }
  }
}
</script>

<style scoped>

</style>