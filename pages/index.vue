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

/* width and height scroll bar */
.frame-content::-webkit-scrollbar{
    width: 5px;
}

/* model and track color */
.frame-content::-webkit-scrollbar-track{
    background-color: #fff6f6;
    border-radius: 100px;
}

/* model and scroll bar color */
.frame-content::-webkit-scrollbar-thumb{
    background-color: #dbdbdb;
    border-radius: 100px;
}
</style>
