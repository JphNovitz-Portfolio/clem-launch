<template>
<div>
    <h2 class="color-orange">{{subtitle}}</h2>
    <h1>{{title}}</h1>
    <h3 class="bg-warning warning">{{warning}}</h3>
</div>
</template>

<script>
export default {
  name: 'headTitle',
  data () {
    return {
      title: 'La Clémentine aura le plaisir de vous faire découvrir ses délices:',
      subtitle: 'Dès le 6 novembre 2017',
      warning: 'Une douceur sucrée maison offerte à l\'achat d\'un sandwiche pour tous détenteur de ce bon (offre valable uniquement du 6 au 30 novembre 2017)  '
    }
  }
}
</script>

<style scoped>
.warning {
  padding: 1em;
  border-radius: 10px;
}
</style>