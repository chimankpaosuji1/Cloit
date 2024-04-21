<template>
  <footer class="footer">
    <div class="container">
      <div class="row">
        <div class="footer-col logo">
          <q-img src="../assets/logo2.svg" width="170px" />
          <ul>
            <li>
              <a href="#"
                >우리는 국가의 장벽을 넘어 최고의 인재를 매칭해드립니다.</a
              >
            </li>
            <li><a href="#">010-0000-0000</a></li>
            <li><a href="#">aaaaa@naver.com</a></li>
          </ul>
        </div>
        <div class="footer-col">
          <q-img src="../assets/ficon1.svg" width="35px" />
          <ul>
            <li><a href="#">해외 개발자 원격 채용</a></li>
            <li>
              <a href="#"
                >바로가기
                <q-img src="../assets/icon-left.svg" width="20px" />
              </a>
            </li>
          </ul>
        </div>
        <div class="footer-col">
          <q-img src="../assets/ficon2.svg" width="35px" />
          <ul>
            <li><a href="#">외국인 원격 채용 (비개발)</a></li>
            <li>
              <a href="#"
                >바로가기 <q-img src="../assets/icon-left.svg" width="20px"
              /></a>
            </li>
          </ul>
        </div>
        <div class="footer-col">
          <q-img src="../assets/ficon3.svg" width="35px" />
          <ul>
            <li><a href="#">한국어 가능 외국인 채용 바로가기</a></li>
            <li>
              <a href="#"
                >바로가기 <q-img src="../assets/icon-left.svg" width="20px"
              /></a>
            </li>
          </ul>
        </div>
        <div class="footer-col">
          <q-img src="../assets/ficon4.svg" width="35px" />
          <ul>
            <li><a href="#">해외 개발자 활용 서비스</a></li>
            <li>
              <a href="#"
                >바로가기 <q-img src="../assets/icon-left.svg" width="20px"
              /></a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
  <SocialLink />
  <div class="copyright">© {{ currentYear }} Hyperhire</div>
</template>

<script>
import SocialLink from "components/SocialLink.vue";

export default {
  name: "MyFooter",

  components: {
    SocialLink,
  },

  computed: {
    currentYear() {
      return new Date().getFullYear();
    },
    height() {
      return 60;
    },
  },
};
</script>

<style lang="scss" scoped>
.container {
  max-width: 1170px;
  margin: auto;
}
.row {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
ul {
  list-style: none;
  margin-left: -40px;
}
.footer {
  padding: 70px 0 0px 0;
}
.footer-col {
  width: 17%;
  padding: 0 15px;
}
.logo {
  width: 30%;
}
.footer-col h4 {
  font-size: 18px;
  color: #000;
  margin-bottom: 35px;
  font-weight: 500;
  position: relative;
}
.footer-col ul li:not(:last-child) {
  margin-bottom: 10px;
}
.footer-col ul li a {
  font-size: 14px;
  text-decoration: none;
  font-weight: 300;
  color: #000;
  display: block;
  transition: all 0.3s ease;
}
.footer-col ul li a:hover {
  opacity: 0.8;
  padding-left: 8px;
}

.copyright {
  font-size: 14px;
  max-width: 1170px;
  margin: auto;
  padding-left: 10px;
  margin-bottom: 20px;
}

/*responsive*/
@media (max-width: 767px) {
  .footer-col {
    width: 50%;
    margin-bottom: 30px;
  }
    .footer-col h4 {
    font-size: 20px;
  }
  .footer-col ul li a {
    font-size: 18px;
  }
  .copyright {
  font-size: 18px;
}
}
@media (max-width: 574px) {
  .footer-col {
    width: 100%;
  }

}
</style>
