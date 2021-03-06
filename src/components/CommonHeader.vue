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
    <div class="menu" id="menu">
      <span class="menu-line-top"></span>
      <span class="menu-line-middle"></span>
      <span class="menu-line-bottom"></span>
    </div>
    <nav class="drawer-nav" id="drawer-nav">
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

<style scoped>

@charset "UTF-8";

* {
  box-sizing: border-box;
}

body {
  font-family: "Hiragino Kaku Gothic Pro", "ヒラギノ角ゴ Pro",
    "Yu Gothic Medium", "游ゴシック Medium", sans-serif;
  line-height: 1.6;
}

a {
  text-decoration: none;
  color: inherit;
  transition: 0.3s;
}

a:hover {
  opacity: 0.7;
  transition: 0.3s;
}

img {
  width: 100%;
  height: auto;
}

.wrap {
  width: 1080px;
  margin: 0 auto;
}

.wrap-s {
  width: 960px;
  margin: 0 auto;
}

.ptb-m {
  padding: 80px 0;
}

.btn {
  display: block;
  width: 300px;
  text-align: center;
  font-weight: bold;
  padding: 10px;
  background-color: #cd0224;
  color: #fff;
}

.ttl {
  font-size: 30px;
  font-weight: bold;
}

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
</style>