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
                <article class="media" v-for="(post, index) in replys" :key="index">
                    <figure class="media-left">
                        <div class="image is-64x64">
                            <img :src="post.image" alt="">
                        </div>
                    </figure>
                    <div class="media-content">
                        <div class="content">
                            <p>
                                <strong>{{post.title}}</strong><br>
                                {{post.content}}
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
                        <input name="" class="input" placeholder="Escribe un enunciado" v-model="title"></textarea>
                    </p>
                </div>
                <div class="field">
                    <p class="control">
                        <textarea name="" class="textarea" placeholder="Escribe tu mensaje" v-model="content"></textarea>
                    </p>
                </div>
                <div class="field">
                    <p class="control">
                        <button
                            class="button is-primary is-pulled-right"
                            :class="{'is-loading':loading, 'is-static':!dirty}"
                            @click="postMessage"
                        >
                            Enviar
                        </button>
                    </p>
                </div>
            </div>
        </article>
        <modal :class="{'is-active':modalActive}" @close="closeModal"></modal>
  </div>
</template>
<script>
import News from '../data/news.json'
import Modal from '@/components/Modal'
export default {
    data() {
        return {
            News,
            modalActive:false,
            loading:false,
            content:'',
            title:'',
            replys:[],
        }
    },
    components: {
        Modal
    },
    methods: {
        postMessage() {
            this.loading = true
            setTimeout(this.showModal,2000)
        },
        showModal() {
            this.modalActive = true
            this.loading = false
            this.replys.push(this.post)
            this.clearForm()
        },
        closeModal() {
            this.modalActive = false
        },
        clearForm() {
            this.content = this.title = ''
        }
    },
    computed: {
        dirty() {
            return this.content !== '' && this.title !== ''
        },
        post() {
            return {
                image: this.News[0].image,
                title: this.title,
                content: this.content,
            }
        }
    }
}
</script>

