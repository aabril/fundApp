<template>
  <div class="Container">
    <div class="Content">
      <LemoorApp/>
    </div>
  </div>
</template>

<script>
import LemoorApp from '~components/LemoorApp.vue'

export default {
  components: { LemoorApp }
}
</script>

<style>
.Container {
  width: 416px;
  height: 850px;
  margin: 60px auto;
  background: url('~assets/iphone6-portrait.png') no-repeat;
}

.Content {
  position: absolute;
  margin-top: 85px;
  margin-left: 20px;
  width: 375px;
  height: 667px;
  background: white;
  cursor: url('~assets/mobile-cursor.png')  39 39, auto;
}

</style>
