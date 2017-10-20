<template>
    <div>
        <div class="text-center">
          <img src="" />
            <transition-group tag="ul" name="slider">
            <li v-for="product in products" :key="product"><i class="fa-li fa fa-hashtag" aria-hidden="true"></i>{{product}}</li>
            </transition-group>
          
        </div>
    </div>
</template>

<script>
export default {
  name: 'products',
  data () {
    return {
      products: [
        'Pain soleil au sésame',
        'Potages de saison',
        'Sandwiches garnis fait maison',
        'Service traiteur pour réunions entre amis , anniversaires, fêtes d\'entreprises.'

      ]
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
</style>