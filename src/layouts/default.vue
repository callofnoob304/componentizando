<template>
  <v-app :theme="!modoEscuro ? 'light' : 'dark'">
    <v-app-bar>
      <CHeader :inset="true" :width="85" :appendIcon="!modoEscuro ? 'mdi-white-balance-sunny' : 'mdi-weather-night'"
        :onClick="alternarModo" />
    </v-app-bar>
    <v-main>
      <v-container>
        <router-view />
      </v-container>
    </v-main>
  </v-app>
</template>

<script lang="ts">
import CHeader from '../components/CHeader.vue'

export default {
  components: { CHeader, },

  data() {
    return {
      modoEscuro: false as Boolean
    }
  },

  methods: {
    alternarModo() {
      this.modoEscuro = !this.modoEscuro;
    }
  }
}
</script>