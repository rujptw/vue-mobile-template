<template>
  <div class="demo-content">
    <img class="logo" alt="Vue logo" src="~@/assets/logo_vue3.png">
    <div class="demo-content__title">
      <a href="https://github.com/yulimchen/vue3-h5-template" target="_blank">
        <svg-icon icon-class="github" />
        <h3>Vue3-h5-template</h3>
        <svg-icon class="link-icon" icon-class="link" />
      </a>
    </div>
    <div class="demo-content__desc">
      <p>ð± åºäº Vue3 å¨å®¶æ¡¶ãVant3 ç»ä»¶åºï¼å¼ç®±å³ç¨ç H5 ç§»å¨ç«¯é¡¹ç®åºç¡æ¨¡æ¿</p>
    </div>

    <div class="demo-main">
      <van-cell v-for="(item, idx) in contentList" :key="idx" :title="item" />
    </div>
  </div>
</template>

<script>
import { reactive } from 'vue'

export default {
  name: 'Demo',
  setup() {
    const contentList = reactive([
      'â Vue3â¨',
      'â Vant3â¨',
      'â æ¯æ SVG å¾æ èªå¨æ³¨åç»ä»¶â¨',
      'â vw è§å£éé',
      'â Axios å°è£',
      'â çäº§ç¯å¢ CDN ä¾èµ',
      'â æåèµæº gzip åç¼©',
      'â ESLint',
      'â é¦å±å è½½å¨ç»',
      'â é¡¹ç®èµæºè·¯å¾ alias å«å',
      'â å¼åç¯å¢è°è¯é¢æ¿',
      'â Vuex éæ',
      'â Vue-router éæ',
      'â å¼åç¯å¢ Mock æ°æ®'
    ])

    return {
      contentList
    }
  }
}
</script>

<style lang="less" scoped>
.demo-content {
  padding: 0 12px;

  .logo {
    display: block;
    width: 120px;
    margin: 30px auto 20px;
  }

  &__title {
    border-left: 3px solid #41b883;
    padding-left: 12px;

    .svg-icon {
      font-size: 20px;
      margin-right: 8px;
    }

    h3 {
      margin: 6px 0;
      font-size: 18px;
    }

    > a {
      display: flex;
      align-items: center;

      .link-icon {
        font-size: 12px;
        margin-left: 5px;
      }
    }
  }

  &__desc {
    font-size: 14px;
    padding: 2px 10px;
    border-radius: 4px;
    background-color: #eee;
    margin-top: 14px;

    p {
      line-height: 24px;
    }
  }

  .demo-main {

  }
}
</style>
