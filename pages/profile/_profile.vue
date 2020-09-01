<template>
  <div class="container mb-4">
    <div class="row">
      <div class="profile_List mt-2 col-12 col-xl-4 col-md-4">
        <nuxt-link :class="[!id ? 'active-list-button' : '']" to="/profile">
          <icon name="person" />Profile
        </nuxt-link>
        <nuxt-link
          :class="[id === 'followlist' ? 'active-list-button' : '']"
          to="/profile/followlist"
        >
          <icon name="star" />Follow list
        </nuxt-link>
        <nuxt-link
          :class="[id === 'setting' ? 'active-list-button' : '']"
          to="/profile/setting"
        >
          <icon name="setting" />setting
        </nuxt-link>
        <a href="javascript:0"> <icon name="sign_out" />Sign out </a>
      </div>
      <div class="profileDiv col-12 col-xl-8 col-md-8 " v-if="!id">
        <h1 style="color: #FD6060;">Profile</h1>
        <form method="POST" autocomplete="off">
          <input class="mb-3" type="text" name="name" placeholder="Your Name" />
          <input
            class="mb-3"
            type="password"
            name="password"
            placeholder="Your Password"
          />
          <input
            class="mb-3"
            type="email"
            name="email"
            placeholder="Your Email"
          />
          <input
            class="mb-3"
            type="password"
            name="password"
            placeholder="New Password"
          />
          <button>SEND</button>
        </form>
      </div>
      <div class="col-12 col-xl-8 col-md-8 " v-else-if="id === 'setting'">
        <h1 style="color: #FD6060;">Settings</h1>
      </div>
      <!-- whatch list div -->
      <div
        class="row whatch-list col-12 col-xl-8 col-md-8"
        v-else-if="id === 'followlist'"
      >
        <center
          style="width:100%;height:100px; font-size: 40px;margin: 0; color:#FD6060;
		    	display: block!important;"
        >
          Follow List
        </center>
        <div class="col-6 col-sm-6 col-md-6 col-xl-4 mb-4">
          <div class="card card-list">
            <div class="card__cover">
              <img
                src="http://static3.businessinsider.com/image/511cffe5eab8ea1355000012-948-1445/new%20harry%20potter%20cover.jpg"
                alt=""
              />
              <a href="#" class="card__play">
                <i class="fa fa-play" aria-hidden="true"></i>
              </a>
              <a class="details" href="moviedetail.html">details</a>
              <span class="card__rate"
                ><i class="fa fa-star" aria-hidden="true"></i> 8.4</span
              >
              <span class="card__year">2020</span>
            </div>
            <div class="card__content">
              <h3 class="card__title">
                <a href="#">I Dream in Another Language</a>
              </h3>
              <span class="card__category">
                <a href="#">Action</a>
                <a href="#">Triler</a>
              </span>
            </div>
          </div>
        </div>
        <div class="text-center mt-1 mb-4 col-12">
          <div class="spinner-border text-light" role="status">
            <span class="sr-only">Loading...</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      id: this.$route.params.profile,
      description_profile: "Profile ayarlari",
      title_profile: this.$route.params.profile === undefined ? 'Profile': 'Profile / ' + this.$route.params.profile,
    };
  },
  head() {
    return {
      title: this.title_profile + " - filmsite.com",
      meta: [{ name: "description", content: this.description_profile }]
    };
  }
};
</script>

<style></style>
