// dependency: //
<template>
  <div class="index">
    <h1>篮球🏀</h1>
    <v-divider class="my-4"></v-divider>
    <h3>要领分享</h3>
    <h4 class="my-3">传切配合</h4>
    <p>
      传切配合是队员利用传球和切入组成的简单配合，是我们运用的最多的一种配合方式。它和简单的手递手，或者直接将球传给队友不同，分为两种一种是一传一切，一种是空切，掌握好要领的球员，可以很好的甩开防守，制造空位得分机会。
    </p>
    <h4>【配合方法】</h4>
    <p>
      一传一切：持球人5号将球传给1号，同时迅速向篮下切入，此时1号立刻将球回传给5号，无人盯防的5号可直接投篮得分。空切跑位：5号利用假动作抓住时机，迅速切入篮下摆脱防守球员，此刻1号将球传给无人盯防的5号，5号投篮得分。
    </p>
    <h4>【配合要点】</h4>
    <p>
      切入队员要掌握好切入时机，利用好假动作和速度，传球队员注意用假动作吸引牵制对手。
    </p>
    <v-divider class="my-4"></v-divider>
    <h3>我喜欢的球星: 科比</h3>
    <v-parallax class="my-5" dark :src="require('~/static/img/2.jpg')">
      <v-row align="center" justify="center">
        <v-col class="text-center" cols="12">
          <h1 class="display-1 font-weight-thin mb-4">Kobe Bryant</h1>
          <h4 class="subheading">Forever with us</h4>
        </v-col>
      </v-row>
    </v-parallax>
    <v-carousel
      cycle
      height="400"
      hide-delimiter-background
      show-arrows-on-hover
      interval="3000"
      class="mx-auto my-5"
    >
      <v-carousel-item v-for="(item, i) in images" :key="i">
        <v-sheet height="100%">
          <v-row class="fill-height" align="center" justify="center">
            <img
              height="400"
              :src="require(`~/static/img/${item}.jpg`)"
              alt=""
            />
          </v-row>
        </v-sheet>
      </v-carousel-item>
    </v-carousel>
  </div>
</template>

<script>
  export default {
    name: "index",
    components: {},
    data() {
      return {
        images: [3, 4, 6, 7],
      };
    },
    computed: {},
    watch: {},
    methods: {},
    created() {},
    mounted() {},
  };
</script>
<style scoped></style>
