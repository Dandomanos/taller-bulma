<template>
    <div>
        <article class="media">
            <figure class="media-left">
                <div class="image is-64x64">
                    <img :src="News[0].image" alt="">
                </div>
            </figure>
            <div class="media-content">
                <div class="content">
                    <p>
                        <strong>{{News[0].title}}</strong><br>
                        {{News[0].content}}
                    </p>
                </div>
            </div>
            <div class="media-right">
                <a class="delete is-large"></a>
            </div>
        </article>
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

