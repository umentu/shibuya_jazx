<template lang="pug">
    div
        v-row
            v-col(
                cols="12"
            )
                v-sheet(
                    color="grey lighten-3"
                    width="3px"
                    height="120vh"
                ).jazzman.jazzman_back_0_pc
                v-sheet(
                    color="grey lighten-3"
                    width="30px"
                    height="120vh"
                ).jazzman.jazzman_back_1_pc
                v-sheet(
                    color="grey lighten-3"
                    width="100px"
                    height="120vh"
                ).jazzman.jazzman_back_2_pc
                v-sheet(
                    color="grey lighten-3"
                    width="400px"
                    height="140vh"
                ).jazzman.jazzman_back_3_pc
                v-img(
                    src="/jazzman/terai.png"
                    max-width="400px"
                ).jazzman.jazzman_photo_pc
                v-sheet(
                    color="purple darken-1"
                    width="300px"
                    height="100px"
                ).jazzman.jazzman_instrument_pc
                    v-row(
                        align="center"
                        justify="center"
                    )
                        v-col.align-center.pa-3.display-3 SAX
                v-sheet(
                    color="amber darken-1"
                    width="90%"
                    height="200px"
                ).jazzman.jazzman_name_pc.display-3.text-align-center.pa-3 寺井雄一 (Yuichi Terai)
                div(
                ).jazzman.jazzman_profile_pc 東京都生まれ。あいうえおかきくけこあいうえおかきくけこあいうえおかきくけこあいうえおかきくけこあいうえおかきくけこあいうえおかきくけこあいうえおかきくけこあいうえおかきくけこあいうえおかきくけこあいうえおかきくけこあいうえおかきくけこあいうえおかきくけこあいうえおかきくけこあいうえおかきくけこ

</template>

<script>
export default {
    props: {
        isView: {
            type: Boolean,
            default: true
        }
    },
    watch: {
        isView(val) {
            const jazzman = document.getElementsByClassName('jazzman')
            if (val == true) {
                for (let i = 0; i < jazzman.length; i++){
                    jazzman[i].classList.add('view')
                }
            } else {
                const jazzman = document.getElementsByClassName('jazzman')
                for (let i = 0; i < jazzman.length; i++){
                    jazzman[i].classList.remove('view')
                }
            }
        }
    }
}
</script>

<style lang="stylus">
.jazzman_back_0_pc {
    position: absolute;
    right: 0;
    z-index: 10;
    opacity: 0;
}

.jazzman_back_0_pc.view {
    text-align: right;
    -webkit-transition: all 0.1s;
    transform: skew(10deg, 10deg) translate(-1100px, -10vh);
    opacity: 0.5;
}

.jazzman_back_1_pc {
    position: absolute;
    right: 0;
    z-index: 10;
    opacity: 0;
}

.jazzman_back_1_pc.view {
    text-align: right;
    -webkit-transition: all 0.3s;
    transform: skew(10deg, 10deg) translate(-850px, -10vh);
    opacity: 0.4;
}

.jazzman_back_2_pc {
    position: absolute;
    right: 0;
    z-index: 10;
    opacity: 0;
}

.jazzman_back_2_pc.view {
    text-align: right;
    -webkit-transition: all 0.5s;
    transform: skew(10deg, 10deg) translate(-600px, -10vh);
    opacity: 0.3;
}

.jazzman_back_3_pc {
    position: absolute;
    right: 0;
    z-index: 10;
    opacity: 0;
}

.jazzman_back_3_pc.view {
    text-align: right;
    -webkit-transition: all 0.6s;
    transform: skew(10deg, 10deg) translate(-100px, -10vh);
    opacity: 0.2;
}

.jazzman_photo_pc {
    position: absolute;
    right: 0;
    z-index: 20;
    opacity: 0;
    transform: translate(200px, 0);
}

.jazzman_photo_pc.view {
    text-align: right;
    -webkit-transition: all 1s;
    -webkit-transform: translate(-200px, 0);
    opacity: 1;
}

.jazzman_name_pc {
    position: absolute;
    z-index: 30;
    transform: skew(-10deg, -10deg);
    -webkit-transform: translate(-100px, 0);
    opacity: 0;
}

.jazzman_name_pc.view {
    text-align: center;
    -webkit-transition: all 0.8s;
    transform: skew(-10deg, -10deg) translate(0, 80vh);
    opacity: 1;
}

.jazzman_instrument_pc {
    position: absolute;
    bottom: 0px;
    left: -100px;
    z-index: 40;
    opacity: 0;
}

.jazzman_instrument_pc.view {
    text-align: center;
    -webkit-transition: all 0.6s;
    -webkit-transform: skew(-10deg, -10deg) translate(200px, 0);
    opacity: 1;
}

.jazzman_profile_pc {
    position: absolute;
    left: 100px;
    width: 50%;
    opacity: 0;
    z-index: 50;
}

.jazzman_profile_pc.view {
    -webkit-transition: all 3s;
    -webkit-transform: translate(0, 10vh);
    opacity: 1;
}
</style>
