<template>
    <div class="homepage">
      <header1></header1>
      <slider></slider>
      <div id="cat1"><category name="مردانه"></category></div>
      <div id="cat2"><category name="زنانه"></category></div>
      <div id="cat3"><category name="بچه‌گانه"></category></div>
      <news></news>
      <footer1></footer1>
    
    </div>
</template>


<script>
import footer1 from "@/components/footer1";
import news from "@/components/news";
import header1 from "@/components/header1";
import slider from "@/components/slider";
import category from "@/components/category";
export default {
  components: {
    footer1,
    header1,
    slider,
    category,
    news
  },
  head: {
    // To use "this" in the component, it is necessary to return the object through a function
    title: {
      inner: "clouthster"
    },
    meta: [
      { name: "viewport", content: "width=device-width, initial-scale=1" }
    ],
    script: [
      {
        src:
          "https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"
      },
      {
        src: "https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"
      }
    ],
    link: [
      {
        rel: "stylesheet",
        href:
          "https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css"
      }
    ]
  }
};
</script>

<style scoped>
@import "./CSSFiles/general.css";
.homepage{
    position: absolute;
    width: 1200px;
}

#cat3{
  position: absolute;
  top: 500px;
  right: 700px;
}

#cat2{
  position: absolute;
  top: 500px;
  right: 450px;
}

#cat1{
  position: absolute;
  top: 500px;
  right: 200px;
}

</style>
