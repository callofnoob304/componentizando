<template>
  <div class="bg-red">
    <v-row>
      <v-col>
        <CCard :cardSubTitle="true" :cardTitle="true" :cardText="true" :cardActions="true" :titulo="'Teste titulo'"
          :subTitulo="'teste subtitulo'" :textAlign="'start'" />
      </v-col>
    </v-row>
  </div>
</template>

<script lang="ts">
import CCard from '../components/CCard.vue'

export default {
  components: { CCard },

  data() {
    return {

    }
  }
}
</script>
