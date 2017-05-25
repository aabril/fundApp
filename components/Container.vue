<template>
  <div class="Container">
    <div class="Content" :class="{ onTap : tapping }"  @mousedown="onClick" @click.stop="onClickStop">
      <LemoorApp/>
    </div>
  </div>
</template>

<script>
import LemoorApp from '~components/LemoorApp.vue'

export default {
  components: { LemoorApp },
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
      console.log('mouseDown')
      // alert('mouse down')
      // alert(this.tapping)
    },
    onClickStop () {
      this.tapping = false
      console.log('mouseDownStop')
      // alert('mouse down stop')
    }
  }
}
</script>

<style>
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
