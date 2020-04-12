<template lang="pug">

    v-container
        v-btn(
            color="pink"
            @click="viewJazzman"
        ) ここを押すと表示
        Jazzman(
            :isView="isView"
        )
</template>

<script>

import Jazzman from '@/components/Jazzman'
export default {
    components: {
        Jazzman
    },
    data: () => ({
        isView: false
    }),
    methods: {
        viewJazzman() {
            this.isView = !this.isView
        }
    }
}
</script>

<style lang="stylus"></style>
