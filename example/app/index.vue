<template>
<div class="app-container">
    <header-bar title="vue-pure" style="background: #20A0FF;color: #fff;height:4rem;" :left-icon="isBack" @on-left="$router.back();" right-text="共8个组件" right-icon=""  @on-right="alert('点到我了')"></header-bar>
    <keep-alive>
      <router-view></router-view>
    </keep-alive>
</div>
</template>
<script>
import { HeaderBar } from 'components';

export default {
  computed: {
    isBack() {
      if(this.$route.path === '/') {
        return '';
      } else {
        return 'i i-backrow';
      }
    },
  },
  components: {
    HeaderBar,
  },
};
</script>
<style lang="scss">
@import 'init.scss';
@import '~mobi.css/src/mobi';
@import '~style/components/index.scss';
</style>
