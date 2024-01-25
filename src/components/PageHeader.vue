<script>

import MenuHeader from './MenuHeader.vue';
import { store } from '../store';

export default {

    components: {
        MenuHeader,
    },

    data() {
        return {
            store,
            menu: [
                {
                    text: 'home',
                    href: '#'
                },
                {
                    text: 'about',
                    href: '#'
                },
                {
                    text: 'services',
                    href: '#'
                },
                {
                    text: 'showcase',
                    href: '#'
                },
                {
                    text: 'blog',
                    href: '#'
                },
                {
                    text: 'contacts',
                    href: '#'
                },
            ],
            menuBar: false,
        };
    },
    methods: {
        getMenuBar() {
            this.menuBar = !this.menuBar
            // console.log(this.menuBar);
        }
    },
}
</script>

<template>
    <header id="home">
        <nav class="row nav-bar container">
            <div>
                <ul class="row logo-items">
                    <li><img class="page-logo" src="/bfslogo.png" alt=""></li>
                    <li>
                        <h1 class="campony-name">BFS</h1>
                    </li>
                </ul>
            </div>
            <div>
                <MenuHeader class="row nav-items" :menu="menu" />
                <div @click="getMenuBar()" class="menu-bar">
                    <div>
                        <font-awesome-icon :icon="['fas', 'bars']" />
                    </div>
                </div>
                <div @click="getMenuBar()" :class="menuBar ? 'active' : ''" class="bg-menu">
                    <MenuHeader class="menu-bar-items" :menu="menu" />
                </div>
            </div>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/parstials/variables' as*;

header {
    background-color: $bg-white;
}

.nav-items {
    display: none;
}

.nav-bar {
    padding: 20px 40px;
    align-items: center;
    justify-content: space-between;
}


.campony-name {
    font-size: 30px;
    color: $bg-orange;
}

.menu-bar {
    cursor: pointer;
    font-size: 20px;

    &:hover {
        color: $bg-orange;
    }
}

.menu-bar-items {
    flex-direction: column;
    font-size: 40px;
    color: $bg-light;
    text-transform: uppercase;
    text-align: center
}

.bg-menu {
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: rgba($color: #0000006a, $alpha: 0.8);
    display: none;
    align-items: center;
    justify-content: center;
    z-index: 999;

    &.active {
        display: flex;
    }
}


// Small devices (landscape phones, 576px and up)
@media (min-width: 576px) {}

// Medium devices (tablets, 768px and up)
@media (min-width: 768px) {

    .nav-items {
        display: flex;
        gap: 30px;
        align-items: center;
        text-transform: uppercase;
        font-size: 18px;
    }

    .menu-bar {
        display: none;
    }


}

// Large devices (desktops, 992px and up)
@media (min-width: 992px) {}

// X-Large devices (large desktops, 1200px and up)
@media (min-width: 1200px) {}
</style>
