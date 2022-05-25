<template>
  <footer>
    <div class="cols container">
      <div class="logo">
        <img src="../assets/logo-molisana.jpg" alt="logo">
      </div>
      <div class="footer-links">
        <h4>Pastificio</h4>
        <ul>
          <li>
            <a href="#">Il Pastificio</a>
          </li>
          <li>
            <a href="#">Grano</a>
          </li>
          <li>
            <a href="#">Filiera</a>
          </li>
          <li>
            <a href="#">100 Anni di Pasta</a>
          </li>
          <li>
            <a href="#">Storia della Pasta</a>
          </li>
        </ul>
      </div>
      <div class="footer-links">
        <h4>Prodotti</h4>
        <ul>
          <li>
            <a href="#">Le Classiche</a>
          </li>
          <li>
            <a href="#">Le Integrali</a>
          </li>
          <li>
            <a href="#">Le speciali</a>
          </li>
          <li>
            <a href="#">Le Biologiche</a>
          </li>
          <li>
            <a href="#">Le Gluten-free</a>
          </li>
        </ul>
      </div>
    </div>
    <div class="footer-pic">
      <!-- <img src="../assets/montagne-footer.jpg" alt="Le montagne del Molise"> -->
    </div>
  </footer>
</template>

<script>
export default {
  name: 'FooterComponent'
}
</script>

<style lang="scss" scoped>
  @import '../assets/style/_vars.scss';
  @import '../assets/style/_mixins.scss';
  footer {
    padding-top: 20px;
  }
  .cols {
    padding: 20px 0;
    display: flex;
    .logo, 
    .footer-links {
      flex-basis: calc(100% / 3);
      h4 {
        color: $primary-color;
        text-transform: uppercase;
        margin-bottom: 15px;
      }
      ul {
        list-style: none;
      }
      a {
        text-decoration: none;
        color: gray;
        display: inline-block;
        padding: 3px 0;
        font-size: 0.9rem;
        &:hover {
          color: $primary-color;
        }
      }
    }
  }
  .footer-pic {
    height: 100px;
    background-image: url('../assets/montagne-footer.jpg');
  }

</style>