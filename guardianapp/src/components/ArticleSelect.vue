<template lang="html">
  <select @change="articleSelected" >
    <option selected disabled></option>

    <option v-for="(article, index) in articles" :value ="index"> {{article.webTitle}} </option>

  </select>
</template>






<script>

import {eventBus} from '@/main.js';

export default {
  name: 'ArticlesSelect',
  props: ['Articles_prop'],
  methods: {
    articleSelected(event) {
    const selectedIndex = event.target.value;
    eventBus.$emit('article-selected', selectedindex )
  }
}
}
</script>








<style lang="css" scoped>
</style>
