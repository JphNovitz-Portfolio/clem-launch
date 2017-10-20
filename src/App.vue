<template>
  <div id="app">
   <div class="container">
     <div class="row">
       <div class="col-lg-3">
         <logo></logo>
         <contact></contact>
       </div>
       <div class="col-lg-9">
          <head-title></head-title>
          <products></products>
       </div>
     </div>
   </div>
  </div>
</template>

<script>
import logo from './components/logo/Logo'
import contact from './components/contact/Contact'
import HeadTitle from './components/HeadTitle'
import products from './components/Products/Products'

export default {
  name: 'app',
  components: {
    logo,
    contact,
    HeadTitle,
    products
  }
}
</script>

<style>

#app {
  font-family: 'NK_Monotype Corsiva', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.color-orange {
      background-color: inherit;
      color: #EB5E00;
  }
</style>
