<template>
  <div class="ds-main-header">
    <menu-item v-for="(headerItem, index) in headerItems"
      :key="index"
      :title="headerItem.name"
      :items="headerItem.menuItems"></menu-item>
  </div>
</template>


<script>
import MenuItem from '@/components/MenuItem.vue';
import HeaderConfig from '@/config/HeaderConfig';

export default {
  components: {
    'menu-item': MenuItem,
  },
  data: () => ({
    headerItems: HeaderConfig,
  }),
};
</script>


<style lang="scss">
@import "~@/styles/app";

.ds-main-header {
  display: flex;
  flex-wrap: wrap;
  width: 100%;
  align-items: center;

  .ds-menu-item {
    color: $offWhite;
    margin: 0 20px;
    text-decoration: none;
    letter-spacing: 1px;
    font-size: 14px;
  }
}
</style>
