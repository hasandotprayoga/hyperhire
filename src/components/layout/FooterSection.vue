<template>
  <footer>
    <div class="column container" style="gap: 48px">
      <div
        class="grid"
        :class="{
          'grid-cols-12': !$q.screen.xs,
          'grid-cols-2': $q.screen.xs,
        }"
        style="gap: 14px"
      >
        <div
          class="column"
          :class="{
            'col-span-2': $q.screen.xs,
            'col-span-4': !$q.screen.xs,
          }"
          style="gap: 16px"
        >
          <img
            alt="Hyperhire Logo"
            :src="LogoDark"
            style="width: 187px; height: 34px"
          />
          <div class="text-weight-bolder text-color-1">
            우리는 국가의 장벽을 넘어 최고의 인재를 매칭해드립니다.
          </div>

          <div class="text-color-f">
            <div>010-0000-0000</div>
            <div>aaaaa@naver.com</div>
          </div>
        </div>

        <div
          v-for="(service, si) in services"
          :key="si"
          class="bg-white q-pa-md column"
          :class="{
            'col-span-2': !$q.screen.xs,
          }"
          style="border-radius: 12px; gap: 16px"
        >
          <div class="column" style="gap: 12px">
            <div
              class="flex items-center justify-center"
              style="
                width: 40px;
                height: 40px;
                background-color: #eff1f6;
                border-radius: 8px;
              "
            >
              <component :is="service.icon" />
            </div>
            <div class="text-color-1">{{ service.name }}</div>
          </div>
          <div class="text-color-f flex items-center" style="gap: 8px">
            바로가기 <ArrowRightIcon />
          </div>
        </div>
      </div>

      <div
        class="grid"
        :class="{
          'grid-cols-12': !$q.screen.xs,
          'grid-cols-2': $q.screen.xs,
        }"
        :style="$q.screen.xs ? 'gap:36px' : 'gap: 14px'"
      >
        <div
          class="row"
          :class="{
            'col-span-2': $q.screen.xs,
            'col-span-4': !$q.screen.xs,
          }"
          style="gap: 16px"
        >
          <div class="column" style="gap: 8px">
            <div class="text-color-1" style="font-size: 12px">상호명</div>
            <div class="column" style="gap: 4px">
              <div class="text-color-f" style="font-size: 13px">
                하이퍼하이어
              </div>
              <div class="text-color-f" style="font-size: 13px">
                Hyperhire India Private Limited
              </div>
            </div>
          </div>

          <div class="column" style="gap: 8px">
            <div class="text-color-1" style="font-size: 12px">대표 CEO</div>
            <div class="column" style="gap: 4px">
              <div class="text-color-f" style="font-size: 13px">김주현</div>
              <div class="text-color-f" style="font-size: 13px">Juhyun Kim</div>
            </div>
          </div>
        </div>

        <div class="column col-span-2" style="gap: 8px">
          <div class="text-color-1" style="font-size: 12px">
            사업자등록번호 CIN
          </div>
          <div class="column" style="gap: 4px">
            <div class="text-color-f" style="font-size: 13px">427-86-01187</div>
            <div class="text-color-f" style="font-size: 13px">
              U74110DL2016PTC290812
            </div>
          </div>
        </div>

        <div
          class="column"
          :class="{
            'col-span-2': $q.screen.xs,
            'col-span-6': !$q.screen.xs,
          }"
          style="gap: 8px"
        >
          <div class="text-color-1" style="font-size: 12px">주소 ADDRESS</div>
          <div class="column" style="gap: 4px">
            <div class="text-color-f" style="font-size: 13px">
              서울특별시 강남대로 479, 지하 1층 238호
            </div>
            <div class="text-color-f" style="font-size: 13px">
              D-138, Street number 11, Jagjeet Nagar, North East Delhi, New
              Delhi, 110053 India
            </div>
          </div>
        </div>
      </div>

      <div class="text-color-f" style="font-size: 13px">
        ⓒ {{ new Date().getFullYear() }} Hyperhire
      </div>
    </div>
  </footer>
</template>

<script setup>
import LogoDark from "assets/logo/dark.png";

import ArrowRightIcon from "components/icons/ArrowRightIcon.vue";
import CodeIcon from "components/icons/CodeIcon.vue";
import UserIcon from "components/icons/UserIcon.vue";
import SettingIcon from "components/icons/SettingIcon.vue";
import KorIcon from "components/icons/KorIcon.vue";

const services = [
  {
    name: "해외 개발자 원격 채용",
    icon: CodeIcon,
  },
  {
    name: "외국인 원격 채용 (비개발)",
    icon: UserIcon,
  },
  {
    name: "한국어 가능 외국인 채용",
    icon: SettingIcon,
  },
  {
    name: "해외 개발자 활용 서비스",
    icon: KorIcon,
  },
];
</script>
