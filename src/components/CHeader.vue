<template>
  <v-row class="align-center justify-space-between px-10">
    <v-col cols="4">
      <h2>Meus exemplos de componentes</h2>
    </v-col>
    <v-col cols="1" class="d-flex justify-center">
      <v-switch hide-details :width="width" :append-icon="appendIcon" :inset="inset" @click="onClick" />
    </v-col>
  </v-row>
</template>

<script>
export default {
  props: {
    appendIcon: {
      type: String,
      required: false
    },
    inset: {
      type: Boolean,
      required: false
    },
    width: {
      type: Number,
      required: false
    },
    onClick: {
      type: Function,
      required: true
    }
  }
}
</script>