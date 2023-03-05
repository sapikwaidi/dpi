<template>
  <v-row>
    <v-col cols="8" class="frame-content">
      <Products/>
    </v-col>

    <v-col cols="4">
      ORDER
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
  height:90vh;
  overflow-y: auto;
}
</style>
