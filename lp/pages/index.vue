<template lang="pug">

    v-container
        v-row(
            justify="center"
            align="center"
        ).section.section_title.display-4 Shibuya Jazz
        v-divider
        v-row(
            justify="center"
            align="center"
        ).section.section_title.display-4 Concept
        v-divider
        v-row.section
            div.section_title.display-4 Member
            v-btn(
                color="pink"
                @click="viewJazzman"
            ) ここを押すと表示
            Jazzman(
                :isView="isView"
            )
        v-divider
        v-row(
            justify="center"
            align="center"
        ).section.section_title.display-4 Movie
        v-divider
        v-row(
            justify="center"
            align="center"
        ).section.section_title.display-4 Inquiry
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

<style lang="stylus">
.section {
    postion: relative;
    height: 100vh;
}

.section_title.display-4 {
    font-family: 'kimetsu' !important;
}

.section_title.display-3 {
    font-family: 'kimetsu' !important;
}
</style>
