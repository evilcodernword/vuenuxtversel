<template>
  <nav class="navbar navbar-expand-lg sticky-top mb-4" id="nav" v-click-outside="hideNavbar">
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
          <li
            class="nav-item dropdown profile-on-navbar"
            v-click-outside="hideProfile"
          >
            <a
              class="nav-link text-light dropdown-toggle"
              href="javascript:0"
              @click="toggleProfile"
            >
              Profile
            </a>
            <div class="dropdown-menu" v-bind:class="{ show: profileShow }">
              <nuxt-link
                class="dropdown-item"
                to="/profile"
                v-on:click.native="toggleProfile();hideNavbar();"
                >Profile</nuxt-link
              >
              <nuxt-link
                to="/"
                class="dropdown-item"
                v-on:click.native="toggleProfile();hideNavbar();"
              >
                Notifications <span class="badge badge-light">400</span>
              </nuxt-link>
              <nuxt-link
                class="dropdown-item"
                to="/profile/followlist"
                v-on:click.native="toggleProfile();hideNavbar();"
                >Follow list</nuxt-link
              >
              <nuxt-link
                class="dropdown-item"
                to="/profile/setting"
                v-on:click.native="toggleProfile();hideNavbar();"
                >Setting</nuxt-link
              >
              <div class="dropdown-divider"></div>
              <a class="dropdown-item" href="javascript:0" @click="alert"
                >Sign out</a
              >
            </div>
          </li>
          <li class="nav-item active">
            <nuxt-link class="nav-link text-light" to="/" v-on:click.native="hideNavbar"
              >Home <span class="sr-only">(current)</span></nuxt-link
            >
          </li>
          <li class="nav-item">
            <nuxt-link class="nav-link text-light" to="/people" v-on:click.native="hideNavbar"
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
              v-on:click.native="hideNavbar"
              >SIGN UP</nuxt-link
            >
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
import vClickOutside from "v-click-outside";

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
    hideNavbar() {
      this.navbarShow = false;
    },
    toggleProfile() {
      this.profileShow = !this.profileShow;
    },
    hideProfile() {
      this.profileShow = false;
    },
    alert() {
      alert("cikmak istediyinizden eminsinizmi ?");
    }
  }
};
</script>
