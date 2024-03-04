<script>
  export default {
    props:{
      list:{
        type:Array,
        required:true,
      },
      link:{
        type:String,
        required: true
      }
    }
  }
</script>

<template>
  <nav class="nav">
    <a class="nav__link" href="#">
      <img src="@/assets/img/logo.svg" alt="logo">
      <div>
        <p>O'ZBEKISTON TEMIR YO'LLARI</p>
        <p>AKSIYADOLIK JAMIYATI</p>
      </div>
    </a>
    <ul class="nav__item">
      <li>
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
          <!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.-->
          <path
              d="M464 256A208 208 0 1 1 48 256a208 208 0 1 1 416 0zM0 256a256 256 0 1 0 512 0A256 256 0 1 0 0 256zM232 120V256c0 8 4 15.5 10.7 20l96 64c11 7.4 25.9 4.4 33.3-6.7s4.4-25.9-6.7-33.3L280 243.2V120c0-13.3-10.7-24-24-24s-24 10.7-24 24z"/>
        </svg>
        <a href="#">Poyezdlar jadvali</a>
      </li>
      <li>
        <a href="#">Kirish</a>
      </li>
      <li :class="link" v-for="listItem in list">{{listItem}}</li>
    </ul>
  </nav>
</template>

<style scoped>
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 13px 0;
}

.nav__link {
  display: flex;
  width: max-content;
  height: 50px;
  text-decoration: none;
  color: rgba(0, 0, 0, 0.75);
}

.nav__link img {
  height: 100%;
}

.nav__link div {
  margin: auto 1rem;
}

.nav__link p:first-child {
  font-size: 16px;
  font-weight: 700;
  padding-bottom: 2px;
  margin: 0;
}

.nav__link p:last-child {
  font-size: 14px;
  margin: 0;
  padding: 0;
}

.nav__item {
  display: flex;
  justify-content:space-between;
  align-items: center;
}

.nav__item li {
  display: flex;
  align-items: center;
  margin-right: 10px;
  height: 30px;
}

.nav__item li {
  svg {
    height: 18px;
  }

  a {
    text-decoration: none;
    color: black;
    padding: 2px 5px;
  }

  &:last-child {
    a:hover {
      border-radius: 5px;
      border: 1px solid #ff0000;
      padding: 2px 5px;
      transition: 0.5s;
    }
  }
}
.link:hover{
  border: 1px solid red;
  border-radius: 5px;
  transition: 1s;
}

</style>