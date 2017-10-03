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

        <div class="tile is-ancestor">
            <div class="tile is-vertical is-8">
                <div class="tile">
                    <div class="tile is-parent">
                        <div class="tile is-child">
                            <figure class="image is-square content">
                                <img :src="News[0].image" alt="">
                            </figure>
                        </div>
                    </div>
                    <div class="tile is-parent">
                        <div class="tile is-child">
                            <h1 class="title">{{News[0].title}}</h1>
                            <p>{{News[0].content}}</p>
                        </div>
                    </div>
                </div>
                <div class="tile">
                    <div class="tile is-parent">
                        <div class="tile is-child">
                            <h1 class="title">{{News[1].title}}</h1>
                            <p>{{News[1].content}}</p>
                        </div>
                    </div>
                    <div class="tile is-parent">
                        <div class="tile is-child">
                            <figure class="image is-square content">
                                <img :src="News[1].image" alt="">
                            </figure>
                        </div>
                    </div>
                </div>
                <div class="tile is-parent">
                    <div class="tile is-child">
                        <h1 class="title">{{News[3].title}}</h1>
                        <p>{{News[3].content}}</p>
                    </div>
                </div>
            </div>
            <div class="tile is-vertical">
                <div class="tile is-parent">
                    <div class="tile is-child">
                        <h1 class="title">{{News[2].title}}</h1>
                        <p>{{News[2].content}}</p>
                        <p>{{News[2].content}}</p>
                        <p>{{News[2].content}}</p>
                    </div>
                </div>
                <div class="tile">
                    <div class="tile is-parent">
                        <div class="tile is-child">
                            <figure class="image is-square content">
                                <img :src="News[2].image" alt="">
                            </figure>
                        </div>
                    </div>
                </div>

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

