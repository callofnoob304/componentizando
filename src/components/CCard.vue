<template>
  <v-card>
    <v-card-title v-if="cardTitle" :class="'text-'+textAlign">{{ titulo }}</v-card-title>
    <v-card-subtitle v-if="cardSubTitle">{{ subTitulo }}</v-card-subtitle>
    <v-card-text v-if="cardText">
      corpo e conteudo
    </v-card-text>
    <v-card-action v-if="cardActions">
      botoes
    </v-card-action>
  </v-card>
</template>
<script>
export default {
  props: {
    cardTitle: {
      type: Boolean,
    },
    cardSubTitle: {
      type: Boolean,
    },
    cardText: {
      type: Boolean,
    },
    cardActions: {
      type: Boolean,
    },
    titulo: {
      type: String,
    },
    subTitulo: {
      type: String,
    },
    textAlign: {
      type: String,
      validator: value => ['start', 'center', 'end'].includes(value)
    }
  }
}
</script>