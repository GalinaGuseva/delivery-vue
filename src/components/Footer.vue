<template>
  <footer class="footer">
        <div class="container">
          <div class="footer-box">
            <router-link to="/" class="footer-logo logo">
              <img src="../assets/img/logo.png" alt="logo" />
            </router-link>
            <div class="footer-nav">
              <ul>
                <li><router-link to="/rest">Ресторанам</router-link></li>
                <li><router-link to="/rest">Курьерам</router-link></li>
                <li><router-link to="/rest">Пресс-центр</router-link></li>
                <li><router-link to="/rest">Контакты</router-link></li>
              </ul>
            </div>
            <div class="footer-social">
              <img src="../assets/img/social/instagram.png" alt="instagram" />
              <img src="../assets/img/social/facebook.png" alt="facebook" />
              <img src="../assets/img/social/vk.png" alt="vk" />
            </div>
          </div>
        </div>
      </footer>
</template>

<script>
export default {

}
</script>

<style>

</style>