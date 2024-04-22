<template>
  <q-layout view="lHh Lpr lFf" class="layout">
    <q-header elevated class="navbar">
      <div class="text-white toolbar">
        <div-title>
          <q-img src="../assets/logo.svg" style="width: 170px"></q-img>
        </div-title>
        <div class="q-mr-xl gt-sm">
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
        <div class="gt-sm">
          <q-btn color="white" text-color="blue" label="문의하기" />
        </div>
       <div class="lt-md"> <q-btn    
            flat
            dense
            round
            icon="menu"
            aria-label="Menu"
            @click="toggleLeftDrawer"
          /></div>
      </div>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      bordered
    >
      <q-list class="q-py-xl">
        

        <EssentialLink
          v-for="link in linksList"
          :key="link.title"
          v-bind="link"
        />

        <div class="q-py-xl" style="margin-left:auto; dispaly:block; margin-right: auto; width:50%">
          <q-btn outline text-color="blue" to="/" label="문의하기"/>
        </div>
      </q-list>
    </q-drawer>

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
    title: "채용",
    link: "/",
  },
  {
    title: "해외 개발자 원격 채용",
    icon: "code",
    link: "/",
  },
  {
    title: "외국인 원격 채용 (비개발 직군)",
    icon: "code",
    link: "/",
  },
  {
    title: "한국어 가능 외국인 채용",
    icon: "code",
    link: "/",
  },
  {
    title: "해외 개발자 활용 서비스",
    link: "/",
  }
];

const leftDrawerOpen = ref(false);

function toggleLeftDrawer() {
  leftDrawerOpen.value = !leftDrawerOpen.value;
}
</script>
