<template>
  <div>
    <a-row v-for="(feature, j) in features" class="features" :key="feature.id">
      <a-col v-if="j % 2 == 0" :xs="2" :sm="4" :md="12" :lg="12" :xl="12">
        <img :src="require('../static/' + feature.img)" class="feauture-img img-even" />
      </a-col>
      <a-col :xs="2" :sm="4" :md="12" :lg="12" :xl="12" class="feature-desc">
        <h3>{{ feature.title }}</h3>
        <p>{{ feature.description }}</p>
        <a href="http://" class="desc-link">{{ feature.link }}</a>
      </a-col>
      <a-col v-if="j % 2 != 0" :xs="2" :sm="4" :md="12" :lg="12" :xl="12">
        <img :src="require('../static/' + feature.img)" class="feauture-img" />
      </a-col>
    </a-row>
  </div>
</template>
<script>
export default {
  name: "Features",
  data() {
    return {
      features: [
        {
          title: "Sell everywhere ",
          description:
            "Use one platform to sell products to anyone,anywhere—in person with Point of Sale and online through your website, social media, and online marketplaces.",
          link: "Explore ways to sell!",
          img: "sellEverywhere.png",
          id: 1,
        },
        {
          title: "Market your business",
          description:
            "Take the guesswork out of marketing with built-in tools that help you create, execute, and analyze digital marketing campaigns.",
          link: "Explore ways to market your business!",
          img: "marketYourBusiness.png",
          id: 2,
        },
      ],
    };
  },
};
</script>
<style scoped>
.feauture-img {
  margin-top: 4em;
  width: 20em;
  margin-left: 14em;
}
.img-even{
    margin-left: 3em;
}
a-row {
  margin-top: 3em;
  padding: 15px;
}
.feature-desc {
  width: 30em;
  margin-top: 3em;
}
.feature-desc p{
  font-size: 12px
}
.feature-desc h3{
  font-weight: bold;
}
.desc-link{
    color:#FFD335;
}
</style>