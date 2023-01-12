<script>
export default {
  data(){
    return{
      navbarMenu:[
        {
          label: 'CHARACTERS',
          url: '#',
          active: false,
        },
        {
          label: 'COMICS',
          url: '#',
          active: true,
        },
        {
          label: 'MOVIES',
          url: '#',
          active: false,
        },
        {
          label: 'TV',
          url: '#',
          active: false,
        },
        {
          label: 'GAMES',
          url: '#',
          active: false,
        },
        {
          label: 'COLLECTIBLES',
          url: '#',
          active: false,
        },
        {
          label: 'VIDEOS',
          url: '#',
          active: false,
        },
        {
          label: 'FANS',
          url: '#',
          active: false,
        },
        {
          label: 'NEWS',
          url: '#',
          active: false,
        },
        {
          label: 'SHOP',
          url: '#',
          active: false,
        },
      ]
    }
  }
}
</script>

<template lang="">
  <header>
    <div class="header-container">
      <a href="/" class="brand">
        <img src="/img/dc-logo.png" alt="" srcset="">
      </a>
      <nav>
        <ul>
          <li v-for="(item,index) in navbarMenu" :key="index">
            <a :href="item.url" :class="(item.active == true) ? 'active' : ''">{{ item.label }}</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style lang="scss">
  @use '../styles/partials/variables' as * ;
  @use '../styles/partials/mixins' as * ;

  
  header {
    background-color: white;

    nav{
      display: flex;
      justify-content: flex-end;
      height: 100%;
    }

    ul{
      list-style: none;
      height: 100%;
      @include flex-align
    }
    li{
      height: 100%;
      @include flex-align;
      a{
        display: inline-block;
      margin: 1rem;
      text-decoration: none;
      color: $GreyTextColor;
      transition: border-bottom 0.3s;
      font-weight: bold;
      }

      &.active,&:hover{
        border-bottom: 5px solid $DCblue;
        color: $DCblue
      }

    }
  }

  .header-container {
    @include flex-align;
    @include borderPage;
    height: 150px;
    justify-content: space-between;
  } 
</style>
