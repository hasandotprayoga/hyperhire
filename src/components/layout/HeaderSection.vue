<template>
  <q-header
    class="bg-transparent text-white container"
    :class="{
      'q-px-md': $q.screen.xs,
    }"
  >
    <q-toolbar
      class="flex items-center justify-between"
      style="gap: 36px; padding: 13px 0"
    >
      <img
        alt="Hyperhire Logo"
        src="~/assets/logo/light.png"
        style="width: 114px; height: 21px"
      />

      <template v-if="$q.screen.xs">
        <q-drawer
          v-model="drawer"
          side="right"
          show-if-above
          :width="300"
          :breakpoint="700"
          class="bg-white"
        >
          <q-scroll-area class="fit">
            <div class="q-pa-lg text-color-1">
              <q-list style="min-width: 100px; margin-bottom: 32px">
                <q-item clickable>
                  <q-item-section class="text-menu-bold">채용</q-item-section>
                </q-item>
                <q-item clickable>
                  <q-item-section class="text-menu q-pl-md"
                    >해외 개발자 원격 채용</q-item-section
                  >
                </q-item>
                <q-item clickable>
                  <q-item-section class="text-menu q-pl-md"
                    >외국인 원격 채용 (비개발 직군)</q-item-section
                  >
                </q-item>
                <q-item clickable>
                  <q-item-section class="text-menu q-pl-md"
                    >한국어 가능 외국인 채용</q-item-section
                  >
                </q-item>
                <q-separator />
                <q-item clickable>
                  <q-item-section class="text-menu-bold">
                    해외 개발자 활용 서비스
                  </q-item-section>
                </q-item>
              </q-list>

              <q-btn
                flat
                style="
                  background-color: #26c2b9;
                  color: #fff;
                  border-radius: 8px;
                  padding: 6px 24px;
                  width: 100%;
                "
              >
                문의하기
              </q-btn>
            </div>
          </q-scroll-area>
        </q-drawer>
        <q-btn flat round dense icon="menu" @click="drawer = !drawer" />
      </template>

      <template v-else>
        <div class="flex" style="gap: 60px">
          <div
            class="cursor-pointer non-selectable flex items-center"
            style="gap: 8px"
          >
            채용 <CaretDownIcon />
            <q-menu auto-close class="text-color-4">
              <q-list style="min-width: 100px">
                <q-item clickable>
                  <q-item-section class="text-menu-bold">채용</q-item-section>
                </q-item>
                <q-item clickable>
                  <q-item-section class="text-menu"
                    >해외 개발자 원격 채용</q-item-section
                  >
                </q-item>
                <q-item clickable>
                  <q-item-section class="text-menu"
                    >외국인 원격 채용 (비개발 직군)</q-item-section
                  >
                </q-item>
                <q-separator />
                <q-item clickable>
                  <q-item-section class="text-menu"
                    >한국어 가능 외국인 채용</q-item-section
                  >
                </q-item>
              </q-list>
            </q-menu>
          </div>
          <div class="cursor-pointer non-selectable">
            해외 개발자 활용 서비스
          </div>
        </div>

        <q-btn
          flat
          style="
            background-color: white;
            color: #4a77ff;
            border-radius: 8px;
            padding: 6px 24px;
          "
          >문의하기</q-btn
        >
      </template>
    </q-toolbar>
  </q-header>
</template>

<script setup>
import CaretDownIcon from "src/components/icons/CaretDownIcon.vue";
import { ref } from "vue";

const drawer = ref(false);
</script>
