<template>
    <header class="header">
    <h1 class="header-ttl">
      <a href="index.html">
        TECH
      </a>
    </h1>
    <nav class="header-nav">
      <ul class="header-nav-list">
        <li class="header-nav-item"><a href="index.html">ホーム</a></li>
        <li class="header-nav-item"><a href="service.html">事業内容</a></li>
        <li class="header-nav-item"><a href="news.html">ニュース</a></li>
        <li class="header-nav-item"><a href="blog.html">社員ブログ</a></li>
        <li class="header-nav-item"><a href="company.html">会社概要</a></li>
        <li class="header-nav-item"><a href="recruit.html">採用情報</a></li>
        <li class="header-nav-item"><a href="contact.html">お問い合わせ</a></li>
      </ul>
    </nav>
    <div class="menu" id="menu" @click= "hamburger()" :class= "{'active':isClass}">
      <span class="menu-line-top"></span>
      <span class="menu-line-middle"></span>
      <span class="menu-line-bottom"></span>
    </div>
    <nav class="drawer-nav" id="drawer-nav" :class= "{'open':isClass}">
      <ul class="drawer-nav-list">
        <li class="drawer-nav-item"><a href="index.html">ホーム</a></li>
        <li class="drawer-nav-item"><a href="service.html">事業内容</a></li>
        <li class="drawer-nav-item"><a href="news.html">ニュース</a></li>
        <li class="drawer-nav-item"><a href="blog.html">社員ブログ</a></li>
        <li class="drawer-nav-item"><a href="company.html">会社概要</a></li>
        <li class="drawer-nav-item"><a href="recruit.html">採用情報</a></li>
        <li class="drawer-nav-item"><a href="contact.html">お問い合わせ</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
    data(){
        return {
            isClass :false
        };
    },
    methods:{
        hamburger() {
            this.isClass = !this.isClass
        }
    }
};
</script>

<style scoped>

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 70px;
  padding: 0 30px;
  background-color: #fff;
  position: sticky;
  left: 0;
  top: 0;
  z-index: 1;
}

.header-ttl {
  font-size: 24px;
  width: 80px;
}

.header-nav-list {
  display: flex;
  font-weight: bold;
}

.header-nav-item:not(:last-child) {
  margin-right: 30px;
}

.menu {
  display: none;
}

.drawer-nav {
  display: none;
}

@media screen and (max-width: 768px) {
  #menu {
    width: 40px;
    height: 40px;
    position: absolute;
    cursor: pointer;
    z-index: 100;
    top: 15px;
    right: 20px;
    transition: 0.4s;
  }
  #menu span {
    position: absolute;
    left: 2px;
    display: block;
    width: 35px;
    height: 2px;
    background-color: black;
    transition: 0.8s;
  }
  #menu span:nth-of-type(1) {
    top: 10px;
  }
  #menu span:nth-of-type(2) {
    top: 20px;
  }
  #menu span:nth-of-type(3) {
    top: 30px;
  }
  .header-nav {
    display: none;
  }

  /* ここを追加 */
  #menu.active span:nth-of-type(1) {
    top: 20px;
    transform: rotate(45deg);
  }

  #menu.active span:nth-of-type(2) {
    opacity: 0;
  }
  #menu.active span:nth-of-type(3) {
    top: 20px;
    transform: rotate(-45deg);
  }
  .drawer-nav-list {
    display: block;
    width: calc(100% - 80px);
    height: 100%;
    text-align: center;
    transition: 0.2s;
    position: fixed;
    top: 0;
    left: calc(-100% - 80px);
    background: white;
    color: #333333;
    box-shadow: 80px 0 rgba(38, 98, 213, 0.3);
    z-index: 999;
  }
  /* .menu-content .menu-title {
    margin: 40px 20px;
    font-size: 2.2rem;
    color: #333333;
    text-align: left;
    font-weight: bold;
  } */
  .menu-content li a {
    color: #333333;
    margin: 15px;
    padding: 5px;
    border-bottom: 0.5px solid #2662d5;
    text-decoration: none;
    display: block;
  }
  .menu-content li {
    width: 100%;
    text-align: left;
  }
  .menu-content.open {
    left: 0;
  }
}
</style>