<template>
  <q-page
    class="bg-gradient text-white"
    :style="{
      padding: $q.screen.xs ? '60px 0' : '122px 0',
      overflow: 'hidden',
    }"
  >
    <div
      class="container"
      :class="{
        'q-pa-md': $q.screen.xs,
      }"
    >
      <div
        class=""
        :class="{
          'grid-cols-2 grid': !$q.screen.xs,
        }"
        style="gap: 36px"
      >
        <div class="column" style="gap: 60px">
          <div class="column" style="gap: 24px">
            <div class="column" style="gap: 16px">
              <transition
                appear
                enter-active-class="animated slow fadeIn delay-3s"
              >
                <div style="position: relative">
                  <div
                    :class="{ 'text-color-8': !$q.screen.xs }"
                    :style="{
                      fontSize: '18px',
                      width: 'fit-content',
                      padding: '6px 12px',
                      borderRadius: '8px',
                      backgroundColor: $q.screen.xs ? '#8bc4ff' : '#fff',
                    }"
                  >
                    풀타임, 파트타임
                  </div>
                  <ArrowDownIcon
                    :style="{
                      position: 'absolute',
                      bottom: '-9px',
                      left: '9px',
                      color: $q.screen.xs ? '#8bc4ff' : '#fff',
                    }"
                  />
                </div>
              </transition>

              <transition appear enter-active-class="animated slow fadeInUp">
                <div
                  :style="{
                    fontSize: $q.screen.xs ? '36px' : '48px',
                  }"
                >
                  최고의 실력을 가진<br />
                  외국인 인재를 찾고 계신가요?
                </div>
              </transition>
              <transition appear enter-active-class="animated slow fadeInUp">
                <div :style="{ fontSize: $q.screen.xs ? '18px' : '24px' }">
                  법률 및 인사관리 부담없이<br />
                  1주일 이내에 원격으로 채용해보세요.
                </div>
              </transition>
            </div>
            <transition
              v-if="!$q.screen.xs"
              appear
              enter-active-class="animated slow fadeInUp"
            >
              <div style="font-size: 18px">개발자가 필요하신가요?</div>
            </transition>
          </div>
          <transition
            v-if="!$q.screen.xs"
            appear
            enter-active-class="animated slow fadeIn "
          >
            <div class="grid grid-cols-3" style="gap: 48px">
              <div
                v-for="i in 3"
                :key="i"
                class="column q-pt-sm"
                style="
                  gap: 8px;
                  border-top-width: 1px;
                  border-color: white;
                  border-top-style: solid;
                "
              >
                <div style="font-size: 18px">평균 월 120만원</div>
                <div style="font-size: 16px">
                  임금을 해당 국가를 기준으로 계산합니다.
                </div>
              </div>
            </div>
          </transition>
        </div>
        <div
          :style="{
            paddingTop: $q.screen.xs ? '36px' : 0,
          }"
        >
          <UserCarousel />

          <template v-if="$q.screen.xs">
            <transition
              appear
              enter-active-class="animated slow fadeInUp"
              style="margin-top: 24px"
            >
              <div
                class="column"
                style="gap: 8px; margin-top: 24px; font-size: 16px"
              >
                <div class="flex" style="gap: 8px">
                  <div class="flex" style="gap: 12px">
                    <CheckboxIcon />
                    한국어 능력
                  </div>
                  <div class="flex" style="gap: 12px">
                    <CheckboxIcon />업무 수행 능력
                  </div>
                </div>
                <div class="flex" style="gap: 8px">
                  <div class="flex" style="gap: 12px">
                    <CheckboxIcon />겸업 여부
                  </div>
                  <div class="flex" style="gap: 12px">
                    <CheckboxIcon />평판 조회
                  </div>
                </div>
              </div>
            </transition>
            <transition
              appear
              enter-active-class="animated slow fadeInUp"
              style="margin-top: 16px"
            >
              <div style="font-size: 18px">개발자가 필요하신가요?</div>
            </transition>
          </template>
        </div>
      </div>
    </div>
    <transition
      v-if="!$q.screen.xs"
      appear
      enter-active-class="animated slow fadeIn"
      style="margin-top: 60px"
    >
      <JobCarousel />
    </transition>
  </q-page>
</template>

<script setup>
import ArrowDownIcon from "components/icons/ArrowDownIcon.vue";

import UserCarousel from "src/components/UserCarousel.vue";
import JobCarousel from "src/components/JobCarousel.vue";
import CheckboxIcon from "src/components/icons/CheckboxIcon.vue";

defineOptions({
  name: "IndexPage",
});
</script>

<style scoped>
.bg-gradient {
  background: url("images/pattern.svg"),
    linear-gradient(151.17deg, #26c2b9 8.69%, #288be7 126.06%);
  background-position: center; /* Center the image */
  background-repeat: no-repeat; /* Do not repeat the image */
  background-size: cover; /* Resize the background image to cover the entire container */
  background-blend-mode: color-burn;
}
</style>
