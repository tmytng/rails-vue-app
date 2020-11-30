<template>
  <div>
    <table class="contents-table">
      <tr>
        <th>名前</th>
        <th>リンク</th>
      </tr>
      <tr v-for="outer_link in contents.outer_links" :key="outer_link.name">
        <td>{{ outer_link.name }}</td>
        <td>
          <a :href="outer_link.url">{{ outer_link.text }}</a>
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  props: {
    contents: {
      type: Object,
      default: () => {}
    }
  }
};
</script>

<style scoped>
  .test {
  border: 1px solid blue;
  }
</style>
