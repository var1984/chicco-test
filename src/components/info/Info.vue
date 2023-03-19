<template>
  <div class="info">
    <h1 class="info-title">Exclusive Deals of <br />Furniture Collection</h1>
    <div class="info-description">
      Explore different categories. Find the best deals.
    </div>
    <button class="info-btn">Shop Now</button>
  </div>
</template>

<script>
export default {
  name: "Title",
};
</script>

<style lang="scss" scoped>
.info {
  &-title {
    font-weight: 700;
    font-size: 64px;
    line-height: 85px;
    margin-bottom: 54px;
    color: $main-color;

    @media (max-width: 768px) {
      font-size: 48px;
      line-height: 62px;
      margin-bottom: 16px;
    }

    @media (max-width: 414px) {
      font-size: 36px;
      line-height: 52px;
    }
  }

  &-description {
    font-family: $second-font;
    font-size: 24px;
    line-height: 33px;
    color: $main-color;

    @media (max-width: 414px) {
      font-size: 18px;
      line-height: 23px;
      width: 286px;
      margin: 0 auto;
    }
  }

  &-btn {
    font-family: $second-font;
    padding: 23.5px 54.5px;
    border-radius: 10px;
    margin-top: 54px;
    font-weight: 700;
    font-size: 24px;
    line-height: 33px;
    color: #fdfbf8;
    border: none;
    background: #70908b;
    cursor: pointer;
  }

  @media (max-width: 414px) {
    text-align: center;
  }
}
</style>
