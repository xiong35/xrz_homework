// dependency: //
<template>
  <div class="web">
    <h1>网络学习分享</h1>
    <v-divider class="my-4"></v-divider>
    <h3 class="ma-3">学习经验</h3>
    <ul>
      <li>
        常做总结: 网络学习知识又多又杂, 必须经常总结, 避免学了前面忘了后面
      </li>
      <li>
        动手实践: 一个html界面很方便就可以打开,
        js代码也是很容易在浏览器里运行, 如此方便, 何不多动手做做呢!
      </li>
      <li>
        多读文档: 官方文档往往都非常详细具体, 而且非常权威, 值得反复研究.
      </li>
    </ul>
    <h3 class="ma-3">资源分享</h3>
    <ul>
      <li>
        <a
          href="https://www.bilibili.com/video/BV14J4114768?from=search&seid=7572041370656622396"
        >
          bilibili 上的 html 教程
        </a>
      </li>
      <li>
        <a href="https://developer.mozilla.org/zh-CN/">
          mdn 文档
        </a>
      </li>
      <li>
        <a href="https://www.runoob.com/html/html-tutorial.html">
          菜鸟教程
        </a>
      </li>
      <li>
        <a href="https://cn.vuejs.org/">
          vue 官方文档
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: "index",
    components: {},
    data() {
      return {};
    },
    computed: {},
    watch: {},
    methods: {},
    created() {},
    mounted() {},
  };
</script>
<style scoped>
  .web {
    font-size: 1.2rem !important;
  }
</style>
