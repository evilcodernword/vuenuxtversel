<template>
  <main>
    <header class="profile-header p-3">
      <h1>Oyuncular</h1>
      <p>
        En iyi Amerikan oyucularindan, en genc erkek aktorlere, Hollywoodun en
        guzel kadin aktorlerinden, en yeni oyunculara kadar tum yabanci film ve
        yabanci dizi aktorleri yabanci oyuncular sayfasiyla takip et.
      </p>
    </header>
    <section class="profile-section mb-4">
      <div class="box-area-1">
        <div class="bg-img-1"></div>
        <div class="img-text">
          <p>Samuel L.Jackson</p>
          <span>68 icerik</span>
        </div>
      </div>
      <div class="box-area-1">
        <div class="bg-img-1"></div>
        <div class="img-text">
          <p>Frank Welker</p>
          <span>67 icerik</span>
        </div>
      </div>
      <div class="box-area-1">
        <div class="bg-img-1"></div>
        <div class="img-text">
          <p>Morgan Freeman</p>
          <span>57 icerik</span>
        </div>
      </div>
      <div class="box-area-1">
        <div class="bg-img-1"></div>
        <div class="img-text">
          <p>Bruce Willis</p>
          <span>54 icerik</span>
        </div>
      </div>
      <div class="box-area-1">
        <div class="bg-img-1"></div>
        <div class="img-text">
          <p>Nicolas Cage</p>
          <span>54 icerik</span>
        </div>
      </div>
      <div class="box-area-1">
        <div class="bg-img-1"></div>
        <div class="img-text">
          <p>Robert De Niro</p>
          <span>53 icerik</span>
        </div>
      </div>
      <div class="box-area-1">
        <div class="bg-img-1"></div>
        <div class="img-text">
          <p>Johnny Depp</p>
          <span>51 icerik</span>
        </div>
      </div>
      <div class="box-area-1">
        <div class="bg-img-1"></div>
        <div class="img-text">
          <p>Danny Trejo</p>
          <span>47 icerik</span>
        </div>
      </div>
      <div class="box-area-1">
        <div class="bg-img-1"></div>
        <div class="img-text">
          <p>Tom Hanks</p>
          <span>38 icerik</span>
        </div>
      </div>
      <div class="box-area-1">
        <div class="bg-img-1"></div>
        <div class="img-text">
          <p>Keanau Reeves</p>
          <span>35 icerik</span>
        </div>
      </div>
    </section>
    <section class="profile-pagination" id="profile-pagination">
      <a href="#">&laquo;</a>
      <a href="#" class="active-page">1</a>
      <a href="#">2</a>
      <a href="#">3</a>
      <a href="#">4</a>
      <a href="#">&raquo;</a>
    </section>
  </main>
</template>

<script>
export default {
  data() {
    return {
      description_detail: "Oyuncular",
      title_detail: "Oyuncular | Yabanci | Turk"
    };
  },
  head() {
    return {
      title: this.title_detail + " - filmsite.com",
      meta: [{ name: "description", content: this.description_detail }]
    };
  }
};
</script>

<style></style>
