<template>
  <div class="Container">
    <div class="Content" :class="{ onTap : tapping }"  @mousedown="onClick" @click.stop="onClickStop">
      <nuxt/>
    </div>
  </div>
</template>

<script>
import App from '~components/App.vue'

export default {
  components: { App },
  beforeMount () {
    this.tapping = false
  },
  data () {
    return {
      tapping: false
    }
  },
  methods: {
    onClick () {
      this.tapping = true
    },
    onClickStop () {
      this.tapping = false
    }
  }
}
</script>

<style>
html
{
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  background: rgb(29,32,41);
}
*, *:before, *:after
{
  box-sizing: border-box;
  margin: 0;
}

.Container {
  width: 416px;
  height: 850px;
  margin: 65px auto;
  background: url('~assets/iphone6-portrait.png') no-repeat;
}

.Content {
  position: absolute;
  margin-top: 86px;
  margin-left: 20px;
  width: 375px;
  height: 667px;
  background: white;
  cursor: url('~assets/mobile-cursor.png') 39 39, auto;

  /* make text not selectable */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  -o-user-select: none;
  user-select: none;
}

.onTap {
  cursor: url('~assets/mobile-cursor-tap.png') 39 39, auto;
}

</style>
