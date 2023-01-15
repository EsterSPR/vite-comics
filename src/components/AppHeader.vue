<script>
export default {
  data(){
    return {
        menuVoices: [
            {
                voice: 'CHARACTERS',
                link: '#',
                active: false,
            },
            {
                voice: 'COMICS',
                link: '#',
                active: true,
            },
            {
                voice: 'MOVIES',
                link: '#',
                active: false,
            },
            {
                voice: 'TV',
                link: '#',
                active: false,
            },
            {
                voice: 'GAMES',
                link: '#',
                active: false,
            },
            {
                voice: 'COLLECTIBLES',
                link: '#',
                active: false,
            },
            {
                voice: 'VIDEOS',
                link: '#',
                active: false,
            },
            {
                voice: 'FANS',
                link: '#',
                active: false,
            },
            {
                voice: 'NEWS',
                link: '#',
                active: false,
            },
            {
                voice: 'SHOP',
                link: '#',
                active: false,
            },
        ]
    }
  }
}
</script>

<template lang="">
  <header>
    <div class="container">
        <div class="navbar">
            <div class="logo">
                <img src="../../public/img/dc-logo.png" alt="dc-logo">
            </div>
            <nav>
                <ul>
                    <li v-for="(item, index) in menuVoices" :key="index" :class="item.active ? 'active' : ''">
                        <a :href="item.link">{{ item.voice }}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </div>
  </header>
</template>

<style lang="scss">
    @use '../styles/singles/variables' as *;
  .navbar{
    padding: 0 10%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-family: 'Roboto Condensed', sans-serif;
    font-weight: bolder;
    position: fixed;
    top: 0;
    width: 100vw;
    background-color: $dc-white;

    .logo img{
        height: 80px;
    }

    ul{
        list-style: none;
        display: flex;
    }
    
    li{
        padding: 50px 10px;
        color: $dc-grey;
    }

    li:hover{
        color: $dc-blue;
    }

    .active{
        color: $dc-blue;
        border-bottom: 5px solid $dc-blue;
    }
  }
</style>