<template>
  <div class="index">
    <v-card class="mx-auto" hover max-width="800" outlined>
      <v-list-item three-line>
        <v-list-item-content>
          <div class="subtitle-2 mb-4">个人简介</div>
          <v-list-item-title class="headline mb-1">
            徐睿泽
          </v-list-item-title>
          <v-list-item-subtitle>
            机械科学与工程学院 1910
          </v-list-item-subtitle>
          <span class="mt-3">
            身高185, 体重185 <br />
            表面上胸无大志混吃等死, 实际上乐观开朗无忧无虑
          </span>
        </v-list-item-content>

        <v-list-item-avatar tile size="120">
          <v-img :src="require('~/static/img/me.jpg')"></v-img>
        </v-list-item-avatar>
      </v-list-item>

      <v-card-actions class="px-4">
        联系我:
        <v-btn text class="ml-2" color="black" @click="copy('q')">
          <v-icon left>mdi-qqchat</v-icon>
          qq
        </v-btn>
        <v-btn text color="black" @click="copy('v')">
          <v-icon left>mdi-wechat</v-icon>
          微信
        </v-btn>
        <v-snackbar
          top
          v-model="snackBarQ"
          color="success"
          :timeout="1400"
        >
          已复制QQ号到剪切板😉
        </v-snackbar>
        <v-snackbar
          top
          v-model="snackBarV"
          color="success"
          :timeout="1400"
        >
          已复制微信号到剪切板😉
        </v-snackbar>
      </v-card-actions>
    </v-card>

    <v-card max-width="800" hover outlined class="mx-auto">
      <v-subheader>学习分享</v-subheader>
      <p class="mx-4 headline">
        网络学习
      </p>

      <v-card-text>
        学海无涯, <del>回头是岸</del>要想学好, 除了要勤奋,
        还得有好的学习方法! <br />
        来看看我总结的学习经验吧!
      </v-card-text>

      <v-card-actions>
        <v-btn nuxt to="web_study" text color="deep-purple accent-4">
          了解更多
        </v-btn>
      </v-card-actions>
    </v-card>

    <v-card max-width="800" hover outlined class="mx-auto">
      <v-subheader>兴趣爱好</v-subheader>
      <p class="mx-4 headline">
        篮球🏀
      </p>

      <v-img :src="require('~/static/img/5.jpg')" height="410"></v-img>

      <v-card-text>
        你见过凌晨四点的洛杉矶吗?
      </v-card-text>

      <v-card-actions>
        <v-btn nuxt to="basketball" text color="deep-purple accent-4">
          了解更多
        </v-btn>
      </v-card-actions>
    </v-card>
  </div>
</template>

<script>
  export default {
    name: "index",
    components: {},
    data() {
      return {
        snackBarQ: false,
        snackBarV: false,
      };
    },
    computed: {},
    watch: {},
    methods: {
      copy(type) {
        let number = "";
        if (type === "q") {
          this.snackBarQ = true;
          number = "404675430";
        } else if (type === "v") {
          this.snackBarV = true;
          number = "xrz666404675430";
        }
        let textArea = document.createElement("textarea");
        textArea.style.zIndex = -1;
        textArea.value = number;
        document.body.appendChild(textArea);
        textArea.select();
        try {
          document.execCommand("copy");
        } catch (err) {
          alert("该浏览器不支持点击复制到剪贴板");
        }
        document.body.removeChild(textArea);
      },
    },
    created() {},
    mounted() {},
  };
</script>
<style scoped>
  .v-card {
    cursor: default;
    margin: 20px 0 20px 0;
  }
</style>
