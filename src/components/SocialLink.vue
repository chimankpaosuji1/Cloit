<template>
  <div class="footer1">
    <div class="container">
      <div class="row">
        <div class="footer-col">
          <h4>상호명</h4>
          <ul>
            <li><a href="#">하이퍼하이어</a></li>
            <li><a href="#">Hyperhire India Private Limited</a></li>
          </ul>
        </div>
        <div class="footer-col">
          <h4>대표 CEO</h4>
          <ul>
            <li><a href="#">김주현</a></li>
            <li><a href="#">Juhyun Kim</a></li>
          </ul>
        </div>
        <div class="footer-col">
          <h4>사업자등록번호 CIN</h4>
          <ul>
            <li><a href="#">427-86-01187</a></li>
            <li><a href="#">U74110DL2016PTC290812 </a></li>
          </ul>
        </div>
        <div class="footer-col logo">
          <h4>주소 ADDRESS</h4>
          <ul>
            <li><a href="#">서울특별시 강남대로 479, 지하 1층 238호 </a></li>
            <li>
              <a href="#"
                >D-138, Street number 11, Jagjeet Nagar, North East Delhi, New
                Delhi, 110053 India</a
              >
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SocialLink",
  setup() {
    return {};
  },
};
</script>

<style>
.footer1 .container {
  max-width: 1170px;
  margin: auto;
}
.footer1 .row {
  display: flex;
  flex-wrap: wrap;
}
.footer1 ul {
  list-style: none;
  margin-left: -40px;
}
.footer1 {
  padding: 0px 0 20px 0;
}
.footer1 .logo {
	width:  35% !important;
}
.footer1 .footer-col {
  width: 20%;
  padding: 0 15px;
}
.footer1 .footer-col h4 {
  font-size: 13px;
  color: #000;
  font-weight: 500;
  position: relative;
}

.footer1 .footer-col ul li:not(:last-child) {
  margin-bottom: 10px;
}
.footer1 .footer-col ul li a {
  font-size: 14px;
  color: #ffffff;
  text-decoration: none;
  font-weight: 300;
  color: #000;
  display: block;
  transition: all 0.3s ease;
}
.footer1 .footer-col ul li a:hover {
  opacity: 0.8;
  padding-left: 8px;
}

/*responsive*/
@media (max-width: 767px) {
  .footer1 .footer-col {
    width: 50%;
    margin-bottom: 30px;
  }
  .footer1 .footer-col h4 {
    font-size: 20px;
  }
  .footer1 .footer-col ul li a {
    font-size: 18px;
  }
	.footer1 .logo {
	width:  100% !important;
}
}
@media (max-width: 574px) {
  .footer1 .footer-col {
    width: 100%;
  }
}
</style>
