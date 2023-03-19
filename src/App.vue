<template>
  <div class="app">
    <section class="top">
      <header class="top-header header">
        <Logo />
        <nav class="nav header-nav">
          <Link :menuLink="menuLink" />
        </nav>
        <div class="header-burger">
          <img src="@/assets/images/burger.png" alt="" />
        </div>
        <div class="header-icons">
          <IconBtn />
        </div>
      </header>
      <main class="main">
        <section class="main-info">
          <Info />
        </section>
      </main>
    </section>
    <section>
      <div class="slider slider-wrap">
        <h2 class="slider-title">Popular Products</h2>
        <div class="image-container">
          <img src="@/assets/images/Image-container1.png" alt="" />
        </div>
        <Slider :products="products" />
        <div class="swiper-scrollbar"></div>
        <div class="swiper-btn-wrap">
          <div class="swiper-button-prev arrow">
            <img src="@/assets/images/arrow-prev.svg" alt="" />
          </div>
          <div class="swiper-button-next arrow">
            <img src="@/assets/images/arrow-next.svg" alt="" />
          </div>
        </div>
      </div>
      <div class="slider-explore">
        <button>
          Explore all items
          <svg
            width="21"
            height="13"
            viewBox="0 0 21 13"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M13.5555 12.7274C13.469 12.6411 13.4004 12.5387 13.3536 12.4259C13.3068 12.3131 13.2827 12.1922 13.2827 12.0701C13.2827 11.948 13.3068 11.8271 13.3536 11.7143C13.4004 11.6015 13.469 11.499 13.5555 11.4128L18.4702 6.49988L13.5555 1.58695C13.3811 1.41263 13.2832 1.17619 13.2832 0.929664C13.2832 0.683134 13.3811 0.446701 13.5555 0.272378C13.7298 0.0980549 13.9662 0.00012204 14.2127 0.00012203C14.4593 0.000122019 14.6957 0.0980548 14.87 0.272378L20.4402 5.84259C20.5267 5.92883 20.5953 6.03128 20.6421 6.14407C20.6889 6.25685 20.713 6.37777 20.713 6.49988C20.713 6.62199 20.6889 6.7429 20.6421 6.85569C20.5953 6.96848 20.5267 7.07093 20.4402 7.15716L14.87 12.7274C14.7838 12.8138 14.6813 12.8824 14.5686 12.9292C14.4558 12.976 14.3349 13.0001 14.2127 13.0001C14.0906 13.0001 13.9697 12.976 13.8569 12.9292C13.7441 12.8824 13.6417 12.8138 13.5555 12.7274Z"
              fill="white"
            />
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M0.287109 6.49998C0.287109 6.25376 0.38492 6.01762 0.559023 5.84352C0.733126 5.66942 0.96926 5.57161 1.21548 5.57161L17.9261 5.57161C18.1723 5.57161 18.4085 5.66941 18.5826 5.84352C18.7567 6.01762 18.8545 6.25376 18.8545 6.49997C18.8545 6.74619 18.7567 6.98233 18.5826 7.15643C18.4085 7.33053 18.1723 7.42834 17.9261 7.42834L1.21548 7.42834C0.96926 7.42834 0.733126 7.33053 0.559023 7.15643C0.38492 6.98233 0.287109 6.74619 0.287109 6.49998Z"
              fill="white"
            />
          </svg>
        </button>
      </div>
    </section>
  </div>
</template>
<script>
import Logo from "./components/logo/Logo";
import Slider from "./components/Slider";
import Link from "./components/link/Link";
import IconBtn from "./components/iconBtn/iconBtn";
import Info from "./components/info/Info";

export default {
  name: "App",
  components: {
    Logo,
    Slider,
    Link,
    IconBtn,
    Info,
  },
  data() {
    return {
      menuLink: ["Home", "Products", "Categories", "About", "Contact Us"],
      products: [
        {
          id: 1,
          image: require("@/assets/images/chair1.png"),
          title: "Armchair",
          description: "Light single chair",
          color: "#CAF3E5",
          price: "$145",
        },
        {
          id: 2,
          image: require("@/assets/images/chair2.png"),
          title: "Premium Sofa",
          description: "Light single chair",
          color: "#E0EFF6",
          price: "$145",
        },
        {
          id: 3,
          image: require("@/assets/images/chair3.png"),
          title: "Minimal Sofa",
          description: "Light single chair",
          color: "#EEEBFF",
          price: "$145",
        },
        {
          id: 4,
          image: require("@/assets/images/chair4.png"),
          title: "Dining Chair",
          description: "Light single chair",
          color: "#FFF4E7",
          price: "$145",
        },
        {
          id: 5,
          image: require("@/assets/images/chair1.png"),
          title: "Armchair",
          description: "Light single chair",
          color: "#CAF3E5",
          price: "$145",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.app {
  padding-bottom: 113px;
  background: #fdfbf8;
}

.top {
  height: 100vh;
  background-image: url("@/assets/images/main-img.png");
  background-size: 100% 100%;
  background-position: center;
  background-repeat: no-repeat;

  @media (max-width: 768px) {
    background-image: url("@/assets/images/main-img-768.png");
  }

  @media (max-width: 414px) {
    background-image: url("@/assets/images/main-img-414.png");
  }
}

.header {
  padding: 26px 150px 38px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: rgba(224, 246, 241, 0.5);

  &-nav {
    @media (max-width: 1300px) {
      display: none;
    }
  }

  &-burger {
    display: none;

    @media (max-width: 1300px) {
      display: block;
    }

    @media (max-width: 414px) {
      order: -1;
    }
  }

  @media (max-width: 1300px) {
    padding: 26px 20px 38px;
  }
}

.main {
  padding-top: 233px;

  @media (max-width: 768px) {
    padding-top: 76px;
  }

  @media (max-width: 414px) {
    padding-top: 132px;
  }
}

.main-info {
  margin: 0 150px;

  @media (max-width: 920px) {
    margin: 0 20px;
  }

  @media (max-width: 414px) {
    margin: 0 16px;
  }
}

.slider {
  padding-top: 120px;
  padding-bottom: 54px;
  font-family: $second-font;

  &-title {
    font-weight: 700;
    font-size: 64px;
    line-height: 85px;
    margin-bottom: 58px;
    text-align: center;
    color: $main-color;

    @media (max-width: 600px) {
      font-size: 36px;
      line-height: 52px;
    }
  }

  &-wrap {
    position: relative;
  }

  @media (max-width: 768px) {
    padding-top: 53px;
  }

  @media (max-width: 414px) {
    padding-top: 42px;
  }
}

.image-container {
  position: absolute;
  top: 0;
  left: 0;
  transform: translate(-50%, 25%);

  @media (max-width: 414px) {
    width: 365px;
    height: 434px;
    transform: translate(-50%, 40%);

    img {
      width: 100%;
      height: 100%;
    }
  }
}

.slider-explore {
  text-align: center;

  button {
    background: #70908b;
    font-family: "Open Sans";
    font-weight: 700;
    font-size: 18px;
    line-height: 25px;
    padding: 24px 35px;
    border: none;
    border-radius: 10px;
    color: #ffffff;
    cursor: pointer;
  }
}
</style>
