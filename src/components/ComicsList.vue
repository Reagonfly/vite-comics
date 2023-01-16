<script>
    import AppJumbotron from './AppJumbotron.vue';
    import comicsData from '../assets/data/dataComics.js';

    export default {
        components:{
            AppJumbotron
        },
        data(){
            return{
                comics: comicsData
            }
        }
    }
</script>

<template lang="">
    <AppJumbotron />
    <div class="dark-bg">
        <div class="container">
            <div class="up-title">
                <h2 class="title">
                    Comics Series
                </h2>
            </div>
        </div>
       <div class="container">
            <div class="comics-cont">
                <div class="comics-card" v-for="(comic, index) in comics" :key="index">
                    <div class="thumb-cont">
                        <img :src="comic.thumb" class="thumb" :alt="comic.series">
                    </div>
                    <div class="title-cont">
                        <h4>{{ comic.series }}</h4>
                    </div>
                </div>
            </div>
        </div> 
    </div>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;

    .dark-bg{
        background-color: #1c1c1c;
    }

    .up-title{
        position: relative;
        
        .title{
            background-color: $primary-color;
            width: 200px;
            padding: 10px;
            text-align: center;
            color: $color-white;
            position: absolute;
            top: -20px;
            border: 1px solid black
        }
    }

    .comics-cont{
        @include flex-center;
        justify-content: space-between;
        flex-wrap: wrap;
        padding-top: 5rem;
        
        .comics-card{
            margin: 10px;
            width: calc(100% / 6 - 20px);
            margin-bottom: 40px;

            .thumb-cont{
                width: 100%;
                height: 100%;
                align-items: bottom;
            }
            
            .title-cont{
                margin-top: 10px;
                color: $color-white;
                text-align: center;
                padding: 10px;
                text-transform: uppercase;
            }
        }
    }
</style>