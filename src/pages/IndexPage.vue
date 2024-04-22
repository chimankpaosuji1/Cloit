<template>
  <q-page class="">
    <div class="banner">
      <div class="home">
        <div class="row">
          <div class="col q-pr-md">
            <div class="text-white text-bold text-h3 q-mt-xl q-pt-xl q-pb-lg">
              최고의 실력을 가진 <br />
              외국인 인재를 찾고 계신가요?
            </div>
            <div class="text-white text-h6 q-pb-lg">
              법률 및 인사관리 부담없이 1주일 이내에 원격으로 채용해보세요.
            </div>
            <div class="text-white text-h6 q-pb-lg">개발자가 필요하신가요?</div>

            <div class="flex items-start justify-start gt-sm">
              <q-card flat class="my-card">
                <q-card-section class="text-white">
                  <div class="text-h6">평균 월 120만원</div>
                  <div class="text-subtitle2">
                    임금을 해당 국가를 기준으로 계산합니다.
                  </div>
                </q-card-section>
              </q-card>
              <q-card flat class="my-card">
                <q-card-section class="text-white">
                  <div class="text-h6">최대 3회 인력교체</div>
                  <div class="text-subtitle2">
                    막상 채용해보니 맞지 않아도 걱정하지 마세요.
                  </div>
                </q-card-section>
              </q-card>
              <q-card flat class="my-card" style="width: 40%">
                <q-card-section class="text-white">
                  <div class="text-h6">평균 3일, 최대 10일</div>
                  <div class="text-subtitle2">
                    급하게 사람이 필요한 경우에도 빠른 채용이 가능합니다.
                  </div>
                </q-card-section>
              </q-card>
            </div>
          </div>
          <div class="col gt-sm">
            <div class="q-py-xl">
             
              <SliderLink />
            </div>
          </div>
        </div>
        <div class="flex items-center justify-center lt-md">
          <div class="q-pa-md">
            <SliderLink />
          </div>
        </div>
        <div class="btn-section gt-sm">
          <div class="btn">
            <q-img src="../assets/icon1.svg" alt="icon1" width="30px" />
            <span class="text-white text-h6 text-bold">외 마케팅</span>
          </div>
          <div class="btn">
            <q-img src="../assets/icon2.svg" alt="icon1" width="30px" />
            <span class="text-white text-h6 text-bold">퍼블리셔</span>
          </div>
          <div class="btn">
            <q-img src="../assets/icon3.svg" alt="icon1" width="30px" />
            <span class="text-white text-h6 text-bold">캐드원(제도사)</span>
          </div>
          <div class="btn">
            <q-img src="../assets/icon4.svg" alt="icon1" width="30px" />
            <span class="text-white text-h6 text-bold">해외 세일즈</span>
          </div>
          <div class="btn">
            <q-img src="../assets/icon5.svg" alt="icon1" width="30px" />
            <span class="text-white text-h6 text-bold">해외 CS</span>
          </div>
          <div class="btn">
            <q-img src="../assets/icon1.svg" alt="icon1" width="30px" />
            <span class="text-white text-h6 text-bold">해외 마케팅</span>
          </div>
        </div>
        <div class="lt-md" style="font-size: 16px; display: block; gap: 10px">
          <q-checkbox
            v-model="checked"
            label="한국어 능력"
            checked-icon="check_box"
            unchecked-icon="check_box_outline_blank"
            class="white-label"
            color="white"
          />
          <q-checkbox
            v-model="checked1"
            label="한국어 능력"
            checked-icon="check_box"
            unchecked-icon="check_box_outline_blank"
            class="white-label"
            color="white"
          />
          <q-checkbox
            v-model="checked2"
            label="한국어 능력"
            checked-icon="check_box"
            unchecked-icon="check_box_outline_blank"
            class="white-label"
            color="white"
          />
          <q-checkbox
            v-model="checked3"
            label="한국어 능력"
            checked-icon="check_box"
            unchecked-icon="check_box_outline_blank"
            class="white-label"
            color="white"
          />
        </div>
        <div class="lt-md q-mb-lg flex justify-start items-end">
          <q-btn
            tag="a"
            href="/"
            flat
            label="개발자가필요하신가요"
            no-caps
            style="
              font-size: larger;
              text-decoration: underline;
              color: #fbff23 !important;
            "
          />
        </div>
      </div>
    </div>
    <MyFooter />
  </q-page>
</template>

<style scoped>
.home {
  max-width: 1170px;
  margin: auto;
}
.banner {
  background-image: url("../assets/banner.png");
  background-repeat: no-repeat;
  background-size: cover;
}
.my-card {
  background-color: transparent !important;
  width: 30%;
  padding-left: 0px;
}

.btn-section {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.btn {
  display: flex;
  align-items: center;
  justify-content: start;
  gap: 10px;
  padding: 10px;
  background: #ffffff33;
  border-radius: 10px;
  /* width: 210px; */
}
@media (max-width: 1200px) {
  .banner {
    background-image: url("../assets/banner.png");
    background-repeat: no-repeat;
    /* background-size: cover; */
    height: fit-content;
  }
  .home {
    padding: 0 20px 20px 20px;
  }
}
.white-label .q-checkbox__label {
  color: white;
}
.white-label {
  color: white;
}
</style>

<script>
import { ref } from "vue";
import Swiper from "swiper";
import "swiper/swiper-bundle.css";

import MyFooter from "components/MyFooter.vue";
import SliderLink from "components/SliderLink.vue";

export default {
  name: "IndexPage",
  components: {
    MyFooter,
    SliderLink,
  },
  data() {
    return {
      checked: true,
      checked1: true,
      checked2: true,
      checked3: true,
    };
  },
};
</script>
