<template>
  <header>
    <img src="../assets/logo-molisana.jpg" alt="Logo La Molisana">
    <nav>
      <ul>
        <li v-for="(item, index) in menu" :key="`menu-${index}`">
          <a :class="{'active': item.isActive}" href="#">{{item.name}}</a>
        </li>
        
      </ul>
    </nav>
  </header>
</template>



<script>
export default {
  name: 'HeaderComponent',
  props: {
    utente: String, 
    saluto: String,
    user: Object
  },
  data() {
    return{
      menu: [
        {
        href: '#', 
        name: 'Home', 
        isActive: 'false'
        },
        {
        href: '#', 
        name: 'Podotti', 
        isActive: 'true'
        },
        {
        href: '#', 
        name: 'Chi Siamo', 
        isActive: 'false'
        },
        {
        href: '#', 
        name: 'Contatti', 
        isActive: 'false'
        },
        {
        href: '#', 
        name: 'Home', 
        isActive: 'false'
        }
      ] 
    }
  }
}
</script>



<style lang="scss" scoped>

@import '../assets/style/_mixins.scss';
@import '../assets/style/_vars.scss';

header {
  .prova {
    background-color: red;
  }
  padding-bottom: 30px;
  img {
    margin-top: 15px;
    margin-bottom: 20px;
  }
  text-align: center; 
  nav {
    ul {
      @include menu;
    }
    a {
      text-decoration: none; 
      display: inline-block;
      padding: 15px;
      margin: 15px;
      color: $primary-color;
      &:hover,
      &.active {
        background-color: lighten($primary-color, 60%);
      }
    }

  }
}

</style>