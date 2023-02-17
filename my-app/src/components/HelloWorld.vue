<template>
  <v-container>
    <v-row>
      <v-col class="mb-4">
        <p v-if="randomGegenstand.length > 0">
          <strong>{{ randomGegenstand }}</strong>
        </p>
        <p v-else>
          <strong>Es gibt noch keinen Gegensatz, musstu klickn ...</strong>
        </p>
        <p>
          Ein Button:
          <v-btn class="v-btn--rounded v-btn--border" color="blue-grey" v-on:click="machWas()">Gegenstand erzeugen
          </v-btn>
        </p>
        <p>
          So stellst man eine Variable dar (Doppel-Schweif-Klammern):
          <br/>
          {{ gegenstaende }}
        </p>
        <p>
          {{ msg }}
        </p>

      </v-col>
    </v-row>
  </v-container>
</template>

<script>

export default {
  name: 'HelloWorld',

  props: ['msg'],

  /* hier werden die variablen, die dargestellt werden sollen, definiert */
  data: () => ({
    textvar: 'lasdhkajhdkahdkjhaskd',
    randomGegenstand: '',
    gegenstaende: ['Topf', 'Nadel', 'Brat-Hühnchen', 'Pfanne', 'Tasse',],
    eigennschaft: ['alt', 'neu', 'müffelt ein bisschen',],
  }),
  methods: {
    machWas() {
      console.log('Ich habe was gemacht, weil Du geklickt hast')
      this.randomizeGegenstand()
    },
    randomizeGegenstand() {
      /* "let" definiert auch Variablen, aber die sind lokal und werden nirgendwo dargestellt */
      let randomNumber = this.getRandomIndexFromArray(this.gegenstaende)
      this.randomGegenstand = this.gegenstaende[randomNumber]
    },
    getRandomIndexFromArray(dasArray) {
      /* "let" definiert auch Variablen, aber die sind lokal und werden nirgendwo dargestellt */
      let maxWert = dasArray.length
      return Math.floor(Math.random() * maxWert)
    },
  }
}
</script>
