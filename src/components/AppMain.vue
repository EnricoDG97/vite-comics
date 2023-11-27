<script>
import AppBluebanner from "./AppBluebanner.vue";
import AppJumbotron from "./AppJumbotron.vue";
import AppSerieCard from "./AppSerieCard.vue";
export default {
  data() {
    return {
      cards: [
        {
          thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book",
        },
        {
          thumb:
            "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book",
        },
        {
          thumb:
            "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel",
        },
        {
          thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book",
        },
        {
          thumb:
            "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
          price: "$3.99",
          series: "Batman",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel",
        },
      ],
    };
  },
  methods: {},
  components: { AppBluebanner, AppJumbotron, AppSerieCard },
};
</script>

<template>
  <AppJumbotron />

  <section class="series-list centered">
    <div class="title">
      <h3>current series</h3>
    </div>
    <div class="series row">
      <div v-for="(card, index) in cards" :key="index" class="col">
        <AppSerieCard :image="card.thumb" :title="card.series"/>
      </div>
    </div>
    <div class="load-more">
      <button>
        <h3>load more</h3>
      </button>
    </div>
  </section>

  <AppBluebanner />
</template>

<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.series-list.centered {
  @include flex(row, start, center);
  color: white;
  font-size: xx-large;
  // test
  background-color: $primary-darkgrey;
  padding-top: 50px;
  padding-bottom: 50px;
  position: relative;
    .title {
      background-color: $primary-blue;
      padding: 8px 12px;
      position: absolute;
      top: -5%;
      left: 10%;
      box-shadow: -1px -5px 15px 5px #000000;
      h3 {
        text-transform: uppercase;
        color: white;
      }
    }
    .row {
    @include flex(row, center, center);
    flex-wrap: wrap;
      .col{
        width: calc(100% / 6);
        padding: 1rem;
      }
    }
    .load-more {
      button {
        text-align: center;
        width: 200px;
        background-color: $primary-blue;
        border-radius: 8px;
        padding: 8px 12px;
        border: none;
        h3 {
          text-transform: uppercase;
          color: white;
        }
      }
      bottom: 2%;
      position: absolute;
      left: calc(50% - 100px );
    }
}
</style>
