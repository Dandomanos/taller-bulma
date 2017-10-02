<template>
  <div>
      <div class="columns">
        <div class="column" v-for="(item, index) in News" :key="index">
          <h1 class="title">{{item.title}}</h1>
          <figure class="image is-square content">
            <img :src="item.image" alt="">
          </figure>
          <p>{{item.content}}</p>
        </div>
      </div>
  </div>
</template>
<script>
import News from '../data/news.json'
export default {
    data() {
        return {
            News
        }
    }
}
</script>

