<template>
    <div>
        <article class="media box">
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
                <article class="media">
                    <figure class="media-left">
                        <div class="image is-64x64">
                            <img :src="News[1].image" alt="">
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
                <article class="media">
                    <figure class="media-left">
                        <div class="image is-64x64">
                            <img :src="News[2].image" alt="">
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
                <article class="media">
                    <figure class="media-left">
                        <div class="image is-64x64">
                            <img :src="News[3].image" alt="">
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
            <div class="media-right">
                <a class="delete is-large"></a>
            </div>
        </article>
        <article class="media box   ">
            <figure class="media-left">
                <div class="image is-64x64">
                    <img :src="News[0].image" alt="">
                </div>
            </figure>
            <div class="media-content">
                <div class="field">
                    <p class="control">
                        <textarea name="" class="textarea" placeholder="Escribe tu mensaje"></textarea>
                    </p>
                </div>
                <div class="field">
                    <p class="control">
                        <button class="button is-primary is-pulled-right">
                            Enviar
                        </button>
                    </p>
                </div>
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

