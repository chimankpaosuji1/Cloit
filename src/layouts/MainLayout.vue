<template>
  <q-layout view="lHh Lpr lFf" class="layout">
    <q-header elevated class="navbar">
      <div class="text-white toolbar">
        <div-title>
          <q-img src="../assets/logo.svg" style="width: 170px"></q-img>
        </div-title>
        <div class="q-mr-xl">
          <q-btn-dropdown flat color="white" label="채용">
            <q-list>
              <q-item clickable v-close-popup @click="onItemClick">
                <q-item-section>
                  <q-item-label>채용</q-item-label>
                </q-item-section>
              </q-item>

              <q-item clickable v-close-popup @click="onItemClick">
                <q-item-section>
                  <q-item-label>해외 개발자 원격 채용</q-item-label>
                </q-item-section>
              </q-item>

              <q-item clickable v-close-popup @click="onItemClick">
                <q-item-section>
                  <q-item-label>외국인 원격 채용 (비개발 직군)</q-item-label>
                </q-item-section>
              </q-item>
              <q-item clickable v-close-popup @click="onItemClick">
                <q-item-section>
                  <q-item-label>한국어 가능 외국인 채용</q-item-label>
                </q-item-section>
              </q-item>
              <q-item clickable v-close-popup @click="onItemClick">
                <q-item-section>
                  <q-item-label>채용 </q-item-label>
                </q-item-section>
              </q-item>
              <q-item clickable v-close-popup @click="onItemClick">
                <q-item-section>
                  <q-item-label>해외 개발자 활용 서비스</q-item-label>
                </q-item-section>
              </q-item>
              <q-item clickable v-close-popup @click="onItemClick">
                <q-item-section>
                  <q-item-label>문의하기</q-item-label>
                </q-item-section>
              </q-item>
              <q-item clickable v-close-popup @click="onItemClick">
                <q-item-section>
                  <q-item-label>외국인 원격 채용 (비개발 직군)</q-item-label>
                </q-item-section>
              </q-item>
            </q-list>
          </q-btn-dropdown>
          <q-btn flat color="white" label="해외 개발자 활용 서비스" />
        </div>
        <div>
          <q-btn color="white" text-color="blue" label="문의하기" />
        </div>
      </div>
    </q-header>

    <!-- <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
    >
      <q-list>
        <q-item-label
          header
        >
          Essential Links
        </q-item-label>

        <EssentialLink
          v-for="link in linksList"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer> -->

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<style>
.toolbar {
  display: flex !important;
  align-items: center !important;
  justify-content: space-between !important;
  padding-top: 0.5rem;
  padding-bottom: 0.5rem;
  max-width: 1170px;
  margin: auto;
}
.navbar {
  background-image: url("../assets/banner.png");
  background-repeat: no-repeat;
  background-size: cover;
}
.title {
  color: white;
  opacity: none;
}
.banner {
  background-image: url("../assets/bgimage.svg");
  height: 98vh;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  /* width: 1920px;
  height: 929px;
  top: -15px;
  left: -92px;
  gap: 0px; */
  opacity: 0.8px;
}
</style>

<script setup>
import { ref } from "vue";
import EssentialLink from "components/EssentialLink.vue";

defineOptions({
  name: "MainLayout",
});

const linksList = [
  {
    title: "Docs",
    caption: "quasar.dev",
    icon: "school",
    link: "https://quasar.dev",
  },
  {
    title: "Github",
    caption: "github.com/quasarframework",
    icon: "code",
    link: "https://github.com/quasarframework",
  },
  {
    title: "Discord Chat Channel",
    caption: "chat.quasar.dev",
    icon: "chat",
    link: "https://chat.quasar.dev",
  },
  {
    title: "Forum",
    caption: "forum.quasar.dev",
    icon: "record_voice_over",
    link: "https://forum.quasar.dev",
  },
  {
    title: "Twitter",
    caption: "@quasarframework",
    icon: "rss_feed",
    link: "https://twitter.quasar.dev",
  },
  {
    title: "Facebook",
    caption: "@QuasarFramework",
    icon: "public",
    link: "https://facebook.quasar.dev",
  },
  {
    title: "Quasar Awesome",
    caption: "Community Quasar projects",
    icon: "favorite",
    link: "https://awesome.quasar.dev",
  },
];

const leftDrawerOpen = ref(false);

function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value;
}
</script>
