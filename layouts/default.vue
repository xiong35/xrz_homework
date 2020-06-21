// dependency: //
<template>
  <v-app>
    <v-app-bar absolute>
      <v-avatar size="30" class="mr-3 d-md-block d-none">
        <img :src="require('~/static/img/avatar.png')" alt="avatar" />
      </v-avatar>
      <v-toolbar-title class="font-weight-black"
        >XRZ's Home</v-toolbar-title
      >
      <div class="mx-auto"></div>
    </v-app-bar>

    <v-main>
      <v-row class="pt-12 ma-3">
        <v-col class="col-3 pa-4 mt-12">
          <v-tabs
            v-model="tab"
            background-color="transparent"
            color="blue-grey darken-3"
            vertical
          >
            <v-tab to="/"><v-icon left>mdi-home</v-icon> 主页</v-tab>
            <v-tab to="web_study"
              ><v-icon left>mdi-web</v-icon> 网络学习</v-tab
            >
            <v-tab to="basketball"
              ><v-icon left>mdi-basketball</v-icon> 篮球!</v-tab
            >
            <v-tab @click="$router.go(-1)">
              <v-icon left>
                mdi-chevron-left-circle-outline
              </v-icon>
              后退
            </v-tab>
          </v-tabs>
        </v-col>
        <v-col class="col-9 pa-4 mt-7">
          <nuxt />
        </v-col>
      </v-row>
    </v-main>
  </v-app>
</template>

<script>
  export default {
    name: "default",
    components: {},
    data() {
      return {
        tab: 0,
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
