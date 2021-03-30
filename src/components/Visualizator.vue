<template>
  <div class="visualizator">
    <Filtering />
    je vais afficher un tableau de donnee ici!
    <Datatable :data="filteredData" />

    <Charts :data="filteredData"/>

  </div>
</template>

<script>
import { mapState, mapGetters } from 'vuex'
import Datatable from "@/components/Datatable";
import Filtering from "@/components/Filtering";
import Charts from "@/components/Charts";

export default {
  name: 'Visualizator',
  components: {Charts, Filtering, Datatable},
  computed:{

    ...mapState(['people']),
    ...mapGetters(['filteredData']),

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
