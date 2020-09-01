<template>
  <div>
    <section>
      <div class="story-line">
        <div class="container">
          <div class="row">
            <VueSlickCarousel
              class="story col-12 col-sm-12 col-md-12 col-lg-6 mb-4"
              style="max-height: auto;"
              v-bind="settings"
            >
              <div v-for="story in stories" :key="story.id">
                <div class="circle">
                  <a
                    v-on:click="callVideoSrc"
                    class="storyButton"
                    href="javascript:0"
                    :data-src="story.src"
                    @click="toggle"
                  >
                    <img :src="story.coverpic" draggable="false" alt="" />
                  </a>
                  <svg
                    viewBox="0 0 100 100"
                    xmlns="http://www.w3.org/2000/svg"
                    style="enable-background:new -580 439 577.9 194;"
                    xml:space="preserve"
                  >
                    <circle cx="50" cy="50" r="40" />
                  </svg>
                </div>
                <div class="col-12 text-center text-truncate text-light">
                  {{ story.name }}
                </div>
              </div>
            </VueSlickCarousel>
            <div class="col-12 col-sm-12 col-md-12 col-lg-6 mb-4 reklam-top">
              <img
                class="mh-100 mw-100"
                src="https://www.kirikkale24.com/wp-content/themes/un-haber-1/images/reklam-ver-1.gif"
                alt="reklam"
              />
            </div>
          </div>
        </div>
      </div>
      <!-- Modal -->
      <div
        class="modal fade"
        tabindex="-1"
        v-bind:class="{ show: show }"
        v-bind:style="modalStyle"
        @click="toggle"
      >
        <div class="modal-dialog modal-dialog-centered">
          <div class="modal-content">
            <!-- 16:9 aspect ratio -->
            <div class="embed-responsive embed-responsive-16by9">
              <iframe
                title="story"
                class="embed-responsive-item"
                :src="iframe.storyVideo"
                id="video"
                allowscriptaccess="always"
                allow="autoplay"
                aria-hidden="true"
              ></iframe>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section>
      <div class="container-fluid filter-part">
        <div class="row">
          <div class="col-xl-3 col-lg-4">
            <div class="filters bg-filters-desktop mb-3">
              <div class="filters-header p-3">
                <h6 class="m-0 text-light">Filter By</h6>
              </div>
              <div class="filters-body">
                <div id="accordion">
                  <div class="filters-card p-3">
                    <div class="filters-card-header">
                      <h6 class="mb-1">
                        <a
                          href="javascript:0"
                          class="btn-link text-light text-decoration-none"
                          @click="collapse1 = !collapse1"
                        >
                          Type
                          <icon name="arrow_down" class="float-right mt-1" />
                        </a>
                      </h6>
                    </div>
                    <div
                      class="collapse"
                      v-bind:class="{ show: collapse1 === true }"
                    >
                      <div class="filters-card-body card-shop-filters">
                        <div class="custom-control custom-checkbox">
                          <input
                            type="checkbox"
                            class="custom-control-input"
                            id="action"
                          />
                          <label class="custom-control-label" for="action"
                            >Action <small>156</small></label
                          >
                        </div>
                        <div class="custom-control custom-checkbox">
                          <input
                            type="checkbox"
                            class="custom-control-input"
                            id="adventure"
                          />
                          <label class="custom-control-label" for="adventure"
                            >Adventure <small>120</small></label
                          >
                        </div>
                        <div class="custom-control custom-checkbox">
                          <input
                            type="checkbox"
                            class="custom-control-input"
                            id="animation"
                          />
                          <label class="custom-control-label" for="animation"
                            >Animation <small>130</small></label
                          >
                        </div>
                        <div class="custom-control custom-checkbox">
                          <input
                            type="checkbox"
                            class="custom-control-input"
                            id="comedy"
                          />
                          <label class="custom-control-label" for="comedy"
                            >Comedy <small>120</small></label
                          >
                        </div>
                        <div class="custom-control custom-checkbox">
                          <input
                            type="checkbox"
                            class="custom-control-input"
                            id="crime"
                          />
                          <label class="custom-control-label" for="crime">
                            Crime <small>111</small></label
                          >
                        </div>
                        <div class="custom-control custom-checkbox">
                          <input
                            type="checkbox"
                            class="custom-control-input"
                            id="drama"
                          />
                          <label class="custom-control-label" for="drama">
                            Drama <small>95</small></label
                          >
                        </div>
                        <div class="custom-control custom-checkbox">
                          <input
                            type="checkbox"
                            class="custom-control-input"
                            id="FantasyD"
                          />
                          <label class="custom-control-label" for="FantasyD">
                            Fantasy <small>50</small></label
                          >
                        </div>
                        <div class="custom-control custom-checkbox">
                          <input
                            type="checkbox"
                            class="custom-control-input"
                            id="HistoricalD"
                          />
                          <label class="custom-control-label" for="HistoricalD">
                            Historical <small>32</small></label
                          >
                        </div>
                        <div class="custom-control custom-checkbox">
                          <input
                            type="checkbox"
                            class="custom-control-input"
                            id="RomanticD"
                          />
                          <label class="custom-control-label" for="RomanticD">
                            Romantic <small>156</small></label
                          >
                        </div>
                      </div>
                    </div>
                  </div>
                  <div class="filters-card p-3">
                    <div class="filters-card-header">
                      <h6 class="mb-1">
                        <a
                          href="javascript:0"
                          class="btn-link text-light text-decoration-none"
                          @click="collapse2 = !collapse2"
                        >
                          Select Language
                          <icon name="arrow_down" class="float-right mt-1" />
                        </a>
                      </h6>
                    </div>
                    <div
                      class="collapse"
                      v-bind:class="{ show: collapse2 === true }"
                    >
                      <div class="filters-card-body card-shop-filters">
                        <div class="custom-control custom-checkbox">
                          <input
                            type="checkbox"
                            class="custom-control-input"
                            id="RussianD"
                          />
                          <label class="custom-control-label" for="RussianD">
                            Russian <small>230</small>
                          </label>
                        </div>
                        <div class="custom-control custom-checkbox">
                          <input
                            type="checkbox"
                            class="custom-control-input"
                            id="EnglishD"
                          />
                          <label class="custom-control-label" for="EnglishD">
                            English <small>95</small>
                          </label>
                        </div>
                        <div class="custom-control custom-checkbox">
                          <input
                            type="checkbox"
                            class="custom-control-input"
                            id="TurkeyD"
                          />
                          <label class="custom-control-label" for="TurkeyD">
                            Turkey <small>35</small>
                          </label>
                        </div>
                      </div>
                    </div>
                  </div>
                  <div class="filters-card p-3">
                    <div class="filters-card-header">
                      <h6 class="mb-1">
                        <a
                          href="javascript:0"
                          class="btn-link text-light text-decoration-none"
                          @click="collapse3 = !collapse3"
                        >
                          Sorted by
                          <icon name="arrow_down" class="float-right mt-1" />
                        </a>
                      </h6>
                    </div>
                    <div
                      class="collapse"
                      v-bind:class="{ show: collapse3 === true }"
                    >
                      <div class="filters-card-body card-shop-filters">
                        <div class="custom-control custom-checkbox">
                          <input
                            type="checkbox"
                            class="custom-control-input "
                            id="RelevanceD"
                          />
                          <label class="custom-control-label" for="RelevanceD"
                            >Relevance
                          </label>
                        </div>
                        <div class="custom-control custom-checkbox">
                          <input
                            type="checkbox"
                            class="custom-control-input"
                            id="PriceLtHD"
                          />
                          <label class="custom-control-label" for="PriceLtHD"
                            >IMDB <small>(Low to Hig)</small>
                          </label>
                        </div>
                        <div class="custom-control custom-checkbox">
                          <input
                            type="checkbox"
                            class="custom-control-input"
                            id="PriceHtLD"
                          />
                          <label class="custom-control-label" for="PriceHtLD"
                            >IMDB <small>(High to Low)</small>
                          </label>
                        </div>
                        <div class="custom-control custom-checkbox">
                          <input
                            type="checkbox"
                            class="custom-control-input"
                            id="DiscountD"
                          />
                          <label class="custom-control-label" for="DiscountD"
                            >Discount <small>(A-Z)</small>
                          </label>
                        </div>
                        <div class="custom-control custom-checkbox">
                          <input
                            type="checkbox"
                            class="custom-control-input"
                            id="NameD"
                          />
                          <label class="custom-control-label" for="NameD"
                            >Name <small>(A-Z)</small>
                          </label>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="col-xl-9 col-lg-8">
            <div class="row" id="app">
              <div class="col-6 col-sm-4 col-md-4 col-xl-3 mb-4">
                <div class="card card-list">
                  <div class="card__cover">
                    <img
                      src="http://static3.businessinsider.com/image/511cffe5eab8ea1355000012-948-1445/new%20harry%20potter%20cover.jpg"
                      alt=""
                    />
                    <nuxt-link to="/stream" class="card__play">
                      <icon name="play_button" />
                    </nuxt-link>
                    <nuxt-link class="details" to="/detail">details</nuxt-link>
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
                      <a href="javascript:0">Action</a>
                      <a href="javascript:0">Triler</a>
                    </span>
                  </div>
                </div>
              </div>
            </div>
            <div class="col-12">
              <button id="loadMore">
                Load more
              </button>
            </div>
            <div class="text-center mt-1 mb-4 col-12 ">
              <div class="spinner-border text-light d-none" role="status">
                <span class="sr-only ">Loading...</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="section mt-1">
      <div class="container">
        <div class="row">
          <div class="col-12 text-white">
            <h2 class="section__title mt-1">
              <b>Film site</b> – Best movie website
            </h2>
            <p class="section__text ">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
              eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
              enim ad minim veniam, quis nostrud exercitation ullamco laboris
              nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in
              reprehenderit in voluptate velit esse cillum dolore eu fugiat
              nulla pariatur. Excepteur sint occaecat cupidatat non proident,
              sunt in culpa qui officia deserunt mollit anim id est laborum.
            </p>

            <p class="section__text">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
              eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
              enim ad minim veniam, quis nostrud exercitation ullamco laboris
              nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in
              reprehenderit in voluptate velit esse cillum dolore eu fugiat
              nulla pariatur. Excepteur sint occaecat cupidatat non proident,
              sunt in culpa qui officia deserunt mollit anim id est laborum.
            </p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
// optional style for arrows & dots
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";

export default {
  components: { VueSlickCarousel },
  data() {
    return {
      show: false,
      collapse1: true,
      collapse2: false,
      collapse3: false,
      iframe: {
        storyVideo: ""
      },
      settings: {
        slidesToShow: 5,
        slidesToScroll: 5,
        infinite: false,
        centerMode: false,
        responsive: [
          {
            breakpoint: 1024,
            settings: {
              slidesToShow: 4,
              slidesToScroll: 4
            }
          },
          {
            breakpoint: 600,
            settings: {
              arrows: false,
              slidesToShow: 3,
              slidesToScroll: 3,
              initialSlide: 3
            }
          },
          {
            breakpoint: 480,
            settings: {
              slidesToShow: 1,
              slidesToScroll: 1
            }
          }
        ]
      },
      stories: [
        {
          name: "The Witcher",
          coverpic:
            "https://th.bing.com/th/id/OIP.FAq6HY6_62GWDhj9RGhgwAHaHa?pid=Api&rs=1",
          src: "https://www.youtube.com/embed/ndl1W4ltcmg"
        },
        {
          name: "The Witcher",
          coverpic:
            "https://th.bing.com/th/id/OIP.FAq6HY6_62GWDhj9RGhgwAHaHa?pid=Api&rs=1",
          src: "https://www.youtube.com/embed/ndl1W4ltcmg"
        },
        {
          name: "The Witcher",
          coverpic:
            "https://th.bing.com/th/id/OIP.FAq6HY6_62GWDhj9RGhgwAHaHa?pid=Api&rs=1",
          src: "https://www.youtube.com/embed/ndl1W4ltcmg"
        },
        {
          name: "The Witcher",
          coverpic:
            "https://th.bing.com/th/id/OIP.FAq6HY6_62GWDhj9RGhgwAHaHa?pid=Api&rs=1",
          src: "https://www.youtube.com/embed/ndl1W4ltcmg"
        },
        {
          name: "The Witcher",
          coverpic:
            "https://th.bing.com/th/id/OIP.FAq6HY6_62GWDhj9RGhgwAHaHa?pid=Api&rs=1",
          src: "https://www.youtube.com/embed/ndl1W4ltcmg"
        },
        {
          name: "The Witcher",
          coverpic:
            "https://th.bing.com/th/id/OIP.FAq6HY6_62GWDhj9RGhgwAHaHa?pid=Api&rs=1",
          src: "https://www.youtube.com/embed/ndl1W4ltcmg"
        },
        {
          name: "The Witcher",
          coverpic:
            "https://th.bing.com/th/id/OIP.FAq6HY6_62GWDhj9RGhgwAHaHa?pid=Api&rs=1",
          src: "https://www.youtube.com/embed/ndl1W4ltcmg"
        }
      ]
    };
  },
  methods: {
    toggle() {
      this.show = !this.show;
      this.show ? null : (this.iframe.storyVideo = "");
    },
    callVideoSrc: function(event) {
      this.iframe.storyVideo =
        event.currentTarget.getAttribute("data-src") +
        "?autoplay=1&amp;modestbranding=1&amp;showinfo=0";
    }
  },
  computed: {
    modalStyle() {
      return this.show
        ? { display: "block", backgroundColor: "rgba(0,0,0,0.8)" }
        : {};
    }
  }
};
</script>
