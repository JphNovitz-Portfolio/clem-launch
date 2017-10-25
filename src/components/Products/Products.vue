<template>
    <div>
        <div class="">
          <img src="" />
            <div class="container-word" >
              <div v-for="(product, index) in products"  :key="product" > 
                <transition name="slide">
                  <div v-show="products[index].showMe" class="word">
                      <i class="" aria-hidden="true"></i>
                      {{product.text}}
                  </div>
              </transition>
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
        { 'id': 1, 'text': 'Pain soleil aux sésames', 'showMe': false },
        { 'id': 2, 'text': 'Potages de saison', 'showMe': false },
        { 'id': 3, 'text': 'Sandwichs garnis fait maison', 'showMe': false },
        { 'id': 4, 'text': 'Service traiteur', 'showMe': false },
        { 'id': 5, 'text': 'Réunions entre amis ', 'showMe': false },
        { 'id': 6, 'text': 'Anniversaires', 'showMe': false },
        { 'id': 7, 'text': 'Fêtes d\'entreprises.', 'showMe': false }
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
    }, 1200
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

.slide-enter-active {
  transition: opacity .9s ease;
}
.slide-enter {
  opacity: 0;
}
.container-word{
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}
.word {
  padding: 0.5em;
  background-color: rgba(249,191,89, .2);
  color: rgb(235,94,0);
  font-size: large;
  border-radius: 10px;
  margin: .5em;
}

</style>