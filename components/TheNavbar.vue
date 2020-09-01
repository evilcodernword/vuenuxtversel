<template>
  <nav class="navbar navbar-expand-lg sticky-top mb-4" id="nav">
    <div class="container">
      <nuxt-link class="navbar-brand text-light" to="/">Logo</nuxt-link>
      <button
        class="navbar-toggler hamburger_button border-0"
        @click="toggleNavbar"
      >
        <div class="animated-icon1 border-0">
          <span></span><span></span><span></span>
        </div>
      </button>
      <div
        class="collapse navbar-collapse width"
        id="navbar"
        v-bind:class="{ show: navbarShow }"
      >
        <ul class="navbar-nav mr-auto">
          <li class="nav-item">
            <button
              class="navbar-toggler hamburger_button border-0 mt-2 mr-0"
              @click="toggleNavbar"
            >
              <div class="animated-icon1 border-0">
                <span></span><span></span><span></span>
              </div>
            </button>
          </li>
          <li class="nav-item dropdown profile-on-navbar">
            <a
              class="nav-link text-light dropdown-toggle"
              href="javascript:0"
              @click="toggleProfile"
            >
              Profile
            </a>
            <div class="dropdown-menu" v-bind:class="{ show: profileShow }">
              <nuxt-link class="dropdown-item" to="/profile"
                >Profile</nuxt-link
              >
              <nuxt-link to="/" class="dropdown-item">
                Notifications <span class="badge badge-light">400</span>
              </nuxt-link>
              <nuxt-link class="dropdown-item" to="/profile/followlist"
                >Follow list</nuxt-link
              >
              <nuxt-link class="dropdown-item" to="/profile/setting"
                >Setting</nuxt-link
              >
              <div class="dropdown-divider"></div>
              <a class="dropdown-item" href="javascript:0">Sign out</a>
            </div>
          </li>
          <li class="nav-item active">
            <nuxt-link class="nav-link text-light" to="/"
              >Home <span class="sr-only">(current)</span></nuxt-link
            >
          </li>
          <li class="nav-item">
            <nuxt-link class="nav-link text-light" to="/people"
              >People</nuxt-link
            >
          </li>
        </ul>
        <form class="navbar-form mr-1" role="search">
          <div class="input-group search-on-nav">
            <input
              type="text"
              class="form-control search-nav-bar"
              placeholder="Search"
              name="srch-term"
              id="srch-term"
            />
            <div class="input-group-btn search_button_header">
              <button class="btn search_button" type="submit">
                <icon name="search"></icon>
              </button>
            </div>
          </div>
        </form>
        <ul class="navbar-nav">
          <li class="nav-item">
            <nuxt-link
              type="button"
              to="/signup"
              class="nav-link btn signup_header"
              >SIGN UP</nuxt-link
            >
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      navbarShow: false,
      profileShow: false
    };
  },
  methods: {
    toggleNavbar() {
      this.navbarShow = !this.navbarShow;
    },
    toggleProfile() {
      this.profileShow = !this.profileShow;
    }
  }
};
</script>
