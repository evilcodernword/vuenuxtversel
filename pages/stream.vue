<template>
  <div class="commonDiv mb-4">
    <iframe height="450px" src="https://www.youtube.com/embed/wtb4z9IUY88">
    </iframe>

    <div class="yorumDiv">
      <p class="yorumYap">Bu Filme Yorum Yap</p>
      <form name="yorumForm" class="yorumForm" title="yorum yap">
        <textarea placeholder="Yorum Yap"></textarea>
        <label
          style="display: block;color: #FF0000;margin-top: 5px;font-size: 14px;margin-left: 20px;height: 45px;"
          >Filmle ilgili sürpriz bir detay vereceğiniz zaman spoiler içine
          alınız.</label
        >

        <button>GONDER</button>

        <button>SPOILER</button>
      </form>
    </div>

    <div class="yorumlarFilm">
      <p class="pYorum2">Bu Filme Yapilan Yorumlar:</p>
      <div class="Yorum">
        <span>Username</span>Henuz Hic Yorum Yok Henuz Hic Yorum Yok Henuz Hic
        Yorum Yok Henuz Hic Yorum Yok

        <div class="actionsOfComments">
          <a
            style="text-decoration:none;display: inline; color: blue;width: 30px;height: 30px;font-size: 20px"
            href="#"
            ><i class="fa fa-thumbs-up" aria-hidden="true"></i
            ><mark style="background-color: transparent;color: white"
              >1</mark
            ></a
          >
          <a
            style="text-decoration:none;  margin-top: 20px!important; color: blue;width: 30px;height: 30px;font-size: 20px"
            href="#"
            ><i
              style="transform: rotate(180deg);color: red"
              class="fa fa-thumbs-up"
              aria-hidden="true"
            ></i
            ><mark style="background-color: transparent;color: white"
              >2</mark
            ></a
          >

          <button
            style="margin-top: -10px; margin-left: 10px;background-color: #0000FF;color: whitesmoke;border:none;border-radius: 7px;padding: 2px 6px 2px 6px!important;"
          >
            cevapla
          </button>
        </div>
      </div>

      <div class="Yorum">
        <span>Username</span>Henuz Hic Yorum Yok

        <div class="actionsOfComments">
          <a
            style="text-decoration:none;display: inline; color: blue;width: 30px;height: 30px;font-size: 20px"
            href="#"
            ><i class="fa fa-thumbs-up" aria-hidden="true"></i
            ><mark style="background-color: transparent;color: white"
              >1</mark
            ></a
          >
          <a
            style="text-decoration:none;  margin-top: 20px!important; color: blue;width: 30px;height: 30px;font-size: 20px"
            href="#"
            ><i
              style="transform: rotate(180deg);"
              class="fa fa-thumbs-up"
              aria-hidden="true"
            ></i
            ><mark style="background-color: transparent;color: white"
              >2</mark
            ></a
          >

          <button
            style="margin-top: -10px; margin-left: 10px;background-color: #0000FF;color: whitesmoke;border:none;border-radius: 7px;padding: 2px 6px 2px 6px!important;"
          >
            cevapla
          </button>
        </div>
      </div>

      <div class="Yorum">
        <span>Username</span>Henuz Hic Yorum Yok

        <div class="actionsOfComments">
          <a
            style="text-decoration:none;display: inline; color: blue;width: 30px;height: 30px;font-size: 20px"
            href="#"
            ><i class="fa fa-thumbs-up" aria-hidden="true"></i
            ><mark style="background-color: transparent;color: white"
              >1</mark
            ></a
          >
          <a
            style="text-decoration:none;  margin-top: 20px!important; color: blue;width: 30px;height: 30px;font-size: 20px;"
            href="#"
            ><i
              style="transform: rotate(180deg);"
              class="fa fa-thumbs-up"
              aria-hidden="true"
            ></i
            ><mark style="background-color: transparent;color: white"
              >2</mark
            ></a
          >

          <button
            style="margin-top: -10px; margin-left: 10px;background-color: #0000FF;color: whitesmoke;border:none;border-radius: 7px;padding: 2px 6px 2px 6px!important;"
          >
            cevapla
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      title_stream:'filmin adi - turkce alt yazi',
      description_stream:'aciklama blav blav blac',
    }
  },
  head() {
    return {
      title: this.title_stream + " - filmsite.com",
      meta: [{ name: "description", content: this.description_stream }]
    };
  }
};
</script>

<style></style>
