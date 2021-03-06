<template>
    <footer class="footer">
    <div class="footer-inner wrap">
      <small class="footer-copyright">&copy; 2020 TECH inc.</small>
      <nav class="footer-nav">
        <ul class="footer-nav-list">
          <li class="footer-nav-item"><a href="index.html">ホーム</a></li>
          <li class="footer-nav-item"><a href="service.html">事業内容</a></li>
          <li class="footer-nav-item"><a href="news.html">ニュース</a></li>
          <li class="footer-nav-item"><a href="blog.html">社員ブログ</a></li>
          <li class="footer-nav-item"><a href="company.html">会社概要</a></li>
          <li class="footer-nav-item"><a href="recruit.html">採用情報</a></li>
          <li class="footer-nav-item"><a href="contact.html">お問い合わせ</a></li>
        </ul>
      </nav>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  padding: 20px 0;
  color: #fff;
  background-color: #222;
}

.footer-inner {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  font-size: 12px;
}

.footer-nav-list {
  display: flex;
  flex-wrap: wrap;
}

.footer-nav-item:after {
  content: "|";
  display: inline-block;
  padding: 0 10px;
}

.footer-nav-item:last-child:after {
  display: none;
}

@media screen and (max-width: 768px) {
  .wrap {
    width: 85%;
  }

  .wrap-s {
    width: 90%;
  }

  .header-nav {
    display: none;
  }

  .menu {
    display: inline-block;
    width: 36px;
    height: 32px;
    cursor: pointer;
    position: relative;
    z-index: 10;
  }

  .menu-line-top,
  .menu-line-middle,
  .menu-line-bottom {
    display: inline-block;
    width: 100%;
    height: 4px;
    background-color: #000;
    position: absolute;
    transition: 0.5s;
  }

  .menu-line-top {
    top: 0;
  }

  .menu-line-middle {
    top: 14px;
  }

  .menu-line-bottom {
    bottom: 0;
  }

  .menu.open span:nth-of-type(1) {
    top: 14px;
    transform: rotate(45deg);
  }

  .menu.open span:nth-of-type(2) {
    opacity: 0;
  }

  .menu.open span:nth-of-type(3) {
    top: 14px;
    transform: rotate(-45deg);
  }

  .drawer-nav{
    display: block;
    position: absolute;
    height: 100vh;
    width: 100%;
    top: 0;
    left: -100%;
    background: #fff;
    transition: .7s;
  }

  .drawer-nav-list {
    padding-top: 80px;
    text-align: center;
  }

  .drawer-nav-item {
    margin-top: 40px;
    color: #0033cc;
    font-size: 18px;
  }

  .in {
    transform: translateX(100%);
  }

  .footer-copyright {
    margin: 0 auto;
  }

  .footer-nav-item {
    text-align: center;
    margin-top: 10px;
    width: 100%;
  }

  .footer-nav-item:after {
    display: none;
  }
}

</style>