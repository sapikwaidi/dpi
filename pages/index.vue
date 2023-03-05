<template>
  <v-row>
    <v-col 
    cols="8" 
    class="frame-content px-6">
      <Products/>
    </v-col>

    <v-col 
    cols="4" 
    class="frame-content">
      <!-- ORDER -->
      <Products/>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>

<style>
.frame-content{
  height: 90vh;
  overflow-y: auto;
}
</style>
