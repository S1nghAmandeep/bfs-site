<script>

export default {


    data() {
        return {

        };
    },
    methods: {


    },
    mounted() {

    }
}
</script>

<template>
    <section class="hero">
        <div class="hero_body container">
            <div class="row justify-center">
                <div class="hero_card col-8">
                    <h1 class="hero_title ">Siamo Esperti <br> Nella <span class="orange-text">Lucidatura</span></h1>
                    <p class="hero_text">Far far away, behind the word mountains, far form th ecountries Vokalia and
                        Consonantia, there live
                        the blind texts. Separated the live in Bookmarksgrove right at the cost of the Semantics, a large
                        language ocean. Separated they live in Bookmarksgrove.
                    </p>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/parstials/variables' as*;

.hero {
    // background-color: $bg-light;
    // background-image: url(../blog3.jpg);

    .hero_body {
        background-image: url(../blog3.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        box-shadow: inset 0 0 0 1000px rgba(0, 0, 0, .4);
        padding: 150px 0 200px;
    }
}

.hero_card {
    color: $bg-light;

    .hero_title {
        font-size: 60px;
        font-weight: 600;
        line-height: 60px;
        padding-top: 10px;

        &::after {
            content: '';
            display: block;
            height: 4px;
            width: 50px;
            background-size: contain;
            background-repeat: no-repeat;
            background-image: url('/public/divider.png');
            margin: 35px 0;
        }
    }

    .hero_text {
        padding: 15px 0 50px;
        font-size: 18px;
    }

    .bottom-text {
        padding-top: 70px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .socials {
        gap: 10px;
        text-transform: uppercase;
        font-weight: 600;

        .tag:not(:last-child)::after {
            content: '-';
            display: inline-block;
            margin-left: 10px
        }
    }

    .slide-num {
        background: linear-gradient(90deg, #5f5f5f 0%, #2F2F2F 100%);
        font-size: 18px;
        color: $bg-grey;
        display: flex;
        align-items: center;
        cursor: pointer;
        border-radius: 50px;
        box-shadow: 3px 7px 20px rgba(0, 0, 0, 0.30);

        &>li {
            width: 50px;
            text-align: center;
        }

        .active {
            background: $bg-gradient;
            padding: 6px 18px;
            margin: 5px;
            border-radius: 50px;
        }
    }


}

div>h5 {
    color: $bg-green;
    font-size: 16px;
    font-weight: 200;
    letter-spacing: 5px;
    text-transform: uppercase;
}
</style>