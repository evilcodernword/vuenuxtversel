<template>
  <section>
    <div class="container-fluid">
      <div class="row">
        <div class="col-xl-3 col-lg-3">
          <div class="p-3 widget shadow rounded mb-4 cover-img">
            <img
              src="https://evilcodernword.github.io/evilcodernword/dist/img/cover/Total-Film-Tenet-covers-1-600x819.webp"
              class="img-fluid img-fluid-temp rounded"
              alt="TENET"
            />
            <h1 class="h6 mb-0 mt-3 font-weight-bold text-light">Director</h1>
            <p class="text-gray-600">Christopher Nolan</p>
            <h1 class="h6 mb-0 mt-3 font-weight-bold text-light">Writers</h1>
            <p class="text-gray-600">Christopher Nolan</p>
            <h1 class="h6 mb-0 mt-3 font-weight-bold text-light">Starring</h1>
            <p class="text-gray-600">
              John David Washington, Robert Pattinson, Elizabeth Debicki
            </p>
          </div>
        </div>

        <div class="col-xl-9 col-lg-9">
          <div class="info-header shadow rounded mb-4">
            <div
              class="row d-flex align-items-center justify-content-between p-3"
            >
              <div class="col-lg-8 m-b-4">
                <h3 class=" mb-0 mt-0 font-weight-bold text-light">
                  Tenet (2020)
                </h3>
                <p class="mb-0">
                  <small class="text-muted"> Action, Sci-Fi </small>
                </p>
              </div>
              <div class="col-lg-4 text-left">
                <a href="#" class="d-sm-inline-block btn btn-danger shadow-sm">
                  Add to Watchlist</a
                >
                <a href="#" class="d-sm-inline-block btn btn-danger shadow-sm">
                  Follow</a
                >
              </div>
            </div>
          </div>

          <div class="info-header shadow rounded mb-4">
            <div
              class="row d-flex align-items-center justify-content-between p-3"
            >
              <div class="col-lg-7 m-b-4">
                <h1 class="h6 mt-2 text-light">
                  8,4 | 2020 | 2h 30min | Birleşik Krallık ve Amerika
                </h1>
              </div>
            </div>
          </div>

          <div class="p-3 widget shadow rounded mb-4 about-fs">
            <ul class="nav nav-tabs">
              <li class="nav-item">
                <a
                  class="nav-link text-light"
                  href="javascript:0"
                  v-bind:class="{ active: tab_detail === 1 }"
                  v-on:click="tab_detail = 1"
                  >Summary</a
                >
              </li>
              <li class="nav-item">
                <a
                  class="nav-link text-light"
                  href="javascript:0"
                  v-bind:class="{ active: tab_detail === 2 }"
                  v-on:click="tab_detail = 2"
                  >Cast
                </a>
              </li>
              <li class="nav-item">
                <a
                  class="nav-link text-light"
                  href="javascript:0"
                  v-bind:class="{ active: tab_detail === 3 }"
                  v-on:click="tab_detail = 3"
                  >Seasons
                </a>
              </li>
              <li class="nav-item">
                <a
                  class="nav-link text-light"
                  href="javascript:0"
                  v-bind:class="{ active: tab_detail === 4 }"
                  v-on:click="tab_detail = 4"
                  >Reviews</a
                >
              </li>
            </ul>
            <div class="tab-content">
              <div
                class="tab-pane fade text-justify mt-3"
                v-bind:class="[tab_detail === 1 ? 'active show' : '']"
              >
                <p class="text-light ">
                  Armed with only one word, Tenet, and fighting for the survival
                  of the entire world, a Protagonist journeys through a twilight
                  world of international espionage on a mission that will unfold
                  in something beyond real time.
                </p>
              </div>

              <div
                class="tab-pane fade"
                v-bind:class="[tab_detail === 2 ? 'active show' : '']"
              >
                <div class="row cast mt-4">
                  <div
                    class="col-lg-3 col-md-4 col-12"
                    v-for="(cast, index) in cast_detail"
                    :key="index"
                  >
                    <div class="artist-list mb-4">
                      <a class="d-flex align-items-center" href="javascript:0">
                        <div class="dropdown-list-image mr-3">
                          <img
                            class="rounded-circle"
                            width="50px"
                            height="50px"
                            :src="cast.img_src"
                            :alt="cast.name"
                          />
                          <div class="status-indicator bg-success"></div>
                        </div>
                        <div class="font-weight-bold">
                          <div class="text-truncate">{{ cast.name }}</div>
                          <div class="small text-gray-500">{{ cast.role }}</div>
                        </div>
                      </a>
                    </div>
                  </div>
                </div>
              </div>

              <div
                class="tab-pane fade"
                v-bind:class="[tab_detail === 3 ? 'active show' : '']"
              >
                <div class="row mt-4">
                  <div class="container-fluid">
                    <div class="row">
                      <div class="col-xl-12 col-lg-12">
                        <div
                          class="filters mb-3 seasons"
                        >
                          <div class="filters-body">
                            <div id="accordion">
                              <div class="filters-card p-3" v-for="(season, index) in seasons" :key="index">
                                <div
                                  class="filters-card-header"
                                >
                                  <h6 class="mb-1">
                                    <a
                                      href="#"
                                      class="btn-link collapsed text-light text-decoration-none"
                                    >
                                      Sezon {{ index + 1 }} :
                                    </a>
                                  </h6>
                                </div>
                                <div
                                  class="collapse show"
                                >
                                  <div class="filters-card-body">
                                    <div class="container mt-3">
                                      <ul
                                        class="list-group list-group-horizontal" v-for="(about, index_about) in season.about" :key='index_about'
                                      >
                                        <li class="list-group-item">
                                          <a href="#">bolum {{ index_about + 1 }}</a>
                                        </li>
                                        <li class="list-group-item">
                                          <p>{{about.title}}</p>
                                        </li>
                                        <li
                                          class="list-group-item text-gray-500"
                                        >
                                          <small>{{about.date}}</small>
                                        </li>
                                      </ul>
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>

              <div
                class="tab-pane fade"
                v-bind:class="[tab_detail === 4 ? 'active show' : '']"
              >
                <div class="mt-4 send-review">
                  <form name="sentMessage">
                    <div class="control-group form-group">
                      <div class="row">
                        <div class="col-12">
                          <textarea
                            id="review-send"
                            placeholder="Leave a review..."
                          ></textarea>
                          <div class="row mt-3">
                            <div class="col-12 d-flex justify-content-between">
                              <div class="custom-control custom-checkbox">
                                <input
                                  type="checkbox"
                                  class="custom-control-input"
                                  id="spoiler-btn"
                                />
                                <label
                                  class="custom-control-label text-light"
                                  for="spoiler-btn"
                                  >Spoiler var
                                </label>
                              </div>
                              <button
                                class="d-sm-inline-block btn btn-danger shadow-sm"
                              >
                                send
                              </button>
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </form>
                </div>
                <div class="card-body p-0 reviews-card mt-4">
                  <div class="media mb-4">
                    <img
                      class="d-flex mr-3 rounded-circle"
                      width="50px"
                      height="50px"
                      src="https://th.bing.com/th/id/OIP.FAq6HY6_62GWDhj9RGhgwAHaHa?pid=Api&rs=1"
                      alt=""
                    />
                    <div class="media-body">
                      <div class="mt-0 mb-1">
                        <span class="h6 mr-2 font-weight-bold text-light"
                          >Scarlett Johansson</span
                        >
                        <span class="text-gray-500"
                          ><i class="fa fa-calendar"></i> 2 saat once</span
                        >
                      </div>
                      <p class="text-light m-2">
                        Cras sit amet nibh libero, in gravida nulla. Nulla vel
                        metus scelerisque ante sollicitudin. Cras purus odio,
                        vestibulum in vulputate at, tempus viverra turpis. Fusce
                        condimentum nunc ac nisi vulputate fringilla. Donec
                        lacinia congue felis in faucibus.
                      </p>
                    </div>
                  </div>
                  <div class="media mt-4">
                    <img
                      class="d-flex mr-3 rounded-circle"
                      width="50px"
                      height="50px"
                      src="https://th.bing.com/th/id/OIP.FAq6HY6_62GWDhj9RGhgwAHaHa?pid=Api&rs=1"
                      alt=""
                    />
                    <div class="media-body">
                      <div class="mt-0 mb-1">
                        <span class="h6 mr-2 font-weight-bold text-light"
                          >Bill Gates</span
                        >
                        <span class="text-gray-500"
                          ><i class="fa fa-calendar"></i> Avg 15, 2020</span
                        >
                      </div>
                      <p class="text-light m-2">
                        Cras sit amet nibh libero, in gravida nulla. Nulla vel
                        metus scelerisque ante sollicitudin. Cras purus odio,
                        vestibulum in vulputate at, tempus viverra turpis. Fusce
                        condimentum nunc ac nisi vulputate fringilla. Donec
                        lacinia congue felis in faucibus.
                      </p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      description_detail: "Tenet izle ucretsiz",
      title_detail: "Tenet (2020) izle | turkce alt yazili",
      tab_detail: 3,
      tab_detail_season: 1,
      seasons:[
        {number:'1',about:[
          {title:'plot',date:'11 ekim 2020'},
          {title:'king is back',date:'12 ekim 2020'},
          {title:'strikes back',date:'14 ekim 2020'},]},
        {number:'2',about:[
          {title:'plot',date:'11 ekim 2021'},
          {title:'night king',date:'15 ekim 2021'},
          {title:'new hope',date:'18 ekim 2021'},
          {title:'new hope',date:'18 ekim 2021'},
          {title:'new hope',date:'18 ekim 2021'},]},
        
      ],
      cast_detail: [
        {
          img_src:
            "https://th.bing.com/th/id/OIP.FAq6HY6_62GWDhj9RGhgwAHaHa?pid=Api&rs=1",
          name: "Kavil Henry",
          role: "acting"
        },
        {
          img_src:
            "https://th.bing.com/th/id/OIP.FAq6HY6_62GWDhj9RGhgwAHaHa?pid=Api&rs=1",
          name: "Kavil Henry",
          role: "bash rol"
        },
        {
          img_src:
            "https://th.bing.com/th/id/OIP.FAq6HY6_62GWDhj9RGhgwAHaHa?pid=Api&rs=1",
          name: "Kavil Henry",
          role: "2ci "
        },
        {
          img_src:
            "https://th.bing.com/th/id/OIP.FAq6HY6_62GWDhj9RGhgwAHaHa?pid=Api&rs=1",
          name: "Kavil Henry",
          role: "3cu "
        },
        {
          img_src:
            "https://th.bing.com/th/id/OIP.FAq6HY6_62GWDhj9RGhgwAHaHa?pid=Api&rs=1",
          name: "Kavil Henry",
          role: "yersiz"
        },
        {
          img_src:
            "https://th.bing.com/th/id/OIP.FAq6HY6_62GWDhj9RGhgwAHaHa?pid=Api&rs=1",
          name: "Kavil Henry",
          role: "evsiz"
        },
        {
          img_src:
            "https://th.bing.com/th/id/OIP.FAq6HY6_62GWDhj9RGhgwAHaHa?pid=Api&rs=1",
          name: "Kavil Henry",
          role: "king"
        },
        {
          img_src:
            "https://th.bing.com/th/id/OIP.FAq6HY6_62GWDhj9RGhgwAHaHa?pid=Api&rs=1",
          name: "Kavil Henry",
          role: "ragnar"
        },
        {
          img_src:
            "https://th.bing.com/th/id/OIP.FAq6HY6_62GWDhj9RGhgwAHaHa?pid=Api&rs=1",
          name: "Kavil Henry",
          role: "lorthbrok"
        }
      ]
    };
  },
  head() {
    return {
      title: this.title_detail + "- filmsite.com",
      meta: [{ name: "description", content: this.description_detail }]
    };
  }
};
</script>

<style></style>
