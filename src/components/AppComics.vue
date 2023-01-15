<script>
import comicsData from '../assets/data/dc-comics.json'

export default {
    data(){
        return{
            comics: comicsData
        }
    }
}
</script>

<template lang="">
    <div class="container">
        <h2 class="current-series">CURRENT SERIES</h2>
        <div class="comics-container">
            <div class="comic-card" v-for="(comic, index) in comics" :key="index">
                <a href="#">
                    <div class="thumb"><img :src="comic.thumb" :alt="comic.series"></div>
                    <br>
                    <p>{{comic.series}}</p>
                </a>
            </div>
        </div>
        <div class="load-more-container">
            <a href="#"><button class="load-more">LOAD MORE</button></a>
        </div>
    </div>
</template>

<style lang="scss" scoped>

@use '../styles/singles/variables' as *;
    .container{
        background-color: $dc-black;
        padding: 50px 10%;
        font-family: 'Roboto Condensed', sans-serif;
        color: $dc-white;
        position: relative;
        
        .current-series{
            background-color: $dc-blue;
            padding: 10px 25px;
            display: inline-block;
            position: absolute;
            top: -25px;
            z-index: 0;
        }
        .comics-container{
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;

            .comic-card {
                margin: 0 3px 50px 3px;
                width: 170px;
            }

            .thumb{
                height: 170px;
                overflow: hidden;
            }

            .thumb img{
                width: 170px;
            }

        }

        .load-more-container{
            width: 100%;
            text-align: center;
        }
        .load-more{
            background-color: $dc-blue;
            padding: 10px 70px;
            display: inline-block;
            border: none;
            font-family: 'Roboto Condensed', sans-serif;
            color: $dc-white;
            font-weight: bold;
            font-size: 13pt;
            border: 2px solid $dc-blue;
            transition: all 0.1s;
        }

        .load-more:hover{
            background-color: $dc-black;
            border: 2px solid $dc-blue;
            cursor: pointer;
        }
    }
</style>