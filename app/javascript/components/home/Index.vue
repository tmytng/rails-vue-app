<template>
<div>
<header-view :title="title" :description="description"></header-view>
<contents :contents="contents"></contents>
</div>
</template>

<script>
import HeaderView from "../HeaderView.vue";
import Contents from "./Contents.vue";

export default {
  components: {
    HeaderView,
    Contents
  },
  props: {
    title: {
      type: String,
      default: () => ""
    },
    description: {
      type: String,
      default: () => ""
    },
    contents: {
      type: Object,
      default: () => {}
    }
  }
};
</script>

<style scoped>
.contents-table {
  border: 1px solid gray;
  margin: 10px;
}
.contents-table th,
.contents-table td {
  border: 1px solid gray;
}
</style>
