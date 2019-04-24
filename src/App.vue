<template>
  <v-app>
    <SideMenu/>
    <v-content>
      <MainPage/>
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import MainPage from './components/MainPage'
import SideMenu from './components/SideMenu'

export default {
  name: 'App',
  components: {
    SideMenu,
    HelloWorld,
    MainPage
  },
  data () {
    return {
      
    }
  }
}
</script>