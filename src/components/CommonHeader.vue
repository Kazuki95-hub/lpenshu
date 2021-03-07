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
            this.isClass = !this.isClass;
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
    z-index: 999;
    font-weight: bold;
  }
  #menu span {
    position: absolute;
    left: 2px;
    display: block;
    width: 35px;
    height: 2px;
    background-color: black;
    transition: 0.8s;
    z-index:999;
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
  .drawer-nav {
    display: block;
    width: 100%;
    height: 100%;
    text-align: center;
    transition: 0.8s;
    position: fixed;
    top: 0;
    left: calc(-100% - 80px);
    background: white;
    color: #333333;
    box-shadow: 80px 0 rgba(38, 98, 213, 0.3);
    z-index: 998;
  }

  .drawer-nav-list li a {
    color: blue;
    margin: 15px;
    padding: 5px;
    text-decoration: none;
    display: block;
  }
  .drawer-nav-list li {
    width: 100%;
    text-align: center;
    z-index:998;
  }
  .drawer-nav.open {
    left: 0;
  }
  .drawer-nav{
    display: block;
    
}
}
</style>