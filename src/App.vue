<template>
  <div id="app">
   <div class="container">
      <section id="one" v-bind:class="{ oneUp: oneUp }" >
        <div class="row">
          <div class="col-lg-3 col-sm-12">
            <div class="row">
              <logo class="col-lg-12 col-sm-4" ></logo>
              <contact class="col-lg-12 col-sm-8"></contact>
              <div class="spacer"> </div>
          </div>
          </div>
          <div class="spacer"> </div>
          <div class="col-lg-9 col-md-12">
              <head-title></head-title>
              <div class="spacer"> </div>
              <products></products>
          </div>
        </div> <!-- row-->
        <div class="row button-bottom" >
              <div class="col-lg-12 " ><button class="btn btn-info" @click="oneUp = !oneUp">click</button></div>
        </div>
      </section>
      <section id="two" class=" bg-green">
        <div class="row">
          <div class="col-lg-3 col-sm-12">
            <div class="row">
              <logo class="col-lg-12 col-sm-4" ></logo>
              <contact class="col-lg-12 col-sm-8"></contact>
              <div class="spacer"> </div>
          </div>
          </div>
          <div class="spacer"> </div>
          <div class="col-lg-9 col-md-12">
              <offer></offer>
          </div>
        </div> <!-- row-->
        <div class="row button-bottom" >
              <div class="col-lg-12 " ></div>
        </div>
      </section>
      </div> <!-- container -->
  </div> <!-- app -->
</template>

<script>
import logo from './components/logo/Logo'
import contact from './components/contact/Contact'
import HeadTitle from './components/HeadTitle'
import products from './components/Products/Products'
import offer from './components/Offer'

export default {
  name: 'app',
  components: {
    logo,
    contact,
    HeadTitle,
    products,
    offer
  },
  data () {
    return {
      oneUp: false
    }
  }
}
</script>

<style>

.container {
  height: 100vh ;
  min-height: 100vh;
  overflow: hidden;
}

#app {
  font-family: 'NK_Monotype Corsiva', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

#one, #two {
  height: 100vh ;
  min-height: 100vh;
  position: relative;
  padding: 1em 0;
  
}

.button-bottom {
  position: absolute;
  bottom: 11vh;
  left: 40vw;
}

.oneUp {
  margin-top: -101vh;
  transition: all .9s
}
.color-orange {
      background-color: inherit;
      color: #EB5E00;
  }

.spacer {
  min-height: 2vh;
  display: none;
}

.bg-green {
  background-color: rgba(40,167,69, .1) ;
  color:  rgb(40,167,69) ;
}

 @media only screen and (min-width:800px) {
 .spacer {
   display: block;
 }
}
</style>
