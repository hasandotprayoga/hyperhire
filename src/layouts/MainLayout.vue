<template>
  <q-layout>
    <HeaderSection />

    <q-page-container style="padding-top: 0">
      <router-view />
    </q-page-container>

    <FooterSection />
  </q-layout>
</template>

<script setup>
import HeaderSection from "src/components/layout/HeaderSection.vue";
import FooterSection from "components/layout/FooterSection.vue";

defineOptions({
  name: "MainLayout",
});
</script>
