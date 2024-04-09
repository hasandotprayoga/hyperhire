<template>
  <transition appear enter-active-class="animated fadeIn">
    <div style="position: relative; width: fit-content; margin: 0 auto">
      <div
        class="text-color-8 bg-white flex items-center"
        style="
          font-size: 18px;
          width: fit-content;
          padding: 6px 12px;
          border-radius: 8px;
          gap: 8px;
        "
      >
        <DollarIcon />
        월 100만원
      </div>
      <ArrowDownIcon style="position: absolute; bottom: -9px; left: 50%" />
    </div>
  </transition>

  <transition appear enter-active-class="animated fadeIn">
    <div style="position: relative">
      <swiper
        ref="swiperRef"
        :modules="[EffectCards]"
        effect="cards"
        :grabCursor="true"
        :centeredSlides="true"
        :initialSlide="1"
        slidesPerView="auto"
        :cardsEffect="{
          perSlideOffset: $q.screen.xs ? 10 : 21,
          perSlideRotate: 0,
          rotate: false,
          slideShadows: false,
        }"
        @swiper="onSwiper"
      >
        <swiper-slide v-for="i in 3" :key="i">
          <UserCard />
        </swiper-slide>
      </swiper>
      <q-btn
        flat
        round
        style="position: absolute; left: -8px; top: 50%; z-index: 1"
        @click="swiperPrevSlide"
      >
        <CaretLeftIcon />
      </q-btn>
      <q-btn
        flat
        round
        style="position: absolute; right: -8px; top: 50%; z-index: 1"
        @click="swiperNextSlide"
      >
        <CaretRightIcon />
      </q-btn>
    </div>
  </transition>
</template>

<script>
import { ref } from "vue";
import { EffectCards } from "swiper/modules";
import { Swiper, SwiperSlide } from "swiper/vue";

import UserCard from "src/components/UserCard.vue";
import CaretRightIcon from "src/components/icons/CaretRightIcon.vue";
import CaretLeftIcon from "src/components/icons/CaretLeftIcon.vue";
import ArrowDownIcon from "components/icons/ArrowDownIcon.vue";
import DollarIcon from "./icons/DollarIcon.vue";

export default {
  components: {
    Swiper,
    SwiperSlide,
    UserCard,
    CaretLeftIcon,
    CaretRightIcon,
    ArrowDownIcon,
    DollarIcon,
  },
  setup() {
    const swiperInstance = ref();

    function onSwiper(swiper) {
      swiperInstance.value = swiper;
    }
    const swiperNextSlide = () => {
      console.log(swiperInstance.value);
      swiperInstance.value.slideNext();
    };

    const swiperPrevSlide = () => {
      swiperInstance.value.slidePrev();
    };

    return {
      EffectCards,
      swiperPrevSlide,
      swiperNextSlide,
      onSwiper,
    };
  },
};
</script>

<style scoped>
.swiper {
  width: 100%;
  height: auto;
  margin-top: 24px;
}

.swiper-slide {
  display: flex;
  align-items: center;
  justify-content: center;
}
.swiper-slide {
  opacity: 0;
}

.swiper-slide-prev,
.swiper-slide-active,
.swiper-slide-next {
  opacity: 1;
}

.swiper-button-next:after,
.swiper-button-prev:after {
  font-size: 32px !important;
  color: white !important;
}
</style>
