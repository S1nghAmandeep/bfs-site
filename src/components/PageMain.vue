<script>

import PageHero from './PageHero.vue';
import { store } from '../store';

export default {
    components: {
        PageHero,
    },

    data() {
        return {
            store,
            options: [
                {
                    icon: ['fas', 'gauge-high'],
                    title: 'Speed Optimization',
                    text: 'Far far away, behind the word ,ountains, far from the countries Vokalia Separated ...'
                },
                {
                    icon: ['fas', 'cloud'],
                    title: 'Cloud Sloutions',
                    text: 'Far far away, behind the word ,ountains, far from the countries Vokalia Separated ...'
                },
                {
                    icon: ['fas', 'tablet-screen-button'],
                    title: 'Website Design',
                    text: 'Far far away, behind the word ,ountains, far from the countries Vokalia Separated ...'
                },
                {
                    icon: ['fas', 'stopwatch'],
                    title: 'Online Marketing',
                    text: 'Far far away, behind the word ,ountains, far from the countries Vokalia Separated ...'
                }

            ],
            imgs: [
                '/img1.jpg',
                '/img2.jpg',
                '/img3.jpg',
                '/img4.jpg',
                '/img5.jpg',
                '/img6.jpg',
                '/img7.jpg',
                '/img8.jpg'
            ],

            news: [
                {
                    img: 'blog1.jpg',
                    date: 'May 24,2018 .by Alex',
                    title: 'Marketing ideas'
                },
                {
                    img: 'blog2.jpg',
                    date: 'May 24,2018 .by Alex',
                    title: 'Rest during working houres'
                },
                {
                    img: 'blog3.jpg',
                    date: 'May 24,2018 .by Alex',
                    title: 'Develop your startup idea'
                }
            ],

            logo: [
                '/client-1-2x.png',
                '/client-9-2x.png',
                '/client-7-2x.png',
                '/client-3-2x.png',
                '/client-4-2x.png',
                '/client-5-2x.png'
            ]
        }

    },
    methods: {
        topFunction() {
            document.body.scrollTop = 0;
            document.documentElement.scrollTo({
                top: 0,
                left: 0,
                behavior: 'smooth'
            })
        },
    },
    mounted() {
        const btn = document.getElementById('goHome')
        document.addEventListener("scroll", () => {
            if (document.documentElement.scrollTop > 500) {
                window.requestAnimationFrame(() => {
                    btn.classList.add('active')
                });
            }
            document.getElementById('goHome').classList.remove('active')

        });
    }
}
</script>

<template>
    <main>
        <PageHero />
        <div id="goHome" @click="topFunction()">&uparrow;</div>
        <!-- inizio sezione 1 -->
        <section id="services" class="section-one">
            <div class="container">
                <div class="row">
                    <div class="col-4">
                        <h1 class="titles caps-letter space-top space-bottom">
                            Siamo esperti nel<br>rendere il tuo <span class="orange-text">prodotto</span> di ottima
                            <span class="orange-text">qualità</span> e dettalita!
                        </h1>
                    </div>
                    <div class="col-8 row">
                        <div class="col-6" v-for="(card, i) in options">
                            <div class="card">
                                <ul>
                                    <li class="card-icon">
                                        <font-awesome-icon :icon="card.icon" />
                                    </li>
                                    <li>
                                        <h2 class="card-title">{{ card.title }}</h2>
                                    </li>
                                    <li>
                                        <p class="text">
                                            {{ card.text }}
                                        </p>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- inizio sezione 2 -->

        <section class="section-two" id="about">
            <div class="container">
                <div class="row card-about">
                    <div class="col-6 imgs-about">
                        <img class="about-img" src="/lisa.jpg" alt="">
                    </div>
                    <div class="col-6">
                        <div class="about-text">
                            <h1 class="titles space-top">learn more about <br> our <span class="green-text">missions</span>
                            </h1>
                            <p class="text">Far far away, behind the word mountains, far form th ecountries Vokalia and
                                Consonantia, there live
                                the blind texts. Separated the live in Bookmarksgrove right at the cost of the Semantics, a
                                large
                                language ocean. Separated they live in Bookmarksgrove.
                            </p>
                            <button class="button">Read more</button>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- inizio sezione 3 -->

        <section class="section-three">
            <div class="container">
                <div class="row justify-center">
                    <div class="col-6">
                        <h1 class="titles divider">Our recent <span class="green-text">web designs</span> & <br>some
                            examples of
                            <br>past
                            <span class="green-text">projects</span>
                        </h1>
                    </div>
                    <div class="col-6 projects-text" id="showcase">
                        <p class="text">Far far away, behind the word mountains, far form th ecountries Vokalia and
                            Consonantia, there live
                            the blind texts. Separated the live in Bookmarksgrove right at the cost of the Semantics, a
                            large
                            language ocean. Separated they live in Bookmarksgrove. Far far away, behind the word mountains.
                            Separated the live in Bookmarksgrove
                        </p>
                    </div>
                    <div class="col-12 project-img-card-body">
                        <div class="col-3 project-img-card" v-for="img in imgs">
                            <img class="project-img" :src="img" alt="">
                            <div class="project-info">
                                <h2>Here goes the text</h2>
                                <p>Here goes the sector</p>
                            </div>
                        </div>
                    </div>
                    <button class="button">Read more</button>
                </div>
            </div>
        </section>


        <!-- inizio sezione 4 -->

        <section class="section-four" id="blog">
            <div class="container">
                <div class="blog-card-body ">
                    <h1 class="sect-four-title caps-letter">Latest news & our <span class="green-text">blog</span></h1>
                    <div class="row space-bottom">
                        <div class="col-4 blog-card" v-for="blog in news">
                            <img class="blog-card_img" :src="blog.img" alt="">
                            <div class="blog-card_info">
                                <p class="blog-card-date">{{ blog.date }}</p>
                                <h3 class="blog-card-title"><span class="dot">&#x2022;</span>{{ blog.title }}</h3>
                            </div>
                        </div>
                    </div>
                    <button class="button bg-black blog-btn">View all post</button>
                </div>
                <div class="row">
                    <div class="col-2 client-logo" v-for="img in logo">
                        <img class="client-logo-img" :src="img" alt="">
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
@use"../styles/main.scss"
</style>