<template>
  <footer class="footer">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <div class="footer__content">
            <span class="footer__copyright"
              >© 2020 evilfilm<br />
              Create by
              <a
                href="https://www.youtube.com/"
                target="_blank"
                >Evil Coder</a
              >
            </span>

            <nav class="footer__nav">
              <nuxt-link to="/contacts">About Us</nuxt-link>
              <nuxt-link to="/contacts">Contacts</nuxt-link>
              <nuxt-link to="/">Privacy Policy</nuxt-link>
            </nav>

            <a class="footer__back" href="javascript:0" @click="toTop">
              <icon name="arrow_up" />
            </a>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  methods: {
    toTop() {
      window.scrollTo(0, 0);
    }
  }
};
</script>

<style></style>
