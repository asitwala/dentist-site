<template>
  <div class="ds-menu-item">
    <v-menu
      :absolute="true"
      :open-on-hover="true"
      nudge-bottom="true"
      offset-y v-if="menuItemsLength > 0">
      <div slot="activator"
        class="ds-menu-item-title">
        {{ title }}
      </div>

      <v-list dense dark color="blue darken-4">
        <v-list-tile
          v-for="(item, index) in items"
          :key="index"
          @click="routeTo(item.itemLink)">
          <v-list-tile-title>{{ item.itemName }}</v-list-tile-title>
        </v-list-tile>
      </v-list>
    </v-menu>

    <div v-else class="ds-menu-item-title">
      {{ title }}
    </div>

  </div>
</template>


<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    items: {
      type: Array,
      required: true,
    },
  },
  data: () => ({

  }),
  methods: {
    routeTo(pathName) {
      this.$router.push({ name: pathName });
    },
  },
  computed: {
    menuItemsLength() {
      return this.items.length;
    },
  },
};
</script>


<style scoped lang="scss">
  .ds-menu-item {
    display: inline-block;
  }
</style>
