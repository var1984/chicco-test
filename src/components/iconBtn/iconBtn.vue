<template>
  <div>
    <div class="icon">
      <div class="icon-item">
        <img src="@/assets/icons/icon-search.png" alt="" />
      </div>
      <div class="icon-item">
        <img src="@/assets/icons/icon-cart.png" alt="" />
      </div>
      <div class="icon-item">
        <img src="@/assets/icons/icon-people.png" alt="" />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "IconBtn",
};
</script>

<style lang="scss" scoped>
.icon {
  display: flex;

  &-item {
    margin-left: 58px;
    cursor: pointer;

    &:first-child {
      margin-left: 0;
    }

    @media (max-width: 414px) {
      margin-left: 12px;
    }
  }
}
</style>
