<script>
export default {
      data(){
        return{
            menuItems: [
                {
                    label: 'Characters',
                    url: '#',
                    active: false
                },
                {
                    label: 'Comics',
                    url: '#',
                    active: false
                },
                {
                    label: 'Movies',
                    url: '#',
                    active: false
                },
                {
                    label: 'TV',
                    url: '#',
                    active: false
                },
                {
                    label: 'Games',
                    url: '#',
                    active: true
                },
                {
                    label: 'Collectables',
                    url: '#',
                    active: false
                },
                {
                    label: 'Videos',
                    url: '#',
                    active: false
                },
                {
                    label: 'Fans',
                    url: '#',
                    active: false
                },
                {
                    label: 'News',
                    url: '#',
                    active: false
                },
                {
                    label: 'Shop',
                    url: '#',
                    active: false
                }
            ]
        }
      }
}
</script>

<template lang="">
  <header class="container">
    <div class="navbar">
        <div class="logo">
            <a href="#">
                <img src="https://www.dccomics.com/sites/all/themes/dc_comics_bp/logo.png" alt="DC Comics">
            </a>
        </div>
        <nav>
            <ul>
                <li v-for="(item, index) in menuItems" :key="index" :class="item.active ? 'active' :''">
                    <a :href="item.url" :class="item.active ? 'active' : ''">
                        {{ item.label }}
                    </a>
                </li>
            </ul>
        </nav>
    </div>
  </header>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    .navbar{
        @include flex-center;
        justify-content: space-between;
        margin: 1rem 0;
        height: 150px;
        margin: 1rem 0 0 0;

        nav{
            @include flex-center;
            height: 100%;

            ul{
                list-style: none;
                display: flex;
                height: 100%;
                            
                li{
                    @include flex-center;
                    padding: 10px;
                    height: 100%;

                    &.active,
                    &:hover{
                        border-bottom: $border-bottom-menu;
                        color: $primary-color;
                    }
                }

            }
        }
    }
</style>