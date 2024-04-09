<script>
import { store } from '../store';

export default {
    props: {
        menu: {
            type: Array,
            required: true
        },
    },

    data() {
        return {
            store,
        }
    },

    methods: {
    },

}
</script>

<template>
    <div>
        <ul v-for="link in menu">
            <li><a :href="link.href" @click="store.goToSection(link.text)">{{ link.text }}</a></li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/parstials/variables' as*;

a {
    border: 1px solid $bg-orange;
    padding: 4px 14px;
    border-radius: 50px;

    &:hover {
        color: $bg-white;
        background-color: $bg-orange;
        cursor: pointer;
    }
}


li {
    margin-bottom: 30px;
}


// Medium devices (tablets, 768px and up)
@media (min-width: 970px) {

    li {
        margin-bottom: 0;
    }

}
</style>