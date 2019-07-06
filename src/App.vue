<template>
  <v-app>
    
    <Toolbar/>


    <Drawer/>


    <HelloWorld/>
    <FooterOmnia/>


  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import datepicker from './components/datepicker'
import Drawer from './components/Drawer'
import Toolbar from './components/Toolbar'
import FooterOmnia from './components/Footer'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Drawer,
    Toolbar,
    FooterOmnia,
    datepicker
  },
  data () {
    return {
      //
    }
  }
}
</script>
