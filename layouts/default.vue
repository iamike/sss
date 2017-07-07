<template>
  <v-app>
    <v-container fluid class="header pa-0 elevation-10">
      <v-toolbar class="primaryNav elevation-0 " >
        <v-toolbar-side-icon @click.native.stop="drawer = !drawer" class="hidden-md-and-up" ></v-toolbar-side-icon>
        <img class="logo mt-3 mb-3" alt="Vuetify Logo" src="../assets/images/logo.svg">
        <v-spacer></v-spacer>
        <v-toolbar-items class="hidden-sm-and-down" >
            <v-btn flat router nuxt to="/" >首页</v-btn>
            <v-btn flat router nuxt to="/service">产品介绍</v-btn>
            <v-btn flat router to="/news">线下活动</v-btn>
            <v-btn flat router to="/about">关于我们</v-btn>
            <v-btn flat router to="/joinus">加入我们</v-btn>
        </v-toolbar-items>
      </v-toolbar>
    </v-container>
    <main>
      <v-container fluid class="pa-0">
        <v-slide-y-transition mode="out-in">
          <nuxt />
        </v-slide-y-transition>
      </v-container>
    </main>
    <v-navigation-drawer
      temporary
      :right="right"
      v-model="drawer"
    >
    </v-navigation-drawer>
    <v-footer :fixed="fixed">
      <span>&copy; 2017</span>
    </v-footer>
  </v-app>
</template>

<script>
  export default {
    data () {
      return {
        clipped: false,
        drawer: false,
        fixed: false,
        miniVariant: false,
        right: false,
        rightDrawer: false
      }
    }
  }
</script>
<style lang="css">

/*.elevation-10 {
    box-shadow: 0 6px 6px -3px rgba(0,0,0,0.2), 0 10px 14px 1px rgba(0,0,0,0.14), 0 4px 18px 3px rgba(0,0,0,0.12) !important;
}*/
.header {
  background-color: #fff;
  z-index: 1;
  position: relative;
}
.elevation-10 {
    box-shadow: 0 6px 6px -3px rgba(0,0,0,0.1), 0 10px 14px 1px rgba(0,0,0,0.07), 0 4px 18px 3px rgba(0,0,0,0.06) !important;
}
.primaryNav {
  max-width: 1170px;
  margin: 0px auto;
  background-color: #fff;
}
.application--light {
  background-color: #fff!important;
}
.primaryNav {
  background-color: #fff!important;
}

</style>
