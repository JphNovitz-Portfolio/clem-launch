<template>
    <div>
        <div class="text-center">
          <p>
           <span class="color-orange">{{opening}}</span>
          <br /><strong>{{phone}}</strong>
          
          </p>
          <p>
            <a v-bind:href="facebook"><i class="fa fa-facebook-official icon text-success" aria-hidden="true"></i></a>
            <a v-bind:href="instagram"><i class="fa fa-instagram icon text-success" aria-hidden="true"></i></a>

          </p>
          <img src="./la_clementine_sandwiches.jpg" />
        </div>
    </div>
</template>

<script>
export default {
  name: 'contact',
  data () {
    return {
      opening: 'Ouvert du lundi au vendredi, de 10h à 15h',
      phone: '0468 53 86 05',
      facebook: 'https://www.facebook.com/LaClementineausoleil/',
      instagram: 'http://www.instagram.com/laclementine.be'
    }
  }
}
</script>
<style scoped>
p{
  font-size: 1.4em;
  font-weight: 800;
}

  img {
    max-width: 60%;

  }

  .color-orange {
      background-color: inherit;
      color: #EB5E00;
  }

  .icon {
    font-size: 2em;
  }
</style>