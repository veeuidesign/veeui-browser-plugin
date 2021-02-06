<template>
  <div class="Wokoo" v-if="show">
    <header class="Wokoo-header">
      <img :src="logo" class="Wokoo-logo" alt="logo" />
      <span
        class="Wokoo-close-icon"
        @click="handleClose"
      >
        ×
      </span>
      <p>
        欢迎使用 <a class="Wokoo-link" href="https://github.com/veeuidesign/veeui-vue#readme">Vee UI</a>
      </p>
    </header>
  </div>
  <div class="Wokoo-hide" @click="handleClose" v-else>
    <img :src="logo" class="Wokoo-hide-logo" alt="logo" />
    open
  </div>
</template>
<script>
import './app.less'
import logo from '../public/icon.jpg'
export default {
  data: function() {
    return {
      logo,
      show: true
    }
  },
  methods: {
    handleClose() {
      this.show = !this.show
    }
  }
}
</script>
<style scoped>
</style>
