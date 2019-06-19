<template>
  <div id="app">



  <div id="wrapper">
    <header id="header">
      <h1 class="logo">
        <span class="logo-title">Hoshi Daisuke</span>
      </h1>
    </header>
    <nav id="gnav">
      <ul>
        <li>
          <a href="#works">WORKS</a>
        </li>
        <li>
          <a href="#about">ABOUT</a>
        </li>
        <li>
          <a href="#contact">CONTACT</a>
        </li>
      </ul>
    </nav>
    <main id="contents">
      <section class="section" id="works">
        <div class="inner">
          <div class="section-title-block">
            <h2 class="section-title">WORKS</h2>
            <div class="section-desc">
              <p class="text">
                これまでの制作実績です。</p>
            </div>
          </div>

          <div class="wrapper my-gallery">
          </div>
          <product-list v-bind:products="products"></product-list>
        </div>
      </section>

      <section class="section" id="about">
        <div class="inner">
          <div class="section-title-block">
            <h2 class="section-title">ABOUT</h2>
          </div>
          <div class="two-column-wrapper">
            <div class="two-column-image">
              <img src="./assets/img/profile/img_profile.png" alt="" width="250">
            </div>
            <div class="two-column-desc">
              <p class="text">
                5年間のWeb制作会社を経てフリーランスになりました。セマンティックなマークアップ、汎用性のあるモジュール設計、動きのあるcss3アニメーション、汎用的な機能のJSプラグイン開発等をしてきました。
                <br>趣味：オムレツをつくること </p>
            </div>
          </div>
        </div>
      </section>
      <section class="section" id="contact">
        <div class="inner">
          <div class="section-title-block">
            <h2 class="section-title">CONTACT</h2>
            <p class="section-desc">
              お問合わせは下記からご連絡をください。
            </p>
          </div>
          <div class="contact-wrapper">
            <div class="contact-list">
              <ul>
                <li>
                  <a href="mail:hoshidaisuke.work@gmail.com">
                    <i class="fas fa-envelope-open" style="font-size: 30px;display: block"></i>
                    <span class="contact-list-desc">メール</span>
                  </a>
                </li>
                <li>
                  <a href="https://www.frontendmemo.xyz/" target="_blank">
                    <i class="fas fa-pen" style="font-size: 30px;display: block"></i>
                    <span class="contact-list-desc">blog</span>
                  </a>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </section>
    </main>
    <footer id="footer">
      <div class="inner">
        <nav class="footer-link">
          <ul>
            <li>
              <a href="#works">WORKS</a>
            </li>
            <li>
              <a href="#about">ABOUT</a>
            </li>
            <li>
              <a href="#contact">CONTACT</a>
            </li>
          </ul>
        </nav>
        <p class="copyright">Copyright&copy;Sho Satoh. All Rights Reserved.</p>
      </div>
    </footer>
  </div>
  </div>
</template>

<script>
import productList from './components/product-list.vue'

export default {
  name: 'app',
  components: {
    'product-list': productList
  },
  data: function () {
    return {
      products: [
        {id: 1, name: 'TIREHOOD', year: '2019', image: require('./assets/img/works/thumb/thumb_01.png'), category: 'ECサイト', use: 'git', info: '新規ページ開発、既存コンテンツ改修'},
      {id: 2, name: '西武鉄道キッズ', year: '2017', image: require('./assets/img/works/thumb/thumb_02.png'), category: 'インタラクティブ', use: 'gulp', info: 'サイト構築、クイズゲーム開発'},
        {id: 3, name: 'サンシャイン60展望台 - サンシャインシティ', year: '2018', image: require('./assets/img/works/thumb/thumb_03.png'), category: '大規模', use: 'gulp', info: 'サイト構築'},
        {id: 4, name: 'ふたば保育園', year: '2019', image: require('./assets/img/works/thumb/thumb_04.png'), category: '受託制作', use: 'Vue.js', info: 'サイト構築、Vue.jsでSPA構築'},
        {id: 5, name: 'ダンキラ!!!', year: '2018', image: require('./assets/img/works/thumb/thumb_05.png'), category: 'インタラクティブ', use: 'ES6', info: 'サイト構築'},
        {id: 6, name: 'frontend-tools', year: '2019', image: require('./assets/img/works/thumb/thumb_06.png'), category: '個人サイト', use: 'Vue.js', info: '個人のツールサイト'},
        {id: 7, name: 'ネオファースト試算ツール', year: '2018', image: require('./assets/img/works/thumb/thumb_07.png'), category: '試算ツール', use: 'API', info: '試算ツール'},
        {id: 8, name: 'Kirarina', year: '2019', image: require('./assets/img/works/thumb/thumb_08.png'), category: '受託制作', use: 'gulp', info: 'LP構築'},
        {id: 9, name: 'とくらく', year: '2016', image: require('./assets/img/works/thumb/thumb_09.png'), category: 'メディア', use: '大規模', info: 'サイト構築'},
        {id: 10, name: '商船三井フェリー', year: '2017', image: require('./assets/img/works/thumb/thumb_10.png'), category: '大規模', use: 'grant', info: 'サイト構築'}
      ]
    }
  }
}
</script>

<style>
  /*
html5doctor.com Reset Stylesheet
v1.6.1
Last Updated: 2010-09-17
Author: Richard Clark - http://richclarkdesign.com
Twitter: @rich_clark
*/

html, body, div, span, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
abbr, address, cite, code,
del, dfn, em, img, ins, kbd, q, samp,
small, strong, sub, sup, var,
b, i,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, figcaption, figure,
footer, header, hgroup, menu, nav, section, summary,
time, mark, audio, video {
    margin:0;
    padding:0;
    border:0;
    outline:0;
    font-size:100%;
    vertical-align:baseline;
    background:transparent;
}

body {
    line-height:1;
}

article,aside,details,figcaption,figure,
footer,header,hgroup,menu,nav,section {
    display:block;
}

nav ul {
    list-style:none;
}

blockquote, q {
    quotes:none;
}
select {

}
blockquote:before, blockquote:after,
q:before, q:after {
    content:'';
    content:none;
}

a {
    margin:0;
    padding:0;
    font-size:100%;
    vertical-align:baseline;
    background:transparent;
}

/* change colours to suit your needs */
ins {
    background-color:#ff9;
    color:#000;
    text-decoration:none;
}

/* change colours to suit your needs */
mark {
    background-color:#ff9;
    color:#000;
    font-style:italic;
    font-weight:bold;
}

del {
    text-decoration: line-through;
}

abbr[title], dfn[title] {
    border-bottom:1px dotted;
    cursor:help;
}

table {
    border-collapse:collapse;
    border-spacing:0;
}

/* change border colour to suit your needs */
hr {
    display:block;
    height:1px;
    border:0;
    border-top:1px solid #cccccc;
    margin:1em 0;
    padding:0;
}

input, select {
    vertical-align:middle;
}

/* CSS Document */

*, *:before, *:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  -o-box-sizing: border-box;
  -ms-box-sizing: border-box;
  box-sizing: border-box;
}

body {
  font-family: 'ヒラギノ角ゴ Pro W3', 'Hiragino Kaku Gothic Pro', "游ゴシック Medium", "Yu Gothic Medium", "游ゴシック体", YuGothic, 'メイリオ', Meiryo, Osaka, 'ＭＳ Ｐゴシック', 'MS PGothic', sans-serif;
  color: #333;
  font-size: 15px;
  line-height: 1.8;
  letter-spacing: 0.8px;
  word-break: break-all;
}

a {
  color: #1ca9e3;
  text-decoration: none;
}

a:hover, a:hover img {
  opacity: .8;
  -webkit-transition: all .3s;
  -moz-transition: all .3s;
  -ms-transition: all .3s;
  -o-transition: all .3s;
  transition: all .3s;
}

img, video, object {
  max-width: 100%;
  height: auto;
  border: none;
  vertical-align: bottom;
  display: block;
}

ul, li {
  list-style: none;
}

/*--------------------------------
　全体
---------------------------------*/

#wrapper {
  background-color: #f3f3f3;
}

.inner {
  max-width: 1320px;
  width: 100%;
  margin: 0 auto;
  padding: 0 10px;
}

#contents {
  padding: 100px 0;
}

/*--------------------------------
　ヘッダー
---------------------------------*/

#header {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  justify-content: center;
  -webkit-align-items: center;
  -ms-align-items: center;
  align-items: center;
  height: 380px;
}

#header .logo {
  display: block;
}

#header .logo-name {
  display: block;
  font-family: 'Yesteryear', cursive;
  display: block;
  position: relative;
  top: -8px;
  left: -60px;
  font-size: 36px;
  color: #125788;
  -webkit-transform: rotate(-10deg);
  transform: rotate(-10deg);
}

#header .logo-title {
  font-family: 'Oswald', sans-serif;
  font-size: 94px;
  color: #125788;
  line-height: 1;
  letter-spacing: -2px;
}

#header .logo-desc {
  display: block;
  font-size: 16px;
  text-align: center;
  margin-top: 5px;
}

/*--------------------------------
　グローバルナビ
---------------------------------*/

#gnav {
  padding: 10px;
  font-family: 'Open sans', sans-serif;
  z-index: 100;
}

#gnav ul {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -ms-flex-wrap: wrap;
  flex-wrap: wrap;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  justify-content: center;
}

#gnav li {
  font-weight: bold;
  font-size: 18px;
  padding: 0 20px;
}

#gnav li:last-child {
  margin-right: 0;
}

#gnav li a {
  color: #333;
  letter-spacing: -0.01em;
}

#gnav.fixed {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: #f3f3f3;
  box-shadow: 0px 6px 3px -3px rgba(0, 0, 0, 0.2);
  -webkit-box-shadow: 0px 6px 3px -3px rgba(0, 0, 0, 0.2);
  -moz-box-shadow: 0px 6px 3px -3px rgba(0, 0, 0, 0.2);
  transform: translate3d(0, 0, 0);
}

/*--------------------------------
　Section
---------------------------------*/

.section .inner {
  padding: 80px 10px;
}

.section .section-title-block {
  text-align: center;
  margin-bottom: 30px;
}

.section .section-title {
  font-family: 'Oswald', sans-serif;
  letter-spacing: -0.01em;
  display: inline-block;
  font-size: 56px;
  font-weight: bold;
  margin-bottom: 10px;
  color: #125788;
}

.section .section-desc {
  text-align: center;
}

.two-column-wrapper {
  width: 80%;
  margin: 0 auto;
  padding: 20px 0;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -ms-flex-wrap: nowrap;
  flex-wrap: nowrap;
  -webkit-box-pack: justify;
  -ms-flex-pack: justify;
  justify-content: space-between;
}

.two-column-image {
  width: 33%;
}

.two-column-image img {
  margin: 0 auto;
}

.two-column-desc {
  width: 62%;
}

/*--------------------------------
　Latestworks
---------------------------------*/

#latestworks .two-column-image {
  width: 48%;
}

#latestworks .two-column-desc {
  width: 48%;
}

/*--------------------------------
　WORKS
---------------------------------*/

#works .card {
  width: calc(100% / 3 - 26px);
}

#works .card {
  margin-bottom: 50px;
  margin-left: 26px;
}

#works .card-image {
  display: block;
  margin-bottom: 8px;
}
#works .card-title-wrap {
  display: flex;
  justify-content: space-between;
  border-bottom: 1px dashed #ccc;
  padding-bottom: 5px;
  margin-bottom: 5px;
}

#works .card-caption-title {
  font-size: 13px;
  font-weight: bold;
}

#works .card-caption-info,
#works .card-caption-use,
#works .card-caption-category {
  font-size: 12px;
}
#works .card-caption-info span,
#works .card-caption-use span,
#works .card-caption-category span {
  font-weight: bold;
}
#works .card-caption-year {
  border: 1px solid #ccc;
  border-radius: 4px;
  font-size: 12px;
  padding: 0px 4px;
  width: 44px;
}


#works .sort-wrap {
  display: flex;
}
#works .condition {
  margin-left: 30px;
}
#works .sorting {
  padding: 2px 4px 2px 4px;
  border-radius: 4px;
  border: 1px solid #ccc;
}
  #works .card-wrapper {
  padding: 20px 0;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -ms-flex-wrap: wrap;
  flex-wrap: wrap;
  margin-left: -26px;
}

/*--------------------------------
　About
---------------------------------*/

#about .two-column-image {
  width: 33%;
}

#about .two-column-desc {
  width: 62%;
}

/*--------------------------------
 SKILL
---------------------------------*/

#skill .card-wrapper {
  width: 80%;
  margin: 0 auto;
  padding: 20px 0;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -ms-flex-wrap: wrap;
  flex-wrap: wrap;
  -webkit-box-pack: justify;
  -ms-flex-pack: justify;
  justify-content: space-between;
}

#skill .card {
  flex-basis: 46%;
  margin-bottom: 50px;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -ms-flex-wrap: nowrap;
  flex-wrap: nowrap;
  -webkit-box-pack: justify;
  -ms-flex-pack: justify;
  justify-content: space-between;
}

#skill .card:first-child {
  flex-basis: 100%;
}

#skill .skill-icon {
  flex-basis: 75px;
}

#skill .skill-icon img {
  width: 75px;
}

#skill .skill-desc {
  flex-basis: calc(100% - 75px - 30px);
}

#skill .skill-desc-title {
  margin-bottom: 3px;
}

#skill .rate {
  position: relative;
  display: inline-block;
  width: 110px;
  height: 20px;
  font-size: 20px;
}

#skill .rate:before, #skill .rate:after {
  position: absolute;
  top: 0;
  left: 0;
  content: '★★★★★';
  display: inline-block;
  height: 20px;
  line-height: 20px;
}

#skill .rate:before {
  color: #ddd;
}

#skill .rate:after {
  color: #1ca9e3;
  overflow: hidden;
  white-space: nowrap;
}

#skill .rate1:after {
  width: 20px;
}

#skill .rate2:after {
  width: 40px;
}

#skill .rate3:after {
  width: 60px;
}

#skill .rate4:after {
  width: 80px;
}

#skill .rate5:after {
  width: 100px;
}

/*--------------------------------
 CONTACT
---------------------------------*/

#contact .contact-list {
  padding: 20px 0;
}

#contact .contact-list ul {
  width: 40%;
  margin: 0 auto;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -ms-flex-wrap: wrap;
  flex-wrap: wrap;
  -webkit-box-pack: justify;
  -ms-flex-pack: justify;
  justify-content: space-between;
  align-self: flex-end;
  ;
}

#contact .contact-list li {
  text-align: center;
}

#contact .contact-list li a {
  color: #333;
}

#contact .contact-list li img {
  width: 60px;
  margin: 0 auto 5px;
}

#contact .contact-list-desc {
  font-weight: bold;
}

/*--------------------------------
 Footer
---------------------------------*/

#footer {
  background-color: #333;
}

#footer .inner {
  padding: 30px;
}

#footer .footer-link ul {
  margin-bottom: 30px;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -ms-flex-wrap: wrap;
  flex-wrap: wrap;
  -webkit-justify-content: center;
  -moz-justify-content: center;
  justify-content: center;
}

#footer .footer-link li {
  font-size: 12px;
  padding: 0 20px;
}

#footer .footer-link li a {
  color: #fff;
  font-weight: bold;
}

#footer .copyright {
  font-size: 10px;
  color: #8c8c8c;
  text-align: center;
}

/*media Queries 767
----------------------------------------------------*/

@media screen and (max-width: 767px) {
  body {
    font-size: 13px;
    line-height: 1.7;
  }
  #header {
    height: 200px;
  }
  #header .logo-title {
    font-size: 56px;
  }
  #header .logo-name {
    top: 0;
    left: -30px;
    font-size: 25px;
  }
  #header .logo-desc {
    font-size: 11px;
  }
  #gnav li {
    font-size: 14px;
    padding: 0 10px;
  }
  #gnav li a:hover {
    opacity: 1;
  }
  #contents {
    padding: 40px 0;
  }
  .section .inner {
    padding: 30px 15px;
  }
  .section .section-title-block {
    margin-bottom: 10px;
  }
  .section .section-title {
    font-size: 36px;
  }
  #latestworks .two-column-wrapper {
    width: 100%;
    -ms-flex-wrap: wrap;
    flex-wrap: wrap;
  }
  #latestworks .two-column-image {
    width: 90%;
    margin: 0 auto 20px;
  }

  #latestworks .two-column-desc {
    width: 100%;
  }
  #works .card {
    width: 48%;
  }
  #works .card-caption-title {
    font-size: 12px;
  }
  #works .card-caption-info {
    font-size: 11px;
  }
  #about .two-column-wrapper {
    width: 100%;
    -ms-flex-wrap: wrap;
    flex-wrap: wrap;
  }
  #about .two-column-image {
    width: 50%;
    margin: 0 auto 20px;
  }
  #about .two-column-desc {
   width: 100%;
 }

  #skill .card-wrapper {
    width: 100%;
  }
  #skill .card {
    flex-basis: 100%;
  }
  #skill .skill-icon {
    flex-basis: 45px;
  }
  #skill .skill-icon img {
    width: 45px;
  }
  #skill .skill-desc {
    flex-basis: calc(100% - 45px - 10px);
  }
  #skill .rate {
    height: 15px;
    font-size: 15px;
  }
  #skill .rate:before, #skill .rate:after {
    height: 15px;
    line-height: 15px;
  }
  #skill .rate1:after {
    width: 15px;
  }
  #skill .rate2:after {
    width: 30px;
  }
  #skill .rate3:after {
    width: 45px;
  }
  #skill .rate4:after {
    width: 60px;
  }
  #skill .rate5:after {
    width: 75px;
  }
  #contact .contact-list ul {
    width: 100%;
  }
  #contact .contact-list li {
    flex-basis: 30%;
  }
  #contact .contact-list li img {
    width: 30px;
  }
  #contact .contact-list-desc {
    font-size: 12px;
  }
  #footer .inner {
    padding: 20px 0;
  }
  #footer .footer-link li {
    font-size: 10px;
    padding: 0 10px;
    margin-bottom: 5px;
  }
}
</style>
