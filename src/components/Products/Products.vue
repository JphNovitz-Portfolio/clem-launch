<template>
    <div>
        <div class="">
          <img src="" />
              
            <div class="container-word" v-for="(product, index) in products"  :key="product" > 
              <div v-show="products[index].showMe">
                <i class="" aria-hidden="true"></i>
               {{product.text}}
              </div>
            </div>
            
        </div>
    </div>
</template>

<script>
export default {
  name: 'products',
  data () {
    return {
      inter: '',
      products: [
        { 'id': 1, 'text': 'Pain soleil au sésame', 'showMe': false },
        { 'id': 2, 'text': 'Potages de saison', 'showMe': false },
        { 'id': 3, 'text': 'Sandwiches garnis fait maison', 'showMe': false },
        { 'id': 4, 'text': 'Service traiteur pour réunions entre amis , anniversaires, fêtes d\'entreprises.', 'showMe': false }
      ]
    }
  },
  computed: { },
  created () {
    let i = 0
    this.inter = setInterval(() => {
      this.showIt(this.products[i], i)
      i++
      if (i === this.products.length) {
        clearInterval(this.inter)
      }
    }, 3000
    )
  },
  methods: {
    showIt: function (element, i) {
      element.showMe = true
    }
  }
}
</script>
<style>
p {
  font-size: 1.2em;
}
img {
  max-width: 60%;
}
li {
  font-size: 1.4em;
  text-align: left;
}

.slide-fade-enter-active {
  transition: all .3s ease;
}
.slide-fade-leave-active {
  transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}
.slide-fade-enter, .slide-fade-leave-to
/* .slide-fade-leave-active below version 2.1.8 */ {
  transform: translateX(10px);
  opacity: 0;
}
.container-word{
   display: flex;
}

</style>