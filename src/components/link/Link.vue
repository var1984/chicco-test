<template>
  <ul class="link">
    <li class="link-item" v-for="item of menuLink" :key="item">{{ item }}</li>
  </ul>
</template>

<script>
export default {
  name: "Link",
  props: ["menuLink"],
};
</script>

<style lang="scss" scoped>
.link {
  display: flex;

  &-item {
    margin-left: 50px;
    font-weight: 700;
    font-size: 20px;
    line-height: 132.9%;
    letter-spacing: 0.05em;
    height: 30px;
    color: $main-color;
    cursor: pointer;

    &:hover {
      border-bottom: 3px solid $main-color;
    }

    &:first-child {
      margin-left: 0;
    }
  }
}
</style>
