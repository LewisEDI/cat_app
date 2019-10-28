<template lang="html">
<div>
  <h1>{{image}}</h1>
  <div id="picture">
        <!-- <cat-image :imageUrl="this.cat_url"></cat-image> -->
      </div>
</div>
</template>
<script>

export default {
  data(){
    return {
      image: null,
      cat_url: null
    }
  },
  components: {

  },
  mounted(){
    fetch('https://api.thecatapi.com/v1/images/search')
    .then(res => res.json())
    .then((fetchedData) => {
      this.image = fetchedData
      
    }
    )
  }
}
</script>

<style lang="css" scoped>
</style>
