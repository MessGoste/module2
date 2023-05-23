<template>
  <div class="header">
    <img src="../assets/logo.png" />
    <div class="ad-menu">
      <nav class="navMenu" tabindex="1">
        <ul>
          <li><a href="#">Главная</a></li>
          <li><a href="#">Каталог</a></li>
          <li><a href="#">Блог</a></li>
          <li><a href="#">Решения</a></li>
          <li><a href="#">Контакты</a></li>
        </ul>
        <div class="dot"></div>
      </nav>
    </div>
    <div class="icons">
      <link
        rel="stylesheet"
        href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@48,400,0,0"
      />
      <span class="material-symbols-outlined search_icon"> search </span>
      <link
        rel="stylesheet"
        href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200"
      />
      <span class="material-symbols-outlined shopping_cart_icon">
        shopping_cart
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: `headers`,
};
</script>

<style scoped>
img {
  margin-left: 150px;
  margin-top: 32px;
  width: 126px;
  height: 32px;
}
.header {
  /*margin: 0px;*/
  background: #d3cbc5;
  height: 79px;
  display: flex;
  justify-content: space-between;
}
.navMenu {
  margin-top: 5px;
}
.navMenu a {
  color: black;
  text-decoration: none;
  font-size: 1.1em;
  text-transform: uppercase;
  font-weight: 500;
  display: inline-block;
  width: 80px;
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  margin: 0px 10px 0px 10px;
}
.material-symbols-outlined {
  font-variation-settings: "FILL" 0, "wght" 400, "GRAD" 0, "opsz" 48;
}
.search_icon {
  margin-right: 27px;
  cursor: pointer;
}
.shopping_cart_icon {
  cursor: pointer;
}
.icons {
  margin-right: 150px;
  margin-top: 32px;
}

.ad-menu *:focus,
.ad-menu *::before,
.ad-menu *::after {
  padding: 0;
  margin: 0;
  outline: 0;
  box-sizing: content-box;
}
.ad-menu li {
  display: inline-block;
  background: #d3cbc5;
  font-size: 1em;
  text-align: center;
  width: 150px;
}
.ad-menu li:hover {
  background: rgba(0, 0, 0, 0);
}
.ad-menu li a {
  display: block;
  text-decoration: none;
  color: #000;
  padding: 1px 0;
  width: 100%;
  font-size: 15px;
}
/*поведение меню при разрешении менее 920 пикселей*/
@media screen and (max-width: 920px) {
  .ad-menu li {
    width: 49.5%;
  }
}
/*поведения и структура при экране менее 680 пикселей*/
@media screen and (max-width: 768px) {
  .ad-menu li {
    width: 100%;
  }
  .ad-menu ul {
    display: none;
  }
  .ad-menu nav::before,
  .ad-menu::after {
    content: "";
    position: absolute;
    top: 0;
    right: 0;
    display: block;
    background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAwCAMAAAA8VkqRAAAABlBMVEUAAAAAAAClZ7nPAAAAAXRSTlMAQObYZgAAAE5JREFUeAFjwAkYcQC6SFAKBt4fo/6AaMMUQTUQIYJpFaqrMIICzkATR2Hi5uDUjmkh7tDAHUq4Qw8ujl+CsFEEHDVowg1n1OJKDLiTDwBLrgJ9vkuXOwAAAABJRU5ErkJggg==);
    cursor: pointer;
    height: 24px;
    width: 24px;
  }
  .ad-menu nav::before,
  .ad-menu::after {
    background-color: #fff;
    border: 9px solid #fff;
  }
  .ad-menu::after {
    background-position: -24px -24px;
    z-index: 1;
  }
  .ad-menu nav::before {
    z-index: 2;
  }
  .ad-menu nav:focus::before {
    z-index: 0;
  }
  .ad-menu nav:focus ul,
  .ad-menu ul:hover {
    /*решаем проблему со скликиванием*/
    display: block;
  }
}
</style>
