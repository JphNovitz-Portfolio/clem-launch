<template>
    <div>
        <div class="text-center">
          <img src="./Klogo_clem.png" itemprop="logo" />
          <p>
          <span itemprop="legalName">La Clémentine <br /></span>
          <span itemprop="location">
          {{street}}
          <br />{{location}}
          </span>
          </p>
        </div>
    </div>
</template>

<script>
export default {
  name: 'logo',
  data () {
    return {
      street: 'Chaussée Roosvelt 101/2',
      location: '4420  Saint-Nicolas'
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
</style>