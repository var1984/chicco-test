<template>
  <div class="swiper">
    <div class="swiper-wrapper products">
      <div
        class="swiper-slide products-item"
        :style="{ 'background-color': product.color }"
        v-for="product of products"
        :key="product.id"
      >
        <div class="product-image">
          <img :src="product.image" alt="" />
        </div>
        <div class="product-info">
          <h3 class="product-title">{{ product.title }}</h3>
          <p class="product-description">{{ product.description }}</p>
          <p class="product-price">{{ product.price }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Swiper, { Navigation, Pagination, Scrollbar } from "swiper";
import "swiper/swiper-bundle.min.css";
export default {
  name: "products",
  props: {
    products: {
      type: Array,
      require: true,
    },
  },
  mounted() {
    new Swiper(".swiper", {
      modules: [Navigation, Pagination, Scrollbar],

      direction: "horizontal",
      slidesPerView: "auto",
      slidesPerGroup: 4,
      spaceBetween: 32,

      navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev",
      },

      scrollbar: {
        el: ".swiper-scrollbar",
        draggable: true,
        dragSize: 120,
      },

      breakpoints: {
        0: {
          slidesPerView: 1,
          spaceBetween: 32,
        },
        414: {
          slidesPerView: 2,
          spaceBetween: 32,
        },
        768: {
          slidesPerView: 3,
          spaceBetween: 32,
        },
        1240: {
          slidesPerView: 4,
          spaceBetween: 32,
        },
        1650: {
          slidesPerView: 4,
          spaceBetween: 32,
        },
      },
    });
  },
};
</script>

<style lang="scss">
.products {
  margin-left: 196px;

  h3,
  p {
    font-family: $second-font;
    color: #70908b;
  }

  &-item {
    min-width: 430.75px;
    height: 585px;
    border-radius: 16px;
    padding: 84px 40px 60px;
    flex-shrink: none;

    @media (max-width: 768px) {
      min-width: 416px;
    }

    @media (max-width: 414px) {
      min-width: 237px;
      height: 340px;
      padding: 46px 20px 60px;
    }
  }

  .product {
    &-title {
      font-weight: 700;
      font-size: 24px;
      line-height: 36px;
      margin-bottom: 20px;

      @media (max-width: 414px) {
        font-size: 18px;
        line-height: 23px;
      }
    }

    &-description {
      font-size: 18px;
      line-height: 25px;
      margin-bottom: 20px;

      @media (max-width: 414px) {
        font-size: 18px;
        line-height: 23px;
      }
    }

    &-price {
      font-size: 18px;
      line-height: 25px;
      font-weight: 700;

      @media (max-width: 414px) {
        font-size: 18px;
        line-height: 23px;
      }
    }

    &-image {
      display: flex;
      justify-content: center;
      align-items: center;

      img {
        @media (max-width: 768px) {
          width: 204px;
          height: 270px;
        }

        @media (max-width: 414px) {
          width: 89px;
          height: 116px;
        }
      }
    }

    &-info {
      margin-top: 40px;
    }
  }

  @media (max-width: 1200px) {
    margin-left: 36px;
  }
}

.swiper-scrollbar {
  background-color: $main-color;
  position: static !important;
  margin-top: 54px;
  margin-left: 150px;
  width: calc(100% - 16 * var(--swiper-scrollbar-sides-offset, 1%)) !important;
}

.swiper-scrollbar-drag {
  --swiper-scrollbar-drag-bg-color: rgba(112, 144, 139);
  border-radius: 0;
  height: 12px;
  top: calc(100% - 8px) !important;
}

.swiper-btn-wrap {
  display: flex;
  justify-content: flex-end;
  margin: 60px 150px 0;
}

.swiper-button-prev,
.swiper-button-next {
  position: relative;
  right: 0;
  left: 0;
}

.swiper-button-next {
  background-color: #f9d9da;
  margin-left: 20px;
}

.swiper-button-prev {
  background-color: #e0eff6;
}

.arrow {
  width: 40px;
  height: 40px;
  border-radius: 50%;

  @media (max-width: 1200px) {
    display: none;
  }
}
</style>
