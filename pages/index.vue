<template>
  <v-container fluid class="pt-0 pb-0 pr-0 pl-0" >
    <v-carousel>
      <v-carousel-item :src="'//via.placeholder.com/1024x768'">
        <figure>
          <h3>用“特技” 学英语</h3>
          <h4>唯一科学有效，全面突破听说、读写</h4><v-btn round primary dark>Small Button</v-btn>
        </figure>
      </v-carousel-item>
      <v-carousel-item :src="'//via.placeholder.com/1024x768'">
        <figure>
          <h3>用“特技” 学英语2</h3>
          <h4>唯一科学有效，全面突破听说、读写2</h4>
        </figure>
      </v-carousel-item>
    </v-carousel>
    <v-parallax src="/images/placeholder/heroimage.jpg" height="420">
      <v-container>
        <h3>积极、进取、持续、</h3>
        <h3>专注、创造、突破。</h3>
      </v-container>
    </v-parallax>
  </v-container>
</template>
<script>
  export default {
    data () {
      return {

      }
    }
  }
</script>
<style lang="stylus">

</style>
