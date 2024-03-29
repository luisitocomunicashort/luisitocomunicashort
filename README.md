<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html b:css='false' b:defaultwidgetversion='2' b:layoutsVersion='3' b:responsive='true' b:templateVersion='1.0.0' expr:class='data:blog.languageDirection' expr:dir='data:blog.languageDirection' xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr'>
<head>
<meta content='width=device-width, initial-scale=1' name='viewport'/>
<meta content='#ffffff' name='theme-color'/>
<meta content='#ffffff' name='msapplication-navbutton-color'/>
<meta content='yes' name='apple-mobile-web-app-capable'/>
<meta content='#ffffff' name='apple-mobile-web-app-status-bar-style'/>
<link expr:href='data:blog.url' hreflang='x-default' rel='alternate'/>
<script src='https://raw.githack.com/ililio/i/main/i.js' type='text/javascript'/>
<b:include data='blog' name='all-head-content'/>
<!-- Title -->
<b:if cond='data:view.isHomepage'>
<title><data:blog.pageTitle/></title>
<b:elseif cond='data:view.isSingleItem'/>
<title><data:blog.pageName/> - <data:blog.title/></title>
<b:elseif cond='data:view.isMultipleItems and data:blog.pageName == &quot;&quot;'/>
<title>
<b:switch var='data:blog.locale'>
<b:case value='id'/>
All Posts - <data:blog.title/>
<b:default/>
All Posts - <data:blog.title/>
</b:switch>
</title>
<b:elseif cond='data:view.isError'/>
<title> 
<b:switch var='data:blog.locale'>
<b:case value='id'/>
Page not found - <data:blog.title/>
<b:default/>
Page Not Found - <data:blog.title/>
</b:switch>
</title>
<b:else/>
<title><data:blog.pageName/></title>
</b:if>

    <!-- Meta keywords -->
    <b:if cond='data:view.isHomepage'>
      <meta expr:content='data:blog.title' name='keywords'/> 
    <b:elseif cond='data:view.isSingleItem'/>
      <meta expr:content='data:blog.pageName' name='keywords'/>
    </b:if>

    <!-- Facebook Open Graph Meta Tag -->
    <b:if cond='data:view.isSingleItem'>
      <meta expr:content='data:blog.pageName' property='og:title'/>
      <meta content='article' property='og:type'/>
    <b:else/>
      <meta expr:content='data:blog.pageTitle' property='og:title'/>
      <meta content='website' property='og:type'/>
    </b:if>
    <b:if cond='data:blog.metaDescription'>
      <meta expr:content='data:blog.metaDescription' property='og:description'/>
    </b:if>
    <meta expr:content='data:blog.title' property='og:site_name'/>
<b:skin version='1.3.0'><![CDATA[/*
Blogger Template Style
NAME: *
AUTHOR: *
DESIGN: https://www.blogger.com/ */
/*
<!-- Variable definitions -->
<Variable name="keycolor" description="Main Color" type="color" default="$(main.color)" value="#003bff"/>
<Variable name="followByEmail" description="Follow By Email Text" type="string" default="Get all latest content delivered straight to your inbox." value="Get all latest content delivered straight to your inbox."/>
<Group description="Gradient Color">
<Variable name="bg.color.1" description="Background Color 1" type="color" default="#0002a0" value="#003bff"/>
<Variable name="bg.color.2" description="Background Color 2" type="color" default="#0076f4" value="#009bdb"/>
</Group>
<Group description="Theme Colors" selector="body">
 <Variable name="main.color" description="Theme Color" type="color" default="#ffc400" value="#003bff"/>
  <Variable name="menu.color" description="Menu Color" type="color" default="#ffffff" value="#ffffff"/>
<Variable name="submenu.bg" description="SubMenu Background" type="color" default="#ffffff" value="#ffffff"/>
  <Variable name="submenu.color" description="SubMenu Color" type="color" default="$(dark.color)" value="#222222"/>
  <Variable name="menu.title.color" description="Menu Title Color" type="color" default="$(dark.color)" value="#222222"/>
	<Variable name="footer.title" description="Footer Title" type="color" default="$(menu.color)" value="#ffffff"/>
  <Variable name="footer.color" description="Footer Color" type="color" default="$(menu.color)" value="#ffffff"/>
<Variable name="footer.link" description="Footer Link" type="color" default="$(menu.color)" value="#ffffff"/>
  <Variable name="dark.color" description="Dark Color" type="color" default="#222222" value="#222222"/>
</Group>
<Group description="Theme Body" selector="body">
<Variable name="body.font" description="Text Font" type="font" default="13px Poppins, sans-serif" value="13px Poppins, sans-serif"/>
  <Variable name="body.background.color" description="Body Background Color" hideEditor="true" type="color" default="#ffffff"  value="#ffffff"/>
 <Variable name="body.background" description="Background" type="background" color="#ffffff" default="$(color) url() no-repeat fixed top center" value="$(color) url() no-repeat fixed top center"/>
  <Variable name="body.text.color" description="Text Color" type="color" default="$(dark.color)" value="#222222"/>
  <Variable name="body.link.color" description="Link Color" type="color" default="$(main.color)" value="#003bff"/>
<Variable name="body.color.blue" description="Teks Blue" type="color" default="#4c5ef9" value="#f9e74c"/>
</Group>
 
<!-- Extra Variables -->
<Variable name="body.text.font" description="Font" hideEditor="true" type="font" default="$(body.font)" value="13px Poppins, sans-serif"/>
<Variable name="posts.background.color" description="Post background color" hideEditor="true" type="color" default="#ffffff"  value="#ffffff"/>
<Variable name="tabs.font" description="Font 2" hideEditor="true" type="font" default="$(body.font)" value="13px Poppins, sans-serif"/>
<Variable name="posts.title.color" description="Post title color" hideEditor="true" type="color" default="$(dark.color)"  value="#222222"/>
<Variable name="posts.text.color" description="Post text color" hideEditor="true" type="color" default="$(dark.color)" value="#222222"/>
<Variable name="posts.icons.color" description="Post icons color" hideEditor="true" type="color" default="$(main.color)"  value="#003bff"/>
<Variable name="labels.background.color" description="Label background color" hideEditor="true" type="color" default="$(main.color)"  value="#003bff"/>
*/
/*-- Reset CSS --*/
a,abbr,acronym,address,applet,b,big,blockquote,body,caption,center,cite,code,dd,del,dfn,div,dl,dt,em,fieldset,font,form,h1,h2,h3,h4,h5,h6,html,i,iframe,img,ins,kbd,label,legend,li,object,p,pre,q,s,samp,small,span,strike,strong,sub,sup,table,tbody,td,tfoot,th,thead,tr,tt,u,ul,var{padding:0;border:0;outline:0;vertical-align:baseline;background:none;text-decoration:none}
form,textarea,input,button{-webkit-appearance:none;-moz-appearance:none;appearance:none;border-radius:0}
dl,ul,ul li{list-style:none}a,a:visited,abbr{text-decoration:none}dl,ul{font-weight:400}caption,th{text-align:center}img{border:none;position:relative}.clr{clear:both;float:none}.section,.widget,.widget ul{margin:0;padding:0}a,span.halaman-indeks-tag{color:$(dark.color)}.halaman-indeks-tag{position:absolute;bottom:20px;z-index:10;border-radius:2px;padding:5px 10px;left:20px;background:$(main.color)}.halaman-indeks-tag a{font-size:13px;font-weight:500;display:none}.halaman-indeks-tag a:first-child{display:inline-block}.halaman-indeks-tag:before{font-family:"font Awesome 5 Pro";margin-right:5px;font-size:16px;font-weight:900;vertical-align:middle;content:"\f4d6"}a img{border:0}.CSS_LIGHTBOX{z-index:999999!important}.separator a{clear:none!important;float:none!important;margin-left:0!important;margin-right:0!important}#navbar-iframe,.feed-links,.home-link,.widget-item-control,a.quickedit{display:none!important}.center{display:table;margin:0 auto;position:relative}.widget>h2,.widget>h3{display:none}
/*-- Body Content CSS --*/
body{background:$(body.background);font:$(body.font);font-weight:400;color:#555555;word-wrap:break-word;margin:0;padding:0}
#header h1,#header p,#main-menu ul#main-enu-nav>li>a,.mobile-menu ul li{text-transform:uppercase}
.headblog,.top-bar-nav,.top-bar-nav ul li{float:left}
.tabs ul,.ui ul{list-style-type:none}
#blog-pager .load-more,#main-menu .mega-menu>ul,#main-menu ul>li>ul>li a,.blog-pager,.halaman-indeks,.item-post-wrap,.main-wrapper,.mega-menu-inner .mega-item,.octf-btn,.post-share .share-links li,.post-share .share-links li a,.tabs ul li{box-sizing:border-box}
.owl-carousel,.owl-carousel .owl-item{-webkit-tap-highlight-color:transparent}
.index .boxhome,.item .boxhome{height:115px}
.home #sticky-wrap{box-shadow:none}
.template-option{display:none}
#sticky-wrap,#sticky-wrap.stickyhead{box-shadow:0 0 10px rgba(128,128,128,.14)}
#main-menu .widget,#main-menu .widget>.widget-title,#sticky-wrap.stickyhead #top-bar,.accordion-body,.awesome-icon span i,.cross,.home .main-wrapper,.mobile-menu,.mobile-menu .m-sub,.octf-btn-no-icon i,.owl-carousel,.owl-carousel .owl-refresh .owl-item,.static_page .sidebar-wrapper,.tabs .content section,.tabs .slider,.tabs input[name=tab-control],.tabs ul li label br,.tabs ul li label span,.top-bar-nav .widget>.widget-title,.top-bar-social .widget>.widget-title,.btn-mobile{display:none}
#sticky-wrap{top:-115px;-webkit-transition:1s all ease;-moz-transition:1s all ease;transition:1s all ease}
#sticky-wrap.stickyhead{position:fixed;top:0;width:100%;background:#ffffff;color:#ffffff;padding:0;z-index:999}
#sticky-wrap.stickyhead .headblog img{margin-top:5px}
#sticky-wrap.stickyhead .iconsearch-label{bottom:-2px}
#sticky-wrap.stickyhead .headblog:before{border-top:117px solid $(main.color)}
.header-wrapper{position:relative;width:1100px;color:#ffffff;margin:0 auto}
.headblog{position:relative;margin:0 30px 0 0;padding:0;width:187px;z-index:100}
.headblog:before{position:absolute;content:'';left:-100%;top:-50px;bottom:0;width:378px;border-right:38px solid transparent;border-top:115px solid $(main.color)}
.btn-dekstop{display:block}
.top-bar-nav,.top-bar-social{position:relative;display:block}
.headblog img{margin-top:-18px}
.header{width:100%;padding:0;display:flex;margin:0 auto}
#header-inner{margin:8px auto;padding:0}
#header h1,#header p{line-height:38px;color:#484848;padding-bottom:10px;margin:0;font-weight:400}
#header h1 a,#header h1.title a:hover{color:#f07468;text-decoration:none}
#header .description{color:#aaa;text-shadow:none;font-style:italic;font-size:13px}
#top-bar{height:50px;overflow:hidden;margin:0}
.top-bar-nav ul li>a{height:50px;display:block;color:#ffffff;font-size:12px;font-weight:400;line-height:50px;margin:0 10px 0 0;padding:0 5px;transition:color .17s}
.top-bar-nav ul li:first-child>a{padding:0 5px 0 0}
.top-bar-nav ul>li:hover>a{text-decoration:underline}
.top-bar-social{float:right;margin:8px 0 0}
.top-bar-social ul>li{float:left;display:inline-block}
.top-bar-social ul>li>a{display:block;width:30px;height:30px;color:#ffffff;font-size:14px;text-align:center;line-height:30px;padding:0;margin:0 0 0 10px;transition:all .17s ease}
.top-bar-social ul>li:hover>a{color:#eee}
.header-menu{position:relative;font-size:15px;width:100%;margin:0;background:$(menu.color)}
#sticky-wrap.stickyhead .iconsearch-label {height: 27px;}
.iconsearch-label:before{position:absolute;top:0;content:'';bottom:0;left:-22%;border-radius:0;border-left:30px solid transparent;border-bottom:65px solid $(main.color)}
.header-menu .container{position:relative;margin:0 auto;padding:0}
.iconsearch-label{cursor:pointer;height:25px;position:absolute;right:0;bottom:0;top:0;color:$(menu.title.color);z-index:99;font-size:16px;padding:20px;font-weight:700;background-color:$(main.color);transition:all .5s ease;-moz-transition:all .5s ease;-webkit-transition:all .5s ease;-ms-transition:all .5s ease;-o-transition:all .5s ease}
.iconsearch-label span{margin:0 10px}
div#searchcontainer{position:fixed;width:100%;height:100%;z-index:100;display:block;background:rgba(0,0,0,.85);left:-100%;top:0;padding-top:20%;opacity:0;cursor:pointer;text-align:center;-webkit-transform:scale(.9) translate3d(0,-50px,0);transform:scale(.9) translate3d(0,-50px,0)}
div#searchcontainer form{opacity:0;-webkit-transform:translate3d(0,-20px,0);transform:translate3d(0,-20px,0)}
div#searchcontainer form input[type=text]{width:40%;top:0;left:0;z-index:10;padding:10px;border:0;border-bottom:1px solid $(main.color);outline:0;font-size:1.75rem;background:none;color:#ffffff;text-align:center}
div#searchcontainer form input::-webkit-input-placeholder{color:#ffffff;opacity:.5}
div#searchcontainer form input::-moz-placeholder{color:#ffffff;opacity:.5}
div#searchcontainer form input::placeholder{color:#ffffff;opacity:.5}
div#searchcontainer form input:-ms-input-placeholder{color:#ffffff;opacity:.5}
div#searchcontainer form input::-ms-input-placeholder{color:#ffffff;opacity:.5}
div#searchcontainer.opensearch{left:0;opacity:1;-webkit-transform:scale(1) translate3d(0,0,0);-webkit-transition:all .9s ease;-ms-transition:all .9s ease;-o-transition:all .9s ease;-moz-transition:all .9s ease;transition:all .9s ease;}
div#searchcontainer.opensearch form{opacity:1;-webkit-transform:scale(1) translate3d(0,0,0);-webkit-transition:all .4s ease-in;transition:all .4s ease-in}
.cd-headline{font-size:4rem;line-height:1em;font-weight:900}
.cd-words-wrapper{display:inline-block;position:relative;text-align:left}
.cd-words-wrapper b{display:inline-block;position:absolute;white-space:nowrap;left:0;top:0}
.cd-words-wrapper b.is-visible{position:relative}
.no-js .cd-words-wrapper b{opacity:0}
.no-js .cd-words-wrapper b.is-visible{opacity:1}
.cd-headline.clip span{display:inline-block;padding:.2em 0}
.cd-headline.clip .cd-words-wrapper{overflow:hidden;vertical-align:top}
.octf-btn,.octf-btn-icon i{vertical-align:middle;display:inline-block}
.cd-headline.clip .cd-words-wrapper::after{content:'';position:absolute;top:5%;right:0;width:1px;height:88%;background-color:$(main.color)}
.cd-headline.clip b{opacity:0}
.cd-headline.clip b.is-visible{opacity:1}
#main-menu .show-menu{display:block}
#main-menu{position:relative;height:65px;z-index:15}
#main-menu ul>li{float:left;position:relative;margin:0;padding:0;transition:background .17s}
#main-menu ul>li>a,.post-body a{transition:color .17s ease}
#main-menu ul>li>a{position:relative;color:$(menu.title.color);font-size:16px;font-weight:600;line-height:65px;display:inline-block;margin:0;padding:0 13px}
#main-menu ul ul,#main-menu ul>li>ul>li,#main-menu ul>li>ul>li a{transition:all .17s ease}
#main-menu ul#main-menu-nav>li:first-child>a{padding:0 13px 0 0}
#main-menu ul>li:hover>a{color:#aaa}
#main-menu ul#main-menu-nav,#top-bar{padding-left:23%}
#main-menu ul>li>ul{position:absolute;float:left;left:0;top:65px;width:270px;background-color:$(submenu.bg);z-index:99999;margin:0;padding:0;box-shadow:0 3px 5px rgba(0,0,0,.2);visibility:hidden;opacity:0}
#main-menu ul>li>ul>li>ul{position:absolute;float:left;top:0;left:100%;margin:0}
#main-menu ul>li>ul>li{display:block;float:none;position:relative}
#main-menu ul>li>ul>li a{display:block;font-size:13px;color:$(submenu.color);font-weight:400;line-height:36px;border-bottom:1px solid #eee;margin:0;padding:2px 15px}
#main-menu ul>li>ul>li:hover>a{color:$(body.color.blue)}
#main-menu ul>li>ul>li:last-child a{border-bottom:0}
#main-menu ul>li.has-sub>a:after{content:'\f107';float:right;font-family:'Font Awesome 5 Pro';font-size:14px;font-weight:400;margin:2px 0 0 8px}
#main-menu ul>li>ul>li.has-sub>a:after{content:'\f105';float:right;margin:0}
#main-menu .mega-menu{position:static!important}
#main-menu .mega-menu>ul{width:100%;padding:20px 10px}
#main-menu .mega-menu>ul.mega-menu-inner{overflow:hidden}
#main-menu ul>li:hover>ul,#main-menu ul>li>ul>li:hover>ul{visibility:visible;opacity:1}
.mega-menu-inner .mega-item{float:left;width:20%;padding:0 10px}
.mega-menu-inner .mega-content{position:relative;width:100%;overflow:hidden;padding:0}
.mega-content .post-image-wrap{width:100%;height:190px;overflow:hidden}
.mega-content .post-image-link{width:100%;height:100%;z-index:1;display:block;position:relative;overflow:hidden}
.mega-content .post-title{position:relative;font-size:14px;font-weight:700;text-transform:uppercase;margin:10px 0 5px}
.mega-content .post-title a{display:block;color:$(body.text.color);transition:color .17s}
.mega-content:hover .post-title a{color:#34bd5c}
.meta-price{color:#aaa;font-size:12px;font-weight:700}
.no-posts{float:left;width:100%;height:100px;line-height:100px;text-align:center}
.mega-menu .no-posts{line-height:60px;color:$(body.text.color)}
.slide-menu-toggle{display:block;position:absolute;line-height:42px;height:42px;width:42px;top:0;left:0;font-family:FontAwesome;color:#ffffff;font-size:17px;font-weight:400;text-align:left;cursor:pointer;z-index:4;padding:0}
.slide-menu-toggle:before{content:"\f0c9"}
.nav-active .slide-menu-toggle:before{content:"\f00d"}
.mobile-menu{position:relative}
.mobile-menu>ul{margin:0}
.mobile-menu .m-sub{padding:0}
.mobile-menu ul li{position:relative;display:block;overflow:hidden;float:left;width:100%;font-size:13px;font-weight:700;line-height:38px;margin:0;padding:0;border-top: 1px solid #d2d2d2;}
.mobile-menu>ul li ul{overflow:hidden}
.mobile-menu>ul>li:first-child{border-top:0}
.mobile-menu ul li a{color:#000000;padding:0;display:block;transition:all .17s ease}
.mobile-menu ul li.has-sub .submenu-toggle{position:absolute;top:0;right:0;color:#000000;cursor:pointer}
.mobile-menu ul li.has-sub .submenu-toggle:after{content:'\f105';font-family:'Font Awesome 5 Pro';font-weight:400;float:right;width:34px;font-size:16px;text-align:center;transition:all .17s ease}
.mobile-menu ul li.has-sub.show>.submenu-toggle:after{transform:rotate(90deg)}
.mobile-menu>ul>li>ul>li{border-color:rgba(255,255,255,.05)}
.mobile-menu>ul>li>ul>li a{font-size:13px;text-transform:initial;font-weight:400}
.mobile-menu>ul>li>ul>li>a{color:#000000;opacity:.7;padding:0 0 0 15px}
.mobile-menu>ul>li>ul>li>ul>li{border-color:rgba(255,255,255,.02)}
.mobile-menu>ul>li>ul>li>ul>li>a{color:#ffffff;opacity:.7;padding:0 0 0 30px}
.mobile-menu ul li a:hover,.mobile-menu ul>li>.submenu-toggle:hover{color:$(body.color.blue)}
.chiller-theme{background:none}
.boxwrap,.statiswrap{overflow:hidden;padding:5% 0}
.boxpixal,.statiswrap{background:#f2f3ff}
.boxstatis .box{float:left;width:17%;margin:10px;-webkit-transition:background .3s,border .3s,-webkit-border-radius .3s,-webkit-box-shadow .3s;-o-transition:background .3s,border .3s,border-radius .3s,box-shadow .3s;transition:background .3s,border .3s,border-radius .3s,box-shadow .3s;transition:background .3s,border .3s,border-radius .3s,box-shadow .3s,-webkit-border-radius .3s,-webkit-box-shadow .3s;padding:36px 30px 36px 38px;background-color:#fff;border-style:solid;border-width:0;border-radius:10px;box-shadow:12px 19px 62px 0 rgba(13,52,79,.07);z-index:999;position:relative}
.boxstatis .boximg{width:70px;height:auto}
.boxstatis .boximg img{width:100%;height:100%}
.boxmarket{overflow:hidden;padding:5% 0}
.marketleft{float:left}
.marketright{float:right}
.marketleft,.marketright{width:45%}
.marketright img{width:100%;height:auto}
.marketleft .title{position:relative;color:#777;font-size:18px;font-weight:600;padding-right:60px;display:inline-block}
.marketleft h2{position:relative;color:#322f2f;font-weight:700;line-height:1.3em;margin-top:15px}
.marketleft p{font-size:15px;color:#424242}
.recent-warpper{padding:5% 0 15%;overflow:hidden;position:relative}
.recent-boxes{position:relative;overflow:hidden}
.recent-boxes h3{font-size:2.5rem;font-weight:400;color:#ffffff;font-family:Playball,cursive}
#breadcrumb .delimiter:after,.YouTubePopUp-Close:before,.accordion__item .accordion-header:after,.owl-next,.owl-prev,.post-share .social a:before{font-family:"Font Awesome 5 Pro"}
.owl-carousel .animated{-webkit-animation-duration:1s;animation-duration:1s;-webkit-animation-fill-mode:both;animation-fill-mode:both}
.owl-carousel .owl-animated-in{z-index:0}
.owl-carousel .owl-animated-out{z-index:1}
.owl-carousel .fadeOut{-webkit-animation-name:fadeOut;animation-name:fadeOut}
@-webkit-keyframes fadeOut{0{opacity:1}
100%{opacity:0}}
@keyframes fadeOut{0{opacity:1}
100%{opacity:0}}
.owl-height{-webkit-transition:height .5s ease-in-out;-moz-transition:height .5s ease-in-out;-ms-transition:height .5s ease-in-out;-o-transition:height .5s ease-in-out;transition:height .5s ease-in-out}
.owl-carousel{width:100%;position:relative;z-index:1}
.owl-carousel .owl-stage{position:relative;-ms-touch-action:pan-Y}
.owl-carousel .owl-stage:after{content:".";display:block;clear:both;visibility:hidden;line-height:0;height:0}
.owl-carousel .owl-stage-outer{position:relative;overflow:hidden;-webkit-transform:translate3d(0,0,0)}
.owl-carousel .owl-controls .owl-dot,.owl-carousel .owl-controls .owl-nav .owl-next,.owl-carousel .owl-controls .owl-nav .owl-prev{cursor:pointer;-webkit-user-select:none;-khtml-user-select:none;-moz-user-select:none;-ms-user-select:none;user-select:none}
.owl-carousel.owl-loaded{display:block}
.owl-carousel.owl-loading{opacity:0;display:block}
.owl-carousel.owl-hidden{opacity:0}
.owl-carousel .owl-item{position:relative;min-height:1px;float:left;-webkit-backface-visibility:hidden;-webkit-touch-callout:none;-webkit-user-select:none;-moz-user-select:none;-ms-user-select:none;user-select:none}
.owl-carousel .owl-item img{display:block;width:100%;-webkit-transform-style:preserve-3d}
.owl-carousel.owl-text-select-on .owl-item{-webkit-user-select:auto;-moz-user-select:auto;-ms-user-select:auto;user-select:auto}
.owl-carousel .owl-grab{cursor:move;cursor:-webkit-grab;cursor:-o-grab;cursor:-ms-grab;cursor:grab}
.owl-carousel.owl-rtl{direction:rtl}
.owl-carousel.owl-rtl .owl-item{float:right}
.no-js .owl-carousel{display:block}
.owl-next,.owl-prev{top:45%;color:#ffffff;background-color:rgba(0,0,0,.75);position:absolute;z-index:1;display:block;padding:0;text-align:center;overflow:hidden;transition:all .3s ease;-webkit-transition:all .3s ease;-moz-transition:all .3s ease;-o-transition:all .3s ease}
.carousel-item,.carousel-item .box-image{position:relative;width:100%;display:block}
.owl-prev{left:0}
.owl-prev:before{content:"\f104"}
.footer-box .footer li a::before,.owl-next:before{content:"\f105"}
.owl-next{right:0}
.owl-next:hover,.owl-prev:hover{background-color:#000}
.owl-dots{position:relative;width:33.33%;left:0;right:0;margin:auto;text-align:center}
.owl-dot{background:#fff;height:3px;width:10px;display:inline-block;margin:0 5px;-webkit-border-radius:2px;-moz-border-radius:2px;border-radius:2px;opacity:.6}
.owl-dot.active,.owl-dot:hover{background:$(main.color)}
.main-carousel{overflow:hidden}
.main-carousel .owl-item{width:100%}
.carousel-item{overflow:hidden;background:#ffffff;-webkit-transition:all .3s linear;transition:all .3s linear;-webkit-box-shadow:0 5px 20px 0 rgba(0,0,0,.06);box-shadow:0 5px 20px 0 rgba(0,0,0,.06)}
.accordion__item,.ot-pricing-table{box-shadow:5px 5px 20px 0 rgba(167,167,167,.1)}
.carousel-img,.carousel-item .box-image{height:300px;position:relative}
.carousel-item .carousel-content{padding:15px 30px;text-align:center}
.carousel-item .carousel-content h2.recent-title{margin:0}
.carousel-item .recent-title a,.halaman-indeks .post-info h2{color:#000000;font-size:16px;font-weight:600;line-height:1.5em;text-decoration:none;margin:5px;display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden}
.carousel-item .recent-title a:hover,.halaman-indeks .post-info h2 a:hover,a.more-link:hover{text-decoration:underline}
.main-carousel .owl-next,.main-carousel .owl-prev{margin-top:0;width:40px;height:40px;font-size:25px;line-height:40px}
.main-carousel .owl-prev{left:-50px}
.main-carousel:hover .owl-prev{left:0}
.main-carousel .owl-next{right:-50px}
.main-carousel:hover .owl-next{right:0}
a.more-link{top:0;right:0;background:$(main.color);line-height:32px;padding:7px 15px;margin:0;font-size:14px;position:absolute;color:$(menu.title.color);font-weight:700;text-transform:uppercase}
a.more-link:before{left:-19%;border-radius:0;border-left:30px solid transparent;border-bottom:47px solid $(main.color);position:absolute;top:-5px;content:'';bottom:0}
.recent-boxes .widget-title{margin:0 auto 3rem;line-height:32px;max-width:1100px;width:100%;position:relative}
.recent-boxes .widget-titl h3.title{display:inline-block;position:relative;float:left;height:32px;line-height:32px;font-size:13px;padding:0;margin:0;text-transform:uppercase}
.recent-boxes .widget-title h3.title a{color:#eee}
.recent-meta span{padding:0 10px 0 0}
.recent-meta{margin:15px 0}
.recent-tag{position:absolute;bottom:20px;border-radius:2px;padding:5px 10px;left:20px;background:$(main.color)}
.recent-tag a{font-size:13px;font-weight:500}
.recent-author::before,.recent-date:before,.recent-tag:before{font-family:"font Awesome 5 Pro";margin-right:5px;font-size:16px;font-weight:900;vertical-align:middle}
.recent-author::before,.recent-date:before{color:#dad7d7}
.recent-tag:before{color:$(dark.color);content:"\f4d6"}
.recent-author::before{content:"\f2bd"}
.recent-date:before{content:"\f017"}
.boxpixal{overflow:hidden;padding:7% 0}
.ot-pricing-table{position:relative;float:left;text-align:center;margin:20px;background:#fff;width:22.424%;padding:80px 40px 0;-webkit-transition:all .3s linear;-moz-transition:all .3s linear;-o-transition:all .3s linear;-ms-transition:all .3s linear;transition:all .3s linear;border-radius:15px;-webkit-border-radius:15px;-moz-border-radius:15px;-webkit-box-shadow:5px 5px 20px 0 rgba(167,167,167,.1);-moz-box-shadow:5px 5px 20px 0 rgba(167,167,167,.1)}
.ot-pricing-table .title-table{position:absolute;top:30px;left:0;font-size:13px;font-weight:700;text-transform:uppercase;color:#ffffff;background:#ff415b;padding:5px 15px;letter-spacing:.5px;-moz-border-radius-topleft:0;-moz-border-radius-topright:17px;-moz-border-radius-bottomright:17px;-moz-border-radius-bottomleft:0;box-shadow:8px 8px 18px 0 #e4e4e4;-webkit-box-shadow:8px 8px 18px 0 #e4e4e4;-moz-box-shadow:8px 8px 18px 0 #e4e4e4;border-radius:0 17px 17px 0;-webkit-border-radius:0 17px 17px 0}
.octf-btn,.tabs{position:relative}
.ot-pricing-table .inner-table img{margin-bottom:35px}
.ot-pricing-table .inner-table h2{font-size:42px;font-weight:500;color:#ff415b;margin-bottom:3px}
.ot-pricing-table .inner-table h2 sup{margin-left:-25px;font-size:30px}
.ot-pricing-table .inner-table p{color:#a5b7d2;font-weight:500;margin-bottom:0}
.ot-pricing-table .inner-table .details{margin-top:35px;padding-top:28px;padding-bottom:30px;line-height:42px;border-top:1px solid #e5e5e5}
.ot-pricing-table .inner-table .details ul{list-style:none;margin:0;padding:0;font-size:15px}
.ot-pricing-table .octf-btn{margin-bottom:-26px;color:#ffffff}
.ot-pricing-table .octf-btn:hover{box-shadow:none!important}
.ot-pricing-table:before{background:#fff;-moz-border-radius-topleft:15px;-moz-border-radius-topright:15px;-moz-border-radius-bottomright:0;-moz-border-radius-bottomleft:0;border-radius:15px 15px 0 0;-webkit-border-radius:15px 15px 0 0}
.ot-pricing-table:after{background:#fff;-moz-border-radius-topleft:0;-moz-border-radius-topright:0;-moz-border-radius-bottomright:15px;-moz-border-radius-bottomleft:15px;border-radius:0 0 15px 15px;-webkit-border-radius:0 0 15px 15px}
.ot-pricing-table.s2 .title-table{background:$(body.color.blue)}
.octf-btn,.ot-pricing-table.s3 .title-table{background:#4cadff}
.ot-pricing-table.s2 h2{color:$(body.color.blue)}
.ot-pricing-table.s3 h2{color:#4cadff}
.octf-btn,.octf-btn:focus,.octf-btn:hover,.octf-btn:visited{color:#ffffff}
.ot-pricing-table:hover{-webkit-transform:translateY(-15px);-ms-transform:translateY(-15px);transform:translateY(-15px)}
.octf-btn{transition:all .2s ease-out;-webkit-transition:all .2s ease-out;-moz-transition:all .2s ease-out;-o-transition:all .2s ease-out;-ms-transition:all .2s ease-out;font-size:14px;padding:16px 28px;line-height:1;margin:0;text-decoration:none;white-space:nowrap;text-transform:uppercase;font-weight:500;letter-spacing:0;text-align:center;cursor:pointer;border:1px solid transparent;outline:0;overflow:hidden;border-radius:25px;-webkit-border-radius:25px;-moz-border-radius:25px;box-shadow:0 10px 25px 0 #a6c6e8;-webkit-box-shadow:0 10px 25px 0 #a6c6e8;-moz-box-shadow:0 10px 25px 0 #a6c6e8}
.octf-btn:focus,.octf-btn:hover{box-shadow:none}
.octf-btn.octf-btn-white{background:#fff;box-shadow:6px 6px 13px 0 rgba(42,67,113,.15);-webkit-box-shadow:6px 6px 13px 0 rgba(42,67,113,.15);-moz-box-shadow:6px 6px 13px 0 rgba(42,67,113,.15);color:#4cadff}
.octf-btn.octf-btn-white i{background:#4cadff;color:#ffffff}
.octf-btn.octf-btn-white:focus,.octf-btn.octf-btn-white:hover,.octf-btn.octf-btn-white:visited{color:#4cadff}
.octf-btn.octf-btn-white:before{background-color:rgba(254,76,28,.5)}
.octf-btn:before{content:"";position:absolute;top:0;left:0;width:100%;height:100%;z-index:0;-webkit-transition:all .5s;-moz-transition:all .5s;-o-transition:all .5s;transition:all .5s;opacity:1;-webkit-transform:translate(-105%,0);transform:translate(-105%,0);background-color:rgba(255,255,255,.8)}
.accordion-header,.octf-btn-icon i{-webkit-transition:all .3s linear;-moz-transition:all .3s linear;-o-transition:all .3s linear}
.octf-btn:hover:before{opacity:0;-webkit-transform:translate(0,0);transform:translate(0,0)}
.octf-btn-icon{text-align:left;padding:5px 5px 5px 28px}
.octf-btn-icon i{background:#fff;color:#4cadff;width:40px;height:40px;line-height:40px;text-align:center;margin-left:14px;border-radius:50%;-webkit-border-radius:50%;-moz-border-radius:50%;-ms-transition:all .3s linear;transition:all .3s linear}
.octf-btn-primary{background:#4cadff}
.octf-btn-primary.octf-btn{box-shadow:12px 12px 20px 0 rgba(254,76,28,.3);-webkit-box-shadow:12px 12px 20px 0 rgba(254,76,28,.3);-moz-box-shadow:12px 12px 20px 0 rgba(254,76,28,.3)}
.octf-btn-primary.octf-btn-icon{box-shadow:8px 8px 18px 0 #d2e8fb;-webkit-box-shadow:8px 8px 18px 0 #d2e8fb;-moz-box-shadow:8px 8px 18px 0 rgba(254,76,28,.3)}
.octf-btn-primary:focus,.octf-btn-primary:hover{box-shadow:none}
.octf-btn-secondary{background:#ff415b}
.octf-btn-secondary.octf-btn{box-shadow:12px 12px 20px 0 rgba(0,195,255,.3);-webkit-box-shadow:12px 12px 20px 0 rgba(0,195,255,.3);-moz-box-shadow:12px 12px 20px 0 rgba(0,195,255,.3)}
.octf-btn-secondary.octf-btn-icon{box-shadow:8px 8px 18px 0 #fdf0c2;-webkit-box-shadow:8px 8px 18px 0 #fdf0c2;-moz-box-shadow:8px 8px 18px 0 #fdf0c2}
.octf-btn-secondary i{color:#ff415b}
.octf-btn-secondary.octf-btn-white{color:#00c3ff;box-shadow:6px 6px 13px 0 rgba(42,67,113,.15);-webkit-box-shadow:6px 6px 13px 0 rgba(42,67,113,.15);-moz-box-shadow:6px 6px 13px 0 rgba(42,67,113,.15)}
.octf-btn-secondary.octf-btn-white:focus,.octf-btn-secondary.octf-btn-white:hover,.octf-btn-secondary.octf-btn-white:visited{color:#00c3ff}
.octf-btn-third i,.octf-btn-third.octf-btn-white:focus,.octf-btn-third.octf-btn-white:hover,.octf-btn-third.octf-btn-white:visited{color:$(body.color.blue)}
.octf-btn-secondary.octf-btn-white i{background:#00c3ff}
.octf-btn-third,.octf-btn-third.octf-btn-white i{background:$(body.color.blue)}
.octf-btn-secondary:focus,.octf-btn-secondary:hover{box-shadow:none}
.octf-btn-third.octf-btn{box-shadow:12px 12px 20px 0 rgba(1,96,231,.3);-webkit-box-shadow:12px 12px 20px 0 rgba(1,96,231,.3);-moz-box-shadow:12px 12px 20px 0 rgba(1,96,231,.3)}
.octf-btn-third.octf-btn-icon{box-shadow:8px 8px 18px 0 #d4d9ff;-webkit-box-shadow:8px 8px 18px 0 #d4d9ff;-moz-box-shadow:8px 8px 18px 0 #d4d9ff}
.octf-btn-third.octf-btn-white{color:$(body.color.blue);box-shadow:6px 6px 13px 0 rgba(42,67,113,.15);-webkit-box-shadow:6px 6px 13px 0 rgba(42,67,113,.15);-moz-box-shadow:6px 6px 13px 0 rgba(42,67,113,.15)}
.octf-btn-third:focus,.octf-btn-third:hover{box-shadow:none}
.btn-readmore a{transition:all .2s ease-out;-webkit-transition:all .2s ease-out;-moz-transition:all .2s ease-out;-o-transition:all .2s ease-out;-ms-transition:all .2s ease-out;font-size:12px;line-height:1;display:inline-block;text-decoration:none;white-space:nowrap;font-weight:500;letter-spacing:1px;text-transform:uppercase}
.accordion{font-size:1rem;margin:0 auto}
.accordion-header{padding:0 5px;cursor:pointer;font-size:16px;font-weight:600;-ms-transition:all .3s linear;transition:all .3s linear}
.accordion-body__contents{padding:20px 5px;font-size:14px;color:#949494;line-height:2;font-weight:400}
.accordion__item .accordion__item .accordion-header{background:#fff;color:#021f2d;padding:10px 20px;font-size:14px}
.accordion__item.active:last-child .accordion-header{border-radius:0}
.accordion:first-child .accordion__item .accordion-header{border-bottom:1px solid transparent}
.accordion__item .accordion-header:after{content:"\f067";float:right;position:relative;transition:.3s all;transform:rotate(0);font-weight:400;height:30px;width:30px;line-height:30px;text-align:center;font-size:13px;background:#eaeaea;color:$(body.color.blue);border-radius:50%;-webkit-border-radius:50%;-moz-border-radius:50%}
.accordion__item.active>.accordion-header:after{content:"\f068";font-family:"Font Awesome 5 Pro";background:$(body.color.blue);color:#ffffff;transform:rotate(-180deg)}
.accordion__item{cursor:pointer;background:#fff;display:block;overflow:hidden;font-weight:500;color:#1a1b1e;padding:13px 10px 13px 25px;-webkit-transition:all .3s linear;-moz-transition:all .3s linear;-o-transition:all .3s linear;margin-bottom:20px;-webkit-box-shadow:5px 5px 20px 0 rgba(167,167,167,.1);-moz-box-shadow:5px 5px 20px 0 rgba(167,167,167,.1);-ms-transition:all .3s linear;transition:all .3s linear}
.tabs{padding:0;width:100%}
.tabs ul li label{font-weight:400;font-size:15px}
.tabs ul li label span{display:block;color:#000000;padding:10px 0;font-weight:500;font-size:14px}
.tabs ul{padding-left:0;display:-webkit-box;display:flex;-webkit-box-orient:horizontal;-webkit-box-direction:normal;flex-direction:row;margin-bottom:40px;-webkit-box-pack:justify;justify-content:space-between;-webkit-box-align:end;align-items:flex-end;flex-wrap:wrap}
.tabs ul li{-webkit-box-flex:1;flex:1;width:25%;padding:0 10px;text-align:center}
.tabs ul li label.color1{background-color:#9fb6ff}
.tabs ul li label.color2{background-color:#a5dce4}
.tabs ul li label.color3{background-color:#f9d8ac}
.tabs ul li label.color4{background-color:#b9f5eb}
.tabs ul li label.color5{background-color:#d0c1f7}
.tabs ul li label i{font-size:30px}
.tabs ul li label.color1 i,.tabs ul li label.color1 span{color:#5962b1}
.tabs ul li label.color2 i,.tabs ul li label.color2 span{color:#1893a5}
.tabs ul li label.color3 i,.tabs ul li label.color3 span{color:#c58024}
.tabs ul li label.color4 i,.tabs ul li label.color4 span{color:#12907b}
.tabs ul li label.color5 i,.tabs ul li label.color5 span{color:#8013af}
.tabs input[name=tab-control]:nth-of-type(1):checked~ul>li:nth-child(1)>label span,.tabs input[name=tab-control]:nth-of-type(1):checked~ul>li:nth-child(1)>label.color1 i,.tabs input[name=tab-control]:nth-of-type(2):checked~ul>li:nth-child(2)>label span,.tabs input[name=tab-control]:nth-of-type(2):checked~ul>li:nth-child(2)>label.color2 i,.tabs input[name=tab-control]:nth-of-type(3):checked~ul>li:nth-child(3)>label span,.tabs input[name=tab-control]:nth-of-type(3):checked~ul>li:nth-child(3)>label.color3 i,.tabs input[name=tab-control]:nth-of-type(4):checked~ul>li:nth-child(4)>label span,.tabs input[name=tab-control]:nth-of-type(4):checked~ul>li:nth-child(4)>label.color4 i,.tabs input[name=tab-control]:nth-of-type(5):checked~ul>li:nth-child(5)>label span,.tabs input[name=tab-control]:nth-of-type(5):checked~ul>li:nth-child(5)>label.color5 i{color:#ffffff}
.boxwrap-wrap{overflow:hidden;padding:20px 0}
.boxwrap-os-left{float:left;width:45%}
.boxwrap-os-right{float:right;width:55%}
.boxwrap-os-left h2{color:$(body.text.color);font-size:3rem;line-height:1.2em;margin:0;font-weight:900;letter-spacing:-2px}
.boxwrap-os-left h2 span{color:$(body.color.blue)}
.boxwrap-os-right p{font-size:15px}
.font-small h2 {font-size: 35px!important;padding:0 0 20px 0;}
.font-big h2{font-size:55px!important;padding: 0;}
.box-ui{margin:-8% auto 3%;display:flex}
.ui{width:900px;margin:0 auto;color:#ffffff;box-shadow:none}
.ui ul{margin:0 30px 10px 0;padding:0;font-size:11px;font-weight:400;line-height:20px}
.ui .drop{z-index:-3;opacity:0;width:100%;height:10px;background:$(body.color.blue);position:absolute;color:#ffffff;bottom:0;padding:12px 0 21px;-webkit-transition-property:bottom,opacity;transition-property:bottom,opacity;-webkit-transition-duration:.3s;transition-duration:.3s}
.ui_box,.ui_box:hover{-webkit-transition-duration:.3s;position:relative;transition-duration:.3s}
.ui .drop p{color:#ffffff;text-align:center}
.ui_box{width:300px;height:220px;background:#3d3d3d;float:left;box-shadow:-1px 0 rgba(255,255,255,.07);-webkit-transform:scale(1);transform:scale(1);-webkit-transition-property:background,-webkit-transform;transition-property:background,-webkit-transform;transition-property:transform,background;transition-property:transform,background,-webkit-transform}
.ui_box__inner{padding:30px}
.ui_box__inner span{font-size:36px;font-weight:700}
.ui_box:hover .ui_box__inner span,.ui_box:hover ul li{color:$(body.color.blue)}
.ui_box:hover h2{color:#333}
.ui_box__inner .progress{width:100%;margin-top:10px;height:6px;background:rgba(101,101,101,.3);margin-bottom:15px}
.ui_box__inner .progress_graph{float:right;border-bottom:1px solid rgba(255,255,255,.09);width:85px;text-align:center;position:relative;padding-left:20px;top:24px}
.ui_box__inner .progress_graph__bar--1{width:10px;height:20px;background:$(body.color.blue);float:left;margin-right:10px;position:relative;bottom:-10px;-webkit-animation:graph 1s}
.ui_box__inner .progress_graph__bar--2{width:10px;-webkit-animation:graph2 1s;height:30px;float:left;margin-right:10px;background:$(body.color.blue)}
.ui_box__inner .progress_graph__bar--3{width:10px;height:24px;margin-right:10px;-webkit-animation:graph3 1s;background:$(body.color.blue);float:left;position:relative;bottom:-6px}
.ui_box__inner .progress_graph__bar--4{width:10px;height:14px;-webkit-animation:graph4 1s;bottom:-16px;position:relative;background:$(body.color.blue);float:left}
.ui_box__inner .progress_bar{height:6px;float:left;width:58%;background:$(body.color.blue);-webkit-animation:bar 2s}
.ui_box__inner .progress_bar--two{height:6px;float:left;width:78%;background:$(body.color.blue);-webkit-animation:bar2 2s}
.ui_box h2{font-weight:400;font-size:16px;margin:-4px 0 3px}
.ui_box p{font-size:11px;color:#b6b6b6;clear:left;font-weight:300;margin:2px 0 15px}
.ui_box:hover{background:#fff;-webkit-transform:scale(1.1);transform:scale(1.1);-webkit-transition-property:background,-webkit-transform;transition-property:background,-webkit-transform;transition-property:transform,background;transition-property:transform,background,-webkit-transform;z-index:1}
.ui_box:hover .ui_box__inner p{color:#333}
.ui_box:hover .drop{-webkit-transition-property:bottom,opacity;transition-property:bottom,opacity;-webkit-transition-duration:.3s;transition-duration:.3s;bottom:-42px;opacity:1}
.stat_left{float:left}
@-webkit-keyframes bar{from{width:0}
to{width:58%}}
@keyframes bar{from{width:0}
to{width:58%}}
@-webkit-keyframes bar2{from{width:0}
to{width:78%}}
@keyframes bar2{from{width:0}
to{width:78%}}
@-webkit-keyframes graph{from{height:0}
to{height:20px}}
@keyframes graph{from{height:0}
to{height:20px}}
@-webkit-keyframes graph2{from{height:0}
to{height:30px}}
@keyframes graph2{from{height:0}
to{height:30px}}
@-webkit-keyframes graph3{from{height:0}
to{height:24px}}
@keyframes graph3{from{height:0}
to{height:24px}}
@-webkit-keyframes graph4{from{height:0}
to{height:13px}}
@keyframes graph4{from{height:0}
to{height:13px}}
.boxwrap-left{float:left}
.boxwrap-right{float:right}
.boxwrap-left,.boxwrap-right{width:45%}
.boxwrap-text h3{color:#696969;font-size:17px;font-weight:500;margin:0;text-transform:uppercase}
.boxwrap-text p{font-size:17px}
.boxwrap-text h2{color:$(body.text.color);font-size:45px;font-weight:800;letter-spacing:-2px;line-height:1;margin:10px 0}
.boxwrap-text h2 span{color:$(body.color.blue)}
.boxwrap-icon{margin:30px 0;display:inline-block}
.boxwrap-number{float:left;width:27%;margin-right:31px}
.boxwrap-number i{font-size:8px;position:relative;color:#ffc400;display:block}
.boxwrap-number h4{color:#ffc400;margin:0;line-height:1;font-size:40px;font-weight:700}
.touc1 h4,.touc1 i{color:#4cadff}
.touc2 h4,.touc2 i{color:$(body.color.blue)}
.boxwrap-number p{margin:0;font-size:15px}
.colorwp{font-weight:400;font-size:13px;background:$(body.color.blue);background:linear-gradient(-35deg,#5ab3ff 0,#4c5ef9 100%);box-shadow:0 10px 25px 0 #a6c6e8}
.center-text{text-align:center;margin-bottom:3%}
.center-text h2{font-size:2rem}
.serviceimg{width:400px;max-width:100%;margin-top:25px}
.serviceimg img{width:100%;height:auto}
.tabs .content p{font-size:14px;line-height:1.7;font-weight:300}
.content-right>ul{padding-left:0;list-style:none;margin-top:40px;margin-bottom:40px}
.content-right>ul>li{line-height:1.4;display:inline-block;width:48%;text-align:left;padding:0}
.content-right>ul>li i{float:left;margin-right:20px;width:40px;font-size:40px;height:40px}
.content-right>ul>li i.icon1{color:#555}
.content-right>ul>li i.icon2{color:#00c3ff}
.tabs input[name=tab-control]:nth-of-type(1):checked~.content>section:nth-child(1).content-right .btncolor{background:#ff9b8f;background:linear-gradient(-35deg,rgba(255,155,143,1) 0,#ff68a2 100%);box-shadow:0 10px 25px 0 #ffc1d4}
.tabs input[name=tab-control]:nth-of-type(2):checked~.content>section:nth-child(2).content-right .btncolor{background:#61d020;background:linear-gradient(-35deg,#61d020 0,#8bec51 100%);box-shadow:0 10px 25px 0 #beeaa4}
.tabs input[name=tab-control]:nth-of-type(3):checked~.content>section:nth-child(3).content-right .btncolor{background:#f9c253;background:linear-gradient(-35deg,#f9c253 0,#ffc54f 100%);box-shadow:0 10px 25px 0 #ffefce}
.tabs input[name=tab-control]:nth-of-type(4):checked~.content>section:nth-child(4).content-right .btncolor{background:#32ecad;background:linear-gradient(-35deg,#5dfbc5 0,#32ecad 100%);box-shadow:0 10px 25px 0 #c6f7e6}
.tabs input[name=tab-control]:nth-of-type(5):checked~.content>section:nth-child(5).content-right .btncolor{background:#975cf4;background:linear-gradient(-35deg,#b58af9 0,#975cf4 100%);box-shadow:0 10px 25px 0 #dec9ff}
.content-right .btnfont{font-size:13px;padding:15px 30px;font-weight:400}
.tabs ul li label{padding:35px 15px;box-shadow:none;color:#ffffff;border-radius:5px;position:relative;text-overflow:ellipsis;display:block;cursor:pointer;-webkit-transition:all .2s ease-in-out;transition:all .2s ease-in-out;white-space:nowrap;-webkit-user-select:none;-moz-user-select:none;-ms-user-select:none;user-select:none}
.tabs input[name=tab-control]:nth-of-type(1):checked~ul>li:nth-child(1)>label.color1{background:#5e6eff}
.tabs input[name=tab-control]:nth-of-type(2):checked~ul>li:nth-child(2)>label.color2{background:#00b8d5}
.tabs input[name=tab-control]:nth-of-type(3):checked~ul>li:nth-child(3)>label.color3{background:#fad961}
.tabs input[name=tab-control]:nth-of-type(4):checked~ul>li:nth-child(4)>label.color4{background:#32ecad}
.tabs input[name=tab-control]:nth-of-type(5):checked~ul>li:nth-child(5)>label.color5{background:#8a63f2}
.tabs input[name=tab-control]:nth-of-type(1):checked~ul>li:nth-child(1)>label.color1::after,.tabs input[name=tab-control]:nth-of-type(2):checked~ul>li:nth-child(2)>label.color2::after,.tabs input[name=tab-control]:nth-of-type(3):checked~ul>li:nth-child(3)>label.color3::after,.tabs input[name=tab-control]:nth-of-type(4):checked~ul>li:nth-child(4)>label.color4::after,.tabs input[name=tab-control]:nth-of-type(5):checked~ul>li:nth-child(5)>label.color5::after{position:absolute;bottom:-20px;margin:0 auto;content:'';left:40%;border-right:20px solid transparent;border-left:20px solid transparent;border-bottom:0 solid transparent}
.tabs input[name=tab-control]:nth-of-type(1):checked~ul>li:nth-child(1)>label.color1::after{border-top:20px solid #5e6eff}
.tabs input[name=tab-control]:nth-of-type(2):checked~ul>li:nth-child(2)>label.color2::after{border-top:20px solid #00b8d5}
.tabs input[name=tab-control]:nth-of-type(3):checked~ul>li:nth-child(3)>label.color3::after{border-top:20px solid #fad961}
.tabs input[name=tab-control]:nth-of-type(4):checked~ul>li:nth-child(4)>label.color4::after{border-top:20px solid #32ecad}
.tabs input[name=tab-control]:nth-of-type(5):checked~ul>li:nth-child(5)>label.color5::after{border-top:20px solid #8a63f2}
.tabs .content{margin:20px 10px;padding:0;display:inline-flex}
.tabs .content section{padding:50px 80px;-webkit-animation-name:content;animation-name:content;-webkit-animation-direction:normal;animation-direction:normal;-webkit-animation-duration:.3s;animation-duration:.3s;-webkit-animation-timing-function:ease-in-out;animation-timing-function:ease-in-out;-webkit-animation-iteration-count:1;animation-iteration-count:1;line-height:1.4;background:url(https://1.bp.blogspot.com/-HS91jMpfhHc/XuyS9ZGQ9pI/AAAAAAAAAKI/I2CEh5buKB0NrZVWzJP0TUgaC1yht2gigCLcBGAsYHQ/s1600/tab-bg.png) 100% 115% no-repeat #fff;background-size:550px 380px}
.tabs .content section h3{font-size:20px;font-weight:600}
.tabs input[name=tab-control]:nth-of-type(1):checked~.content>section:nth-child(1) h3:after{background:#5e6eff}
.tabs input[name=tab-control]:nth-of-type(2):checked~.content>section:nth-child(2) h3:after{background:#00b8d5}
.tabs input[name=tab-control]:nth-of-type(3):checked~.content>section:nth-child(3) h3:after{background:#f9c253}
.tabs input[name=tab-control]:nth-of-type(4):checked~.content>section:nth-child(4) h3:after{background:#32ecad}
.tabs input[name=tab-control]:nth-of-type(5):checked~.content>section:nth-child(5) h3:after{background:#8a63f2}
.tabs .content section h3::after{content:"";position:relative;display:block;width:30px;height:3px;background:#428bff;margin-top:5px;left:1px}
.content-right{float:right}
.content-left{float:left}
.content-left,.content-right{width:50%}
.tabs input[name=tab-control]:nth-of-type(1):checked~.content>section:nth-child(1),.tabs input[name=tab-control]:nth-of-type(2):checked~.content>section:nth-child(2),.tabs input[name=tab-control]:nth-of-type(3):checked~.content>section:nth-child(3),.tabs input[name=tab-control]:nth-of-type(4):checked~.content>section:nth-child(4),.tabs input[name=tab-control]:nth-of-type(5):checked~.content>section:nth-child(5){display:block}
.tabs input[name=tab-control]:nth-of-type(1):checked~.content>section:nth-child(1){box-shadow:0 10px 30px 0 #ccd1ff}
.tabs input[name=tab-control]:nth-of-type(2):checked~.content>section:nth-child(2){box-shadow:0 10px 30px 0 rgba(83,194,3,.2)}
.tabs input[name=tab-control]:nth-of-type(3):checked~.content>section:nth-child(3){box-shadow:0 10px 30px 0 rgba(247,107,28,.2)}
.tabs input[name=tab-control]:nth-of-type(4):checked~.content>section:nth-child(4){box-shadow:0 10px 30px 0 rgba(0,191,141,.2)}
.tabs input[name=tab-control]:nth-of-type(5):checked~.content>section:nth-child(5){box-shadow:0 10px 30px 0 rgba(196,68,251,.2)}
@-webkit-keyframes content{from{opacity:0;-webkit-transform:translateY(5%);transform:translateY(5%)}
to{opacity:1;-webkit-transform:translateY(0);transform:translateY(0)}}
@keyframes content{from{opacity:0;-webkit-transform:translateY(5%);transform:translateY(5%)}
to{opacity:1;-webkit-transform:translateY(0);transform:translateY(0)}}
.home .boxhome{position:relative;display:block;overflow:hidden;width:auto;height:100vh}
#footer-wrapper,.boxhome,.recent-warpper,.subs-wrapper{background-color:$(bg.color.1);background-image: -webkit-gradient(linear,left top,right top,from($(bg.color.1)),to($(bg.color.2)));background-image: linear-gradient(to right,$(bg.color.1),$(bg.color.2))}
.item .boxhome{margin-bottom:30px}
.overlay{position:fixed;left:0;right:0;top:0;bottom:0;display:none}
.overlay.active,div#searchcontainer.opensearch {cursor: url(https://1.bp.blogspot.com/-QfbILf6d4T8/XuzimrIGrNI/AAAAAAAAAKU/fUudHpKYqA886HWu23w3SHzOJsGq08TaACLcBGAsYHQ/s1600/cross-out.png),pointer;}
.overlay.active{z-index:999;background:rgba(0,0,0,0.79);display:block}
.digital-wrapper {z-index:99999;overflow:hidden;padding-top:8%}
.digital-wrapper h3{font-size:40px;font-weight:500;line-height:1.2;color:#ffffff;margin:0}
.box-left p{font-size:16px;line-height:1.5em}
.box-left{float:left;width:45%;color:#ffffff}
.box-right{float:right;width:50%;margin-top:-5%}
.box-right img{width:100%;height:auto}
.boxwrap-left h5{margin:0;font-weight:500;text-transform:uppercase;font-size:17px}
.YouTubePopUp-Wrap{position:fixed;width:100%;height:100%;background-color:rgba(0,0,0,.8);top:0;left:0;z-index:9999999999999}
.YouTubePopUp-animation{opacity:0;animation-name:YouTubePopUp}
@-webkit-keyframes YouTubePopUp{0{opacity:0}
100%{opacity:1}}
@keyframes YouTubePopUp{0{opacity:0}
100%{opacity:1}}
.YouTubePopUp-Content{max-width:800px;display:block;margin:0 auto;height:100%;position:relative}
.YouTubePopUp-Content iframe{max-width:100%!important;width:100%!important;display:block!important;height:500px!important;border:none!important;position:absolute;top:0;bottom:0;margin:auto 0}
.YouTubePopUp-Hide{animation-name:YouTubePopUpHide}
@-webkit-keyframes YouTubePopUpHide{0{opacity:1}
100%{opacity:0}}
@keyframes YouTubePopUpHide{0{opacity:1}
100%{opacity:0}}
.YouTubePopUp-Close{position:absolute;top:0;cursor:pointer;bottom:500px;z-index:10;right:-13px;margin:auto 0;width:24px;color:#ffffff;height:24px;background:$(body.text.color);border:2px solid #fff;border-radius:50px;line-height:24px;text-align:center}
.YouTubePopUp-Close:hover{opacity:.5}
.YouTubePopUp-Close:before{content:'\f00d'}
.wpbtn{padding:30px 0;clear:both;display:block;position:relative;margin:0 auto}
.js-modal-video,.js-modal-video .overlay-box span{display:inline-block;height:60px;width:60px;text-align:center}
.wpbtn a.btn-wite{background:#fff;padding:17px 50px;border-radius:50px}
.wpbtn a{margin-right:20px}
.js-modal-video{position:relative;font-size:18px;border-radius:50px;line-height:60px;margin-right:40px;transition:all .3s ease;-moz-transition:all .3s ease;-webkit-transition:all .3s ease;-ms-transition:all .3s ease;-o-transition:all .3s ease;background-image:linear-gradient(to right,#ff880e 0,#ffb020 100%)}
a.js-modal-video{color:#ffffff}
.js-modal-video .overlay-box span{position:absolute;left:50%;top:50%;z-index:99;color:#ffffff;font-weight:600;font-size:16px;border-radius:50%;padding-left:7px;background-color:#fff;margin-top:-30px;margin-left:-30px;transition:all .9s ease;-moz-transition:all .9s ease;-webkit-transition:all .9s ease;-ms-transition:all .9s ease;-o-transition:all .9s ease;-webkit-box-shadow:0 0 30px rgba(0,0,0,.1);-moz-box-shadow:0 0 30px rgba(0,0,0,.1);box-shadow:0 0 30px rgba(0,0,0,.1)}
.js-modal-video .ripple,.js-modal-video .ripple:after,.js-modal-video .ripple:before{position:absolute;top:50%;left:50%;height:60px;width:60px;-webkit-transform:translate(-50%,-50%);-moz-transform:translate(-50%,-50%);-ms-transform:translate(-50%,-50%);-o-transform:translate(-50%,-50%);transform:translate(-50%,-50%);-webkit-border-radius:50%;-moz-border-radius:50%;-ms-border-radius:50%;-o-border-radius:50%;border-radius:50%;-webkit-box-shadow:0 0 0 0 rgba(255,255,255,.4);-moz-box-shadow:0 0 0 0 rgba(255,255,255,.4);-ms-box-shadow:0 0 0 0 rgba(255,255,255,.4);-o-box-shadow:0 0 0 0 rgba(255,255,255,.4);box-shadow:0 0 0 0 rgba(255,255,255,.4);-webkit-animation:ripple 3s infinite;-moz-animation:ripple 3s infinite;-ms-animation:ripple 3s infinite;-o-animation:ripple 3s infinite;animation:ripple 3s infinite}
.js-modal-video .ripple:before{-webkit-animation-delay:.9s;-moz-animation-delay:.9s;-ms-animation-delay:.9s;-o-animation-delay:.9s;animation-delay:.9s;content:"";position:absolute}
.js-modal-video .ripple:after{-webkit-animation-delay:.6s;-moz-animation-delay:.6s;-ms-animation-delay:.6s;-o-animation-delay:.6s;animation-delay:.6s;content:"";position:absolute}
@-webkit-keyframes ripple{70%{box-shadow:0 0 0 20px rgba(255,255,255,0)}
100%{box-shadow:0 0 0 0 rgba(255,255,255,0)}}
@keyframes ripple{70%{box-shadow:0 0 0 20px rgba(255,255,255,0)}
100%{box-shadow:0 0 0 0 rgba(255,255,255,0)}}
#outer-wrapper{max-width:1100px;margin:0 auto}
.item-post .post-body img,.widget iframe,.widget img{max-width:100%}
#content-wrapper{margin:0 auto;display:block}
.item #content-wrapper{display:inline-flex}
.static_page #content-wrapper{display:block}
#content-wrapper>.container{margin:0 -15px}
.main-wrapper{float:left;overflow:hidden;width:100%;word-wrap:break-word;padding:0 25px;margin:3% 0}
.item .main-wrapper{width:70%;padding:0 15px;margin:0 auto}
.sidebar-wrapper{display:none;float:right;overflow:hidden;width:30%;box-sizing:border-box;word-wrap:break-word;padding:0 15px}
.item .sidebar-wrapper{display:block;position:sticky;position:-webkit-sticky;top:0}
.post-image-wrap,.sizeimg{position:relative;display:block}
.about-author .avatar-container,.comments .avatar-image-container,.post-image-link{background-color:rgba(155,155,155,.07);color:transparent!important}
.sizeimg{width:100%;height:100%;object-fit:cover;z-index:1;border-radius:2px;transition:opacity .17s ease}
.hot-item-inner:hover .post-image-link .sizeimg,.post-image-link:hover .sizeimg,.post-image-wrap:hover .post-image-link .sizeimg{opacity:.9}
.post-title a{display:block}
.post-meta,.post-meta a{overflow:hidden;color:#aaa;font-size:12px;font-weight:300;padding:0}
.item-post .post-meta{line-height:20px}
.post-meta span{float:left;display:inline-block;margin:0 10px 0 0}
.post-meta span img{float:left;width:20px;height:20px;color:$(body.text.color);margin:0 5px 0 0;border-radius:20px}
.post-meta i{margin:0 4px}
.post-meta .post-author:after{content:'-';margin:0 0 0 8px}
.show-hot .no-posts{position:absolute;top:calc(50% - 50px);left:0;width:100%}
.queryMessage{overflow:hidden;background-color:$(body.color.blue);color:$(body.text.color);font-size:13px;font-weight:400;position:relative;padding:8px 10px;margin:0 0 20px}
.queryMessage .query-info{margin:0 5px}
.queryMessage .search-label,.queryMessage .search-query{font-weight:700;text-transform:uppercase}
.queryMessage .search-label:before,.queryMessage .search-query:before{content:"\201c"}
.queryMessage .search-label:after,.queryMessage .search-query:after{content:"\201d"}
.queryMessage a.show-more{position:absolute;right:0;color:#000000;top:0;padding:9px 20px;bottom:0;background:;transition:opacity .17s}
.queryMessage a.show-more:hover{opacity:.8}
.queryEmpty{font-size:13px;font-weight:400;padding:10px 0;margin:0 0 25px;text-align:center}
.title-wrap{display:none}
.post-body .widget-content{text-align:center;margin:.8em 0;display:block}
.post-body .widget-content:blank{margin:0}
.Ad-Slots-below .widget,.Ad-Slots-below .widget-content,.Middle-Ad-Slot1 .widget,.Middle-Ad-Slot1 .widget-content,.Middle-Ad-Slot2 .widget,.Middle-Ad-Slot2 .widget-content,.top-Ad-Slots .widget,.top-Ad-Slots .widget-content{margin:0!important}
.custom-widget li{overflow:hidden;margin:20px 0 0}
.custom-widget li:first-child{padding:0;margin:0;border:0}
.custom-widget .post-image-link{position:relative;width:80px;height:70px;float:left;overflow:hidden;display:block;vertical-align:middle;margin:0 12px 0 0}
.custom-widget .post-info{overflow:hidden}
.custom-widget .post-title{overflow:hidden;font-size:13px;font-weight:500;line-height:1.5em;margin:0 0 3px}
.custom-widget .post-title a{display:block;color:$(body.text.color);transition:color .17s}
.custom-widget li:hover .post-title a{color:$(body.color.blue)}
.halaman-indeks-wrap{position:relative;float:left;width:100%}
.item-post-wrap{padding:20px 0}
.blog-post{display:block;overflow:hidden;word-wrap:break-word}
.bxposts{display:flex;flex-wrap:wrap;margin:0 -15px}
.halaman-indeks{display:block;width:30.632%;padding:0;overflow:visible;margin:15px;height:360px;position:relative;background:#fff;-webkit-transition:all .3s linear;transition:all .3s linear;-webkit-box-shadow:0 5px 20px 0 rgba(0,0,0,.06);box-shadow:0 5px 20px 0 rgba(0,0,0,.06)}
.halaman-indeks:hover{-webkit-box-shadow:none;box-shadow:none}
.halaman-indeks .post-image-wrap{width:100%;height:220px;overflow:hidden;margin:0}
.halaman-indeks .post-image-wrap .post-image-link{width:100%;height:100%;position:relative;display:block;z-index:1;overflow:hidden}
.halaman-indeks .post-info{position:relative;margin:0 auto;text-align:center;padding:15px 30px}
.halaman-indeks .post-info h2 a{display:block;color:$(body.text.color);transition:color .17s}
.date-header{display:block;overflow:hidden;font-weight:400;margin:0!important;padding:0}
.halaman-indeks .post-meta{display:inline-block;text-align:center;margin:20px auto;position:relative}
#breadcrumb{font-size:12px;font-weight:400;color:#aaa;margin:0 0 15px}
#breadcrumb a{color:#aaa;transition:color .17s}
#breadcrumb a:hover{color:$(body.color.blue)}
#breadcrumb a,#breadcrumb em{display:inline-block}
#breadcrumb .delimiter:after{content:'\f105';font-size:8px;font-weight:400;font-style:normal;vertical-align:middle;margin:0 3px}
.item-post h1.post-title{color:#000000;font-size:27px;line-height:1.5em;font-weight:700;position:relative;display:block;margin:0 0 15px;padding:0}
.main .widget,.static_page .item-post h1.post-title{margin:0}
.item-post .post-body{width:100%;font-size:15px;line-height:1.8em;overflow:hidden;padding:20px 0 0;margin:0}
.item-post .post-outer{padding:0}
.main .Blog{border-bottom-width:0}
.post-footer{position:relative;float:left;width:100%;margin:20px 0}
.post-footer .post-labels{margin:0 auto;float:left}
.inline-ad{position:relative;display:block;max-height:60px;margin:0 0 30px}
.inline-ad>ins{display:block!important;margin:0 auto!important}
.item .inline-ad{float:left;width:100%;margin:20px 0 0}
.comments .comments-content .datetime,.post-share{float:right}
.item-post-wrap>.inline-ad{margin:0 0 20px}
.post-share{position:relative;overflow:hidden;line-height:2;margin:0 auto}
.post-labels a,.post-labels span{position:relative;display:inline-block;font-size:13px;line-height:28px;font-weight:400;padding:0 12px;-webkit-transition:all .4s;-o-transition:all .4s;-moz-transition:all .4s;transition:all .4s;border:0;background:#f3f5fe;-webkit-border-radius:3px;-moz-border-radius:3px;border-radius:3px}
.post-labels a:hover,.post-labels span{background-color:$(body.color.blue);color:$(body.text.color)}
.post-labels a{margin:0 10px 0 0;transition:all .17s ease}
.post-labels a:hover{border-color:$(body.color.blue)}
.post-share .share-links li a,.post-share .social a:before{color:#fff;font-weight:400;text-align:center;display:inline-block}
ul.share-links{position:relative}
.post-share .share-links li{display:inline-block;margin:0 0 0 10px}
.post-share .share-links li a{float:left;cursor:pointer;width:100%;line-height:32px;font-size:17px;opacity:1;transition:all .17s ease}
.post-share .social a:before{font-style:normal;height:38px;width:38px;line-height:40px;border-radius:19px;-webkit-border-radius:19px;-moz-border-radius:19px;background:#fe4c1c;transition:all .4s ease-in-out;-webkit-transition:all .4s ease-in-out;-moz-transition:all .4s ease-in-out;-o-transition:all .4s ease-in-out;-ms-transition:all .4s ease-in-out}
.post-share .social .facebook a:before,.post-share .social .linkedin a:before,.post-share .social .pinterest a:before,.post-share .social .twitter a:before,.social .behance a:before,.social .codepen a:before,.social .delicious a:before,.social .digg a:before,.social .dribbble a:before,.social .external-link a:before,.social .facebook a:before,.social .github a:before,.social .instagram a:before,.social .pinterest a:before,.social .reddit a:before,.social .skype a:before,.social .snapchat a:before,.social .soundcloud a:before,.social .stack-overflow a:before,.social .stumbleupon a:before,.social .tumblr a:before,.social .twitch a:before,.social .twitter a:before,.social .vk a:before,.social .whatsapp a:before,.social .youtube a:before{font-family:"Font Awesome 5 Brands"}
.post-share .social .facebook a:before{content:"\f39e";background:#4661c5}
.post-share .social .pinterest a:before{content:"\f231"}
.post-share .social .twitter a:before{content:"\f099";background:#44b1e4}
.post-share .social .linkedin a:before{content:"\f0e1";background:#0073b0}
.post-share .social .whatsapp a:before{background:#20d847}
.social .facebook a:before{content:"\f09a";font-weight:400}
.social .twitter a:before{content:"\f099";font-weight:400}
.social .youtube a:before{content:"\f167";font-weight:400}
.social .skype a:before{content:"\f17e";font-weight:400}
.social .stumbleupon a:before{content:"\f1a4";font-weight:400}
.social .tumblr a:before{content:"\f173";font-weight:400}
.social .vk a:before{content:"\f189";font-weight:400}
.social .stack-overflow a:before{content:"\f16c";font-weight:400}
.social .github a:before{content:"\f09b";font-weight:400}
.social .linkedin a:before{content:"\f0e1";font-family:"Font Awesome 5 Brands";font-weight:400}
.social .dribbble a:before{content:"\f17d";font-weight:400}
.social .soundcloud a:before{content:"\f1be";font-weight:400}
.social .behance a:before{content:"\f1b4";font-weight:400}
.social .digg a:before{content:"\f1a6";font-weight:400}
.social .instagram a:before{content:"\f16d";font-weight:400}
.social .pinterest a:before{content:"\f0d2";font-weight:400}
.social .twitch a:before{content:"\f1e8";font-weight:400}
.social .delicious a:before{content:"\f1a5";font-weight:400}
.social .codepen a:before{content:"\f1cb";font-weight:400}
.social .reddit a:before{content:"\f1a1";font-weight:400}
.social .whatsapp a:before{content:"\f232";font-weight:400}
.social .snapchat a:before{content:"\f2ac";font-weight:400}
.social .email a:before{content:"\f0e0"}
.social .external-link a:before{content:"\f35d";font-weight:400}
.social-color .blogger a{color:#ff5722}
.social-color .facebook a{color:#3b5999}
.social-color .twitter a{color:#00acee}
.social-color .gplus a{color:#db4a39}
.social-color .youtube a{color:#f50000}
.social-color .instagram a{background:linear-gradient(15deg,#ffb13d,#dd277b,#4d5ed4)}
.social-color .pinterest a{color:#ca2127}
.social-color .dribbble a{color:#ea4c89}
.social-color .linkedin a{color:#0077b5}
.social-color .tumblr a{color:#365069}
.social-color .twitch a{color:#6441a5}
.social-color .rss a{color:#ffc200}
.social-color .skype a{color:#00aff0}
.social-color .stumbleupon a{color:#eb4823}
.social-color .vk a{color:#4a76a8}
.social-color .stack-overflow a{color:#f48024}
.social-color .github a{color:#24292e}
.social-color .soundcloud a{background:linear-gradient(#ff7400,#ff3400)}
.social-color .behance a{color:#191919}
.social-color .digg a{color:#1b1a19}
.social-color .delicious a{color:#0076e8}
.social-color .codepen a{color:#000000}
.social-color .reddit a{color:#ff4500}
.social-color .whatsapp a{color:#3fbb50}
.social-color .snapchat a{color:#ffe700}
.social-color .email a{color:#888}
.social-color .external-link a{color:$(body.text.color)}
.blog-pager{float:left;width:100%;font-size:15px;font-weight:500;text-align:center;clear:both;padding:0;margin:30px 0 10px}
#blog-pager .load-more{display:inline-block;height:50px;width:50px;line-height:59px;background-color:$(body.color.blue);font-size:14px;font-weight:400;padding:0;margin:0;border-radius:100px}
#blog-pager #load-grid i{font-size:20px}
#blog-pager #load-grid{color:$(body.text.color);cursor:pointer}
#blog-pager #load-grid:hover{background-color:$(body.color.blue);color:$(body.text.color)}
#blog-pager .endmore,#blog-pager .loading{display:none}
#blog-pager .loading .loader{position:relative;overflow:hidden;display:block;margin:0;height:34px}
#blog-pager .endmore.show,#blog-pager .load-more.endmore,#comments-block .avatar-image-container,.archive #blog-pager,.comments .comments-content .comment-thread:empty,.home .blog-pager .blog-pager-newer-link,.home .blog-pager .blog-pager-older-link,.home .boxsubs{display:none}
#blog-pager .loading .loader:after{content:'';position:absolute;top:50%;left:50%;width:28px;height:28px;margin:-16px 0 0 -16px;border:2px solid;border-right-color:rgba(155,155,155,.2);border-radius:100%;animation:spinner 1.1s infinite linear;transform-origin:center}
@-webkit-keyframes spinner{0{-webkit-transform:rotate(0);transform:rotate(0)}
to{-webkit-transform:rotate(1turn);transform:rotate(1turn)}}
@keyframes spinner{0{-webkit-transform:rotate(0);transform:rotate(0)}
to{-webkit-transform:rotate(1turn);transform:rotate(1turn)}}
.post-animated{-webkit-animation-duration:.5s;animation-duration:.5s;-webkit-animation-fill-mode:both;animation-fill-mode:both}
@keyframes fadeIn{from{opacity:0}
to{opacity:1}}
.post-fadeIn{animation-name:fadeIn}
@keyframes fadeInUp{from{opacity:0;transform:translate3d(0,5px,0)}
to{opacity:1;transform:translate3d(0,0,0)}}
.post-fadeInUp{animation-name:fadeInUp}
#comments{clear:both;list-style:none;position:relative;margin:0 auto;padding:0;overflow:hidden}
comments h3{font-size:14px;display:block;font-weight:400;text-transform:uppercase;margin:0 0 30px;padding:0 0 10px;border-bottom:1px solid rgba(0,0,0,.05);position:relative}
#comments h3 after{content:"";position:absolute;bottom:-1px;left:0;width:60px;height:1px;background:#ffd6be}
#comment-editor,.comment-thread .user,.related-post h4{position:relative}
#comments h3 first-letter{color:#ff5f02}
.comments-content{padding:0 0 15px}
#comments-block{margin:15px 0}
.comment-body{padding:15px 0;margin:0}
.comment-body p{margin:0}
.comment-footer{margin:0 0 30px}
h4#comment-post-message{display:none;margin:0}
.comments{clear:both;margin-top:10px;margin-bottom:0}
.comments .comments-content{font-size:14px;margin-bottom:30px}
.comments .comments-content .comment-thread ol{text-align:left;margin:13px 0;padding:0;list-style:none}
.comments .comment-block{position:relative;margin-left:55px;margin-right:3px;padding:15px;word-break:break-word;background:#fbfbfb;border-radius:5px}
.comments .comment-replies .comment-block{margin-left:50px}
.comments .comments-content .comment-replies{margin:10px 0 10px 45px}
.comments .comment-replybox-single{margin:20px 0}
.comments .comment-replybox-thread{margin:0}
.comments .comments-content .comment{margin-bottom:6px;padding:0}
.comments .comments-content .comment:first-child,.comments .comments-content .comment:last-child{padding:0;margin:0}
.comments .comments-content .inline-thread{margin:0}
.comments .comments-content .comment-header{font-size:14px;margin:0 0 5px}
.comments .comments-content .comment-content{margin:10px 0;text-align:left;font:400 13px/1.71em AcuminPro,arial,helvetica,sans-serif}
.post-body ul li:before,blockquote:after{font-family:"Font Awesome 5 Pro"}
.comments .comments-content .datetime a{color:#555}
.comments .comments-content .user{font-weight:700;font-style:normal}
.comments .comment .comment-actions a{display:inline-block;font-size:13px;line-height:15px;margin:4px 8px 0 0}
.comments .continue a{display:inline-block;font-size:13px;padding:.5em}
.comments .comment .comment-actions a:hover,.comments .continue a:hover{color:#dd4a45}
.deleted-comment{font-style:italic;opacity:.5}
.comments .comments-content .loadmore{cursor:pointer;margin-top:3em;max-height:3em}
.comments .comments-content .loadmore.loaded{max-height:0;opacity:0;overflow:hidden}
.comments .continue,.comments .thread-chrome.thread-collapsed{display:none}
.comments .thread-toggle{display:inline-block}
.comments .thread-toggle .thread-arrow{display:inline-block;height:6px;margin:.3em;overflow:visible;padding-right:4px;width:7px}
.comments .thread-collapsed .thread-arrow,.comments .thread-expanded .thread-arrow{width:24px;height:24px;vertical-align:middle;display:inline-block}
.comments .hidden{display:none}
.item-control a,.secondary-text a.comment-reply{color:#909090;text-align:center;padding:0!important;font-weight:400;text-decoration:none}
.comment-thread .user,.comment-thread .user a{font-size:14px;font-weight:700;padding:0;text-transform:uppercase;text-decoration:none}
.secondary-text a.comment-reply{color:#777}
.item-control a:hover,.secondary-text a:hover.comment-reply{color:#000000!important}
#comment-editor{width:100%!important;background:url(https://1.bp.blogspot.com/-kAp4OwqTq28/XhxAOb139ZI/AAAAAAAAB0o/F-S8gdjOSXwtilbEYncR5S7e2WQElHVYwCLcBGAsYHQ/s1600/loader.gif) 50% 25% no-repeat;max-height:310px!important;transition:1.3s ease-out}
.comment-thread .user a{color:#000000}
.comment-thread .user a:hover{color:inherit}
.comment-thread .datetime a{text-decoration:none;color:#909090;font-size:11px;font-weight:400}
.PopularPosts .post:hover .post-title a,.errorgrid a:hover,.post-body u,.related-post-style-1 li a:hover,.related-post-style-2 a:hover.related-post-item-title,.related-post-style-3 a:hover.related-post-item-title{text-decoration:underline}
.comment-thread .datetime a:hover{color:#000000}
.item-control{margin-left:0}
.thread-chrome a.comment-reply{margin-top:20px!important;display:block;text-align:center;border-radius:99em;background-color:#f4f4f4}
.thread-chrome a:hover.comment-reply{color:#999}
#comments .comments-content .icon.blog-author{width:18px;height:18px;line-height:18px;margin-left:5px;vertical-align:middle;margin-top:-5px;display:inline-block}
#comments .comments-content .icon.blog-author:before{content:"\f005";font-family:"Font Awesome 5 Pro";color:$(body.color.blue);font-size:11px;vertical-align:middle}
.comment .avatar-image-container{width:40px;height:40px;overflow:hidden;float:left;border-radius:99em}
#comments .comment-replies .comment-thread .comment .avatar-image-container img,.comment .avatar-image-container img{display:block;padding:0;margin:0 auto}
#comments .comment-replies .comment-thread .comment .avatar-image-container{width:35px;height:35px;max-width:35px;max-height:35px}
#comments .avatar-image-container img{width:40px;height:40px;max-width:40px;max-height:40px;background:url(https://1.bp.blogspot.com/-ITY2zUo6O8w/XhxBWisGHeI/AAAAAAAAB0w/a_379aQsD6E3RdyzR0zSSeZOBwX2L86pwCLcBGAsYHQ/s1600/no.jpg) center;background-size:cover}
#comments .comment-replies .avatar-image-container img{width:35px;height:35px;max-width:35px;max-height:35px;background:url(https://1.bp.blogspot.com/-ITY2zUo6O8w/XhxBWisGHeI/AAAAAAAAB0w/a_379aQsD6E3RdyzR0zSSeZOBwX2L86pwCLcBGAsYHQ/s1600/no.jpg) center center no-repeat}
.threaded_comments_text{display:block;margin:20px 0}
.threaded_comments_text p{font-size:100%;line-height:inherit}
.post-body h2,.post-body h3,.post-body h4,.post-body h5,.post-body h6,post-body h1{color:#000000;font-weight:600;margin:0 0 15px}
.post-body h1,.post-body h2{font-size:24px}
.post-body h3{font-size:21px}
.post-body h4{font-size:18px}
.post-body h5{font-size:16px}
.post-body h6{font-size:13px}
#related-wrapper{margin:0 auto;padding:0;display:block;overflow:hidden;clear:both}
.related-post{margin:20px auto;padding:0;text-align:center}
.related-post h4{margin:5px 0 15px;font-size:35px;line-height:1.2em;padding:0 15px;color:$(body.text.color);font-weight:400;text-align:center;font-family:Playball,cursive;display:inline-block}
.related-post h4:after,.related-post h4:before{display:block;width:500px;height:0;border-bottom:1px solid #f7f7f7;position:absolute;top:50%;content:''}
.related-post h4:before{right:100%;left:auto}
.related-post h4:after{left:100%;right:auto}
.related-post .related-post-style-1,.related-post .related-post-style-2,.related-post .related-post-style-3{-moz-box-sizing:border-box;-webkit-box-sizing:border-box;box-sizing:border-box;display:-webkit-box;display:-webkit-flex;display:flex;-webkit-flex-wrap:wrap;-ms-flex-wrap:wrap;flex-wrap:wrap}
.related-post .related-post-style-1{margin:10px 0 20px}
.related-post .related-post-style-1 li{display:block;width:100%;text-align:left}
.related-post .related-post-item-summary,.related-post-style-3 span{font-size:110%;color:$(body.text.color);line-height:1.4em;display:inline-block;text-align:left}
.related-post-style-3{margin:0 0 0 -3%!important}
.related-post-style-3 li{list-style:none;margin-left:3%!important;padding:0;width:calc(31.333% - 1%);float:left}
.related-post-style-3 li img{width:100%;height:100%}
.related-post-style-3 a.related-post-item-title{text-align:left;font-size:16px;color:$(body.text.color);margin:10px auto;font-weight:500;line-height:1.5em;display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden}
.related-post-style-3 span,.related-posts-widget h3{display:none!important;height:0;width:0;overflow:hidden}
.related-post-style-2{margin:0 auto!important}
.related-post-style-2 li{list-style:none;margin:0 auto 10px;padding:10px 0 0;display:block;width:100%;border-top:1px solid #eee}
.related-post-style-2 li:first-child{border-top:none}
.related-post-style-2 .related-post-item-thumbnail{align-items:center;justify-content:center;margin:0 auto;width:125px;height:80px;max-width:none;max-height:none;padding:0;overflow:hidden;display:inline-block;float:left}
.related-post-style-2 .related-post-item-thumbnail img{width:100%;height:100%}
.related-post-style-2 a.related-post-item-title{line-height:1.3em;display:block;text-align:left;font-size:16px;color:#2d2d2d;margin:0 0 7px;font-weight:500}
.related-post-style-2 a.related-post-item-more{display:none}
.related-post-style-2 .related-post-item-text{display:inline-block;text-align:left;width:calc(100% - 140px);float:right}
.related-post-style-1 li a{line-height:1.3em;display:block;position:relative;font-size:115%!important;color:#2d2d2d;margin:0 0 10px;padding:0;font-weight:400}
.related-post-style-1 li a:before{content:'';width:7px;height:7px;border-radius:100%;background-color:#0076f4;display:inline-block;position:relative;top:-1px;left:0;margin-right:10px}
blockquote{font-style:italic;padding:17px;margin:10px auto;background:#fbfbfb}
blockquote:after{display:inline-block;font-style:normal;font-weight:900;color:#f1f1f1;line-height:1;content:'\f10e';margin:0 0 0 10px}
.widget .post-body ol,.widget .post-body ul{line-height:1.5;font-weight:400}
.widget .post-body li{margin:5px 0;padding:0;line-height:1.5}
.post-body ul{padding:0 0 0 20px}
.post-body ul li:before{content:"\f111";font-size:13px;font-weight:400;margin:0 5px 0 0}
.post-body strike{text-decoration:line-through}
.contact-form{overflow:hidden}
.contact-form .widget-title{display:none}
.contact-form .contact-form-name{width:calc(50% - 5px)}
.contact-form .contact-form-email{width:calc(50% - 5px);float:right}
.sidebar .widget-content{position:relative;overflow:hidden;padding:0;box-sizing:border-box;float:left;width:100%;margin:0}
.sidebar .widget{margin:0 0 30px;overflow:hidden;padding:20px;background:#f2f3ff}
#social-widget .widget{margin-bottom:35px}
.sidebar .widget-title{position:relative;overflow:hidden;float:left;width:100%;display:block;margin:0 auto}
.sidebar .widget-title>h3{color:#000000;font-size:20px;font-weight:600;text-decoration:none;display:inline-block;padding:0 10px 0 0;margin:0 auto 15px;position:relative;letter-spacing:normal}
#ArchiveList .flat li>a:before,.list-label li a:before{content:"\f054";font-family:"Font Awesome 5 Pro"}
ul.social-counter{margin:0 -5px}
.social-counter li{float:left;width:25%;box-sizing:border-box;padding:0 5px;margin:10px 0 0}
.social-counter li:nth-child(1),.social-counter li:nth-child(2),.social-counter li:nth-child(3),.social-counter li:nth-child(4){margin-top:0}
.social-counter li a{display:block;height:40px;font-size:22px;color:$(body.color.blue);text-align:center;line-height:40px;border:1px solid #eee;transition:color .17s}
.social-counter li a:hover{color:$(body.text.color)}
.list-label li{position:relative;display:block;padding:7px 0;border-top:1px dotted #ebebeb}
.list-label li:first-child{padding-top:0;border-top:0}
.list-label li:last-child{padding-bottom:0;border-bottom:0}
.list-label li a{display:block;font-size:12px;font-weight:400;text-transform:capitalize;transition:color .17s}
.list-label li a:before{float:left;color:$(body.color.blue);font-weight:400;font-size:6px;margin:6px 6px 0 0;transition:color .17s}
.list-label li a:hover{color:$(body.color.blue)}
.list-label .label-count{position:relative;float:right;width:16px;height:16px;background-color:$(body.color.blue);color:$(body.text.color);font-size:11px;font-weight:400;text-align:center;line-height:16px}
.cloud-label li{position:relative;float:left;margin:0 5px 5px 0}
.cloud-label li a{display:block;height:26px;color:$(body.color.blue);font-size:12px;line-height:26px;font-weight:400;padding:0 10px;border:1px solid #eee;transition:all .17s ease}
.cloud-label li a:hover{color:$(body.text.color);background-color:$(body.color.blue);border-color:$(body.color.blue)}
.cloud-label .label-count{display:none}
.sidebar .FollowByEmail>.widget-title>h3{margin:0}
.FollowByEmail .widget-content{position:relative;overflow:hidden;text-align:center;font-weight:400;box-sizing:border-box;padding:20px}
.FollowByEmail .widget-content>h3{font-size:18px;color:$(body.text.color);font-weight:500;text-transform:uppercase;margin:0 0 13px}
.FollowByEmail .before-text{font-size:13px;line-height:1.5em;margin:0 0 15px;display:block;padding:0 10px;overflow:hidden}
.FollowByEmail .follow-by-email-inner{position:relative}
.FollowByEmail .follow-by-email-inner .follow-by-email-address{width:100%;float:left;height:50px;position:relative;color:#060606;font-size:13px;padding:0 20px;margin:0;box-sizing:border-box;border:none;transition:ease .17s}
.FollowByEmail .follow-by-email-inner .follow-by-email-submit{height:50px;position:absolute;right:0;font-size:14px;color:$(menu.title.color);background:$(main.color);text-transform:uppercase;text-align:center;font-weight:700;cursor:pointer;padding:0 30px;margin:0 auto;border:0;transition:opacity .17s ease}
.FollowByEmail .follow-by-email-inner .follow-by-email-submit:hover{opacity:.85}
#ArchiveList ul.flat li{color:$(body.text.color);font-size:13px;font-weight:400;padding:7px 0;border-bottom:1px dotted #eaeaea}
#ArchiveList ul.flat li:first-child{padding-top:0}
#ArchiveList ul.flat li:last-child{padding-bottom:0;border-bottom:0}
#ArchiveList .flat li>a{display:block;color:$(body.text.color);transition:color .17s}
#ArchiveList .flat li>a:hover{color:$(body.color.blue)}
#ArchiveList .flat li>a:before{float:left;color:#161619;font-weight:400;font-size:6px;margin:6px 3px 0 0;display:inline-block;transition:color .17s}
#ArchiveList .flat li>a>span{position:relative;float:right;width:16px;height:16px;background-color:$(body.color.blue);color:$(body.text.color);font-size:11px;font-weight:400;text-align:center;line-height:16px}
.PopularPosts .post{overflow:hidden;margin:20px 0 0}
.PopularPosts .post:first-child{padding:0;margin:0;border:0}
.PopularPosts .post-image-link{position:relative;width:90px;height:80px;float:left;overflow:hidden;display:block;vertical-align:middle;margin:0 12px 0 0}
.PopularPosts .post-info{overflow:hidden}
.PopularPosts .post-title{font-size:14px;font-weight:500;line-height:1.5em;margin:0 0 3px;display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden}
#back-to-top,.contact-form-widget form{font-weight:400}
.PopularPosts .post-title a{display:block;color:#000000;transition:color .17s}
.PopularPosts .post-date:before{font-size:10px}
.contact-form-button-submit,.contact-form-email,.contact-form-email-message,.contact-form-name{float:left;width:100%;font-size:13px;box-sizing:border-box}
.contact-form-email,.contact-form-name{height:30px;font-family:inherit;line-height:30px;padding:5px 10px;margin:0 0 10px;border:1px solid #ebebeb;border-radius:2px}
.contact-form-email-message{font-family:inherit;padding:5px 10px;margin:0 0 10px;border:1px solid #ebebeb;border-radius:2px}
.contact-form-button-submit{height:30px;background-color:$(body.color.blue);color:$(body.text.color);line-height:30px;cursor:pointer;padding:0 10px;margin:0;border:0;border-radius:2px;transition:background .17s ease}
.contact-form-error-message-with-border,.contact-form-success-message-with-border{width:100%;font-size:11px;line-height:11px;padding:3px 0;margin:10px 0;box-sizing:border-box;float:left;text-align:center}
.contact-form-button-submit:hover{background-color:$(body.text.color)}
.contact-form-error-message-with-border{background-color:#fbe5e5;border:1px solid #fc6262}
.contact-form-success-message-with-border{background-color:#eaf6ff;border:1px solid #5ab6f9}
.contact-form-cross{margin:0 0 0 3px}
.contact-form-error-message,.contact-form-success-message{margin:0}
.common-widget .LinkList ul li,.common-widget .PageList ul li{width:calc(50% - 5px);padding:7px 0 0}
.common-widget .LinkList ul li:nth-child(odd),.common-widget .PageList ul li:nth-child(odd){float:left}
.common-widget .LinkList ul li:nth-child(even),.common-widget .PageList ul li:nth-child(even){float:right}
.common-widget .LinkList ul li a,.common-widget .PageList ul li a{display:block;color:$(body.text.color);font-size:13px;font-weight:400;transition:color .17s ease}
.common-widget .LinkList ul li a:hover,.common-widget .PageList ul li a:hover{color:$(body.color.blue)}
.common-widget .LinkList ul li:first-child,.common-widget .LinkList ul li:nth-child(2),.common-widget .PageList ul li:first-child,.common-widget .PageList ul li:nth-child(2){padding:0}
.hidden-widgets{display:none;visibility:hidden}
.back-to-top{line-height:40px;position:fixed;bottom:20px;right:20px;border-radius:5px;z-index:999;border:2px solid $(main.color);height:40px;text-align:center;cursor:pointer;width:40px;background:#fff}
#back-to-top{color:#0856da;padding:0;font-size:18px}
.boxerror .boxhome{height:115px}
.boxerror .main-wrapper{width:100%!important;margin:0!important}
.boxerror #content-wrapper{display:block}
.boxerror #box-banner,.boxerror .brand_wrapper,.boxerror .sidebar-wrapper{display:none}
.errorgrid{color:#5a5a5a;text-align:center;padding:80px 0 100px}
.errorgrid h3{font-size:160px;line-height:1;margin:0 0 30px;color:#ffc400;}
.errorgrid h4{font-size:25px;margin:0 0 20px}
.errorgrid p{margin:0 0 10px}
.errorgrid a{display:block;color:#5a5a5a;padding:10px 0 0}
.errorgrid a i{font-size:20px}
._banner h3{display:none}
#box-banner{text-align:center;overflow:hidden;display:block;clear:both;margin:30px 0 20px}
.parnert h3{display:none}
.customer-parnert .slick-slide{margin:0 20px;-webkit-filter:saturate(.1);filter:saturate(.1);-webkit-transition:all .5s ease-in-out;-moz-transition:all .5s ease-in-out;-ms-transition:all .5s ease-in-out;-o-transition:all .5s ease-in-out;transition:all .5s ease-in-out}
.customer-parnert{width:100%;height:auto;outline:0;overflow:hidden;overflow-x:hidden;white-space:nowrap;margin:0 auto}
.brand-box{padding:10px 20px;margin:0 auto}
.brand-box img{height:auto;width:100%;margin:0 auto;position:relative}
#footer-wrapper{display:block;width:100%;overflow:hidden;padding:0;position:relative}
.lay{background-image:url(https://1.bp.blogspot.com/-lwGmAh06nsg/XuyPbev9LdI/AAAAAAAAAI0/k9B_y4VCIPI7UpaTWgqiOQblDgj-n2AGwCLcBGAsYHQ/s1600/maps8.png);background-size:cover;background-repeat:no-repeat;background-attachment:scroll;background-position:center center;top:0;left:0;width:100%;height:100%}
.PopularPosts .post-tag{position:relative;z-index:5;background-color:#2ad2c9;color:$(body.text.color);font-size:10px;line-height:18px;font-weight:500;text-transform:uppercase;padding:0 7px}
.footer-box{padding:0;overflow:hidden;color:$(footer.color);line-height:1.4em;margin:0;font-size:14px}
.footer-box .footer{float:left;width:23.18323%;margin:20px 20px 20px 0}
.footer-box .footer .widget{margin-bottom:10px}
.footer-box .footer h3{font-size:18px;line-height:1.2em;color:$(footer.title);display:block;margin:0;padding:15px 0;font-weight:600;position:relative}
.footer-box .footer .widget-content{line-height:21px}
.footer-box .footer ul{list-style:none;color:$(footer.link);margin:0;padding:0}
.footer-box .footer li{color:$(footer.link);line-height:1.2em;margin:0;padding:5px 0}
.footer-box .footer a:link,.footer-box .footer li a:visited{color:$(footer.link);text-decoration:none;font-weight:400;line-height:1.6em;font-size:14px}
.credit-footer a:hover,.footer-box .footer li a:hover{text-decoration:underline}
.footer-box .footer li a::before{display:inline-block;font-family:"Font Awesome 5 Pro";font-style:normal;font-weight:400;margin-right:10px;color:$(main.color)}
.testi-wrap{overflow:hidden;position:relative;padding:5% 0}
.boxtestimonial{padding:0 0 50px}
.ithemonial{text-align:center;width:83.33333333%;margin:20px auto 0}
.ithemonialicon:after,.ithemonialicon:before{color:#fdf3ce;font-size:30px;font-family:"Font Awesome 5 Pro";font-weight:900;padding-top:0;margin:0 15px}
.ithemonialicon:before{content:"\f10d";float:left}
.ithemonialicon:after{content:"\f10e";float:right}
.boxtestimonial .owl-next,.boxtestimonial .owl-prev{height:35px;line-height:37px;position:absolute;width:35px;border-radius:50%;border:none;margin:0;padding:0;bottom:40%;font-size:24px;text-align:center;color:#ffffff;background:#dadada;text-shadow:none}
.boxtestimonial .owl-next:hover,.boxtestimonial .owl-prev:hover{transition:all 1s;background:$(main.color)}
.boxtestimonial .owl-prev:before{content:'\f104';font-family:"font awesome 5 Pro"}
.boxtestimonial .owl-next:before{content:'\f105';font-family:"font awesome 5 Pro"}
.boxtestimonial .owl-prev{left:25%;transition:all .5s}
.boxtestimonial .owl-next{right:25%;transition:all .5s}
.monialimg img{width:100px!important;height:100px;border:4px solid #fff;border-radius:50%;box-shadow:0 10px 10px rgba(86,86,86,0.2);padding:2px;margin:0 auto 5px}
.ithemonial p{color:#242c42;font-size:16px;font-weight:400;font-style:italic;padding:0;margin:0 0 30px}
.monialimg h4{color:#000000;font-size:16px;font-weight:600;line-height:20px}
.monialimg h4 span{display:block;margin:8px 0;font-size:13px;color:#7d7d7d;text-transform:uppercase}
.subs-wrapper{padding:20px;-webkit-box-shadow:5px 5px 20px 0 rgba(167,167,167,.1);-moz-box-shadow:5px 5px 20px 0 rgba(167,167,167,.1);border-radius:8px;-webkit-border-radius:8px;-moz-border-radius:8px;max-width:700px;width:100%;margin:0 auto 8%;}
.subs-wrapper .FollowByEmail h3{display:none}
.map-wrapper{overflow:hidden;padding:3% 0 2%;margin-bottom:2%;border-bottom:1px solid rgba(255, 255, 255, 0.16)}
.map-wrapper-left{float:left;width:25%}
.map-wrapper-right{float:right;width:70%}
.elementor-map{float:right;padding:1rem 0;margin:0}
.elementor-map div{position:relative;margin:0 auto 0 30px;padding:0;list-style:none;float:left}
.elementor-map div.icon-box__title{margin:0;padding-top:.05556rem;font-size:16px;font-weight:400;display:block;color:#ffffff}
.elementor-map div.icon-box i{font-size:30px;padding:0;height:35px;color:#ffffff;text-align:center;line-height:35px;margin-top:10px;position:absolute;width:35px;font-weight:300;float:left;margin-right:.55556rem;border-radius:50%;vertical-align:middle}
.elementor-map div .icon-box__title{margin:0;padding-top:.05556rem;font-size:16px;font-weight:500;display:block;color:#ffffff}
.elementor-map div.icon-box__text{margin-left:50px}
.elementor-map div span.icon-box__subtitle{font-size:15px;font-weight:400;color:#ffffff}
.mplogo{width:218px;height:auto;vertical-align:middle;padding-top:10px}
.mplogo img{width:100%;height:auto}
.iconfit{margin-top:20px!important}
ul.iconfit li{float:left;display:inline-block}
ul.iconfit li a:before{display:none!important}
ul.iconfit li>a{display:block;font-size:20px!important;color:#e0ecff!important;padding:0;margin:0 20px 0 0;transition:all .17s ease}
.credit-footer{width:100%;font-size:15px;display:block;height:34px;color:#ffffff;font-weight:400;line-height:34px;padding:20px 0;overflow:hidden;text-align:center}
.credit-footer a{color:#ffffff;transition:color .17s}
@media screen and (max-width:1100px){.header-wrapper{width:95%}
#outer-wrapper{max-width:95%}
.halaman-indeks{width:30.23%}
.ot-pricing-table{width:21.67%}
.footer-box .footer{width:23%}}
@media screen and (max-width:1024px){#main-menu ul#main-menu-nav,#top-bar{padding-left:25%}
.home .boxhome{height:auto}
.tabs ul li label{white-space:initial}
.tabs ul li label br{display:initial}
.ot-pricing-table{width:20.7%}
.footer-box .footer{width:22%}}
@media screen and (max-width:991px){halaman-indeks{width:30%}
.ot-pricing-table{width:100%;padding:20px 0;float:none;margin:30px auto}
.elementor-map{float:none;padding:1rem 0;margin:0 auto;display:block}
.footer-box .footer{width:100%;margin:20px auto}
.map-wrapper-right{float:left;width:100%}
.elementor-map div{position:relative;margin:0 auto 30px;padding:0;list-style:none;float:none;display:block;width:100%}}
@media screen and (max-width:980px){.boxwrap-os-right,.boxwrap-text h2,.boxwrap-text h3,.digital-wrapper h3,.recent-boxes .widget-title,.recent-boxes h3,.tabs .content section h3: :after,a.more-link{text-align:center}
.iconsearch-label:before,a.more-link:before{border-bottom:none}
.index .boxhome,.item .boxhome{height:auto}
#sticky-wrap.stickyhead .iconsearch-label,.btnmenu,.iconsearch-label{height:20px}
.headblog:before{border-top:110px solid $(main.color)}
.btn-mobile{display:block;background:0 0;color:#ffffff;right:5%;font-weight:400;font-size:15px}
#main-menu,#top-bar,.box-right,.btn-dekstop,.content-left,.marketright{display:none}
#sticky-wrap.stickyhead .btn-mobile{color:#000000}
.headblog{width:180px}
.headblog img{margin-top:5px}
#sticky-wrap.stickyhead .headblog:before{border-top:108px solid $(main.color)}
.boxwrap-left,.boxwrap-right{width:100%;float:none;margin:0 auto}
.boxwrap-os-right{float:none;width:auto}
.boxwrap-icon,.mobile-menu,.slide-menu-toggle{display:block}
.box-left,.boxwrap-os-left,.boxwrap-os-right.boxwrap-left,.boxwrap-right,.content-right,.marketleft{float:none;width:100%;margin:0 auto;text-align:center}
.box-left h3{font-size:25px}
.boxwrap-os-left h2,.boxwrap-text h2{font-size:41px}
a.more-link{top:0;right:initial;left:initial;margin:0 auto;position:relative}
a.more-link:before{border-left:none}
.cd-headline{font-size:3rem}
.tabs .content section h3::after{margin:5px auto;left:0;right:0}
.colorwp{margin:50px 0}
#sticky-wrap.stickyhead .headblog{margin:2px 30px 0 0;width:180px}
.btnmenu{display:-webkit-box;display:flex;align-self:center;padding:20px 5px;float:right;-webkit-box-orient:vertical;-webkit-box-direction:normal;flex-direction:column;-webkit-box-pack:justify;justify-content:space-between;width:35px;cursor:pointer}
#menuslide,.ui_box{float:none}
.btnmenu div{align-self:flex-end;height:2px;width:100%;background:#fff}
#sticky-wrap.stickyhead .btnmenu div{background:#000}
.btnmenu .meat{width:75%;-webkit-transition:all .2s ease-in-out;transition:all .2s ease-in-out}
.btnmenu .bottom-bun{width:50%;-webkit-transition:all .4s ease-in-out;transition:all .4s ease-in-out}
.btnmenu:hover div{width:100%}
.btnmenu:hover .top-bun{-webkit-animation:burger-hover 1s infinite ease-in-out alternate;animation:burger-hover 1s infinite ease-in-out alternate}
.btnmenu:hover .meat{-webkit-animation:burger-hover 1s infinite ease-in-out alternate forwards .2s;animation:burger-hover 1s infinite ease-in-out alternate forwards .2s}
.btnmenu:hover .bottom-bun{-webkit-animation:burger-hover 1s infinite ease-in-out alternate forwards .4s;animation:burger-hover 1s infinite ease-in-out alternate forwards .4s}
@-webkit-keyframes burger-hover{0,100%{width:100%}
50%{width:50%}}
@keyframes burger-hover{0,100%{width:100%}
50%{width:50%}}
.menu{width:280px;height:100%;left:-280px;z-index:99999;bottom:0;background:#fff;top:0;position:fixed;transition:.5s linear}
.menu.active,.page-wrapper.toggled{left:0}
@keyframes swing{0,100%,30%,50%,70%{transform:rotate(0)}
10%{transform:rotate(10deg)}
40%{transform:rotate(-10deg)}
60%{transform:rotate(5deg)}
80%{transform:rotate(-5deg)}}
#close-sidebar,#show-sidebar,.page-wrapper,.page-wrapper .page-content,.sidebar-brand a,.sidebar-dropdown a:after,.sidebar-menu .sidebar-dropdown .sidebar-submenu li a:before,.sidebar-menu ul li a,ul li a i{-webkit-transition:all .3s ease;-moz-transition:all .3s ease;-ms-transition:all .3s ease;-o-transition:all .3s ease;transition:all .3s ease}
.page-wrapper{height:100vh;padding:20px}
.page-wrapper .theme{width:40px;height:40px;display:inline-block;border-radius:4px;margin:2px}
.page-wrapper .theme.chiller-theme{background:#1e2229}
.cross{display:block;padding:10px 20px;background:0 0;text-align:right;cursor:pointer}
#menuslide ul{width:100%;height:auto;-webkit-box-shadow:0 2px 8px 0 rgba(0,0,0,.15);box-shadow:0 2px 8px 0 rgba(0,0,0,.15)}
#menuslide ul ul{-webkit-box-shadow:none;box-shadow:none;display:none;opacity:1;transform:translateY(0);transition:unset}
#menuslide ul ul li{background:0 0;margin:0}
#menuslide li:hover ul{transition-delay:0,0,0}
#menuslide ul li{width:100%;border-top:1px solid #2b2b2b;background:0 0;float:none;position:relative}
#menuslide ul li.active a,#menuslide ul li:hover a{color:#555}
#menuslide ul ul li a{padding:0 25px}
#menuslide ul li a,#menuslide ul ul li a{width:100%;border-bottom:0;color:#ffffff}
#menuslide ul li a:hover,#menuslide ul ul li a:hover{color:#eee}
#menuslide ul ul li.has-sub ul li a{padding-left:35px}
#menuslide ul ul,#menuslide ul ul ul{position:relative;left:0;width:100%;margin:0;text-align:left}
#menuslide ul li.has-sub a::after,#menuslide ul ul li.has-sub a::after{display:none}
#menuslide .submenu-button{position:absolute;z-index:99;right:0;top:0;cursor:pointer}
#menuslide .submenu-button::after{content:"\f0d7";font-family:"Font Awesome 5 Pro";font-style:normal;font-weight:900;text-decoration:inherit;margin:0 20px;color:#555;line-height:42px}
#menuslide .submenu-opened::after{content:"\f0d8"}
#menuslide ul ul .submenu-button::after{line-height:36px}
#menuslide ul ul ul li.active a{border-left:none}
#menuslide ul li.has-sub ul li.active a,#menuslide ul ul li.has-sub ul li.active a{border-top:none}
.ui_box{width:71%;height:auto;margin:0 auto}}
@media screen and (max-width:800px){.header-wrapper,.item .main-wrapper{width:100%}
#outer-wrapper{max-width:96%}
.headblog{margin:0 25px 0 0}
.halaman-indeks,.halaman-indeks:nth-child(12),.halaman-indeks:nth-child(16),.halaman-indeks:nth-child(19),.halaman-indeks:nth-child(2),.halaman-indeks:nth-child(23),.halaman-indeks:nth-child(24),.halaman-indeks:nth-child(25),.halaman-indeks:nth-child(29),.halaman-indeks:nth-child(6){width:100%;height:auto}
.halaman-indeks:nth-child(12).homebox,.halaman-indeks:nth-child(16).homebox,.halaman-indeks:nth-child(19).homebox,.halaman-indeks:nth-child(2).homebox,.halaman-indeks:nth-child(6).homebox{width:auto}
.halaman-indeks .post-image-wrap{height:auto}
.item .sidebar-wrapper{display:block;position:relative;top:initial;float:none;margin:0 auto;width:100%}
.item .sidebar-wrapper .widget{margin:15px 0}
#main-menu ul#main-menu-nav{padding-left:0}
.chiller-theme{background:#fff}}
@media screen and (max-width:768px){
.cd-headline{font-size:2.5rem}.boxwrap-text h3,.digital-wrapper h3,.recent-boxes h3{margin:0 auto;text-align:center}.boxwrap-text p{font-size:14px;text-align:center}a.more-link{top:15px;right:0;left:35%;margin:0 auto;position:relative}.font-big h2{font-size:36px!important;padding:0}.btn-mobile{right:10%}
.tabs ul li label span{display:none}
.tabs ul li label{padding:25px 15px}
.tabs ul li label i{font-size:23px}
.tabs input[name=tab-control]:nth-of-type(1):checked~ul>li:nth-child(1)>label.color1::after,.tabs input[name=tab-control]:nth-of-type(2):checked~ul>li:nth-child(2)>label.color2::after,.tabs input[name=tab-control]:nth-of-type(3):checked~ul>li:nth-child(3)>label.color3::after,.tabs input[name=tab-control]:nth-of-type(4):checked~ul>li:nth-child(4)>label.color4::after,.tabs input[name=tab-control]:nth-of-type(5):checked~ul>li:nth-child(5)>label.color5::after{left:37%;border-right:15px solid transparent;border-left:15px solid transparent;border-bottom:0 solid transparent}
.boxwrap-left,.boxwrap-right{width:100%;float:none;margin:0 auto;text-align:center}
.boxwrap-os-left h2,.boxwrap-text h2{font-size:30px}
.subs-wrapper{max-width:400px}}
@media screen and (max-width:600px){.tabs input[name=tab-control]:nth-of-type(1):checked~ul>li:nth-child(1)>label,.tabs input[name=tab-control]:nth-of-type(2):checked~ul>li:nth-child(2)>label,.tabs input[name=tab-control]:nth-of-type(3):checked~ul>li:nth-child(3)>label,.tabs input[name=tab-control]:nth-of-type(4):checked~ul>li:nth-child(4)>label{background:rgba(0,0,0,.08)}
.tabs .content{margin-top:20px}
.tabs .content section h3{display:block}
.related-post-style-3 .related-post-item-thumbnail{height:110px}}
@media screen and (max-width:480px){.headblog img{margin-top:14px;margin-left:10px;max-width:70%}
.headblog:before{width:320px}
#sticky-wrap.stickyhead .headblog img{margin-top:10px}
.tabs input[name=tab-control]:nth-of-type(1):checked~ul>li:nth-child(1)>label.color1::after,.tabs input[name=tab-control]:nth-of-type(2):checked~ul>li:nth-child(2)>label.color2::after,.tabs input[name=tab-control]:nth-of-type(3):checked~ul>li:nth-child(3)>label.color3::after,.tabs input[name=tab-control]:nth-of-type(4):checked~ul>li:nth-child(4)>label.color4::after,.tabs input[name=tab-control]:nth-of-type(5):checked~ul>li:nth-child(5)>label.color5::after{left:30%;border-right:15px solid transparent;border-left:15px solid transparent;border-bottom:0 solid transparent}
.tabs ul li label{padding:13px 15px}
.boxwrap-number{float:left;width:100%;margin-right:0;margin-bottom:20px}
.tabs .content section{padding:30px 20px}
.content-right>ul>li{display:block;width:100%;text-align:left;padding:0;margin-bottom:20px;-webkit-box-flex:initial;flex:auto}
.related-post-style-2 a.related-post-item-title{line-height:1.2em;font-size:100%!important;margin:0 0 5px}
.related-post-style-3 .related-post-item-thumbnail{height:75px}
.related-post-style-3 a.related-post-item-title{line-height:1.2em;font-size:95%!important;margin:0 auto 9px}
.related-post .related-post-item-summary,.related-post-style-3 span{font-size:90%}
.post-footer{text-align:center}
.post-footer .post-labels{margin:15px auto;float:none}
.post-share{margin:0 auto;float:none}
.post-share .share-links li{display:inline-block;margin:0}}
@media screen and (max-width: 414px){
.tabs input[name=tab-control]:nth-of-type(1):checked~ul>li:nth-child(1)>label.color1::after,.tabs input[name=tab-control]:nth-of-type(2):checked~ul>li:nth-child(2)>label.color2::after,.tabs input[name=tab-control]:nth-of-type(3):checked~ul>li:nth-child(3)>label.color3::after,.tabs input[name=tab-control]:nth-of-type(4):checked~ul>li:nth-child(4)>label.color4::after,.tabs input[name=tab-control]:nth-of-type(5):checked~ul>li:nth-child(5)>label.color5::after{left:26%;border-right:15px solid transparent;border-left:15px solid transparent;border-bottom:0 solid transparent}.boxwrap-text h3,.digital-wrapper h3,.recent-boxes h3{margin:0 auto;text-align:center}.digital-wrapper h3{font-size:25px}.box-left p,.wpbtn span{display:none}
}
@media screen and (max-width:360px){
.wpbtn a.btn-wite{padding:10px 20px}
.js-modal-video,.js-modal-video .overlay-box span{display:inline-block;height:47px;width:47px;line-height:47px;text-align:center}
.boxcontent{padding-top:0}
.tabs ul li{-webkit-box-flex:1;flex:initial;width:100%;padding:4px;text-align:center}
.tabs input[name=tab-control]:nth-of-type(1):checked~ul>li:nth-child(1)>label.color1::after,.tabs input[name=tab-control]:nth-of-type(2):checked~ul>li:nth-child(2)>label.color2::after,.tabs input[name=tab-control]:nth-of-type(3):checked~ul>li:nth-child(3)>label.color3::after,.tabs input[name=tab-control]:nth-of-type(4):checked~ul>li:nth-child(4)>label.color4::after,.tabs input[name=tab-control]:nth-of-type(5):checked~ul>li:nth-child(5)>label.color5::after{display:none}
.boxwrap-os-left h2,.boxwrap-text h2{font-size:25px}
.subs-wrapper{max-width:100%;margin:0 auto;padding:0}
}
@media screen and (max-width:320px){.related-post-style-1 li a{line-height:1.2em}
.related-post-style-3{margin:0 auto!important}
.related-post-style-3 li{margin:0 auto 20px!important;padding:0;width:100%;float:none}
.related-post-style-3 li img{display:flex;align-items:center}
.related-post-style-3 .related-post-item-thumbnail{height:auto;margin:0 auto 8px}
.related-post-style-3 a.related-post-item-title{line-height:1.3em;font-size:100%!important}}
]]></b:skin>
<b:if cond='data:view.isLayoutMode'>
<b:template-skin>
<![CDATA[
body#layout{max-width:800px;border:none;padding:0;position:relative}body#layout .header-wrapper{position:relative;width:100%;margin:0 auto}body#layout #top-bar{overflow:hidden;margin:0;height:auto;padding-left:0}body#layout .top-bar-nav,body#layout .top-bar-social{display:block}body#layout .top-bar-nav{width:60%}body#layout .top-bar-social{width:30%;display:block}body#layout .boxhome{height:auto}body#layout .headblog{width:280px}body#layout .boxmarket,body#layout .boxwrap,body#layout .recent-warpper,body#layout .statiswrap{overflow:hidden;padding:0}body#layout .menu{float:right;width:60%}body#layout .sidebar-wrapper{width:38%;float:right}body#layout .main-wrapper{width:62%;float:left}body#layout .boxwrap-left,body#layout .boxwrap-right{width:50%;overflow:hidden}body#layout .boxwrap-left{float:left},body#layout .boxwrap-right{float:right}body#layout .section h4{font-weight:400;padding:10px;margin:0;background:#4c5ef9;color:#fff;text-align:center;font-size:1em;line-height:1em}body#layout div.section{background-color:transparent;border:0}body#layout .widget-content{-webkit-box-shadow:rgba(0,0,0,.12) 0 0 6px 0,rgba(0,0,0,.24) 0 6px 6px 0;box-shadow:0 0 6px 0 rgba(0,0,0,.12),0 6px 6px 0 rgba(0,0,0,.24)}body#layout .add_widget a,body#layout div.layout-title,body#layout div.layout-widget-description{font-size:1em}body#layout #related-posts-widget{visibility:visible!important;display:block!important;padding:10px;margin:0 20px;background-color:#dbe3e4;box-sizing:border-box}body#layout #related-posts-widget:before,body#layout .notex:after,body#layout .notex:before{color:#4a866d;background-color:#f7f7f7;display:block;text-align:center;margin:0 5px 13px;padding:10px;box-sizing:border-box;font-size:16px;font-weight:400}body#layout #related-posts-widget:before{content:'The number for the numPosts code is "1 - whatever"'}body#layout .notex:before{content:'The number for the Style widget code is "1, 2, or 3"'}body#layout .notex:after{content:'The number for the Length code is "0 - whatever". (special style 2)'}body#layout #related-posts-widget .section>h4{margin-left:0!important}#layout #related-post-set-desktop{background:#c7d6d8!important;border:none!important}#layout #related-post-set-mobile{background:#cdd1d2!important;border:none!important}body#layout .footer-box .footer{float:left;width:21%;margin:0}body#layout #template-option{width:48%}body#layout #template-option h4{background:#ffc400}body#layout #template-option div.widget{margin-top:0}body#layout #template-option div.widget .widget-content{padding:8px 16px}
body#layout .iconsearch-label {display:none;}
]]></b:template-skin>
</b:if>
<b:defaultmarkups>
<b:defaultmarkup type='Common'>
<b:includable id='widget-title'>
      <b:if cond='data:defaultTitle or data:title'>
        <div class='widget-title'>
          <h3 class='title'>
            <data:title/>
          </h3>
        </div>
      </b:if>
    </b:includable> 
<b:includable id='translate'>
      <b:switch var='data:blog.locale.language'>
        <b:case value='en'/><b:include name='customLang'/>
        <b:default/><b:include name='customLang'/>
      </b:switch>
    </b:includable> 
<b:includable id='customLang'>
    <b:switch var='data:message'>
        <b:case value='prevPost'/>
        <b:if cond='data:blog.locale.language == &quot;en&quot;'>Previous Post<b:else/><data:messages.newer/></b:if>
        <b:case value='nextPost'/>
        <b:if cond='data:blog.locale.language == &quot;en&quot;'>Next Post<b:else/><data:messages.older/></b:if>
        <b:case value='loadMorePosts'/>
        <b:if cond='data:blog.locale.language == &quot;en&quot;'>Load More<b:else/><data:messages.loadMorePosts/></b:if>
        <b:case value='noMorePosts'/>
        <b:if cond='data:blog.locale.language == &quot;en&quot;'>That is All<b:else/><data:messages.noResultsFound/></b:if>
    </b:switch>
</b:includable> 
<b:includable id='btnmenu'>
<div class='btnmenu' onclick='toggleMenu()'>
<div class='top-bun'/>
<div class='meat'/>
<div class='bottom-bun'/>
</div>
</b:includable>
<b:includable id='searchdesktop'>
                <label class='iconsearch-label btn-dekstop' for='search-terms'>
                  <i class='far fa-search'/><span>Buscar</span></label>
            </b:includable>
<b:includable id='searchmobile'>
                <label class='iconsearch-label btn-mobile' for='search-terms'>
                  <i class='far fa-search'/><span>Buscar</span></label>
            </b:includable>
<b:includable id='searchFormContainer'>
                <div id='searchcontainer'>
                    <form expr:action='data:blog.searchUrl' id='search'>
                        <input autocomplete='off' expr:aria-label='data:messages.searchThisBlog' expr:placeholder='data:messages.searchThisBlog' expr:value='data:view.isSearch ? data:view.search.query.escaped : &quot;&quot;' id='search-terms' name='q' tabindex='-1' type='text'/>
                    </form>
                </div>
            </b:includable>
<b:includable id='fontstyle'>
<style>
@font-face {
  font-family: &#39;Playball&#39;;
  font-style: normal;
  font-weight: 400;
  font-display: swap;
  src: local(&#39;Playball&#39;), local(&#39;Playball-Regular&#39;), url(https://fonts.gstatic.com/s/playball/v9/TK3gWksYAxQ7jbsKcj8Al-1PKw.woff) format(&#39;woff&#39;);
}
@font-face {
  font-family: &#39;Poppins&#39;;
  font-style: italic;
  font-weight: 400;
  src: local(&#39;Poppins Italic&#39;), local(&#39;Poppins-Italic&#39;), url(https://fonts.gstatic.com/s/poppins/v9/pxiGyp8kv8JHgFVrJJLucHtGOvWDSA.woff) format(&#39;woff&#39;);
font-display: swap;
}
@font-face {
  font-family: &#39;Poppins&#39;;
  font-style: italic;
  font-weight: 500;
  src: local(&#39;Poppins Medium Italic&#39;), local(&#39;Poppins-MediumItalic&#39;), url(https://fonts.gstatic.com/s/poppins/v9/pxiDyp8kv8JHgFVrJJLmg1hVF9eIYktMqg.woff) format(&#39;woff&#39;);
font-display: swap;
}
@font-face {
  font-family: &#39;Poppins&#39;;
  font-style: italic;
  font-weight: 600;
  src: local(&#39;Poppins SemiBold Italic&#39;), local(&#39;Poppins-SemiBoldItalic&#39;), url(https://fonts.gstatic.com/s/poppins/v9/pxiDyp8kv8JHgFVrJJLmr19VF9eIYktMqg.woff) format(&#39;woff&#39;);
font-display: swap;
}
@font-face {
  font-family: &#39;Poppins&#39;;
  font-style: italic;
  font-weight: 700;
  src: local(&#39;Poppins Bold Italic&#39;), local(&#39;Poppins-BoldItalic&#39;), url(https://fonts.gstatic.com/s/poppins/v9/pxiDyp8kv8JHgFVrJJLmy15VF9eIYktMqg.woff) format(&#39;woff&#39;);
font-display: swap;
}
@font-face {
  font-family: &#39;Poppins&#39;;
  font-style: normal;
  font-weight: 400;
  src: local(&#39;Poppins Regular&#39;), local(&#39;Poppins-Regular&#39;), url(https://fonts.gstatic.com/s/poppins/v9/pxiEyp8kv8JHgFVrJJfedHFHGPc.woff) format(&#39;woff&#39;);
font-display: swap;
}
@font-face {
  font-family: &#39;Poppins&#39;;
  font-style: normal;
  font-weight: 500;
  src: local(&#39;Poppins Medium&#39;), local(&#39;Poppins-Medium&#39;), url(https://fonts.gstatic.com/s/poppins/v9/pxiByp8kv8JHgFVrLGT9Z1xlE92JQEk.woff) format(&#39;woff&#39;);
font-display: swap;
}
@font-face {
  font-family: &#39;Poppins&#39;;
  font-style: normal;
  font-weight: 600;
  src: local(&#39;Poppins SemiBold&#39;), local(&#39;Poppins-SemiBold&#39;), url(https://fonts.gstatic.com/s/poppins/v9/pxiByp8kv8JHgFVrLEj6Z1xlE92JQEk.woff) format(&#39;woff&#39;);
font-display: swap;
}
@font-face {
  font-family: &#39;Poppins&#39;;
  font-style: normal;
  font-weight: 700;
  src: local(&#39;Poppins Bold&#39;), local(&#39;Poppins-Bold&#39;), url(https://fonts.gstatic.com/s/poppins/v9/pxiByp8kv8JHgFVrLCz7Z1xlE92JQEk.woff) format(&#39;woff&#39;);
font-display: swap;
}
</style>
<script>
//<![CDATA[
"use strict";function loadCSS(e,t,o){"use strict";var i=window.document.createElement("link"),s=t||window.document.getElementsByTagName("script")[0];i.rel="stylesheet",i.href=e,i.media="only x",s.parentNode.insertBefore(i,s),setTimeout(function(){i.media=o||"all"})}loadCSS("https://kit-pro.fontawesome.com/releases/v5.13.0/css/pro.min.css");
//]]>
</script>
</b:includable>
<b:includable id='jsall'>
<script>
//<![CDATA[
/*! jQuery v2.1.3 | (c) 2005, 2014 jQuery Foundation, Inc. | jquery.org/license */
!function(a,b){"object"==typeof module&&"object"==typeof module.exports?module.exports=a.document?b(a,!0):function(a){if(!a.document)throw new Error("jQuery requires a window with a document");return b(a)}:b(a)}("undefined"!=typeof window?window:this,function(a,b){var c=[],d=c.slice,e=c.concat,f=c.push,g=c.indexOf,h={},i=h.toString,j=h.hasOwnProperty,k={},l=a.document,m="2.1.3",n=function(a,b){return new n.fn.init(a,b)},o=/^[\s\uFEFF\xA0]+|[\s\uFEFF\xA0]+$/g,p=/^-ms-/,q=/-([\da-z])/gi,r=function(a,b){return b.toUpperCase()};n.fn=n.prototype={jquery:m,constructor:n,selector:"",length:0,toArray:function(){return d.call(this)},get:function(a){return null!=a?0>a?this[a+this.length]:this[a]:d.call(this)},pushStack:function(a){var b=n.merge(this.constructor(),a);return b.prevObject=this,b.context=this.context,b},each:function(a,b){return n.each(this,a,b)},map:function(a){return this.pushStack(n.map(this,function(b,c){return a.call(b,c,b)}))},slice:function(){return this.pushStack(d.apply(this,arguments))},first:function(){return this.eq(0)},last:function(){return this.eq(-1)},eq:function(a){var b=this.length,c=+a+(0>a?b:0);return this.pushStack(c>=0&&b>c?[this[c]]:[])},end:function(){return this.prevObject||this.constructor(null)},push:f,sort:c.sort,splice:c.splice},n.extend=n.fn.extend=function(){var a,b,c,d,e,f,g=arguments[0]||{},h=1,i=arguments.length,j=!1;for("boolean"==typeof g&&(j=g,g=arguments[h]||{},h++),"object"==typeof g||n.isFunction(g)||(g={}),h===i&&(g=this,h--);i>h;h++)if(null!=(a=arguments[h]))for(b in a)c=g[b],d=a[b],g!==d&&(j&&d&&(n.isPlainObject(d)||(e=n.isArray(d)))?(e?(e=!1,f=c&&n.isArray(c)?c:[]):f=c&&n.isPlainObject(c)?c:{},g[b]=n.extend(j,f,d)):void 0!==d&&(g[b]=d));return g},n.extend({expando:"jQuery"+(m+Math.random()).replace(/\D/g,""),isReady:!0,error:function(a){throw new Error(a)},noop:function(){},isFunction:function(a){return"function"===n.type(a)},isArray:Array.isArray,isWindow:function(a){return null!=a&&a===a.window},isNumeric:function(a){return!n.isArray(a)&&a-parseFloat(a)+1>=0},isPlainObject:function(a){return"object"!==n.type(a)||a.nodeType||n.isWindow(a)?!1:a.constructor&&!j.call(a.constructor.prototype,"isPrototypeOf")?!1:!0},isEmptyObject:function(a){var b;for(b in a)return!1;return!0},type:function(a){return null==a?a+"":"object"==typeof a||"function"==typeof a?h[i.call(a)]||"object":typeof a},globalEval:function(a){var b,c=eval;a=n.trim(a),a&&(1===a.indexOf("use strict")?(b=l.createElement("script"),b.text=a,l.head.appendChild(b).parentNode.removeChild(b)):c(a))},camelCase:function(a){return a.replace(p,"ms-").replace(q,r)},nodeName:function(a,b){return a.nodeName&&a.nodeName.toLowerCase()===b.toLowerCase()},each:function(a,b,c){var d,e=0,f=a.length,g=s(a);if(c){if(g){for(;f>e;e++)if(d=b.apply(a[e],c),d===!1)break}else for(e in a)if(d=b.apply(a[e],c),d===!1)break}else if(g){for(;f>e;e++)if(d=b.call(a[e],e,a[e]),d===!1)break}else for(e in a)if(d=b.call(a[e],e,a[e]),d===!1)break;return a},trim:function(a){return null==a?"":(a+"").replace(o,"")},makeArray:function(a,b){var c=b||[];return null!=a&&(s(Object(a))?n.merge(c,"string"==typeof a?[a]:a):f.call(c,a)),c},inArray:function(a,b,c){return null==b?-1:g.call(b,a,c)},merge:function(a,b){for(var c=+b.length,d=0,e=a.length;c>d;d++)a[e++]=b[d];return a.length=e,a},grep:function(a,b,c){for(var d,e=[],f=0,g=a.length,h=!c;g>f;f++)d=!b(a[f],f),d!==h&&e.push(a[f]);return e},map:function(a,b,c){var d,f=0,g=a.length,h=s(a),i=[];if(h)for(;g>f;f++)d=b(a[f],f,c),null!=d&&i.push(d);else for(f in a)d=b(a[f],f,c),null!=d&&i.push(d);return e.apply([],i)},guid:1,proxy:function(a,b){var c,e,f;return"string"==typeof b&&(c=a[b],b=a,a=c),n.isFunction(a)?(e=d.call(arguments,2),f=function(){return a.apply(b||this,e.concat(d.call(arguments)))},f.guid=a.guid=a.guid||n.guid++,f):void 0},now:Date.now,support:k}),n.each("Boolean Number String Function Array Date RegExp Object Error".split(" "),function(a,b){h["[object "+b+"]"]=b.toLowerCase()});function s(a){var b=a.length,c=n.type(a);return"function"===c||n.isWindow(a)?!1:1===a.nodeType&&b?!0:"array"===c||0===b||"number"==typeof b&&b>0&&b-1 in a}var t=function(a){var b,c,d,e,f,g,h,i,j,k,l,m,n,o,p,q,r,s,t,u="sizzle"+1*new Date,v=a.document,w=0,x=0,y=hb(),z=hb(),A=hb(),B=function(a,b){return a===b&&(l=!0),0},C=1<<31,D={}.hasOwnProperty,E=[],F=E.pop,G=E.push,H=E.push,I=E.slice,J=function(a,b){for(var c=0,d=a.length;d>c;c++)if(a[c]===b)return c;return-1},K="checked|selected|async|autofocus|autoplay|controls|defer|disabled|hidden|ismap|loop|multiple|open|readonly|required|scoped",L="[\\x20\\t\\r\\n\\f]",M="(?:\\\\.|[\\w-]|[^\\x00-\\xa0])+",N=M.replace("w","w#"),O="\\["+L+"*("+M+")(?:"+L+"*([*^$|!~]?=)"+L+"*(?:'((?:\\\\.|[^\\\\'])*)'|\"((?:\\\\.|[^\\\\\"])*)\"|("+N+"))|)"+L+"*\\]",P=":("+M+")(?:\\((('((?:\\\\.|[^\\\\'])*)'|\"((?:\\\\.|[^\\\\\"])*)\")|((?:\\\\.|[^\\\\()[\\]]|"+O+")*)|.*)\\)|)",Q=new RegExp(L+"+","g"),R=new RegExp("^"+L+"+|((?:^|[^\\\\])(?:\\\\.)*)"+L+"+$","g"),S=new RegExp("^"+L+"*,"+L+"*"),T=new RegExp("^"+L+"*([>+~]|"+L+")"+L+"*"),U=new RegExp("="+L+"*([^\\]'\"]*?)"+L+"*\\]","g"),V=new RegExp(P),W=new RegExp("^"+N+"$"),X={ID:new RegExp("^#("+M+")"),CLASS:new RegExp("^\\.("+M+")"),TAG:new RegExp("^("+M.replace("w","w*")+")"),ATTR:new RegExp("^"+O),PSEUDO:new RegExp("^"+P),CHILD:new RegExp("^:(only|first|last|nth|nth-last)-(child|of-type)(?:\\("+L+"*(even|odd|(([+-]|)(\\d*)n|)"+L+"*(?:([+-]|)"+L+"*(\\d+)|))"+L+"*\\)|)","i"),bool:new RegExp("^(?:"+K+")$","i"),needsContext:new RegExp("^"+L+"*[>+~]|:(even|odd|eq|gt|lt|nth|first|last)(?:\\("+L+"*((?:-\\d)?\\d*)"+L+"*\\)|)(?=[^-]|$)","i")},Y=/^(?:input|select|textarea|button)$/i,Z=/^h\d$/i,$=/^[^{]+\{\s*\[native \w/,_=/^(?:#([\w-]+)|(\w+)|\.([\w-]+))$/,ab=/[+~]/,bb=/'|\\/g,cb=new RegExp("\\\\([\\da-f]{1,6}"+L+"?|("+L+")|.)","ig"),db=function(a,b,c){var d="0x"+b-65536;return d!==d||c?b:0>d?String.fromCharCode(d+65536):String.fromCharCode(d>>10|55296,1023&d|56320)},eb=function(){m()};try{H.apply(E=I.call(v.childNodes),v.childNodes),E[v.childNodes.length].nodeType}catch(fb){H={apply:E.length?function(a,b){G.apply(a,I.call(b))}:function(a,b){var c=a.length,d=0;while(a[c++]=b[d++]);a.length=c-1}}}function gb(a,b,d,e){var f,h,j,k,l,o,r,s,w,x;if((b?b.ownerDocument||b:v)!==n&&m(b),b=b||n,d=d||[],k=b.nodeType,"string"!=typeof a||!a||1!==k&&9!==k&&11!==k)return d;if(!e&&p){if(11!==k&&(f=_.exec(a)))if(j=f[1]){if(9===k){if(h=b.getElementById(j),!h||!h.parentNode)return d;if(h.id===j)return d.push(h),d}else if(b.ownerDocument&&(h=b.ownerDocument.getElementById(j))&&t(b,h)&&h.id===j)return d.push(h),d}else{if(f[2])return H.apply(d,b.getElementsByTagName(a)),d;if((j=f[3])&&c.getElementsByClassName)return H.apply(d,b.getElementsByClassName(j)),d}if(c.qsa&&(!q||!q.test(a))){if(s=r=u,w=b,x=1!==k&&a,1===k&&"object"!==b.nodeName.toLowerCase()){o=g(a),(r=b.getAttribute("id"))?s=r.replace(bb,"\\$&"):b.setAttribute("id",s),s="[id='"+s+"'] ",l=o.length;while(l--)o[l]=s+rb(o[l]);w=ab.test(a)&&pb(b.parentNode)||b,x=o.join(",")}if(x)try{return H.apply(d,w.querySelectorAll(x)),d}catch(y){}finally{r||b.removeAttribute("id")}}}return i(a.replace(R,"$1"),b,d,e)}function hb(){var a=[];function b(c,e){return a.push(c+" ")>d.cacheLength&&delete b[a.shift()],b[c+" "]=e}return b}function ib(a){return a[u]=!0,a}function jb(a){var b=n.createElement("div");try{return!!a(b)}catch(c){return!1}finally{b.parentNode&&b.parentNode.removeChild(b),b=null}}function kb(a,b){var c=a.split("|"),e=a.length;while(e--)d.attrHandle[c[e]]=b}function lb(a,b){var c=b&&a,d=c&&1===a.nodeType&&1===b.nodeType&&(~b.sourceIndex||C)-(~a.sourceIndex||C);if(d)return d;if(c)while(c=c.nextSibling)if(c===b)return-1;return a?1:-1}function mb(a){return function(b){var c=b.nodeName.toLowerCase();return"input"===c&&b.type===a}}function nb(a){return function(b){var c=b.nodeName.toLowerCase();return("input"===c||"button"===c)&&b.type===a}}function ob(a){return ib(function(b){return b=+b,ib(function(c,d){var e,f=a([],c.length,b),g=f.length;while(g--)c[e=f[g]]&&(c[e]=!(d[e]=c[e]))})})}function pb(a){return a&&"undefined"!=typeof a.getElementsByTagName&&a}c=gb.support={},f=gb.isXML=function(a){var b=a&&(a.ownerDocument||a).documentElement;return b?"HTML"!==b.nodeName:!1},m=gb.setDocument=function(a){var b,e,g=a?a.ownerDocument||a:v;return g!==n&&9===g.nodeType&&g.documentElement?(n=g,o=g.documentElement,e=g.defaultView,e&&e!==e.top&&(e.addEventListener?e.addEventListener("unload",eb,!1):e.attachEvent&&e.attachEvent("onunload",eb)),p=!f(g),c.attributes=jb(function(a){return a.className="i",!a.getAttribute("className")}),c.getElementsByTagName=jb(function(a){return a.appendChild(g.createComment("")),!a.getElementsByTagName("*").length}),c.getElementsByClassName=$.test(g.getElementsByClassName),c.getById=jb(function(a){return o.appendChild(a).id=u,!g.getElementsByName||!g.getElementsByName(u).length}),c.getById?(d.find.ID=function(a,b){if("undefined"!=typeof b.getElementById&&p){var c=b.getElementById(a);return c&&c.parentNode?[c]:[]}},d.filter.ID=function(a){var b=a.replace(cb,db);return function(a){return a.getAttribute("id")===b}}):(delete d.find.ID,d.filter.ID=function(a){var b=a.replace(cb,db);return function(a){var c="undefined"!=typeof a.getAttributeNode&&a.getAttributeNode("id");return c&&c.value===b}}),d.find.TAG=c.getElementsByTagName?function(a,b){return"undefined"!=typeof b.getElementsByTagName?b.getElementsByTagName(a):c.qsa?b.querySelectorAll(a):void 0}:function(a,b){var c,d=[],e=0,f=b.getElementsByTagName(a);if("*"===a){while(c=f[e++])1===c.nodeType&&d.push(c);return d}return f},d.find.CLASS=c.getElementsByClassName&&function(a,b){return p?b.getElementsByClassName(a):void 0},r=[],q=[],(c.qsa=$.test(g.querySelectorAll))&&(jb(function(a){o.appendChild(a).innerHTML="<a id='"+u+"'></a><select id='"+u+"-\f]' msallowcapture=''><option selected=''></option></select>",a.querySelectorAll("[msallowcapture^='']").length&&q.push("[*^$]="+L+"*(?:''|\"\")"),a.querySelectorAll("[selected]").length||q.push("\\["+L+"*(?:value|"+K+")"),a.querySelectorAll("[id~="+u+"-]").length||q.push("~="),a.querySelectorAll(":checked").length||q.push(":checked"),a.querySelectorAll("a#"+u+"+*").length||q.push(".#.+[+~]")}),jb(function(a){var b=g.createElement("input");b.setAttribute("type","hidden"),a.appendChild(b).setAttribute("name","D"),a.querySelectorAll("[name=d]").length&&q.push("name"+L+"*[*^$|!~]?="),a.querySelectorAll(":enabled").length||q.push(":enabled",":disabled"),a.querySelectorAll("*,:x"),q.push(",.*:")})),(c.matchesSelector=$.test(s=o.matches||o.webkitMatchesSelector||o.mozMatchesSelector||o.oMatchesSelector||o.msMatchesSelector))&&jb(function(a){c.disconnectedMatch=s.call(a,"div"),s.call(a,"[s!='']:x"),r.push("!=",P)}),q=q.length&&new RegExp(q.join("|")),r=r.length&&new RegExp(r.join("|")),b=$.test(o.compareDocumentPosition),t=b||$.test(o.contains)?function(a,b){var c=9===a.nodeType?a.documentElement:a,d=b&&b.parentNode;return a===d||!(!d||1!==d.nodeType||!(c.contains?c.contains(d):a.compareDocumentPosition&&16&a.compareDocumentPosition(d)))}:function(a,b){if(b)while(b=b.parentNode)if(b===a)return!0;return!1},B=b?function(a,b){if(a===b)return l=!0,0;var d=!a.compareDocumentPosition-!b.compareDocumentPosition;return d?d:(d=(a.ownerDocument||a)===(b.ownerDocument||b)?a.compareDocumentPosition(b):1,1&d||!c.sortDetached&&b.compareDocumentPosition(a)===d?a===g||a.ownerDocument===v&&t(v,a)?-1:b===g||b.ownerDocument===v&&t(v,b)?1:k?J(k,a)-J(k,b):0:4&d?-1:1)}:function(a,b){if(a===b)return l=!0,0;var c,d=0,e=a.parentNode,f=b.parentNode,h=[a],i=[b];if(!e||!f)return a===g?-1:b===g?1:e?-1:f?1:k?J(k,a)-J(k,b):0;if(e===f)return lb(a,b);c=a;while(c=c.parentNode)h.unshift(c);c=b;while(c=c.parentNode)i.unshift(c);while(h[d]===i[d])d++;return d?lb(h[d],i[d]):h[d]===v?-1:i[d]===v?1:0},g):n},gb.matches=function(a,b){return gb(a,null,null,b)},gb.matchesSelector=function(a,b){if((a.ownerDocument||a)!==n&&m(a),b=b.replace(U,"='$1']"),!(!c.matchesSelector||!p||r&&r.test(b)||q&&q.test(b)))try{var d=s.call(a,b);if(d||c.disconnectedMatch||a.document&&11!==a.document.nodeType)return d}catch(e){}return gb(b,n,null,[a]).length>0},gb.contains=function(a,b){return(a.ownerDocument||a)!==n&&m(a),t(a,b)},gb.attr=function(a,b){(a.ownerDocument||a)!==n&&m(a);var e=d.attrHandle[b.toLowerCase()],f=e&&D.call(d.attrHandle,b.toLowerCase())?e(a,b,!p):void 0;return void 0!==f?f:c.attributes||!p?a.getAttribute(b):(f=a.getAttributeNode(b))&&f.specified?f.value:null},gb.error=function(a){throw new Error("Syntax error, unrecognized expression: "+a)},gb.uniqueSort=function(a){var b,d=[],e=0,f=0;if(l=!c.detectDuplicates,k=!c.sortStable&&a.slice(0),a.sort(B),l){while(b=a[f++])b===a[f]&&(e=d.push(f));while(e--)a.splice(d[e],1)}return k=null,a},e=gb.getText=function(a){var b,c="",d=0,f=a.nodeType;if(f){if(1===f||9===f||11===f){if("string"==typeof a.textContent)return a.textContent;for(a=a.firstChild;a;a=a.nextSibling)c+=e(a)}else if(3===f||4===f)return a.nodeValue}else while(b=a[d++])c+=e(b);return c},d=gb.selectors={cacheLength:50,createPseudo:ib,match:X,attrHandle:{},find:{},relative:{">":{dir:"parentNode",first:!0}," ":{dir:"parentNode"},"+":{dir:"previousSibling",first:!0},"~":{dir:"previousSibling"}},preFilter:{ATTR:function(a){return a[1]=a[1].replace(cb,db),a[3]=(a[3]||a[4]||a[5]||"").replace(cb,db),"~="===a[2]&&(a[3]=" "+a[3]+" "),a.slice(0,4)},CHILD:function(a){return a[1]=a[1].toLowerCase(),"nth"===a[1].slice(0,3)?(a[3]||gb.error(a[0]),a[4]=+(a[4]?a[5]+(a[6]||1):2*("even"===a[3]||"odd"===a[3])),a[5]=+(a[7]+a[8]||"odd"===a[3])):a[3]&&gb.error(a[0]),a},PSEUDO:function(a){var b,c=!a[6]&&a[2];return X.CHILD.test(a[0])?null:(a[3]?a[2]=a[4]||a[5]||"":c&&V.test(c)&&(b=g(c,!0))&&(b=c.indexOf(")",c.length-b)-c.length)&&(a[0]=a[0].slice(0,b),a[2]=c.slice(0,b)),a.slice(0,3))}},filter:{TAG:function(a){var b=a.replace(cb,db).toLowerCase();return"*"===a?function(){return!0}:function(a){return a.nodeName&&a.nodeName.toLowerCase()===b}},CLASS:function(a){var b=y[a+" "];return b||(b=new RegExp("(^|"+L+")"+a+"("+L+"|$)"))&&y(a,function(a){return b.test("string"==typeof a.className&&a.className||"undefined"!=typeof a.getAttribute&&a.getAttribute("class")||"")})},ATTR:function(a,b,c){return function(d){var e=gb.attr(d,a);return null==e?"!="===b:b?(e+="","="===b?e===c:"!="===b?e!==c:"^="===b?c&&0===e.indexOf(c):"*="===b?c&&e.indexOf(c)>-1:"$="===b?c&&e.slice(-c.length)===c:"~="===b?(" "+e.replace(Q," ")+" ").indexOf(c)>-1:"|="===b?e===c||e.slice(0,c.length+1)===c+"-":!1):!0}},CHILD:function(a,b,c,d,e){var f="nth"!==a.slice(0,3),g="last"!==a.slice(-4),h="of-type"===b;return 1===d&&0===e?function(a){return!!a.parentNode}:function(b,c,i){var j,k,l,m,n,o,p=f!==g?"nextSibling":"previousSibling",q=b.parentNode,r=h&&b.nodeName.toLowerCase(),s=!i&&!h;if(q){if(f){while(p){l=b;while(l=l[p])if(h?l.nodeName.toLowerCase()===r:1===l.nodeType)return!1;o=p="only"===a&&!o&&"nextSibling"}return!0}if(o=[g?q.firstChild:q.lastChild],g&&s){k=q[u]||(q[u]={}),j=k[a]||[],n=j[0]===w&&j[1],m=j[0]===w&&j[2],l=n&&q.childNodes[n];while(l=++n&&l&&l[p]||(m=n=0)||o.pop())if(1===l.nodeType&&++m&&l===b){k[a]=[w,n,m];break}}else if(s&&(j=(b[u]||(b[u]={}))[a])&&j[0]===w)m=j[1];else while(l=++n&&l&&l[p]||(m=n=0)||o.pop())if((h?l.nodeName.toLowerCase()===r:1===l.nodeType)&&++m&&(s&&((l[u]||(l[u]={}))[a]=[w,m]),l===b))break;return m-=e,m===d||m%d===0&&m/d>=0}}},PSEUDO:function(a,b){var c,e=d.pseudos[a]||d.setFilters[a.toLowerCase()]||gb.error("unsupported pseudo: "+a);return e[u]?e(b):e.length>1?(c=[a,a,"",b],d.setFilters.hasOwnProperty(a.toLowerCase())?ib(function(a,c){var d,f=e(a,b),g=f.length;while(g--)d=J(a,f[g]),a[d]=!(c[d]=f[g])}):function(a){return e(a,0,c)}):e}},pseudos:{not:ib(function(a){var b=[],c=[],d=h(a.replace(R,"$1"));return d[u]?ib(function(a,b,c,e){var f,g=d(a,null,e,[]),h=a.length;while(h--)(f=g[h])&&(a[h]=!(b[h]=f))}):function(a,e,f){return b[0]=a,d(b,null,f,c),b[0]=null,!c.pop()}}),has:ib(function(a){return function(b){return gb(a,b).length>0}}),contains:ib(function(a){return a=a.replace(cb,db),function(b){return(b.textContent||b.innerText||e(b)).indexOf(a)>-1}}),lang:ib(function(a){return W.test(a||"")||gb.error("unsupported lang: "+a),a=a.replace(cb,db).toLowerCase(),function(b){var c;do if(c=p?b.lang:b.getAttribute("xml:lang")||b.getAttribute("lang"))return c=c.toLowerCase(),c===a||0===c.indexOf(a+"-");while((b=b.parentNode)&&1===b.nodeType);return!1}}),target:function(b){var c=a.location&&a.location.hash;return c&&c.slice(1)===b.id},root:function(a){return a===o},focus:function(a){return a===n.activeElement&&(!n.hasFocus||n.hasFocus())&&!!(a.type||a.href||~a.tabIndex)},enabled:function(a){return a.disabled===!1},disabled:function(a){return a.disabled===!0},checked:function(a){var b=a.nodeName.toLowerCase();return"input"===b&&!!a.checked||"option"===b&&!!a.selected},selected:function(a){return a.parentNode&&a.parentNode.selectedIndex,a.selected===!0},empty:function(a){for(a=a.firstChild;a;a=a.nextSibling)if(a.nodeType<6)return!1;return!0},parent:function(a){return!d.pseudos.empty(a)},header:function(a){return Z.test(a.nodeName)},input:function(a){return Y.test(a.nodeName)},button:function(a){var b=a.nodeName.toLowerCase();return"input"===b&&"button"===a.type||"button"===b},text:function(a){var b;return"input"===a.nodeName.toLowerCase()&&"text"===a.type&&(null==(b=a.getAttribute("type"))||"text"===b.toLowerCase())},first:ob(function(){return[0]}),last:ob(function(a,b){return[b-1]}),eq:ob(function(a,b,c){return[0>c?c+b:c]}),even:ob(function(a,b){for(var c=0;b>c;c+=2)a.push(c);return a}),odd:ob(function(a,b){for(var c=1;b>c;c+=2)a.push(c);return a}),lt:ob(function(a,b,c){for(var d=0>c?c+b:c;--d>=0;)a.push(d);return a}),gt:ob(function(a,b,c){for(var d=0>c?c+b:c;++d<b;)a.push(d);return a})}},d.pseudos.nth=d.pseudos.eq;for(b in{radio:!0,checkbox:!0,file:!0,password:!0,image:!0})d.pseudos[b]=mb(b);for(b in{submit:!0,reset:!0})d.pseudos[b]=nb(b);function qb(){}qb.prototype=d.filters=d.pseudos,d.setFilters=new qb,g=gb.tokenize=function(a,b){var c,e,f,g,h,i,j,k=z[a+" "];if(k)return b?0:k.slice(0);h=a,i=[],j=d.preFilter;while(h){(!c||(e=S.exec(h)))&&(e&&(h=h.slice(e[0].length)||h),i.push(f=[])),c=!1,(e=T.exec(h))&&(c=e.shift(),f.push({value:c,type:e[0].replace(R," ")}),h=h.slice(c.length));for(g in d.filter)!(e=X[g].exec(h))||j[g]&&!(e=j[g](e))||(c=e.shift(),f.push({value:c,type:g,matches:e}),h=h.slice(c.length));if(!c)break}return b?h.length:h?gb.error(a):z(a,i).slice(0)};function rb(a){for(var b=0,c=a.length,d="";c>b;b++)d+=a[b].value;return d}function sb(a,b,c){var d=b.dir,e=c&&"parentNode"===d,f=x++;return b.first?function(b,c,f){while(b=b[d])if(1===b.nodeType||e)return a(b,c,f)}:function(b,c,g){var h,i,j=[w,f];if(g){while(b=b[d])if((1===b.nodeType||e)&&a(b,c,g))return!0}else while(b=b[d])if(1===b.nodeType||e){if(i=b[u]||(b[u]={}),(h=i[d])&&h[0]===w&&h[1]===f)return j[2]=h[2];if(i[d]=j,j[2]=a(b,c,g))return!0}}}function tb(a){return a.length>1?function(b,c,d){var e=a.length;while(e--)if(!a[e](b,c,d))return!1;return!0}:a[0]}function ub(a,b,c){for(var d=0,e=b.length;e>d;d++)gb(a,b[d],c);return c}function vb(a,b,c,d,e){for(var f,g=[],h=0,i=a.length,j=null!=b;i>h;h++)(f=a[h])&&(!c||c(f,d,e))&&(g.push(f),j&&b.push(h));return g}function wb(a,b,c,d,e,f){return d&&!d[u]&&(d=wb(d)),e&&!e[u]&&(e=wb(e,f)),ib(function(f,g,h,i){var j,k,l,m=[],n=[],o=g.length,p=f||ub(b||"*",h.nodeType?[h]:h,[]),q=!a||!f&&b?p:vb(p,m,a,h,i),r=c?e||(f?a:o||d)?[]:g:q;if(c&&c(q,r,h,i),d){j=vb(r,n),d(j,[],h,i),k=j.length;while(k--)(l=j[k])&&(r[n[k]]=!(q[n[k]]=l))}if(f){if(e||a){if(e){j=[],k=r.length;while(k--)(l=r[k])&&j.push(q[k]=l);e(null,r=[],j,i)}k=r.length;while(k--)(l=r[k])&&(j=e?J(f,l):m[k])>-1&&(f[j]=!(g[j]=l))}}else r=vb(r===g?r.splice(o,r.length):r),e?e(null,g,r,i):H.apply(g,r)})}function xb(a){for(var b,c,e,f=a.length,g=d.relative[a[0].type],h=g||d.relative[" "],i=g?1:0,k=sb(function(a){return a===b},h,!0),l=sb(function(a){return J(b,a)>-1},h,!0),m=[function(a,c,d){var e=!g&&(d||c!==j)||((b=c).nodeType?k(a,c,d):l(a,c,d));return b=null,e}];f>i;i++)if(c=d.relative[a[i].type])m=[sb(tb(m),c)];else{if(c=d.filter[a[i].type].apply(null,a[i].matches),c[u]){for(e=++i;f>e;e++)if(d.relative[a[e].type])break;return wb(i>1&&tb(m),i>1&&rb(a.slice(0,i-1).concat({value:" "===a[i-2].type?"*":""})).replace(R,"$1"),c,e>i&&xb(a.slice(i,e)),f>e&&xb(a=a.slice(e)),f>e&&rb(a))}m.push(c)}return tb(m)}function yb(a,b){var c=b.length>0,e=a.length>0,f=function(f,g,h,i,k){var l,m,o,p=0,q="0",r=f&&[],s=[],t=j,u=f||e&&d.find.TAG("*",k),v=w+=null==t?1:Math.random()||.1,x=u.length;for(k&&(j=g!==n&&g);q!==x&&null!=(l=u[q]);q++){if(e&&l){m=0;while(o=a[m++])if(o(l,g,h)){i.push(l);break}k&&(w=v)}c&&((l=!o&&l)&&p--,f&&r.push(l))}if(p+=q,c&&q!==p){m=0;while(o=b[m++])o(r,s,g,h);if(f){if(p>0)while(q--)r[q]||s[q]||(s[q]=F.call(i));s=vb(s)}H.apply(i,s),k&&!f&&s.length>0&&p+b.length>1&&gb.uniqueSort(i)}return k&&(w=v,j=t),r};return c?ib(f):f}return h=gb.compile=function(a,b){var c,d=[],e=[],f=A[a+" "];if(!f){b||(b=g(a)),c=b.length;while(c--)f=xb(b[c]),f[u]?d.push(f):e.push(f);f=A(a,yb(e,d)),f.selector=a}return f},i=gb.select=function(a,b,e,f){var i,j,k,l,m,n="function"==typeof a&&a,o=!f&&g(a=n.selector||a);if(e=e||[],1===o.length){if(j=o[0]=o[0].slice(0),j.length>2&&"ID"===(k=j[0]).type&&c.getById&&9===b.nodeType&&p&&d.relative[j[1].type]){if(b=(d.find.ID(k.matches[0].replace(cb,db),b)||[])[0],!b)return e;n&&(b=b.parentNode),a=a.slice(j.shift().value.length)}i=X.needsContext.test(a)?0:j.length;while(i--){if(k=j[i],d.relative[l=k.type])break;if((m=d.find[l])&&(f=m(k.matches[0].replace(cb,db),ab.test(j[0].type)&&pb(b.parentNode)||b))){if(j.splice(i,1),a=f.length&&rb(j),!a)return H.apply(e,f),e;break}}}return(n||h(a,o))(f,b,!p,e,ab.test(a)&&pb(b.parentNode)||b),e},c.sortStable=u.split("").sort(B).join("")===u,c.detectDuplicates=!!l,m(),c.sortDetached=jb(function(a){return 1&a.compareDocumentPosition(n.createElement("div"))}),jb(function(a){return a.innerHTML="<a href='#'></a>","#"===a.firstChild.getAttribute("href")})||kb("type|href|height|width",function(a,b,c){return c?void 0:a.getAttribute(b,"type"===b.toLowerCase()?1:2)}),c.attributes&&jb(function(a){return a.innerHTML="<input/>",a.firstChild.setAttribute("value",""),""===a.firstChild.getAttribute("value")})||kb("value",function(a,b,c){return c||"input"!==a.nodeName.toLowerCase()?void 0:a.defaultValue}),jb(function(a){return null==a.getAttribute("disabled")})||kb(K,function(a,b,c){var d;return c?void 0:a[b]===!0?b.toLowerCase():(d=a.getAttributeNode(b))&&d.specified?d.value:null}),gb}(a);n.find=t,n.expr=t.selectors,n.expr[":"]=n.expr.pseudos,n.unique=t.uniqueSort,n.text=t.getText,n.isXMLDoc=t.isXML,n.contains=t.contains;var u=n.expr.match.needsContext,v=/^<(\w+)\s*\/?>(?:<\/\1>|)$/,w=/^.[^:#\[\.,]*$/;function x(a,b,c){if(n.isFunction(b))return n.grep(a,function(a,d){return!!b.call(a,d,a)!==c});if(b.nodeType)return n.grep(a,function(a){return a===b!==c});if("string"==typeof b){if(w.test(b))return n.filter(b,a,c);b=n.filter(b,a)}return n.grep(a,function(a){return g.call(b,a)>=0!==c})}n.filter=function(a,b,c){var d=b[0];return c&&(a=":not("+a+")"),1===b.length&&1===d.nodeType?n.find.matchesSelector(d,a)?[d]:[]:n.find.matches(a,n.grep(b,function(a){return 1===a.nodeType}))},n.fn.extend({find:function(a){var b,c=this.length,d=[],e=this;if("string"!=typeof a)return this.pushStack(n(a).filter(function(){for(b=0;c>b;b++)if(n.contains(e[b],this))return!0}));for(b=0;c>b;b++)n.find(a,e[b],d);return d=this.pushStack(c>1?n.unique(d):d),d.selector=this.selector?this.selector+" "+a:a,d},filter:function(a){return this.pushStack(x(this,a||[],!1))},not:function(a){return this.pushStack(x(this,a||[],!0))},is:function(a){return!!x(this,"string"==typeof a&&u.test(a)?n(a):a||[],!1).length}});var y,z=/^(?:\s*(<[\w\W]+>)[^>]*|#([\w-]*))$/,A=n.fn.init=function(a,b){var c,d;if(!a)return this;if("string"==typeof a){if(c="<"===a[0]&&">"===a[a.length-1]&&a.length>=3?[null,a,null]:z.exec(a),!c||!c[1]&&b)return!b||b.jquery?(b||y).find(a):this.constructor(b).find(a);if(c[1]){if(b=b instanceof n?b[0]:b,n.merge(this,n.parseHTML(c[1],b&&b.nodeType?b.ownerDocument||b:l,!0)),v.test(c[1])&&n.isPlainObject(b))for(c in b)n.isFunction(this[c])?this[c](b[c]):this.attr(c,b[c]);return this}return d=l.getElementById(c[2]),d&&d.parentNode&&(this.length=1,this[0]=d),this.context=l,this.selector=a,this}return a.nodeType?(this.context=this[0]=a,this.length=1,this):n.isFunction(a)?"undefined"!=typeof y.ready?y.ready(a):a(n):(void 0!==a.selector&&(this.selector=a.selector,this.context=a.context),n.makeArray(a,this))};A.prototype=n.fn,y=n(l);var B=/^(?:parents|prev(?:Until|All))/,C={children:!0,contents:!0,next:!0,prev:!0};n.extend({dir:function(a,b,c){var d=[],e=void 0!==c;while((a=a[b])&&9!==a.nodeType)if(1===a.nodeType){if(e&&n(a).is(c))break;d.push(a)}return d},sibling:function(a,b){for(var c=[];a;a=a.nextSibling)1===a.nodeType&&a!==b&&c.push(a);return c}}),n.fn.extend({has:function(a){var b=n(a,this),c=b.length;return this.filter(function(){for(var a=0;c>a;a++)if(n.contains(this,b[a]))return!0})},closest:function(a,b){for(var c,d=0,e=this.length,f=[],g=u.test(a)||"string"!=typeof a?n(a,b||this.context):0;e>d;d++)for(c=this[d];c&&c!==b;c=c.parentNode)if(c.nodeType<11&&(g?g.index(c)>-1:1===c.nodeType&&n.find.matchesSelector(c,a))){f.push(c);break}return this.pushStack(f.length>1?n.unique(f):f)},index:function(a){return a?"string"==typeof a?g.call(n(a),this[0]):g.call(this,a.jquery?a[0]:a):this[0]&&this[0].parentNode?this.first().prevAll().length:-1},add:function(a,b){return this.pushStack(n.unique(n.merge(this.get(),n(a,b))))},addBack:function(a){return this.add(null==a?this.prevObject:this.prevObject.filter(a))}});function D(a,b){while((a=a[b])&&1!==a.nodeType);return a}n.each({parent:function(a){var b=a.parentNode;return b&&11!==b.nodeType?b:null},parents:function(a){return n.dir(a,"parentNode")},parentsUntil:function(a,b,c){return n.dir(a,"parentNode",c)},next:function(a){return D(a,"nextSibling")},prev:function(a){return D(a,"previousSibling")},nextAll:function(a){return n.dir(a,"nextSibling")},prevAll:function(a){return n.dir(a,"previousSibling")},nextUntil:function(a,b,c){return n.dir(a,"nextSibling",c)},prevUntil:function(a,b,c){return n.dir(a,"previousSibling",c)},siblings:function(a){return n.sibling((a.parentNode||{}).firstChild,a)},children:function(a){return n.sibling(a.firstChild)},contents:function(a){return a.contentDocument||n.merge([],a.childNodes)}},function(a,b){n.fn[a]=function(c,d){var e=n.map(this,b,c);return"Until"!==a.slice(-5)&&(d=c),d&&"string"==typeof d&&(e=n.filter(d,e)),this.length>1&&(C[a]||n.unique(e),B.test(a)&&e.reverse()),this.pushStack(e)}});var E=/\S+/g,F={};function G(a){var b=F[a]={};return n.each(a.match(E)||[],function(a,c){b[c]=!0}),b}n.Callbacks=function(a){a="string"==typeof a?F[a]||G(a):n.extend({},a);var b,c,d,e,f,g,h=[],i=!a.once&&[],j=function(l){for(b=a.memory&&l,c=!0,g=e||0,e=0,f=h.length,d=!0;h&&f>g;g++)if(h[g].apply(l[0],l[1])===!1&&a.stopOnFalse){b=!1;break}d=!1,h&&(i?i.length&&j(i.shift()):b?h=[]:k.disable())},k={add:function(){if(h){var c=h.length;!function g(b){n.each(b,function(b,c){var d=n.type(c);"function"===d?a.unique&&k.has(c)||h.push(c):c&&c.length&&"string"!==d&&g(c)})}(arguments),d?f=h.length:b&&(e=c,j(b))}return this},remove:function(){return h&&n.each(arguments,function(a,b){var c;while((c=n.inArray(b,h,c))>-1)h.splice(c,1),d&&(f>=c&&f--,g>=c&&g--)}),this},has:function(a){return a?n.inArray(a,h)>-1:!(!h||!h.length)},empty:function(){return h=[],f=0,this},disable:function(){return h=i=b=void 0,this},disabled:function(){return!h},lock:function(){return i=void 0,b||k.disable(),this},locked:function(){return!i},fireWith:function(a,b){return!h||c&&!i||(b=b||[],b=[a,b.slice?b.slice():b],d?i.push(b):j(b)),this},fire:function(){return k.fireWith(this,arguments),this},fired:function(){return!!c}};return k},n.extend({Deferred:function(a){var b=[["resolve","done",n.Callbacks("once memory"),"resolved"],["reject","fail",n.Callbacks("once memory"),"rejected"],["notify","progress",n.Callbacks("memory")]],c="pending",d={state:function(){return c},always:function(){return e.done(arguments).fail(arguments),this},then:function(){var a=arguments;return n.Deferred(function(c){n.each(b,function(b,f){var g=n.isFunction(a[b])&&a[b];e[f[1]](function(){var a=g&&g.apply(this,arguments);a&&n.isFunction(a.promise)?a.promise().done(c.resolve).fail(c.reject).progress(c.notify):c[f[0]+"With"](this===d?c.promise():this,g?[a]:arguments)})}),a=null}).promise()},promise:function(a){return null!=a?n.extend(a,d):d}},e={};return d.pipe=d.then,n.each(b,function(a,f){var g=f[2],h=f[3];d[f[1]]=g.add,h&&g.add(function(){c=h},b[1^a][2].disable,b[2][2].lock),e[f[0]]=function(){return e[f[0]+"With"](this===e?d:this,arguments),this},e[f[0]+"With"]=g.fireWith}),d.promise(e),a&&a.call(e,e),e},when:function(a){var b=0,c=d.call(arguments),e=c.length,f=1!==e||a&&n.isFunction(a.promise)?e:0,g=1===f?a:n.Deferred(),h=function(a,b,c){return function(e){b[a]=this,c[a]=arguments.length>1?d.call(arguments):e,c===i?g.notifyWith(b,c):--f||g.resolveWith(b,c)}},i,j,k;if(e>1)for(i=new Array(e),j=new Array(e),k=new Array(e);e>b;b++)c[b]&&n.isFunction(c[b].promise)?c[b].promise().done(h(b,k,c)).fail(g.reject).progress(h(b,j,i)):--f;return f||g.resolveWith(k,c),g.promise()}});var H;n.fn.ready=function(a){return n.ready.promise().done(a),this},n.extend({isReady:!1,readyWait:1,holdReady:function(a){a?n.readyWait++:n.ready(!0)},ready:function(a){(a===!0?--n.readyWait:n.isReady)||(n.isReady=!0,a!==!0&&--n.readyWait>0||(H.resolveWith(l,[n]),n.fn.triggerHandler&&(n(l).triggerHandler("ready"),n(l).off("ready"))))}});function I(){l.removeEventListener("DOMContentLoaded",I,!1),a.removeEventListener("load",I,!1),n.ready()}n.ready.promise=function(b){return H||(H=n.Deferred(),"complete"===l.readyState?setTimeout(n.ready):(l.addEventListener("DOMContentLoaded",I,!1),a.addEventListener("load",I,!1))),H.promise(b)},n.ready.promise();var J=n.access=function(a,b,c,d,e,f,g){var h=0,i=a.length,j=null==c;if("object"===n.type(c)){e=!0;for(h in c)n.access(a,b,h,c[h],!0,f,g)}else if(void 0!==d&&(e=!0,n.isFunction(d)||(g=!0),j&&(g?(b.call(a,d),b=null):(j=b,b=function(a,b,c){return j.call(n(a),c)})),b))for(;i>h;h++)b(a[h],c,g?d:d.call(a[h],h,b(a[h],c)));return e?a:j?b.call(a):i?b(a[0],c):f};n.acceptData=function(a){return 1===a.nodeType||9===a.nodeType||!+a.nodeType};function K(){Object.defineProperty(this.cache={},0,{get:function(){return{}}}),this.expando=n.expando+K.uid++}K.uid=1,K.accepts=n.acceptData,K.prototype={key:function(a){if(!K.accepts(a))return 0;var b={},c=a[this.expando];if(!c){c=K.uid++;try{b[this.expando]={value:c},Object.defineProperties(a,b)}catch(d){b[this.expando]=c,n.extend(a,b)}}return this.cache[c]||(this.cache[c]={}),c},set:function(a,b,c){var d,e=this.key(a),f=this.cache[e];if("string"==typeof b)f[b]=c;else if(n.isEmptyObject(f))n.extend(this.cache[e],b);else for(d in b)f[d]=b[d];return f},get:function(a,b){var c=this.cache[this.key(a)];return void 0===b?c:c[b]},access:function(a,b,c){var d;return void 0===b||b&&"string"==typeof b&&void 0===c?(d=this.get(a,b),void 0!==d?d:this.get(a,n.camelCase(b))):(this.set(a,b,c),void 0!==c?c:b)},remove:function(a,b){var c,d,e,f=this.key(a),g=this.cache[f];if(void 0===b)this.cache[f]={};else{n.isArray(b)?d=b.concat(b.map(n.camelCase)):(e=n.camelCase(b),b in g?d=[b,e]:(d=e,d=d in g?[d]:d.match(E)||[])),c=d.length;while(c--)delete g[d[c]]}},hasData:function(a){return!n.isEmptyObject(this.cache[a[this.expando]]||{})},discard:function(a){a[this.expando]&&delete this.cache[a[this.expando]]}};var L=new K,M=new K,N=/^(?:\{[\w\W]*\}|\[[\w\W]*\])$/,O=/([A-Z])/g;function P(a,b,c){var d;if(void 0===c&&1===a.nodeType)if(d="data-"+b.replace(O,"-$1").toLowerCase(),c=a.getAttribute(d),"string"==typeof c){try{c="true"===c?!0:"false"===c?!1:"null"===c?null:+c+""===c?+c:N.test(c)?n.parseJSON(c):c}catch(e){}M.set(a,b,c)}else c=void 0;return c}n.extend({hasData:function(a){return M.hasData(a)||L.hasData(a)},data:function(a,b,c){return M.access(a,b,c)
},removeData:function(a,b){M.remove(a,b)},_data:function(a,b,c){return L.access(a,b,c)},_removeData:function(a,b){L.remove(a,b)}}),n.fn.extend({data:function(a,b){var c,d,e,f=this[0],g=f&&f.attributes;if(void 0===a){if(this.length&&(e=M.get(f),1===f.nodeType&&!L.get(f,"hasDataAttrs"))){c=g.length;while(c--)g[c]&&(d=g[c].name,0===d.indexOf("data-")&&(d=n.camelCase(d.slice(5)),P(f,d,e[d])));L.set(f,"hasDataAttrs",!0)}return e}return"object"==typeof a?this.each(function(){M.set(this,a)}):J(this,function(b){var c,d=n.camelCase(a);if(f&&void 0===b){if(c=M.get(f,a),void 0!==c)return c;if(c=M.get(f,d),void 0!==c)return c;if(c=P(f,d,void 0),void 0!==c)return c}else this.each(function(){var c=M.get(this,d);M.set(this,d,b),-1!==a.indexOf("-")&&void 0!==c&&M.set(this,a,b)})},null,b,arguments.length>1,null,!0)},removeData:function(a){return this.each(function(){M.remove(this,a)})}}),n.extend({queue:function(a,b,c){var d;return a?(b=(b||"fx")+"queue",d=L.get(a,b),c&&(!d||n.isArray(c)?d=L.access(a,b,n.makeArray(c)):d.push(c)),d||[]):void 0},dequeue:function(a,b){b=b||"fx";var c=n.queue(a,b),d=c.length,e=c.shift(),f=n._queueHooks(a,b),g=function(){n.dequeue(a,b)};"inprogress"===e&&(e=c.shift(),d--),e&&("fx"===b&&c.unshift("inprogress"),delete f.stop,e.call(a,g,f)),!d&&f&&f.empty.fire()},_queueHooks:function(a,b){var c=b+"queueHooks";return L.get(a,c)||L.access(a,c,{empty:n.Callbacks("once memory").add(function(){L.remove(a,[b+"queue",c])})})}}),n.fn.extend({queue:function(a,b){var c=2;return"string"!=typeof a&&(b=a,a="fx",c--),arguments.length<c?n.queue(this[0],a):void 0===b?this:this.each(function(){var c=n.queue(this,a,b);n._queueHooks(this,a),"fx"===a&&"inprogress"!==c[0]&&n.dequeue(this,a)})},dequeue:function(a){return this.each(function(){n.dequeue(this,a)})},clearQueue:function(a){return this.queue(a||"fx",[])},promise:function(a,b){var c,d=1,e=n.Deferred(),f=this,g=this.length,h=function(){--d||e.resolveWith(f,[f])};"string"!=typeof a&&(b=a,a=void 0),a=a||"fx";while(g--)c=L.get(f[g],a+"queueHooks"),c&&c.empty&&(d++,c.empty.add(h));return h(),e.promise(b)}});var Q=/[+-]?(?:\d*\.|)\d+(?:[eE][+-]?\d+|)/.source,R=["Top","Right","Bottom","Left"],S=function(a,b){return a=b||a,"none"===n.css(a,"display")||!n.contains(a.ownerDocument,a)},T=/^(?:checkbox|radio)$/i;!function(){var a=l.createDocumentFragment(),b=a.appendChild(l.createElement("div")),c=l.createElement("input");c.setAttribute("type","radio"),c.setAttribute("checked","checked"),c.setAttribute("name","t"),b.appendChild(c),k.checkClone=b.cloneNode(!0).cloneNode(!0).lastChild.checked,b.innerHTML="<textarea>x</textarea>",k.noCloneChecked=!!b.cloneNode(!0).lastChild.defaultValue}();var U="undefined";k.focusinBubbles="onfocusin"in a;var V=/^key/,W=/^(?:mouse|pointer|contextmenu)|click/,X=/^(?:focusinfocus|focusoutblur)$/,Y=/^([^.]*)(?:\.(.+)|)$/;function Z(){return!0}function $(){return!1}function _(){try{return l.activeElement}catch(a){}}n.event={global:{},add:function(a,b,c,d,e){var f,g,h,i,j,k,l,m,o,p,q,r=L.get(a);if(r){c.handler&&(f=c,c=f.handler,e=f.selector),c.guid||(c.guid=n.guid++),(i=r.events)||(i=r.events={}),(g=r.handle)||(g=r.handle=function(b){return typeof n!==U&&n.event.triggered!==b.type?n.event.dispatch.apply(a,arguments):void 0}),b=(b||"").match(E)||[""],j=b.length;while(j--)h=Y.exec(b[j])||[],o=q=h[1],p=(h[2]||"").split(".").sort(),o&&(l=n.event.special[o]||{},o=(e?l.delegateType:l.bindType)||o,l=n.event.special[o]||{},k=n.extend({type:o,origType:q,data:d,handler:c,guid:c.guid,selector:e,needsContext:e&&n.expr.match.needsContext.test(e),namespace:p.join(".")},f),(m=i[o])||(m=i[o]=[],m.delegateCount=0,l.setup&&l.setup.call(a,d,p,g)!==!1||a.addEventListener&&a.addEventListener(o,g,!1)),l.add&&(l.add.call(a,k),k.handler.guid||(k.handler.guid=c.guid)),e?m.splice(m.delegateCount++,0,k):m.push(k),n.event.global[o]=!0)}},remove:function(a,b,c,d,e){var f,g,h,i,j,k,l,m,o,p,q,r=L.hasData(a)&&L.get(a);if(r&&(i=r.events)){b=(b||"").match(E)||[""],j=b.length;while(j--)if(h=Y.exec(b[j])||[],o=q=h[1],p=(h[2]||"").split(".").sort(),o){l=n.event.special[o]||{},o=(d?l.delegateType:l.bindType)||o,m=i[o]||[],h=h[2]&&new RegExp("(^|\\.)"+p.join("\\.(?:.*\\.|)")+"(\\.|$)"),g=f=m.length;while(f--)k=m[f],!e&&q!==k.origType||c&&c.guid!==k.guid||h&&!h.test(k.namespace)||d&&d!==k.selector&&("**"!==d||!k.selector)||(m.splice(f,1),k.selector&&m.delegateCount--,l.remove&&l.remove.call(a,k));g&&!m.length&&(l.teardown&&l.teardown.call(a,p,r.handle)!==!1||n.removeEvent(a,o,r.handle),delete i[o])}else for(o in i)n.event.remove(a,o+b[j],c,d,!0);n.isEmptyObject(i)&&(delete r.handle,L.remove(a,"events"))}},trigger:function(b,c,d,e){var f,g,h,i,k,m,o,p=[d||l],q=j.call(b,"type")?b.type:b,r=j.call(b,"namespace")?b.namespace.split("."):[];if(g=h=d=d||l,3!==d.nodeType&&8!==d.nodeType&&!X.test(q+n.event.triggered)&&(q.indexOf(".")>=0&&(r=q.split("."),q=r.shift(),r.sort()),k=q.indexOf(":")<0&&"on"+q,b=b[n.expando]?b:new n.Event(q,"object"==typeof b&&b),b.isTrigger=e?2:3,b.namespace=r.join("."),b.namespace_re=b.namespace?new RegExp("(^|\\.)"+r.join("\\.(?:.*\\.|)")+"(\\.|$)"):null,b.result=void 0,b.target||(b.target=d),c=null==c?[b]:n.makeArray(c,[b]),o=n.event.special[q]||{},e||!o.trigger||o.trigger.apply(d,c)!==!1)){if(!e&&!o.noBubble&&!n.isWindow(d)){for(i=o.delegateType||q,X.test(i+q)||(g=g.parentNode);g;g=g.parentNode)p.push(g),h=g;h===(d.ownerDocument||l)&&p.push(h.defaultView||h.parentWindow||a)}f=0;while((g=p[f++])&&!b.isPropagationStopped())b.type=f>1?i:o.bindType||q,m=(L.get(g,"events")||{})[b.type]&&L.get(g,"handle"),m&&m.apply(g,c),m=k&&g[k],m&&m.apply&&n.acceptData(g)&&(b.result=m.apply(g,c),b.result===!1&&b.preventDefault());return b.type=q,e||b.isDefaultPrevented()||o._default&&o._default.apply(p.pop(),c)!==!1||!n.acceptData(d)||k&&n.isFunction(d[q])&&!n.isWindow(d)&&(h=d[k],h&&(d[k]=null),n.event.triggered=q,d[q](),n.event.triggered=void 0,h&&(d[k]=h)),b.result}},dispatch:function(a){a=n.event.fix(a);var b,c,e,f,g,h=[],i=d.call(arguments),j=(L.get(this,"events")||{})[a.type]||[],k=n.event.special[a.type]||{};if(i[0]=a,a.delegateTarget=this,!k.preDispatch||k.preDispatch.call(this,a)!==!1){h=n.event.handlers.call(this,a,j),b=0;while((f=h[b++])&&!a.isPropagationStopped()){a.currentTarget=f.elem,c=0;while((g=f.handlers[c++])&&!a.isImmediatePropagationStopped())(!a.namespace_re||a.namespace_re.test(g.namespace))&&(a.handleObj=g,a.data=g.data,e=((n.event.special[g.origType]||{}).handle||g.handler).apply(f.elem,i),void 0!==e&&(a.result=e)===!1&&(a.preventDefault(),a.stopPropagation()))}return k.postDispatch&&k.postDispatch.call(this,a),a.result}},handlers:function(a,b){var c,d,e,f,g=[],h=b.delegateCount,i=a.target;if(h&&i.nodeType&&(!a.button||"click"!==a.type))for(;i!==this;i=i.parentNode||this)if(i.disabled!==!0||"click"!==a.type){for(d=[],c=0;h>c;c++)f=b[c],e=f.selector+" ",void 0===d[e]&&(d[e]=f.needsContext?n(e,this).index(i)>=0:n.find(e,this,null,[i]).length),d[e]&&d.push(f);d.length&&g.push({elem:i,handlers:d})}return h<b.length&&g.push({elem:this,handlers:b.slice(h)}),g},props:"altKey bubbles cancelable ctrlKey currentTarget eventPhase metaKey relatedTarget shiftKey target timeStamp view which".split(" "),fixHooks:{},keyHooks:{props:"char charCode key keyCode".split(" "),filter:function(a,b){return null==a.which&&(a.which=null!=b.charCode?b.charCode:b.keyCode),a}},mouseHooks:{props:"button buttons clientX clientY offsetX offsetY pageX pageY screenX screenY toElement".split(" "),filter:function(a,b){var c,d,e,f=b.button;return null==a.pageX&&null!=b.clientX&&(c=a.target.ownerDocument||l,d=c.documentElement,e=c.body,a.pageX=b.clientX+(d&&d.scrollLeft||e&&e.scrollLeft||0)-(d&&d.clientLeft||e&&e.clientLeft||0),a.pageY=b.clientY+(d&&d.scrollTop||e&&e.scrollTop||0)-(d&&d.clientTop||e&&e.clientTop||0)),a.which||void 0===f||(a.which=1&f?1:2&f?3:4&f?2:0),a}},fix:function(a){if(a[n.expando])return a;var b,c,d,e=a.type,f=a,g=this.fixHooks[e];g||(this.fixHooks[e]=g=W.test(e)?this.mouseHooks:V.test(e)?this.keyHooks:{}),d=g.props?this.props.concat(g.props):this.props,a=new n.Event(f),b=d.length;while(b--)c=d[b],a[c]=f[c];return a.target||(a.target=l),3===a.target.nodeType&&(a.target=a.target.parentNode),g.filter?g.filter(a,f):a},special:{load:{noBubble:!0},focus:{trigger:function(){return this!==_()&&this.focus?(this.focus(),!1):void 0},delegateType:"focusin"},blur:{trigger:function(){return this===_()&&this.blur?(this.blur(),!1):void 0},delegateType:"focusout"},click:{trigger:function(){return"checkbox"===this.type&&this.click&&n.nodeName(this,"input")?(this.click(),!1):void 0},_default:function(a){return n.nodeName(a.target,"a")}},beforeunload:{postDispatch:function(a){void 0!==a.result&&a.originalEvent&&(a.originalEvent.returnValue=a.result)}}},simulate:function(a,b,c,d){var e=n.extend(new n.Event,c,{type:a,isSimulated:!0,originalEvent:{}});d?n.event.trigger(e,null,b):n.event.dispatch.call(b,e),e.isDefaultPrevented()&&c.preventDefault()}},n.removeEvent=function(a,b,c){a.removeEventListener&&a.removeEventListener(b,c,!1)},n.Event=function(a,b){return this instanceof n.Event?(a&&a.type?(this.originalEvent=a,this.type=a.type,this.isDefaultPrevented=a.defaultPrevented||void 0===a.defaultPrevented&&a.returnValue===!1?Z:$):this.type=a,b&&n.extend(this,b),this.timeStamp=a&&a.timeStamp||n.now(),void(this[n.expando]=!0)):new n.Event(a,b)},n.Event.prototype={isDefaultPrevented:$,isPropagationStopped:$,isImmediatePropagationStopped:$,preventDefault:function(){var a=this.originalEvent;this.isDefaultPrevented=Z,a&&a.preventDefault&&a.preventDefault()},stopPropagation:function(){var a=this.originalEvent;this.isPropagationStopped=Z,a&&a.stopPropagation&&a.stopPropagation()},stopImmediatePropagation:function(){var a=this.originalEvent;this.isImmediatePropagationStopped=Z,a&&a.stopImmediatePropagation&&a.stopImmediatePropagation(),this.stopPropagation()}},n.each({mouseenter:"mouseover",mouseleave:"mouseout",pointerenter:"pointerover",pointerleave:"pointerout"},function(a,b){n.event.special[a]={delegateType:b,bindType:b,handle:function(a){var c,d=this,e=a.relatedTarget,f=a.handleObj;return(!e||e!==d&&!n.contains(d,e))&&(a.type=f.origType,c=f.handler.apply(this,arguments),a.type=b),c}}}),k.focusinBubbles||n.each({focus:"focusin",blur:"focusout"},function(a,b){var c=function(a){n.event.simulate(b,a.target,n.event.fix(a),!0)};n.event.special[b]={setup:function(){var d=this.ownerDocument||this,e=L.access(d,b);e||d.addEventListener(a,c,!0),L.access(d,b,(e||0)+1)},teardown:function(){var d=this.ownerDocument||this,e=L.access(d,b)-1;e?L.access(d,b,e):(d.removeEventListener(a,c,!0),L.remove(d,b))}}}),n.fn.extend({on:function(a,b,c,d,e){var f,g;if("object"==typeof a){"string"!=typeof b&&(c=c||b,b=void 0);for(g in a)this.on(g,b,c,a[g],e);return this}if(null==c&&null==d?(d=b,c=b=void 0):null==d&&("string"==typeof b?(d=c,c=void 0):(d=c,c=b,b=void 0)),d===!1)d=$;else if(!d)return this;return 1===e&&(f=d,d=function(a){return n().off(a),f.apply(this,arguments)},d.guid=f.guid||(f.guid=n.guid++)),this.each(function(){n.event.add(this,a,d,c,b)})},one:function(a,b,c,d){return this.on(a,b,c,d,1)},off:function(a,b,c){var d,e;if(a&&a.preventDefault&&a.handleObj)return d=a.handleObj,n(a.delegateTarget).off(d.namespace?d.origType+"."+d.namespace:d.origType,d.selector,d.handler),this;if("object"==typeof a){for(e in a)this.off(e,b,a[e]);return this}return(b===!1||"function"==typeof b)&&(c=b,b=void 0),c===!1&&(c=$),this.each(function(){n.event.remove(this,a,c,b)})},trigger:function(a,b){return this.each(function(){n.event.trigger(a,b,this)})},triggerHandler:function(a,b){var c=this[0];return c?n.event.trigger(a,b,c,!0):void 0}});var ab=/<(?!area|br|col|embed|hr|img|input|link|meta|param)(([\w:]+)[^>]*)\/>/gi,bb=/<([\w:]+)/,cb=/<|&#?\w+;/,db=/<(?:script|style|link)/i,eb=/checked\s*(?:[^=]|=\s*.checked.)/i,fb=/^$|\/(?:java|ecma)script/i,gb=/^true\/(.*)/,hb=/^\s*<!(?:\[CDATA\[|--)|(?:\]\]|--)>\s*$/g,ib={option:[1,"<select multiple='multiple'>","</select>"],thead:[1,"<table>","</table>"],col:[2,"<table><colgroup>","</colgroup></table>"],tr:[2,"<table><tbody>","</tbody></table>"],td:[3,"<table><tbody><tr>","</tr></tbody></table>"],_default:[0,"",""]};ib.optgroup=ib.option,ib.tbody=ib.tfoot=ib.colgroup=ib.caption=ib.thead,ib.th=ib.td;function jb(a,b){return n.nodeName(a,"table")&&n.nodeName(11!==b.nodeType?b:b.firstChild,"tr")?a.getElementsByTagName("tbody")[0]||a.appendChild(a.ownerDocument.createElement("tbody")):a}function kb(a){return a.type=(null!==a.getAttribute("type"))+"/"+a.type,a}function lb(a){var b=gb.exec(a.type);return b?a.type=b[1]:a.removeAttribute("type"),a}function mb(a,b){for(var c=0,d=a.length;d>c;c++)L.set(a[c],"globalEval",!b||L.get(b[c],"globalEval"))}function nb(a,b){var c,d,e,f,g,h,i,j;if(1===b.nodeType){if(L.hasData(a)&&(f=L.access(a),g=L.set(b,f),j=f.events)){delete g.handle,g.events={};for(e in j)for(c=0,d=j[e].length;d>c;c++)n.event.add(b,e,j[e][c])}M.hasData(a)&&(h=M.access(a),i=n.extend({},h),M.set(b,i))}}function ob(a,b){var c=a.getElementsByTagName?a.getElementsByTagName(b||"*"):a.querySelectorAll?a.querySelectorAll(b||"*"):[];return void 0===b||b&&n.nodeName(a,b)?n.merge([a],c):c}function pb(a,b){var c=b.nodeName.toLowerCase();"input"===c&&T.test(a.type)?b.checked=a.checked:("input"===c||"textarea"===c)&&(b.defaultValue=a.defaultValue)}n.extend({clone:function(a,b,c){var d,e,f,g,h=a.cloneNode(!0),i=n.contains(a.ownerDocument,a);if(!(k.noCloneChecked||1!==a.nodeType&&11!==a.nodeType||n.isXMLDoc(a)))for(g=ob(h),f=ob(a),d=0,e=f.length;e>d;d++)pb(f[d],g[d]);if(b)if(c)for(f=f||ob(a),g=g||ob(h),d=0,e=f.length;e>d;d++)nb(f[d],g[d]);else nb(a,h);return g=ob(h,"script"),g.length>0&&mb(g,!i&&ob(a,"script")),h},buildFragment:function(a,b,c,d){for(var e,f,g,h,i,j,k=b.createDocumentFragment(),l=[],m=0,o=a.length;o>m;m++)if(e=a[m],e||0===e)if("object"===n.type(e))n.merge(l,e.nodeType?[e]:e);else if(cb.test(e)){f=f||k.appendChild(b.createElement("div")),g=(bb.exec(e)||["",""])[1].toLowerCase(),h=ib[g]||ib._default,f.innerHTML=h[1]+e.replace(ab,"<$1></$2>")+h[2],j=h[0];while(j--)f=f.lastChild;n.merge(l,f.childNodes),f=k.firstChild,f.textContent=""}else l.push(b.createTextNode(e));k.textContent="",m=0;while(e=l[m++])if((!d||-1===n.inArray(e,d))&&(i=n.contains(e.ownerDocument,e),f=ob(k.appendChild(e),"script"),i&&mb(f),c)){j=0;while(e=f[j++])fb.test(e.type||"")&&c.push(e)}return k},cleanData:function(a){for(var b,c,d,e,f=n.event.special,g=0;void 0!==(c=a[g]);g++){if(n.acceptData(c)&&(e=c[L.expando],e&&(b=L.cache[e]))){if(b.events)for(d in b.events)f[d]?n.event.remove(c,d):n.removeEvent(c,d,b.handle);L.cache[e]&&delete L.cache[e]}delete M.cache[c[M.expando]]}}}),n.fn.extend({text:function(a){return J(this,function(a){return void 0===a?n.text(this):this.empty().each(function(){(1===this.nodeType||11===this.nodeType||9===this.nodeType)&&(this.textContent=a)})},null,a,arguments.length)},append:function(){return this.domManip(arguments,function(a){if(1===this.nodeType||11===this.nodeType||9===this.nodeType){var b=jb(this,a);b.appendChild(a)}})},prepend:function(){return this.domManip(arguments,function(a){if(1===this.nodeType||11===this.nodeType||9===this.nodeType){var b=jb(this,a);b.insertBefore(a,b.firstChild)}})},before:function(){return this.domManip(arguments,function(a){this.parentNode&&this.parentNode.insertBefore(a,this)})},after:function(){return this.domManip(arguments,function(a){this.parentNode&&this.parentNode.insertBefore(a,this.nextSibling)})},remove:function(a,b){for(var c,d=a?n.filter(a,this):this,e=0;null!=(c=d[e]);e++)b||1!==c.nodeType||n.cleanData(ob(c)),c.parentNode&&(b&&n.contains(c.ownerDocument,c)&&mb(ob(c,"script")),c.parentNode.removeChild(c));return this},empty:function(){for(var a,b=0;null!=(a=this[b]);b++)1===a.nodeType&&(n.cleanData(ob(a,!1)),a.textContent="");return this},clone:function(a,b){return a=null==a?!1:a,b=null==b?a:b,this.map(function(){return n.clone(this,a,b)})},html:function(a){return J(this,function(a){var b=this[0]||{},c=0,d=this.length;if(void 0===a&&1===b.nodeType)return b.innerHTML;if("string"==typeof a&&!db.test(a)&&!ib[(bb.exec(a)||["",""])[1].toLowerCase()]){a=a.replace(ab,"<$1></$2>");try{for(;d>c;c++)b=this[c]||{},1===b.nodeType&&(n.cleanData(ob(b,!1)),b.innerHTML=a);b=0}catch(e){}}b&&this.empty().append(a)},null,a,arguments.length)},replaceWith:function(){var a=arguments[0];return this.domManip(arguments,function(b){a=this.parentNode,n.cleanData(ob(this)),a&&a.replaceChild(b,this)}),a&&(a.length||a.nodeType)?this:this.remove()},detach:function(a){return this.remove(a,!0)},domManip:function(a,b){a=e.apply([],a);var c,d,f,g,h,i,j=0,l=this.length,m=this,o=l-1,p=a[0],q=n.isFunction(p);if(q||l>1&&"string"==typeof p&&!k.checkClone&&eb.test(p))return this.each(function(c){var d=m.eq(c);q&&(a[0]=p.call(this,c,d.html())),d.domManip(a,b)});if(l&&(c=n.buildFragment(a,this[0].ownerDocument,!1,this),d=c.firstChild,1===c.childNodes.length&&(c=d),d)){for(f=n.map(ob(c,"script"),kb),g=f.length;l>j;j++)h=c,j!==o&&(h=n.clone(h,!0,!0),g&&n.merge(f,ob(h,"script"))),b.call(this[j],h,j);if(g)for(i=f[f.length-1].ownerDocument,n.map(f,lb),j=0;g>j;j++)h=f[j],fb.test(h.type||"")&&!L.access(h,"globalEval")&&n.contains(i,h)&&(h.src?n._evalUrl&&n._evalUrl(h.src):n.globalEval(h.textContent.replace(hb,"")))}return this}}),n.each({appendTo:"append",prependTo:"prepend",insertBefore:"before",insertAfter:"after",replaceAll:"replaceWith"},function(a,b){n.fn[a]=function(a){for(var c,d=[],e=n(a),g=e.length-1,h=0;g>=h;h++)c=h===g?this:this.clone(!0),n(e[h])[b](c),f.apply(d,c.get());return this.pushStack(d)}});var qb,rb={};function sb(b,c){var d,e=n(c.createElement(b)).appendTo(c.body),f=a.getDefaultComputedStyle&&(d=a.getDefaultComputedStyle(e[0]))?d.display:n.css(e[0],"display");return e.detach(),f}function tb(a){var b=l,c=rb[a];return c||(c=sb(a,b),"none"!==c&&c||(qb=(qb||n("<iframe frameborder='0' width='0' height='0'/>")).appendTo(b.documentElement),b=qb[0].contentDocument,b.write(),b.close(),c=sb(a,b),qb.detach()),rb[a]=c),c}var ub=/^margin/,vb=new RegExp("^("+Q+")(?!px)[a-z%]+$","i"),wb=function(b){return b.ownerDocument.defaultView.opener?b.ownerDocument.defaultView.getComputedStyle(b,null):a.getComputedStyle(b,null)};function xb(a,b,c){var d,e,f,g,h=a.style;return c=c||wb(a),c&&(g=c.getPropertyValue(b)||c[b]),c&&(""!==g||n.contains(a.ownerDocument,a)||(g=n.style(a,b)),vb.test(g)&&ub.test(b)&&(d=h.width,e=h.minWidth,f=h.maxWidth,h.minWidth=h.maxWidth=h.width=g,g=c.width,h.width=d,h.minWidth=e,h.maxWidth=f)),void 0!==g?g+"":g}function yb(a,b){return{get:function(){return a()?void delete this.get:(this.get=b).apply(this,arguments)}}}!function(){var b,c,d=l.documentElement,e=l.createElement("div"),f=l.createElement("div");if(f.style){f.style.backgroundClip="content-box",f.cloneNode(!0).style.backgroundClip="",k.clearCloneStyle="content-box"===f.style.backgroundClip,e.style.cssText="border:0;width:0;height:0;top:0;left:-9999px;margin-top:1px;position:absolute",e.appendChild(f);function g(){f.style.cssText="-webkit-box-sizing:border-box;-moz-box-sizing:border-box;box-sizing:border-box;display:block;margin-top:1%;top:1%;border:1px;padding:1px;width:4px;position:absolute",f.innerHTML="",d.appendChild(e);var g=a.getComputedStyle(f,null);b="1%"!==g.top,c="4px"===g.width,d.removeChild(e)}a.getComputedStyle&&n.extend(k,{pixelPosition:function(){return g(),b},boxSizingReliable:function(){return null==c&&g(),c},reliableMarginRight:function(){var b,c=f.appendChild(l.createElement("div"));return c.style.cssText=f.style.cssText="-webkit-box-sizing:content-box;-moz-box-sizing:content-box;box-sizing:content-box;display:block;margin:0;border:0;padding:0",c.style.marginRight=c.style.width="0",f.style.width="1px",d.appendChild(e),b=!parseFloat(a.getComputedStyle(c,null).marginRight),d.removeChild(e),f.removeChild(c),b}})}}(),n.swap=function(a,b,c,d){var e,f,g={};for(f in b)g[f]=a.style[f],a.style[f]=b[f];e=c.apply(a,d||[]);for(f in b)a.style[f]=g[f];return e};var zb=/^(none|table(?!-c[ea]).+)/,Ab=new RegExp("^("+Q+")(.*)$","i"),Bb=new RegExp("^([+-])=("+Q+")","i"),Cb={position:"absolute",visibility:"hidden",display:"block"},Db={letterSpacing:"0",fontWeight:"400"},Eb=["Webkit","O","Moz","ms"];function Fb(a,b){if(b in a)return b;var c=b[0].toUpperCase()+b.slice(1),d=b,e=Eb.length;while(e--)if(b=Eb[e]+c,b in a)return b;return d}function Gb(a,b,c){var d=Ab.exec(b);return d?Math.max(0,d[1]-(c||0))+(d[2]||"px"):b}function Hb(a,b,c,d,e){for(var f=c===(d?"border":"content")?4:"width"===b?1:0,g=0;4>f;f+=2)"margin"===c&&(g+=n.css(a,c+R[f],!0,e)),d?("content"===c&&(g-=n.css(a,"padding"+R[f],!0,e)),"margin"!==c&&(g-=n.css(a,"border"+R[f]+"Width",!0,e))):(g+=n.css(a,"padding"+R[f],!0,e),"padding"!==c&&(g+=n.css(a,"border"+R[f]+"Width",!0,e)));return g}function Ib(a,b,c){var d=!0,e="width"===b?a.offsetWidth:a.offsetHeight,f=wb(a),g="border-box"===n.css(a,"boxSizing",!1,f);if(0>=e||null==e){if(e=xb(a,b,f),(0>e||null==e)&&(e=a.style[b]),vb.test(e))return e;d=g&&(k.boxSizingReliable()||e===a.style[b]),e=parseFloat(e)||0}return e+Hb(a,b,c||(g?"border":"content"),d,f)+"px"}function Jb(a,b){for(var c,d,e,f=[],g=0,h=a.length;h>g;g++)d=a[g],d.style&&(f[g]=L.get(d,"olddisplay"),c=d.style.display,b?(f[g]||"none"!==c||(d.style.display=""),""===d.style.display&&S(d)&&(f[g]=L.access(d,"olddisplay",tb(d.nodeName)))):(e=S(d),"none"===c&&e||L.set(d,"olddisplay",e?c:n.css(d,"display"))));for(g=0;h>g;g++)d=a[g],d.style&&(b&&"none"!==d.style.display&&""!==d.style.display||(d.style.display=b?f[g]||"":"none"));return a}n.extend({cssHooks:{opacity:{get:function(a,b){if(b){var c=xb(a,"opacity");return""===c?"1":c}}}},cssNumber:{columnCount:!0,fillOpacity:!0,flexGrow:!0,flexShrink:!0,fontWeight:!0,lineHeight:!0,opacity:!0,order:!0,orphans:!0,widows:!0,zIndex:!0,zoom:!0},cssProps:{"float":"cssFloat"},style:function(a,b,c,d){if(a&&3!==a.nodeType&&8!==a.nodeType&&a.style){var e,f,g,h=n.camelCase(b),i=a.style;return b=n.cssProps[h]||(n.cssProps[h]=Fb(i,h)),g=n.cssHooks[b]||n.cssHooks[h],void 0===c?g&&"get"in g&&void 0!==(e=g.get(a,!1,d))?e:i[b]:(f=typeof c,"string"===f&&(e=Bb.exec(c))&&(c=(e[1]+1)*e[2]+parseFloat(n.css(a,b)),f="number"),null!=c&&c===c&&("number"!==f||n.cssNumber[h]||(c+="px"),k.clearCloneStyle||""!==c||0!==b.indexOf("background")||(i[b]="inherit"),g&&"set"in g&&void 0===(c=g.set(a,c,d))||(i[b]=c)),void 0)}},css:function(a,b,c,d){var e,f,g,h=n.camelCase(b);return b=n.cssProps[h]||(n.cssProps[h]=Fb(a.style,h)),g=n.cssHooks[b]||n.cssHooks[h],g&&"get"in g&&(e=g.get(a,!0,c)),void 0===e&&(e=xb(a,b,d)),"normal"===e&&b in Db&&(e=Db[b]),""===c||c?(f=parseFloat(e),c===!0||n.isNumeric(f)?f||0:e):e}}),n.each(["height","width"],function(a,b){n.cssHooks[b]={get:function(a,c,d){return c?zb.test(n.css(a,"display"))&&0===a.offsetWidth?n.swap(a,Cb,function(){return Ib(a,b,d)}):Ib(a,b,d):void 0},set:function(a,c,d){var e=d&&wb(a);return Gb(a,c,d?Hb(a,b,d,"border-box"===n.css(a,"boxSizing",!1,e),e):0)}}}),n.cssHooks.marginRight=yb(k.reliableMarginRight,function(a,b){return b?n.swap(a,{display:"inline-block"},xb,[a,"marginRight"]):void 0}),n.each({margin:"",padding:"",border:"Width"},function(a,b){n.cssHooks[a+b]={expand:function(c){for(var d=0,e={},f="string"==typeof c?c.split(" "):[c];4>d;d++)e[a+R[d]+b]=f[d]||f[d-2]||f[0];return e}},ub.test(a)||(n.cssHooks[a+b].set=Gb)}),n.fn.extend({css:function(a,b){return J(this,function(a,b,c){var d,e,f={},g=0;if(n.isArray(b)){for(d=wb(a),e=b.length;e>g;g++)f[b[g]]=n.css(a,b[g],!1,d);return f}return void 0!==c?n.style(a,b,c):n.css(a,b)},a,b,arguments.length>1)},show:function(){return Jb(this,!0)},hide:function(){return Jb(this)},toggle:function(a){return"boolean"==typeof a?a?this.show():this.hide():this.each(function(){S(this)?n(this).show():n(this).hide()})}});function Kb(a,b,c,d,e){return new Kb.prototype.init(a,b,c,d,e)}n.Tween=Kb,Kb.prototype={constructor:Kb,init:function(a,b,c,d,e,f){this.elem=a,this.prop=c,this.easing=e||"swing",this.options=b,this.start=this.now=this.cur(),this.end=d,this.unit=f||(n.cssNumber[c]?"":"px")},cur:function(){var a=Kb.propHooks[this.prop];return a&&a.get?a.get(this):Kb.propHooks._default.get(this)},run:function(a){var b,c=Kb.propHooks[this.prop];return this.pos=b=this.options.duration?n.easing[this.easing](a,this.options.duration*a,0,1,this.options.duration):a,this.now=(this.end-this.start)*b+this.start,this.options.step&&this.options.step.call(this.elem,this.now,this),c&&c.set?c.set(this):Kb.propHooks._default.set(this),this}},Kb.prototype.init.prototype=Kb.prototype,Kb.propHooks={_default:{get:function(a){var b;return null==a.elem[a.prop]||a.elem.style&&null!=a.elem.style[a.prop]?(b=n.css(a.elem,a.prop,""),b&&"auto"!==b?b:0):a.elem[a.prop]},set:function(a){n.fx.step[a.prop]?n.fx.step[a.prop](a):a.elem.style&&(null!=a.elem.style[n.cssProps[a.prop]]||n.cssHooks[a.prop])?n.style(a.elem,a.prop,a.now+a.unit):a.elem[a.prop]=a.now}}},Kb.propHooks.scrollTop=Kb.propHooks.scrollLeft={set:function(a){a.elem.nodeType&&a.elem.parentNode&&(a.elem[a.prop]=a.now)}},n.easing={linear:function(a){return a},swing:function(a){return.5-Math.cos(a*Math.PI)/2}},n.fx=Kb.prototype.init,n.fx.step={};var Lb,Mb,Nb=/^(?:toggle|show|hide)$/,Ob=new RegExp("^(?:([+-])=|)("+Q+")([a-z%]*)$","i"),Pb=/queueHooks$/,Qb=[Vb],Rb={"*":[function(a,b){var c=this.createTween(a,b),d=c.cur(),e=Ob.exec(b),f=e&&e[3]||(n.cssNumber[a]?"":"px"),g=(n.cssNumber[a]||"px"!==f&&+d)&&Ob.exec(n.css(c.elem,a)),h=1,i=20;if(g&&g[3]!==f){f=f||g[3],e=e||[],g=+d||1;do h=h||".5",g/=h,n.style(c.elem,a,g+f);while(h!==(h=c.cur()/d)&&1!==h&&--i)}return e&&(g=c.start=+g||+d||0,c.unit=f,c.end=e[1]?g+(e[1]+1)*e[2]:+e[2]),c}]};function Sb(){return setTimeout(function(){Lb=void 0}),Lb=n.now()}function Tb(a,b){var c,d=0,e={height:a};for(b=b?1:0;4>d;d+=2-b)c=R[d],e["margin"+c]=e["padding"+c]=a;return b&&(e.opacity=e.width=a),e}function Ub(a,b,c){for(var d,e=(Rb[b]||[]).concat(Rb["*"]),f=0,g=e.length;g>f;f++)if(d=e[f].call(c,b,a))return d}function Vb(a,b,c){var d,e,f,g,h,i,j,k,l=this,m={},o=a.style,p=a.nodeType&&S(a),q=L.get(a,"fxshow");c.queue||(h=n._queueHooks(a,"fx"),null==h.unqueued&&(h.unqueued=0,i=h.empty.fire,h.empty.fire=function(){h.unqueued||i()}),h.unqueued++,l.always(function(){l.always(function(){h.unqueued--,n.queue(a,"fx").length||h.empty.fire()})})),1===a.nodeType&&("height"in b||"width"in b)&&(c.overflow=[o.overflow,o.overflowX,o.overflowY],j=n.css(a,"display"),k="none"===j?L.get(a,"olddisplay")||tb(a.nodeName):j,"inline"===k&&"none"===n.css(a,"float")&&(o.display="inline-block")),c.overflow&&(o.overflow="hidden",l.always(function(){o.overflow=c.overflow[0],o.overflowX=c.overflow[1],o.overflowY=c.overflow[2]}));for(d in b)if(e=b[d],Nb.exec(e)){if(delete b[d],f=f||"toggle"===e,e===(p?"hide":"show")){if("show"!==e||!q||void 0===q[d])continue;p=!0}m[d]=q&&q[d]||n.style(a,d)}else j=void 0;if(n.isEmptyObject(m))"inline"===("none"===j?tb(a.nodeName):j)&&(o.display=j);else{q?"hidden"in q&&(p=q.hidden):q=L.access(a,"fxshow",{}),f&&(q.hidden=!p),p?n(a).show():l.done(function(){n(a).hide()}),l.done(function(){var b;L.remove(a,"fxshow");for(b in m)n.style(a,b,m[b])});for(d in m)g=Ub(p?q[d]:0,d,l),d in q||(q[d]=g.start,p&&(g.end=g.start,g.start="width"===d||"height"===d?1:0))}}function Wb(a,b){var c,d,e,f,g;for(c in a)if(d=n.camelCase(c),e=b[d],f=a[c],n.isArray(f)&&(e=f[1],f=a[c]=f[0]),c!==d&&(a[d]=f,delete a[c]),g=n.cssHooks[d],g&&"expand"in g){f=g.expand(f),delete a[d];for(c in f)c in a||(a[c]=f[c],b[c]=e)}else b[d]=e}function Xb(a,b,c){var d,e,f=0,g=Qb.length,h=n.Deferred().always(function(){delete i.elem}),i=function(){if(e)return!1;for(var b=Lb||Sb(),c=Math.max(0,j.startTime+j.duration-b),d=c/j.duration||0,f=1-d,g=0,i=j.tweens.length;i>g;g++)j.tweens[g].run(f);return h.notifyWith(a,[j,f,c]),1>f&&i?c:(h.resolveWith(a,[j]),!1)},j=h.promise({elem:a,props:n.extend({},b),opts:n.extend(!0,{specialEasing:{}},c),originalProperties:b,originalOptions:c,startTime:Lb||Sb(),duration:c.duration,tweens:[],createTween:function(b,c){var d=n.Tween(a,j.opts,b,c,j.opts.specialEasing[b]||j.opts.easing);return j.tweens.push(d),d},stop:function(b){var c=0,d=b?j.tweens.length:0;if(e)return this;for(e=!0;d>c;c++)j.tweens[c].run(1);return b?h.resolveWith(a,[j,b]):h.rejectWith(a,[j,b]),this}}),k=j.props;for(Wb(k,j.opts.specialEasing);g>f;f++)if(d=Qb[f].call(j,a,k,j.opts))return d;return n.map(k,Ub,j),n.isFunction(j.opts.start)&&j.opts.start.call(a,j),n.fx.timer(n.extend(i,{elem:a,anim:j,queue:j.opts.queue})),j.progress(j.opts.progress).done(j.opts.done,j.opts.complete).fail(j.opts.fail).always(j.opts.always)}n.Animation=n.extend(Xb,{tweener:function(a,b){n.isFunction(a)?(b=a,a=["*"]):a=a.split(" ");for(var c,d=0,e=a.length;e>d;d++)c=a[d],Rb[c]=Rb[c]||[],Rb[c].unshift(b)},prefilter:function(a,b){b?Qb.unshift(a):Qb.push(a)}}),n.speed=function(a,b,c){var d=a&&"object"==typeof a?n.extend({},a):{complete:c||!c&&b||n.isFunction(a)&&a,duration:a,easing:c&&b||b&&!n.isFunction(b)&&b};return d.duration=n.fx.off?0:"number"==typeof d.duration?d.duration:d.duration in n.fx.speeds?n.fx.speeds[d.duration]:n.fx.speeds._default,(null==d.queue||d.queue===!0)&&(d.queue="fx"),d.old=d.complete,d.complete=function(){n.isFunction(d.old)&&d.old.call(this),d.queue&&n.dequeue(this,d.queue)},d},n.fn.extend({fadeTo:function(a,b,c,d){return this.filter(S).css("opacity",0).show().end().animate({opacity:b},a,c,d)},animate:function(a,b,c,d){var e=n.isEmptyObject(a),f=n.speed(b,c,d),g=function(){var b=Xb(this,n.extend({},a),f);(e||L.get(this,"finish"))&&b.stop(!0)};return g.finish=g,e||f.queue===!1?this.each(g):this.queue(f.queue,g)},stop:function(a,b,c){var d=function(a){var b=a.stop;delete a.stop,b(c)};return"string"!=typeof a&&(c=b,b=a,a=void 0),b&&a!==!1&&this.queue(a||"fx",[]),this.each(function(){var b=!0,e=null!=a&&a+"queueHooks",f=n.timers,g=L.get(this);if(e)g[e]&&g[e].stop&&d(g[e]);else for(e in g)g[e]&&g[e].stop&&Pb.test(e)&&d(g[e]);for(e=f.length;e--;)f[e].elem!==this||null!=a&&f[e].queue!==a||(f[e].anim.stop(c),b=!1,f.splice(e,1));(b||!c)&&n.dequeue(this,a)})},finish:function(a){return a!==!1&&(a=a||"fx"),this.each(function(){var b,c=L.get(this),d=c[a+"queue"],e=c[a+"queueHooks"],f=n.timers,g=d?d.length:0;for(c.finish=!0,n.queue(this,a,[]),e&&e.stop&&e.stop.call(this,!0),b=f.length;b--;)f[b].elem===this&&f[b].queue===a&&(f[b].anim.stop(!0),f.splice(b,1));for(b=0;g>b;b++)d[b]&&d[b].finish&&d[b].finish.call(this);delete c.finish})}}),n.each(["toggle","show","hide"],function(a,b){var c=n.fn[b];n.fn[b]=function(a,d,e){return null==a||"boolean"==typeof a?c.apply(this,arguments):this.animate(Tb(b,!0),a,d,e)}}),n.each({slideDown:Tb("show"),slideUp:Tb("hide"),slideToggle:Tb("toggle"),fadeIn:{opacity:"show"},fadeOut:{opacity:"hide"},fadeToggle:{opacity:"toggle"}},function(a,b){n.fn[a]=function(a,c,d){return this.animate(b,a,c,d)}}),n.timers=[],n.fx.tick=function(){var a,b=0,c=n.timers;for(Lb=n.now();b<c.length;b++)a=c[b],a()||c[b]!==a||c.splice(b--,1);c.length||n.fx.stop(),Lb=void 0},n.fx.timer=function(a){n.timers.push(a),a()?n.fx.start():n.timers.pop()},n.fx.interval=13,n.fx.start=function(){Mb||(Mb=setInterval(n.fx.tick,n.fx.interval))},n.fx.stop=function(){clearInterval(Mb),Mb=null},n.fx.speeds={slow:600,fast:200,_default:400},n.fn.delay=function(a,b){return a=n.fx?n.fx.speeds[a]||a:a,b=b||"fx",this.queue(b,function(b,c){var d=setTimeout(b,a);c.stop=function(){clearTimeout(d)}})},function(){var a=l.createElement("input"),b=l.createElement("select"),c=b.appendChild(l.createElement("option"));a.type="checkbox",k.checkOn=""!==a.value,k.optSelected=c.selected,b.disabled=!0,k.optDisabled=!c.disabled,a=l.createElement("input"),a.value="t",a.type="radio",k.radioValue="t"===a.value}();var Yb,Zb,$b=n.expr.attrHandle;n.fn.extend({attr:function(a,b){return J(this,n.attr,a,b,arguments.length>1)},removeAttr:function(a){return this.each(function(){n.removeAttr(this,a)})}}),n.extend({attr:function(a,b,c){var d,e,f=a.nodeType;if(a&&3!==f&&8!==f&&2!==f)return typeof a.getAttribute===U?n.prop(a,b,c):(1===f&&n.isXMLDoc(a)||(b=b.toLowerCase(),d=n.attrHooks[b]||(n.expr.match.bool.test(b)?Zb:Yb)),void 0===c?d&&"get"in d&&null!==(e=d.get(a,b))?e:(e=n.find.attr(a,b),null==e?void 0:e):null!==c?d&&"set"in d&&void 0!==(e=d.set(a,c,b))?e:(a.setAttribute(b,c+""),c):void n.removeAttr(a,b))
},removeAttr:function(a,b){var c,d,e=0,f=b&&b.match(E);if(f&&1===a.nodeType)while(c=f[e++])d=n.propFix[c]||c,n.expr.match.bool.test(c)&&(a[d]=!1),a.removeAttribute(c)},attrHooks:{type:{set:function(a,b){if(!k.radioValue&&"radio"===b&&n.nodeName(a,"input")){var c=a.value;return a.setAttribute("type",b),c&&(a.value=c),b}}}}}),Zb={set:function(a,b,c){return b===!1?n.removeAttr(a,c):a.setAttribute(c,c),c}},n.each(n.expr.match.bool.source.match(/\w+/g),function(a,b){var c=$b[b]||n.find.attr;$b[b]=function(a,b,d){var e,f;return d||(f=$b[b],$b[b]=e,e=null!=c(a,b,d)?b.toLowerCase():null,$b[b]=f),e}});var _b=/^(?:input|select|textarea|button)$/i;n.fn.extend({prop:function(a,b){return J(this,n.prop,a,b,arguments.length>1)},removeProp:function(a){return this.each(function(){delete this[n.propFix[a]||a]})}}),n.extend({propFix:{"for":"htmlFor","class":"className"},prop:function(a,b,c){var d,e,f,g=a.nodeType;if(a&&3!==g&&8!==g&&2!==g)return f=1!==g||!n.isXMLDoc(a),f&&(b=n.propFix[b]||b,e=n.propHooks[b]),void 0!==c?e&&"set"in e&&void 0!==(d=e.set(a,c,b))?d:a[b]=c:e&&"get"in e&&null!==(d=e.get(a,b))?d:a[b]},propHooks:{tabIndex:{get:function(a){return a.hasAttribute("tabindex")||_b.test(a.nodeName)||a.href?a.tabIndex:-1}}}}),k.optSelected||(n.propHooks.selected={get:function(a){var b=a.parentNode;return b&&b.parentNode&&b.parentNode.selectedIndex,null}}),n.each(["tabIndex","readOnly","maxLength","cellSpacing","cellPadding","rowSpan","colSpan","useMap","frameBorder","contentEditable"],function(){n.propFix[this.toLowerCase()]=this});var ac=/[\t\r\n\f]/g;n.fn.extend({addClass:function(a){var b,c,d,e,f,g,h="string"==typeof a&&a,i=0,j=this.length;if(n.isFunction(a))return this.each(function(b){n(this).addClass(a.call(this,b,this.className))});if(h)for(b=(a||"").match(E)||[];j>i;i++)if(c=this[i],d=1===c.nodeType&&(c.className?(" "+c.className+" ").replace(ac," "):" ")){f=0;while(e=b[f++])d.indexOf(" "+e+" ")<0&&(d+=e+" ");g=n.trim(d),c.className!==g&&(c.className=g)}return this},removeClass:function(a){var b,c,d,e,f,g,h=0===arguments.length||"string"==typeof a&&a,i=0,j=this.length;if(n.isFunction(a))return this.each(function(b){n(this).removeClass(a.call(this,b,this.className))});if(h)for(b=(a||"").match(E)||[];j>i;i++)if(c=this[i],d=1===c.nodeType&&(c.className?(" "+c.className+" ").replace(ac," "):"")){f=0;while(e=b[f++])while(d.indexOf(" "+e+" ")>=0)d=d.replace(" "+e+" "," ");g=a?n.trim(d):"",c.className!==g&&(c.className=g)}return this},toggleClass:function(a,b){var c=typeof a;return"boolean"==typeof b&&"string"===c?b?this.addClass(a):this.removeClass(a):this.each(n.isFunction(a)?function(c){n(this).toggleClass(a.call(this,c,this.className,b),b)}:function(){if("string"===c){var b,d=0,e=n(this),f=a.match(E)||[];while(b=f[d++])e.hasClass(b)?e.removeClass(b):e.addClass(b)}else(c===U||"boolean"===c)&&(this.className&&L.set(this,"__className__",this.className),this.className=this.className||a===!1?"":L.get(this,"__className__")||"")})},hasClass:function(a){for(var b=" "+a+" ",c=0,d=this.length;d>c;c++)if(1===this[c].nodeType&&(" "+this[c].className+" ").replace(ac," ").indexOf(b)>=0)return!0;return!1}});var bc=/\r/g;n.fn.extend({val:function(a){var b,c,d,e=this[0];{if(arguments.length)return d=n.isFunction(a),this.each(function(c){var e;1===this.nodeType&&(e=d?a.call(this,c,n(this).val()):a,null==e?e="":"number"==typeof e?e+="":n.isArray(e)&&(e=n.map(e,function(a){return null==a?"":a+""})),b=n.valHooks[this.type]||n.valHooks[this.nodeName.toLowerCase()],b&&"set"in b&&void 0!==b.set(this,e,"value")||(this.value=e))});if(e)return b=n.valHooks[e.type]||n.valHooks[e.nodeName.toLowerCase()],b&&"get"in b&&void 0!==(c=b.get(e,"value"))?c:(c=e.value,"string"==typeof c?c.replace(bc,""):null==c?"":c)}}}),n.extend({valHooks:{option:{get:function(a){var b=n.find.attr(a,"value");return null!=b?b:n.trim(n.text(a))}},select:{get:function(a){for(var b,c,d=a.options,e=a.selectedIndex,f="select-one"===a.type||0>e,g=f?null:[],h=f?e+1:d.length,i=0>e?h:f?e:0;h>i;i++)if(c=d[i],!(!c.selected&&i!==e||(k.optDisabled?c.disabled:null!==c.getAttribute("disabled"))||c.parentNode.disabled&&n.nodeName(c.parentNode,"optgroup"))){if(b=n(c).val(),f)return b;g.push(b)}return g},set:function(a,b){var c,d,e=a.options,f=n.makeArray(b),g=e.length;while(g--)d=e[g],(d.selected=n.inArray(d.value,f)>=0)&&(c=!0);return c||(a.selectedIndex=-1),f}}}}),n.each(["radio","checkbox"],function(){n.valHooks[this]={set:function(a,b){return n.isArray(b)?a.checked=n.inArray(n(a).val(),b)>=0:void 0}},k.checkOn||(n.valHooks[this].get=function(a){return null===a.getAttribute("value")?"on":a.value})}),n.each("blur focus focusin focusout load resize scroll unload click dblclick mousedown mouseup mousemove mouseover mouseout mouseenter mouseleave change select submit keydown keypress keyup error contextmenu".split(" "),function(a,b){n.fn[b]=function(a,c){return arguments.length>0?this.on(b,null,a,c):this.trigger(b)}}),n.fn.extend({hover:function(a,b){return this.mouseenter(a).mouseleave(b||a)},bind:function(a,b,c){return this.on(a,null,b,c)},unbind:function(a,b){return this.off(a,null,b)},delegate:function(a,b,c,d){return this.on(b,a,c,d)},undelegate:function(a,b,c){return 1===arguments.length?this.off(a,"**"):this.off(b,a||"**",c)}});var cc=n.now(),dc=/\?/;n.parseJSON=function(a){return JSON.parse(a+"")},n.parseXML=function(a){var b,c;if(!a||"string"!=typeof a)return null;try{c=new DOMParser,b=c.parseFromString(a,"text/xml")}catch(d){b=void 0}return(!b||b.getElementsByTagName("parsererror").length)&&n.error("Invalid XML: "+a),b};var ec=/#.*$/,fc=/([?&])_=[^&]*/,gc=/^(.*?):[ \t]*([^\r\n]*)$/gm,hc=/^(?:about|app|app-storage|.+-extension|file|res|widget):$/,ic=/^(?:GET|HEAD)$/,jc=/^\/\//,kc=/^([\w.+-]+:)(?:\/\/(?:[^\/?#]*@|)([^\/?#:]*)(?::(\d+)|)|)/,lc={},mc={},nc="*/".concat("*"),oc=a.location.href,pc=kc.exec(oc.toLowerCase())||[];function qc(a){return function(b,c){"string"!=typeof b&&(c=b,b="*");var d,e=0,f=b.toLowerCase().match(E)||[];if(n.isFunction(c))while(d=f[e++])"+"===d[0]?(d=d.slice(1)||"*",(a[d]=a[d]||[]).unshift(c)):(a[d]=a[d]||[]).push(c)}}function rc(a,b,c,d){var e={},f=a===mc;function g(h){var i;return e[h]=!0,n.each(a[h]||[],function(a,h){var j=h(b,c,d);return"string"!=typeof j||f||e[j]?f?!(i=j):void 0:(b.dataTypes.unshift(j),g(j),!1)}),i}return g(b.dataTypes[0])||!e["*"]&&g("*")}function sc(a,b){var c,d,e=n.ajaxSettings.flatOptions||{};for(c in b)void 0!==b[c]&&((e[c]?a:d||(d={}))[c]=b[c]);return d&&n.extend(!0,a,d),a}function tc(a,b,c){var d,e,f,g,h=a.contents,i=a.dataTypes;while("*"===i[0])i.shift(),void 0===d&&(d=a.mimeType||b.getResponseHeader("Content-Type"));if(d)for(e in h)if(h[e]&&h[e].test(d)){i.unshift(e);break}if(i[0]in c)f=i[0];else{for(e in c){if(!i[0]||a.converters[e+" "+i[0]]){f=e;break}g||(g=e)}f=f||g}return f?(f!==i[0]&&i.unshift(f),c[f]):void 0}function uc(a,b,c,d){var e,f,g,h,i,j={},k=a.dataTypes.slice();if(k[1])for(g in a.converters)j[g.toLowerCase()]=a.converters[g];f=k.shift();while(f)if(a.responseFields[f]&&(c[a.responseFields[f]]=b),!i&&d&&a.dataFilter&&(b=a.dataFilter(b,a.dataType)),i=f,f=k.shift())if("*"===f)f=i;else if("*"!==i&&i!==f){if(g=j[i+" "+f]||j["* "+f],!g)for(e in j)if(h=e.split(" "),h[1]===f&&(g=j[i+" "+h[0]]||j["* "+h[0]])){g===!0?g=j[e]:j[e]!==!0&&(f=h[0],k.unshift(h[1]));break}if(g!==!0)if(g&&a["throws"])b=g(b);else try{b=g(b)}catch(l){return{state:"parsererror",error:g?l:"No conversion from "+i+" to "+f}}}return{state:"success",data:b}}n.extend({active:0,lastModified:{},etag:{},ajaxSettings:{url:oc,type:"GET",isLocal:hc.test(pc[1]),global:!0,processData:!0,async:!0,contentType:"application/x-www-form-urlencoded; charset=UTF-8",accepts:{"*":nc,text:"text/plain",html:"text/html",xml:"application/xml, text/xml",json:"application/json, text/javascript"},contents:{xml:/xml/,html:/html/,json:/json/},responseFields:{xml:"responseXML",text:"responseText",json:"responseJSON"},converters:{"* text":String,"text html":!0,"text json":n.parseJSON,"text xml":n.parseXML},flatOptions:{url:!0,context:!0}},ajaxSetup:function(a,b){return b?sc(sc(a,n.ajaxSettings),b):sc(n.ajaxSettings,a)},ajaxPrefilter:qc(lc),ajaxTransport:qc(mc),ajax:function(a,b){"object"==typeof a&&(b=a,a=void 0),b=b||{};var c,d,e,f,g,h,i,j,k=n.ajaxSetup({},b),l=k.context||k,m=k.context&&(l.nodeType||l.jquery)?n(l):n.event,o=n.Deferred(),p=n.Callbacks("once memory"),q=k.statusCode||{},r={},s={},t=0,u="canceled",v={readyState:0,getResponseHeader:function(a){var b;if(2===t){if(!f){f={};while(b=gc.exec(e))f[b[1].toLowerCase()]=b[2]}b=f[a.toLowerCase()]}return null==b?null:b},getAllResponseHeaders:function(){return 2===t?e:null},setRequestHeader:function(a,b){var c=a.toLowerCase();return t||(a=s[c]=s[c]||a,r[a]=b),this},overrideMimeType:function(a){return t||(k.mimeType=a),this},statusCode:function(a){var b;if(a)if(2>t)for(b in a)q[b]=[q[b],a[b]];else v.always(a[v.status]);return this},abort:function(a){var b=a||u;return c&&c.abort(b),x(0,b),this}};if(o.promise(v).complete=p.add,v.success=v.done,v.error=v.fail,k.url=((a||k.url||oc)+"").replace(ec,"").replace(jc,pc[1]+"//"),k.type=b.method||b.type||k.method||k.type,k.dataTypes=n.trim(k.dataType||"*").toLowerCase().match(E)||[""],null==k.crossDomain&&(h=kc.exec(k.url.toLowerCase()),k.crossDomain=!(!h||h[1]===pc[1]&&h[2]===pc[2]&&(h[3]||("http:"===h[1]?"80":"443"))===(pc[3]||("http:"===pc[1]?"80":"443")))),k.data&&k.processData&&"string"!=typeof k.data&&(k.data=n.param(k.data,k.traditional)),rc(lc,k,b,v),2===t)return v;i=n.event&&k.global,i&&0===n.active++&&n.event.trigger("ajaxStart"),k.type=k.type.toUpperCase(),k.hasContent=!ic.test(k.type),d=k.url,k.hasContent||(k.data&&(d=k.url+=(dc.test(d)?"&":"?")+k.data,delete k.data),k.cache===!1&&(k.url=fc.test(d)?d.replace(fc,"$1_="+cc++):d+(dc.test(d)?"&":"?")+"_="+cc++)),k.ifModified&&(n.lastModified[d]&&v.setRequestHeader("If-Modified-Since",n.lastModified[d]),n.etag[d]&&v.setRequestHeader("If-None-Match",n.etag[d])),(k.data&&k.hasContent&&k.contentType!==!1||b.contentType)&&v.setRequestHeader("Content-Type",k.contentType),v.setRequestHeader("Accept",k.dataTypes[0]&&k.accepts[k.dataTypes[0]]?k.accepts[k.dataTypes[0]]+("*"!==k.dataTypes[0]?", "+nc+"; q=0.01":""):k.accepts["*"]);for(j in k.headers)v.setRequestHeader(j,k.headers[j]);if(k.beforeSend&&(k.beforeSend.call(l,v,k)===!1||2===t))return v.abort();u="abort";for(j in{success:1,error:1,complete:1})v[j](k[j]);if(c=rc(mc,k,b,v)){v.readyState=1,i&&m.trigger("ajaxSend",[v,k]),k.async&&k.timeout>0&&(g=setTimeout(function(){v.abort("timeout")},k.timeout));try{t=1,c.send(r,x)}catch(w){if(!(2>t))throw w;x(-1,w)}}else x(-1,"No Transport");function x(a,b,f,h){var j,r,s,u,w,x=b;2!==t&&(t=2,g&&clearTimeout(g),c=void 0,e=h||"",v.readyState=a>0?4:0,j=a>=200&&300>a||304===a,f&&(u=tc(k,v,f)),u=uc(k,u,v,j),j?(k.ifModified&&(w=v.getResponseHeader("Last-Modified"),w&&(n.lastModified[d]=w),w=v.getResponseHeader("etag"),w&&(n.etag[d]=w)),204===a||"HEAD"===k.type?x="nocontent":304===a?x="notmodified":(x=u.state,r=u.data,s=u.error,j=!s)):(s=x,(a||!x)&&(x="error",0>a&&(a=0))),v.status=a,v.statusText=(b||x)+"",j?o.resolveWith(l,[r,x,v]):o.rejectWith(l,[v,x,s]),v.statusCode(q),q=void 0,i&&m.trigger(j?"ajaxSuccess":"ajaxError",[v,k,j?r:s]),p.fireWith(l,[v,x]),i&&(m.trigger("ajaxComplete",[v,k]),--n.active||n.event.trigger("ajaxStop")))}return v},getJSON:function(a,b,c){return n.get(a,b,c,"json")},getScript:function(a,b){return n.get(a,void 0,b,"script")}}),n.each(["get","post"],function(a,b){n[b]=function(a,c,d,e){return n.isFunction(c)&&(e=e||d,d=c,c=void 0),n.ajax({url:a,type:b,dataType:e,data:c,success:d})}}),n._evalUrl=function(a){return n.ajax({url:a,type:"GET",dataType:"script",async:!1,global:!1,"throws":!0})},n.fn.extend({wrapAll:function(a){var b;return n.isFunction(a)?this.each(function(b){n(this).wrapAll(a.call(this,b))}):(this[0]&&(b=n(a,this[0].ownerDocument).eq(0).clone(!0),this[0].parentNode&&b.insertBefore(this[0]),b.map(function(){var a=this;while(a.firstElementChild)a=a.firstElementChild;return a}).append(this)),this)},wrapInner:function(a){return this.each(n.isFunction(a)?function(b){n(this).wrapInner(a.call(this,b))}:function(){var b=n(this),c=b.contents();c.length?c.wrapAll(a):b.append(a)})},wrap:function(a){var b=n.isFunction(a);return this.each(function(c){n(this).wrapAll(b?a.call(this,c):a)})},unwrap:function(){return this.parent().each(function(){n.nodeName(this,"body")||n(this).replaceWith(this.childNodes)}).end()}}),n.expr.filters.hidden=function(a){return a.offsetWidth<=0&&a.offsetHeight<=0},n.expr.filters.visible=function(a){return!n.expr.filters.hidden(a)};var vc=/%20/g,wc=/\[\]$/,xc=/\r?\n/g,yc=/^(?:submit|button|image|reset|file)$/i,zc=/^(?:input|select|textarea|keygen)/i;function Ac(a,b,c,d){var e;if(n.isArray(b))n.each(b,function(b,e){c||wc.test(a)?d(a,e):Ac(a+"["+("object"==typeof e?b:"")+"]",e,c,d)});else if(c||"object"!==n.type(b))d(a,b);else for(e in b)Ac(a+"["+e+"]",b[e],c,d)}n.param=function(a,b){var c,d=[],e=function(a,b){b=n.isFunction(b)?b():null==b?"":b,d[d.length]=encodeURIComponent(a)+"="+encodeURIComponent(b)};if(void 0===b&&(b=n.ajaxSettings&&n.ajaxSettings.traditional),n.isArray(a)||a.jquery&&!n.isPlainObject(a))n.each(a,function(){e(this.name,this.value)});else for(c in a)Ac(c,a[c],b,e);return d.join("&").replace(vc,"+")},n.fn.extend({serialize:function(){return n.param(this.serializeArray())},serializeArray:function(){return this.map(function(){var a=n.prop(this,"elements");return a?n.makeArray(a):this}).filter(function(){var a=this.type;return this.name&&!n(this).is(":disabled")&&zc.test(this.nodeName)&&!yc.test(a)&&(this.checked||!T.test(a))}).map(function(a,b){var c=n(this).val();return null==c?null:n.isArray(c)?n.map(c,function(a){return{name:b.name,value:a.replace(xc,"\r\n")}}):{name:b.name,value:c.replace(xc,"\r\n")}}).get()}}),n.ajaxSettings.xhr=function(){try{return new XMLHttpRequest}catch(a){}};var Bc=0,Cc={},Dc={0:200,1223:204},Ec=n.ajaxSettings.xhr();a.attachEvent&&a.attachEvent("onunload",function(){for(var a in Cc)Cc[a]()}),k.cors=!!Ec&&"withCredentials"in Ec,k.ajax=Ec=!!Ec,n.ajaxTransport(function(a){var b;return k.cors||Ec&&!a.crossDomain?{send:function(c,d){var e,f=a.xhr(),g=++Bc;if(f.open(a.type,a.url,a.async,a.username,a.password),a.xhrFields)for(e in a.xhrFields)f[e]=a.xhrFields[e];a.mimeType&&f.overrideMimeType&&f.overrideMimeType(a.mimeType),a.crossDomain||c["X-Requested-With"]||(c["X-Requested-With"]="XMLHttpRequest");for(e in c)f.setRequestHeader(e,c[e]);b=function(a){return function(){b&&(delete Cc[g],b=f.onload=f.onerror=null,"abort"===a?f.abort():"error"===a?d(f.status,f.statusText):d(Dc[f.status]||f.status,f.statusText,"string"==typeof f.responseText?{text:f.responseText}:void 0,f.getAllResponseHeaders()))}},f.onload=b(),f.onerror=b("error"),b=Cc[g]=b("abort");try{f.send(a.hasContent&&a.data||null)}catch(h){if(b)throw h}},abort:function(){b&&b()}}:void 0}),n.ajaxSetup({accepts:{script:"text/javascript, application/javascript, application/ecmascript, application/x-ecmascript"},contents:{script:/(?:java|ecma)script/},converters:{"text script":function(a){return n.globalEval(a),a}}}),n.ajaxPrefilter("script",function(a){void 0===a.cache&&(a.cache=!1),a.crossDomain&&(a.type="GET")}),n.ajaxTransport("script",function(a){if(a.crossDomain){var b,c;return{send:function(d,e){b=n("<script>").prop({async:!0,charset:a.scriptCharset,src:a.url}).on("load error",c=function(a){b.remove(),c=null,a&&e("error"===a.type?404:200,a.type)}),l.head.appendChild(b[0])},abort:function(){c&&c()}}}});var Fc=[],Gc=/(=)\?(?=&|$)|\?\?/;n.ajaxSetup({jsonp:"callback",jsonpCallback:function(){var a=Fc.pop()||n.expando+"_"+cc++;return this[a]=!0,a}}),n.ajaxPrefilter("json jsonp",function(b,c,d){var e,f,g,h=b.jsonp!==!1&&(Gc.test(b.url)?"url":"string"==typeof b.data&&!(b.contentType||"").indexOf("application/x-www-form-urlencoded")&&Gc.test(b.data)&&"data");return h||"jsonp"===b.dataTypes[0]?(e=b.jsonpCallback=n.isFunction(b.jsonpCallback)?b.jsonpCallback():b.jsonpCallback,h?b[h]=b[h].replace(Gc,"$1"+e):b.jsonp!==!1&&(b.url+=(dc.test(b.url)?"&":"?")+b.jsonp+"="+e),b.converters["script json"]=function(){return g||n.error(e+" was not called"),g[0]},b.dataTypes[0]="json",f=a[e],a[e]=function(){g=arguments},d.always(function(){a[e]=f,b[e]&&(b.jsonpCallback=c.jsonpCallback,Fc.push(e)),g&&n.isFunction(f)&&f(g[0]),g=f=void 0}),"script"):void 0}),n.parseHTML=function(a,b,c){if(!a||"string"!=typeof a)return null;"boolean"==typeof b&&(c=b,b=!1),b=b||l;var d=v.exec(a),e=!c&&[];return d?[b.createElement(d[1])]:(d=n.buildFragment([a],b,e),e&&e.length&&n(e).remove(),n.merge([],d.childNodes))};var Hc=n.fn.load;n.fn.load=function(a,b,c){if("string"!=typeof a&&Hc)return Hc.apply(this,arguments);var d,e,f,g=this,h=a.indexOf(" ");return h>=0&&(d=n.trim(a.slice(h)),a=a.slice(0,h)),n.isFunction(b)?(c=b,b=void 0):b&&"object"==typeof b&&(e="POST"),g.length>0&&n.ajax({url:a,type:e,dataType:"html",data:b}).done(function(a){f=arguments,g.html(d?n("<div>").append(n.parseHTML(a)).find(d):a)}).complete(c&&function(a,b){g.each(c,f||[a.responseText,b,a])}),this},n.each(["ajaxStart","ajaxStop","ajaxComplete","ajaxError","ajaxSuccess","ajaxSend"],function(a,b){n.fn[b]=function(a){return this.on(b,a)}}),n.expr.filters.animated=function(a){return n.grep(n.timers,function(b){return a===b.elem}).length};var Ic=a.document.documentElement;function Jc(a){return n.isWindow(a)?a:9===a.nodeType&&a.defaultView}n.offset={setOffset:function(a,b,c){var d,e,f,g,h,i,j,k=n.css(a,"position"),l=n(a),m={};"static"===k&&(a.style.position="relative"),h=l.offset(),f=n.css(a,"top"),i=n.css(a,"left"),j=("absolute"===k||"fixed"===k)&&(f+i).indexOf("auto")>-1,j?(d=l.position(),g=d.top,e=d.left):(g=parseFloat(f)||0,e=parseFloat(i)||0),n.isFunction(b)&&(b=b.call(a,c,h)),null!=b.top&&(m.top=b.top-h.top+g),null!=b.left&&(m.left=b.left-h.left+e),"using"in b?b.using.call(a,m):l.css(m)}},n.fn.extend({offset:function(a){if(arguments.length)return void 0===a?this:this.each(function(b){n.offset.setOffset(this,a,b)});var b,c,d=this[0],e={top:0,left:0},f=d&&d.ownerDocument;if(f)return b=f.documentElement,n.contains(b,d)?(typeof d.getBoundingClientRect!==U&&(e=d.getBoundingClientRect()),c=Jc(f),{top:e.top+c.pageYOffset-b.clientTop,left:e.left+c.pageXOffset-b.clientLeft}):e},position:function(){if(this[0]){var a,b,c=this[0],d={top:0,left:0};return"fixed"===n.css(c,"position")?b=c.getBoundingClientRect():(a=this.offsetParent(),b=this.offset(),n.nodeName(a[0],"html")||(d=a.offset()),d.top+=n.css(a[0],"borderTopWidth",!0),d.left+=n.css(a[0],"borderLeftWidth",!0)),{top:b.top-d.top-n.css(c,"marginTop",!0),left:b.left-d.left-n.css(c,"marginLeft",!0)}}},offsetParent:function(){return this.map(function(){var a=this.offsetParent||Ic;while(a&&!n.nodeName(a,"html")&&"static"===n.css(a,"position"))a=a.offsetParent;return a||Ic})}}),n.each({scrollLeft:"pageXOffset",scrollTop:"pageYOffset"},function(b,c){var d="pageYOffset"===c;n.fn[b]=function(e){return J(this,function(b,e,f){var g=Jc(b);return void 0===f?g?g[c]:b[e]:void(g?g.scrollTo(d?a.pageXOffset:f,d?f:a.pageYOffset):b[e]=f)},b,e,arguments.length,null)}}),n.each(["top","left"],function(a,b){n.cssHooks[b]=yb(k.pixelPosition,function(a,c){return c?(c=xb(a,b),vb.test(c)?n(a).position()[b]+"px":c):void 0})}),n.each({Height:"height",Width:"width"},function(a,b){n.each({padding:"inner"+a,content:b,"":"outer"+a},function(c,d){n.fn[d]=function(d,e){var f=arguments.length&&(c||"boolean"!=typeof d),g=c||(d===!0||e===!0?"margin":"border");return J(this,function(b,c,d){var e;return n.isWindow(b)?b.document.documentElement["client"+a]:9===b.nodeType?(e=b.documentElement,Math.max(b.body["scroll"+a],e["scroll"+a],b.body["offset"+a],e["offset"+a],e["client"+a])):void 0===d?n.css(b,c,g):n.style(b,c,d,g)},b,f?d:void 0,f,null)}})}),n.fn.size=function(){return this.length},n.fn.andSelf=n.fn.addBack,"function"==typeof define&&define.amd&&define("jquery",[],function(){return n});var Kc=a.jQuery,Lc=a.$;return n.noConflict=function(b){return a.$===n&&(a.$=Lc),b&&a.jQuery===n&&(a.jQuery=Kc),n},typeof b===U&&(a.jQuery=a.$=n),n});

!function(a,b,c,d){function e(b,c){this.settings=null,this.options=a.extend({},e.Defaults,c),this.$element=a(b),this.drag=a.extend({},m),this.state=a.extend({},n),this.e=a.extend({},o),this._plugins={},this._supress={},this._current=null,this._speed=null,this._coordinates=[],this._breakpoint=null,this._width=null,this._items=[],this._clones=[],this._mergers=[],this._invalidated={},this._pipe=[],a.each(e.Plugins,a.proxy(function(a,b){this._plugins[a[0].toLowerCase()+a.slice(1)]=new b(this)},this)),a.each(e.Pipe,a.proxy(function(b,c){this._pipe.push({filter:c.filter,run:a.proxy(c.run,this)})},this)),this.setup(),this.initialize()}function f(a){if(a.touches!==d)return{x:a.touches[0].pageX,y:a.touches[0].pageY};if(a.touches===d){if(a.pageX!==d)return{x:a.pageX,y:a.pageY};if(a.pageX===d)return{x:a.clientX,y:a.clientY}}}function g(a){var b,d,e=c.createElement("div"),f=a;for(b in f)if(d=f[b],"undefined"!=typeof e.style[d])return e=null,[d,b];return[!1]}function h(){return g(["transition","WebkitTransition","MozTransition","OTransition"])[1]}function i(){return g(["transform","WebkitTransform","MozTransform","OTransform","msTransform"])[0]}function j(){return g(["perspective","webkitPerspective","MozPerspective","OPerspective","MsPerspective"])[0]}function k(){return"ontouchstart"in b||!!navigator.msMaxTouchPoints}function l(){return b.navigator.msPointerEnabled}var m,n,o;m={start:0,startX:0,startY:0,current:0,currentX:0,currentY:0,offsetX:0,offsetY:0,distance:null,startTime:0,endTime:0,updatedX:0,targetEl:null},n={isTouch:!1,isScrolling:!1,isSwiping:!1,direction:!1,inMotion:!1},o={_onDragStart:null,_onDragMove:null,_onDragEnd:null,_transitionEnd:null,_resizer:null,_responsiveCall:null,_goToLoop:null,_checkVisibile:null},e.Defaults={items:3,loop:!1,center:!1,mouseDrag:!0,touchDrag:!0,pullDrag:!0,freeDrag:!1,margin:0,stagePadding:0,merge:!1,mergeFit:!0,autoWidth:!1,startPosition:0,rtl:!1,smartSpeed:250,fluidSpeed:!1,dragEndSpeed:!1,responsive:{},responsiveRefreshRate:200,responsiveBaseElement:b,responsiveClass:!1,fallbackEasing:"swing",info:!1,nestedItemSelector:!1,itemElement:"div",stageElement:"div",themeClass:"owl-theme",baseClass:"owl-carousel",itemClass:"owl-item",centerClass:"center",activeClass:"active"},e.Width={Default:"default",Inner:"inner",Outer:"outer"},e.Plugins={},e.Pipe=[{filter:["width","items","settings"],run:function(a){a.current=this._items&&this._items[this.relative(this._current)]}},{filter:["items","settings"],run:function(){var a=this._clones,b=this.$stage.children(".cloned");(b.length!==a.length||!this.settings.loop&&a.length>0)&&(this.$stage.children(".cloned").remove(),this._clones=[])}},{filter:["items","settings"],run:function(){var a,b,c=this._clones,d=this._items,e=this.settings.loop?c.length-Math.max(2*this.settings.items,4):0;for(a=0,b=Math.abs(e/2);b>a;a++)e>0?(this.$stage.children().eq(d.length+c.length-1).remove(),c.pop(),this.$stage.children().eq(0).remove(),c.pop()):(c.push(c.length/2),this.$stage.append(d[c[c.length-1]].clone().addClass("cloned")),c.push(d.length-1-(c.length-1)/2),this.$stage.prepend(d[c[c.length-1]].clone().addClass("cloned")))}},{filter:["width","items","settings"],run:function(){var a,b,c,d=this.settings.rtl?1:-1,e=(this.width()/this.settings.items).toFixed(3),f=0;for(this._coordinates=[],b=0,c=this._clones.length+this._items.length;c>b;b++)a=this._mergers[this.relative(b)],a=this.settings.mergeFit&&Math.min(a,this.settings.items)||a,f+=(this.settings.autoWidth?this._items[this.relative(b)].width()+this.settings.margin:e*a)*d,this._coordinates.push(f)}},{filter:["width","items","settings"],run:function(){var b,c,d=(this.width()/this.settings.items).toFixed(3),e={width:Math.abs(this._coordinates[this._coordinates.length-1])+2*this.settings.stagePadding,"padding-left":this.settings.stagePadding||"","padding-right":this.settings.stagePadding||""};if(this.$stage.css(e),e={width:this.settings.autoWidth?"auto":d-this.settings.margin},e[this.settings.rtl?"margin-left":"margin-right"]=this.settings.margin,!this.settings.autoWidth&&a.grep(this._mergers,function(a){return a>1}).length>0)for(b=0,c=this._coordinates.length;c>b;b++)e.width=Math.abs(this._coordinates[b])-Math.abs(this._coordinates[b-1]||0)-this.settings.margin,this.$stage.children().eq(b).css(e);else this.$stage.children().css(e)}},{filter:["width","items","settings"],run:function(a){a.current&&this.reset(this.$stage.children().index(a.current))}},{filter:["position"],run:function(){this.animate(this.coordinates(this._current))}},{filter:["width","position","items","settings"],run:function(){var a,b,c,d,e=this.settings.rtl?1:-1,f=2*this.settings.stagePadding,g=this.coordinates(this.current())+f,h=g+this.width()*e,i=[];for(c=0,d=this._coordinates.length;d>c;c++)a=this._coordinates[c-1]||0,b=Math.abs(this._coordinates[c])+f*e,(this.op(a,"<=",g)&&this.op(a,">",h)||this.op(b,"<",g)&&this.op(b,">",h))&&i.push(c);this.$stage.children("."+this.settings.activeClass).removeClass(this.settings.activeClass),this.$stage.children(":eq("+i.join("), :eq(")+")").addClass(this.settings.activeClass),this.settings.center&&(this.$stage.children("."+this.settings.centerClass).removeClass(this.settings.centerClass),this.$stage.children().eq(this.current()).addClass(this.settings.centerClass))}}],e.prototype.initialize=function(){if(this.trigger("initialize"),this.$element.addClass(this.settings.baseClass).addClass(this.settings.themeClass).toggleClass("owl-rtl",this.settings.rtl),this.browserSupport(),this.settings.autoWidth&&this.state.imagesLoaded!==!0){var b,c,e;if(b=this.$element.find("img"),c=this.settings.nestedItemSelector?"."+this.settings.nestedItemSelector:d,e=this.$element.children(c).width(),b.length&&0>=e)return this.preloadAutoWidthImages(b),!1}this.$element.addClass("owl-loading"),this.$stage=a("<"+this.settings.stageElement+' class="owl-stage"/>').wrap('<div class="owl-stage-outer">'),this.$element.append(this.$stage.parent()),this.replace(this.$element.children().not(this.$stage.parent())),this._width=this.$element.width(),this.refresh(),this.$element.removeClass("owl-loading").addClass("owl-loaded"),this.eventsCall(),this.internalEvents(),this.addTriggerableEvents(),this.trigger("initialized")},e.prototype.setup=function(){var b=this.viewport(),c=this.options.responsive,d=-1,e=null;c?(a.each(c,function(a){b>=a&&a>d&&(d=Number(a))}),e=a.extend({},this.options,c[d]),delete e.responsive,e.responsiveClass&&this.$element.attr("class",function(a,b){return b.replace(/\b owl-responsive-\S+/g,"")}).addClass("owl-responsive-"+d)):e=a.extend({},this.options),(null===this.settings||this._breakpoint!==d)&&(this.trigger("change",{property:{name:"settings",value:e}}),this._breakpoint=d,this.settings=e,this.invalidate("settings"),this.trigger("changed",{property:{name:"settings",value:this.settings}}))},e.prototype.optionsLogic=function(){this.$element.toggleClass("owl-center",this.settings.center),this.settings.loop&&this._items.length<this.settings.items&&(this.settings.loop=!1),this.settings.autoWidth&&(this.settings.stagePadding=!1,this.settings.merge=!1)},e.prototype.prepare=function(b){var c=this.trigger("prepare",{content:b});return c.data||(c.data=a("<"+this.settings.itemElement+"/>").addClass(this.settings.itemClass).append(b)),this.trigger("prepared",{content:c.data}),c.data},e.prototype.update=function(){for(var b=0,c=this._pipe.length,d=a.proxy(function(a){return this[a]},this._invalidated),e={};c>b;)(this._invalidated.all||a.grep(this._pipe[b].filter,d).length>0)&&this._pipe[b].run(e),b++;this._invalidated={}},e.prototype.width=function(a){switch(a=a||e.Width.Default){case e.Width.Inner:case e.Width.Outer:return this._width;default:return this._width-2*this.settings.stagePadding+this.settings.margin}},e.prototype.refresh=function(){if(0===this._items.length)return!1;(new Date).getTime();this.trigger("refresh"),this.setup(),this.optionsLogic(),this.$stage.addClass("owl-refresh"),this.update(),this.$stage.removeClass("owl-refresh"),this.state.orientation=b.orientation,this.watchVisibility(),this.trigger("refreshed")},e.prototype.eventsCall=function(){this.e._onDragStart=a.proxy(function(a){this.onDragStart(a)},this),this.e._onDragMove=a.proxy(function(a){this.onDragMove(a)},this),this.e._onDragEnd=a.proxy(function(a){this.onDragEnd(a)},this),this.e._onResize=a.proxy(function(a){this.onResize(a)},this),this.e._transitionEnd=a.proxy(function(a){this.transitionEnd(a)},this),this.e._preventClick=a.proxy(function(a){this.preventClick(a)},this)},e.prototype.onThrottledResize=function(){b.clearTimeout(this.resizeTimer),this.resizeTimer=b.setTimeout(this.e._onResize,this.settings.responsiveRefreshRate)},e.prototype.onResize=function(){return this._items.length?this._width===this.$element.width()?!1:this.trigger("resize").isDefaultPrevented()?!1:(this._width=this.$element.width(),this.invalidate("width"),this.refresh(),void this.trigger("resized")):!1},e.prototype.eventsRouter=function(a){var b=a.type;"mousedown"===b||"touchstart"===b?this.onDragStart(a):"mousemove"===b||"touchmove"===b?this.onDragMove(a):"mouseup"===b||"touchend"===b?this.onDragEnd(a):"touchcancel"===b&&this.onDragEnd(a)},e.prototype.internalEvents=function(){var c=(k(),l());this.settings.mouseDrag?(this.$stage.on("mousedown",a.proxy(function(a){this.eventsRouter(a)},this)),this.$stage.on("dragstart",function(){return!1}),this.$stage.get(0).onselectstart=function(){return!1}):this.$element.addClass("owl-text-select-on"),this.settings.touchDrag&&!c&&this.$stage.on("touchstart touchcancel",a.proxy(function(a){this.eventsRouter(a)},this)),this.transitionEndVendor&&this.on(this.$stage.get(0),this.transitionEndVendor,this.e._transitionEnd,!1),this.settings.responsive!==!1&&this.on(b,"resize",a.proxy(this.onThrottledResize,this))},e.prototype.onDragStart=function(d){var e,g,h,i;if(e=d.originalEvent||d||b.event,3===e.which||this.state.isTouch)return!1;if("mousedown"===e.type&&this.$stage.addClass("owl-grab"),this.trigger("drag"),this.drag.startTime=(new Date).getTime(),this.speed(0),this.state.isTouch=!0,this.state.isScrolling=!1,this.state.isSwiping=!1,this.drag.distance=0,g=f(e).x,h=f(e).y,this.drag.offsetX=this.$stage.position().left,this.drag.offsetY=this.$stage.position().top,this.settings.rtl&&(this.drag.offsetX=this.$stage.position().left+this.$stage.width()-this.width()+this.settings.margin),this.state.inMotion&&this.support3d)i=this.getTransformProperty(),this.drag.offsetX=i,this.animate(i),this.state.inMotion=!0;else if(this.state.inMotion&&!this.support3d)return this.state.inMotion=!1,!1;this.drag.startX=g-this.drag.offsetX,this.drag.startY=h-this.drag.offsetY,this.drag.start=g-this.drag.startX,this.drag.targetEl=e.target||e.srcElement,this.drag.updatedX=this.drag.start,("IMG"===this.drag.targetEl.tagName||"A"===this.drag.targetEl.tagName)&&(this.drag.targetEl.draggable=!1),a(c).on("mousemove.owl.dragEvents mouseup.owl.dragEvents touchmove.owl.dragEvents touchend.owl.dragEvents",a.proxy(function(a){this.eventsRouter(a)},this))},e.prototype.onDragMove=function(a){var c,e,g,h,i,j;this.state.isTouch&&(this.state.isScrolling||(c=a.originalEvent||a||b.event,e=f(c).x,g=f(c).y,this.drag.currentX=e-this.drag.startX,this.drag.currentY=g-this.drag.startY,this.drag.distance=this.drag.currentX-this.drag.offsetX,this.drag.distance<0?this.state.direction=this.settings.rtl?"right":"left":this.drag.distance>0&&(this.state.direction=this.settings.rtl?"left":"right"),this.settings.loop?this.op(this.drag.currentX,">",this.coordinates(this.minimum()))&&"right"===this.state.direction?this.drag.currentX-=(this.settings.center&&this.coordinates(0))-this.coordinates(this._items.length):this.op(this.drag.currentX,"<",this.coordinates(this.maximum()))&&"left"===this.state.direction&&(this.drag.currentX+=(this.settings.center&&this.coordinates(0))-this.coordinates(this._items.length)):(h=this.coordinates(this.settings.rtl?this.maximum():this.minimum()),i=this.coordinates(this.settings.rtl?this.minimum():this.maximum()),j=this.settings.pullDrag?this.drag.distance/5:0,this.drag.currentX=Math.max(Math.min(this.drag.currentX,h+j),i+j)),(this.drag.distance>8||this.drag.distance<-8)&&(c.preventDefault!==d?c.preventDefault():c.returnValue=!1,this.state.isSwiping=!0),this.drag.updatedX=this.drag.currentX,(this.drag.currentY>16||this.drag.currentY<-16)&&this.state.isSwiping===!1&&(this.state.isScrolling=!0,this.drag.updatedX=this.drag.start),this.animate(this.drag.updatedX)))},e.prototype.onDragEnd=function(b){var d,e,f;if(this.state.isTouch){if("mouseup"===b.type&&this.$stage.removeClass("owl-grab"),this.trigger("dragged"),this.drag.targetEl.removeAttribute("draggable"),this.state.isTouch=!1,this.state.isScrolling=!1,this.state.isSwiping=!1,0===this.drag.distance&&this.state.inMotion!==!0)return this.state.inMotion=!1,!1;this.drag.endTime=(new Date).getTime(),d=this.drag.endTime-this.drag.startTime,e=Math.abs(this.drag.distance),(e>3||d>300)&&this.removeClick(this.drag.targetEl),f=this.closest(this.drag.updatedX),this.speed(this.settings.dragEndSpeed||this.settings.smartSpeed),this.current(f),this.invalidate("position"),this.update(),this.settings.pullDrag||this.drag.updatedX!==this.coordinates(f)||this.transitionEnd(),this.drag.distance=0,a(c).off(".owl.dragEvents")}},e.prototype.removeClick=function(c){this.drag.targetEl=c,a(c).on("click.preventClick",this.e._preventClick),b.setTimeout(function(){a(c).off("click.preventClick")},300)},e.prototype.preventClick=function(b){b.preventDefault?b.preventDefault():b.returnValue=!1,b.stopPropagation&&b.stopPropagation(),a(b.target).off("click.preventClick")},e.prototype.getTransformProperty=function(){var a,c;return a=b.getComputedStyle(this.$stage.get(0),null).getPropertyValue(this.vendorName+"transform"),a=a.replace(/matrix(3d)?\(|\)/g,"").split(","),c=16===a.length,c!==!0?a[4]:a[12]},e.prototype.closest=function(b){var c=-1,d=30,e=this.width(),f=this.coordinates();return this.settings.freeDrag||a.each(f,a.proxy(function(a,g){return b>g-d&&g+d>b?c=a:this.op(b,"<",g)&&this.op(b,">",f[a+1]||g-e)&&(c="left"===this.state.direction?a+1:a),-1===c},this)),this.settings.loop||(this.op(b,">",f[this.minimum()])?c=b=this.minimum():this.op(b,"<",f[this.maximum()])&&(c=b=this.maximum())),c},e.prototype.animate=function(b){this.trigger("translate"),this.state.inMotion=this.speed()>0,this.support3d?this.$stage.css({transform:"translate3d("+b+"px,0px, 0px)",transition:this.speed()/1e3+"s"}):this.state.isTouch?this.$stage.css({left:b+"px"}):this.$stage.animate({left:b},this.speed()/1e3,this.settings.fallbackEasing,a.proxy(function(){this.state.inMotion&&this.transitionEnd()},this))},e.prototype.current=function(a){if(a===d)return this._current;if(0===this._items.length)return d;if(a=this.normalize(a),this._current!==a){var b=this.trigger("change",{property:{name:"position",value:a}});b.data!==d&&(a=this.normalize(b.data)),this._current=a,this.invalidate("position"),this.trigger("changed",{property:{name:"position",value:this._current}})}return this._current},e.prototype.invalidate=function(a){this._invalidated[a]=!0},e.prototype.reset=function(a){a=this.normalize(a),a!==d&&(this._speed=0,this._current=a,this.suppress(["translate","translated"]),this.animate(this.coordinates(a)),this.release(["translate","translated"]))},e.prototype.normalize=function(b,c){var e=c?this._items.length:this._items.length+this._clones.length;return!a.isNumeric(b)||1>e?d:b=this._clones.length?(b%e+e)%e:Math.max(this.minimum(c),Math.min(this.maximum(c),b))},e.prototype.relative=function(a){return a=this.normalize(a),a-=this._clones.length/2,this.normalize(a,!0)},e.prototype.maximum=function(a){var b,c,d,e=0,f=this.settings;if(a)return this._items.length-1;if(!f.loop&&f.center)b=this._items.length-1;else if(f.loop||f.center)if(f.loop||f.center)b=this._items.length+f.items;else{if(!f.autoWidth&&!f.merge)throw"Can not detect maximum absolute position.";for(revert=f.rtl?1:-1,c=this.$stage.width()-this.$element.width();(d=this.coordinates(e))&&!(d*revert>=c);)b=++e}else b=this._items.length-f.items;return b},e.prototype.minimum=function(a){return a?0:this._clones.length/2},e.prototype.items=function(a){return a===d?this._items.slice():(a=this.normalize(a,!0),this._items[a])},e.prototype.mergers=function(a){return a===d?this._mergers.slice():(a=this.normalize(a,!0),this._mergers[a])},e.prototype.clones=function(b){var c=this._clones.length/2,e=c+this._items.length,f=function(a){return a%2===0?e+a/2:c-(a+1)/2};return b===d?a.map(this._clones,function(a,b){return f(b)}):a.map(this._clones,function(a,c){return a===b?f(c):null})},e.prototype.speed=function(a){return a!==d&&(this._speed=a),this._speed},e.prototype.coordinates=function(b){var c=null;return b===d?a.map(this._coordinates,a.proxy(function(a,b){return this.coordinates(b)},this)):(this.settings.center?(c=this._coordinates[b],c+=(this.width()-c+(this._coordinates[b-1]||0))/2*(this.settings.rtl?-1:1)):c=this._coordinates[b-1]||0,c)},e.prototype.duration=function(a,b,c){return Math.min(Math.max(Math.abs(b-a),1),6)*Math.abs(c||this.settings.smartSpeed)},e.prototype.to=function(c,d){if(this.settings.loop){var e=c-this.relative(this.current()),f=this.current(),g=this.current(),h=this.current()+e,i=0>g-h?!0:!1,j=this._clones.length+this._items.length;h<this.settings.items&&i===!1?(f=g+this._items.length,this.reset(f)):h>=j-this.settings.items&&i===!0&&(f=g-this._items.length,this.reset(f)),b.clearTimeout(this.e._goToLoop),this.e._goToLoop=b.setTimeout(a.proxy(function(){this.speed(this.duration(this.current(),f+e,d)),this.current(f+e),this.update()},this),30)}else this.speed(this.duration(this.current(),c,d)),this.current(c),this.update()},e.prototype.next=function(a){a=a||!1,this.to(this.relative(this.current())+1,a)},e.prototype.prev=function(a){a=a||!1,this.to(this.relative(this.current())-1,a)},e.prototype.transitionEnd=function(a){return a!==d&&(a.stopPropagation(),(a.target||a.srcElement||a.originalTarget)!==this.$stage.get(0))?!1:(this.state.inMotion=!1,void this.trigger("translated"))},e.prototype.viewport=function(){var d;if(this.options.responsiveBaseElement!==b)d=a(this.options.responsiveBaseElement).width();else if(b.innerWidth)d=b.innerWidth;else{if(!c.documentElement||!c.documentElement.clientWidth)throw"Can not detect viewport width.";d=c.documentElement.clientWidth}return d},e.prototype.replace=function(b){this.$stage.empty(),this._items=[],b&&(b=b instanceof jQuery?b:a(b)),this.settings.nestedItemSelector&&(b=b.find("."+this.settings.nestedItemSelector)),b.filter(function(){return 1===this.nodeType}).each(a.proxy(function(a,b){b=this.prepare(b),this.$stage.append(b),this._items.push(b),this._mergers.push(1*b.find("[data-merge]").andSelf("[data-merge]").attr("data-merge")||1)},this)),this.reset(a.isNumeric(this.settings.startPosition)?this.settings.startPosition:0),this.invalidate("items")},e.prototype.add=function(a,b){b=b===d?this._items.length:this.normalize(b,!0),this.trigger("add",{content:a,position:b}),0===this._items.length||b===this._items.length?(this.$stage.append(a),this._items.push(a),this._mergers.push(1*a.find("[data-merge]").andSelf("[data-merge]").attr("data-merge")||1)):(this._items[b].before(a),this._items.splice(b,0,a),this._mergers.splice(b,0,1*a.find("[data-merge]").andSelf("[data-merge]").attr("data-merge")||1)),this.invalidate("items"),this.trigger("added",{content:a,position:b})},e.prototype.remove=function(a){a=this.normalize(a,!0),a!==d&&(this.trigger("remove",{content:this._items[a],position:a}),this._items[a].remove(),this._items.splice(a,1),this._mergers.splice(a,1),this.invalidate("items"),this.trigger("removed",{content:null,position:a}))},e.prototype.addTriggerableEvents=function(){var b=a.proxy(function(b,c){return a.proxy(function(a){a.relatedTarget!==this&&(this.suppress([c]),b.apply(this,[].slice.call(arguments,1)),this.release([c]))},this)},this);a.each({next:this.next,prev:this.prev,to:this.to,destroy:this.destroy,refresh:this.refresh,replace:this.replace,add:this.add,remove:this.remove},a.proxy(function(a,c){this.$element.on(a+".owl.carousel",b(c,a+".owl.carousel"))},this))},e.prototype.watchVisibility=function(){function c(a){return a.offsetWidth>0&&a.offsetHeight>0}function d(){c(this.$element.get(0))&&(this.$element.removeClass("owl-hidden"),this.refresh(),b.clearInterval(this.e._checkVisibile))}c(this.$element.get(0))||(this.$element.addClass("owl-hidden"),b.clearInterval(this.e._checkVisibile),this.e._checkVisibile=b.setInterval(a.proxy(d,this),500))},e.prototype.preloadAutoWidthImages=function(b){var c,d,e,f;c=0,d=this,b.each(function(g,h){e=a(h),f=new Image,f.onload=function(){c++,e.attr("src",f.src),e.css("opacity",1),c>=b.length&&(d.state.imagesLoaded=!0,d.initialize())},f.src=e.attr("src")||e.attr("data-src")||e.attr("data-src-retina")})},e.prototype.destroy=function(){this.$element.hasClass(this.settings.themeClass)&&this.$element.removeClass(this.settings.themeClass),this.settings.responsive!==!1&&a(b).off("resize.owl.carousel"),this.transitionEndVendor&&this.off(this.$stage.get(0),this.transitionEndVendor,this.e._transitionEnd);for(var d in this._plugins)this._plugins[d].destroy();(this.settings.mouseDrag||this.settings.touchDrag)&&(this.$stage.off("mousedown touchstart touchcancel"),a(c).off(".owl.dragEvents"),this.$stage.get(0).onselectstart=function(){},this.$stage.off("dragstart",function(){return!1})),this.$element.off(".owl"),this.$stage.children(".cloned").remove(),this.e=null,this.$element.removeData("owlCarousel"),this.$stage.children().contents().unwrap(),this.$stage.children().unwrap(),this.$stage.unwrap()},e.prototype.op=function(a,b,c){var d=this.settings.rtl;switch(b){case"<":return d?a>c:c>a;case">":return d?c>a:a>c;case">=":return d?c>=a:a>=c;case"<=":return d?a>=c:c>=a}},e.prototype.on=function(a,b,c,d){a.addEventListener?a.addEventListener(b,c,d):a.attachEvent&&a.attachEvent("on"+b,c)},e.prototype.off=function(a,b,c,d){a.removeEventListener?a.removeEventListener(b,c,d):a.detachEvent&&a.detachEvent("on"+b,c)},e.prototype.trigger=function(b,c,d){var e={item:{count:this._items.length,index:this.current()}},f=a.camelCase(a.grep(["on",b,d],function(a){return a}).join("-").toLowerCase()),g=a.Event([b,"owl",d||"carousel"].join(".").toLowerCase(),a.extend({relatedTarget:this},e,c));return this._supress[b]||(a.each(this._plugins,function(a,b){b.onTrigger&&b.onTrigger(g)}),this.$element.trigger(g),this.settings&&"function"==typeof this.settings[f]&&this.settings[f].apply(this,g)),g},e.prototype.suppress=function(b){a.each(b,a.proxy(function(a,b){this._supress[b]=!0},this))},e.prototype.release=function(b){a.each(b,a.proxy(function(a,b){delete this._supress[b]},this))},e.prototype.browserSupport=function(){if(this.support3d=j(),this.support3d){this.transformVendor=i();var a=["transitionend","webkitTransitionEnd","transitionend","oTransitionEnd"];this.transitionEndVendor=a[h()],this.vendorName=this.transformVendor.replace(/Transform/i,""),this.vendorName=""!==this.vendorName?"-"+this.vendorName.toLowerCase()+"-":""}this.state.orientation=b.orientation},a.fn.owlCarousel=function(b){return this.each(function(){a(this).data("owlCarousel")||a(this).data("owlCarousel",new e(this,b))})},a.fn.owlCarousel.Constructor=e}(window.Zepto||window.jQuery,window,document),function(a,b){var c=function(b){this._core=b,this._loaded=[],this._handlers={"initialized.owl.carousel change.owl.carousel":a.proxy(function(b){if(b.namespace&&this._core.settings&&this._core.settings.lazyLoad&&(b.property&&"position"==b.property.name||"initialized"==b.type))for(var c=this._core.settings,d=c.center&&Math.ceil(c.items/2)||c.items,e=c.center&&-1*d||0,f=(b.property&&b.property.value||this._core.current())+e,g=this._core.clones().length,h=a.proxy(function(a,b){this.load(b)},this);e++<d;)this.load(g/2+this._core.relative(f)),g&&a.each(this._core.clones(this._core.relative(f++)),h)},this)},this._core.options=a.extend({},c.Defaults,this._core.options),this._core.$element.on(this._handlers)};c.Defaults={lazyLoad:!1},c.prototype.load=function(c){var d=this._core.$stage.children().eq(c),e=d&&d.find(".owl-lazy");!e||a.inArray(d.get(0),this._loaded)>-1||(e.each(a.proxy(function(c,d){var e,f=a(d),g=b.devicePixelRatio>1&&f.attr("data-src-retina")||f.attr("data-src");this._core.trigger("load",{element:f,url:g},"lazy"),f.is("img")?f.one("load.owl.lazy",a.proxy(function(){f.css("opacity",1),this._core.trigger("loaded",{element:f,url:g},"lazy")},this)).attr("src",g):(e=new Image,e.onload=a.proxy(function(){f.css({"background-image":"url("+g+")",opacity:"1"}),this._core.trigger("loaded",{element:f,url:g},"lazy")},this),e.src=g)},this)),this._loaded.push(d.get(0)))},c.prototype.destroy=function(){var a,b;for(a in this.handlers)this._core.$element.off(a,this.handlers[a]);for(b in Object.getOwnPropertyNames(this))"function"!=typeof this[b]&&(this[b]=null)},a.fn.owlCarousel.Constructor.Plugins.Lazy=c}(window.Zepto||window.jQuery,window,document),function(a){var b=function(c){this._core=c,this._handlers={"initialized.owl.carousel":a.proxy(function(){this._core.settings.autoHeight&&this.update()},this),"changed.owl.carousel":a.proxy(function(a){this._core.settings.autoHeight&&"position"==a.property.name&&this.update()},this),"loaded.owl.lazy":a.proxy(function(a){this._core.settings.autoHeight&&a.element.closest("."+this._core.settings.itemClass)===this._core.$stage.children().eq(this._core.current())&&this.update()},this)},this._core.options=a.extend({},b.Defaults,this._core.options),this._core.$element.on(this._handlers)};b.Defaults={autoHeight:!1,autoHeightClass:"owl-height"},b.prototype.update=function(){this._core.$stage.parent().height(this._core.$stage.children().eq(this._core.current()).height()).addClass(this._core.settings.autoHeightClass)},b.prototype.destroy=function(){var a,b;for(a in this._handlers)this._core.$element.off(a,this._handlers[a]);for(b in Object.getOwnPropertyNames(this))"function"!=typeof this[b]&&(this[b]=null)},a.fn.owlCarousel.Constructor.Plugins.AutoHeight=b}(window.Zepto||window.jQuery,window,document),function(a,b,c){var d=function(b){this._core=b,this._videos={},this._playing=null,this._fullscreen=!1,this._handlers={"resize.owl.carousel":a.proxy(function(a){this._core.settings.video&&!this.isInFullScreen()&&a.preventDefault()},this),"refresh.owl.carousel changed.owl.carousel":a.proxy(function(){this._playing&&this.stop()},this),"prepared.owl.carousel":a.proxy(function(b){var c=a(b.content).find(".owl-video");c.length&&(c.css("display","none"),this.fetch(c,a(b.content)))},this)},this._core.options=a.extend({},d.Defaults,this._core.options),this._core.$element.on(this._handlers),this._core.$element.on("click.owl.video",".owl-video-play-icon",a.proxy(function(a){this.play(a)},this))};d.Defaults={video:!1,videoHeight:!1,videoWidth:!1},d.prototype.fetch=function(a,b){var c=a.attr("data-vimeo-id")?"vimeo":"youtube",d=a.attr("data-vimeo-id")||a.attr("data-youtube-id"),e=a.attr("data-width")||this._core.settings.videoWidth,f=a.attr("data-height")||this._core.settings.videoHeight,g=a.attr("href");if(!g)throw new Error("Missing video URL.");if(d=g.match(/(http:|https:|)\/\/(player.|www.)?(vimeo\.com|youtu(be\.com|\.be|be\.googleapis\.com))\/(video\/|embed\/|watch\?v=|v\/)?([A-Za-z0-9._%-]*)(\&\S+)?/),d[3].indexOf("youtu")>-1)c="youtube";else{if(!(d[3].indexOf("vimeo")>-1))throw new Error("Video URL not supported.");c="vimeo"}d=d[6],this._videos[g]={type:c,id:d,width:e,height:f},b.attr("data-video",g),this.thumbnail(a,this._videos[g])},d.prototype.thumbnail=function(b,c){var d,e,f,g=c.width&&c.height?'style="width:'+c.width+"px;height:"+c.height+'px;"':"",h=b.find("img"),i="src",j="",k=this._core.settings,l=function(a){e='<div class="owl-video-play-icon"></div>',d=k.lazyLoad?'<div class="owl-video-tn '+j+'" '+i+'="'+a+'"></div>':'<div class="owl-video-tn" style="opacity:1;background-image:url('+a+')"></div>',b.after(d),b.after(e)};return b.wrap('<div class="owl-video-wrapper"'+g+"></div>"),this._core.settings.lazyLoad&&(i="data-src",j="owl-lazy"),h.length?(l(h.attr(i)),h.remove(),!1):void("youtube"===c.type?(f="http://img.youtube.com/vi/"+c.id+"/hqdefault.jpg",l(f)):"vimeo"===c.type&&a.ajax({type:"GET",url:"http://vimeo.com/api/v2/video/"+c.id+".json",jsonp:"callback",dataType:"jsonp",success:function(a){f=a[0].thumbnail_large,l(f)}}))},d.prototype.stop=function(){this._core.trigger("stop",null,"video"),this._playing.find(".owl-video-frame").remove(),this._playing.removeClass("owl-video-playing"),this._playing=null},d.prototype.play=function(b){this._core.trigger("play",null,"video"),this._playing&&this.stop();var c,d,e=a(b.target||b.srcElement),f=e.closest("."+this._core.settings.itemClass),g=this._videos[f.attr("data-video")],h=g.width||"100%",i=g.height||this._core.$stage.height();"youtube"===g.type?c='<iframe width="'+h+'" height="'+i+'" src="http://www.youtube.com/embed/'+g.id+"?autoplay=1&v="+g.id+'" frameborder="0" allowfullscreen></iframe>':"vimeo"===g.type&&(c='<iframe src="http://player.vimeo.com/video/'+g.id+'?autoplay=1" width="'+h+'" height="'+i+'" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>'),f.addClass("owl-video-playing"),this._playing=f,d=a('<div style="height:'+i+"px; width:"+h+'px" class="owl-video-frame">'+c+"</div>"),e.after(d)},d.prototype.isInFullScreen=function(){var d=c.fullscreenElement||c.mozFullScreenElement||c.webkitFullscreenElement;return d&&a(d).parent().hasClass("owl-video-frame")&&(this._core.speed(0),this._fullscreen=!0),d&&this._fullscreen&&this._playing?!1:this._fullscreen?(this._fullscreen=!1,!1):this._playing&&this._core.state.orientation!==b.orientation?(this._core.state.orientation=b.orientation,!1):!0},d.prototype.destroy=function(){var a,b;this._core.$element.off("click.owl.video");for(a in this._handlers)this._core.$element.off(a,this._handlers[a]);for(b in Object.getOwnPropertyNames(this))"function"!=typeof this[b]&&(this[b]=null)},a.fn.owlCarousel.Constructor.Plugins.Video=d}(window.Zepto||window.jQuery,window,document),function(a,b,c,d){var e=function(b){this.core=b,this.core.options=a.extend({},e.Defaults,this.core.options),this.swapping=!0,this.previous=d,this.next=d,this.handlers={"change.owl.carousel":a.proxy(function(a){"position"==a.property.name&&(this.previous=this.core.current(),this.next=a.property.value)},this),"drag.owl.carousel dragged.owl.carousel translated.owl.carousel":a.proxy(function(a){this.swapping="translated"==a.type},this),"translate.owl.carousel":a.proxy(function(){this.swapping&&(this.core.options.animateOut||this.core.options.animateIn)&&this.swap()},this)},this.core.$element.on(this.handlers)};e.Defaults={animateOut:!1,animateIn:!1},e.prototype.swap=function(){if(1===this.core.settings.items&&this.core.support3d){this.core.speed(0);var b,c=a.proxy(this.clear,this),d=this.core.$stage.children().eq(this.previous),e=this.core.$stage.children().eq(this.next),f=this.core.settings.animateIn,g=this.core.settings.animateOut;this.core.current()!==this.previous&&(g&&(b=this.core.coordinates(this.previous)-this.core.coordinates(this.next),d.css({left:b+"px"}).addClass("animated owl-animated-out").addClass(g).one("webkitAnimationEnd mozAnimationEnd MSAnimationEnd oanimationend animationend",c)),f&&e.addClass("animated owl-animated-in").addClass(f).one("webkitAnimationEnd mozAnimationEnd MSAnimationEnd oanimationend animationend",c))}},e.prototype.clear=function(b){a(b.target).css({left:""}).removeClass("animated owl-animated-out owl-animated-in").removeClass(this.core.settings.animateIn).removeClass(this.core.settings.animateOut),this.core.transitionEnd()},e.prototype.destroy=function(){var a,b;for(a in this.handlers)this.core.$element.off(a,this.handlers[a]);for(b in Object.getOwnPropertyNames(this))"function"!=typeof this[b]&&(this[b]=null)},a.fn.owlCarousel.Constructor.Plugins.Animate=e}(window.Zepto||window.jQuery,window,document),function(a,b,c){var d=function(b){this.core=b,this.core.options=a.extend({},d.Defaults,this.core.options),this.handlers={"translated.owl.carousel refreshed.owl.carousel":a.proxy(function(){this.autoplay()
},this),"play.owl.autoplay":a.proxy(function(a,b,c){this.play(b,c)},this),"stop.owl.autoplay":a.proxy(function(){this.stop()},this),"mouseover.owl.autoplay":a.proxy(function(){this.core.settings.autoplayHoverPause&&this.pause()},this),"mouseleave.owl.autoplay":a.proxy(function(){this.core.settings.autoplayHoverPause&&this.autoplay()},this)},this.core.$element.on(this.handlers)};d.Defaults={autoplay:!1,autoplayTimeout:5e3,autoplayHoverPause:!1,autoplaySpeed:!1},d.prototype.autoplay=function(){this.core.settings.autoplay&&!this.core.state.videoPlay?(b.clearInterval(this.interval),this.interval=b.setInterval(a.proxy(function(){this.play()},this),this.core.settings.autoplayTimeout)):b.clearInterval(this.interval)},d.prototype.play=function(){return c.hidden===!0||this.core.state.isTouch||this.core.state.isScrolling||this.core.state.isSwiping||this.core.state.inMotion?void 0:this.core.settings.autoplay===!1?void b.clearInterval(this.interval):void this.core.next(this.core.settings.autoplaySpeed)},d.prototype.stop=function(){b.clearInterval(this.interval)},d.prototype.pause=function(){b.clearInterval(this.interval)},d.prototype.destroy=function(){var a,c;b.clearInterval(this.interval);for(a in this.handlers)this.core.$element.off(a,this.handlers[a]);for(c in Object.getOwnPropertyNames(this))"function"!=typeof this[c]&&(this[c]=null)},a.fn.owlCarousel.Constructor.Plugins.autoplay=d}(window.Zepto||window.jQuery,window,document),function(a){"use strict";var b=function(c){this._core=c,this._initialized=!1,this._pages=[],this._controls={},this._templates=[],this.$element=this._core.$element,this._overrides={next:this._core.next,prev:this._core.prev,to:this._core.to},this._handlers={"prepared.owl.carousel":a.proxy(function(b){this._core.settings.dotsData&&this._templates.push(a(b.content).find("[data-dot]").andSelf("[data-dot]").attr("data-dot"))},this),"add.owl.carousel":a.proxy(function(b){this._core.settings.dotsData&&this._templates.splice(b.position,0,a(b.content).find("[data-dot]").andSelf("[data-dot]").attr("data-dot"))},this),"remove.owl.carousel prepared.owl.carousel":a.proxy(function(a){this._core.settings.dotsData&&this._templates.splice(a.position,1)},this),"change.owl.carousel":a.proxy(function(a){if("position"==a.property.name&&!this._core.state.revert&&!this._core.settings.loop&&this._core.settings.navRewind){var b=this._core.current(),c=this._core.maximum(),d=this._core.minimum();a.data=a.property.value>c?b>=c?d:c:a.property.value<d?c:a.property.value}},this),"changed.owl.carousel":a.proxy(function(a){"position"==a.property.name&&this.draw()},this),"refreshed.owl.carousel":a.proxy(function(){this._initialized||(this.initialize(),this._initialized=!0),this._core.trigger("refresh",null,"navigation"),this.update(),this.draw(),this._core.trigger("refreshed",null,"navigation")},this)},this._core.options=a.extend({},b.Defaults,this._core.options),this.$element.on(this._handlers)};b.Defaults={nav:!1,navRewind:!0,navText:["prev","next"],navSpeed:!1,navElement:"div",navContainer:!1,navContainerClass:"owl-nav",navClass:["owl-prev","owl-next"],slideBy:1,dotClass:"owl-dot",dotsClass:"owl-dots",dots:!0,dotsEach:!1,dotData:!1,dotsSpeed:!1,dotsContainer:!1,controlsClass:"owl-controls"},b.prototype.initialize=function(){var b,c,d=this._core.settings;d.dotsData||(this._templates=[a("<div>").addClass(d.dotClass).append(a("<span>")).prop("outerHTML")]),d.navContainer&&d.dotsContainer||(this._controls.$container=a("<div>").addClass(d.controlsClass).appendTo(this.$element)),this._controls.$indicators=d.dotsContainer?a(d.dotsContainer):a("<div>").hide().addClass(d.dotsClass).appendTo(this._controls.$container),this._controls.$indicators.on("click","div",a.proxy(function(b){var c=a(b.target).parent().is(this._controls.$indicators)?a(b.target).index():a(b.target).parent().index();b.preventDefault(),this.to(c,d.dotsSpeed)},this)),b=d.navContainer?a(d.navContainer):a("<div>").addClass(d.navContainerClass).prependTo(this._controls.$container),this._controls.$next=a("<"+d.navElement+">"),this._controls.$previous=this._controls.$next.clone(),this._controls.$previous.addClass(d.navClass[0]).html(d.navText[0]).hide().prependTo(b).on("click",a.proxy(function(){this.prev(d.navSpeed)},this)),this._controls.$next.addClass(d.navClass[1]).html(d.navText[1]).hide().appendTo(b).on("click",a.proxy(function(){this.next(d.navSpeed)},this));for(c in this._overrides)this._core[c]=a.proxy(this[c],this)},b.prototype.destroy=function(){var a,b,c,d;for(a in this._handlers)this.$element.off(a,this._handlers[a]);for(b in this._controls)this._controls[b].remove();for(d in this.overides)this._core[d]=this._overrides[d];for(c in Object.getOwnPropertyNames(this))"function"!=typeof this[c]&&(this[c]=null)},b.prototype.update=function(){var a,b,c,d=this._core.settings,e=this._core.clones().length/2,f=e+this._core.items().length,g=d.center||d.autoWidth||d.dotData?1:d.dotsEach||d.items;if("page"!==d.slideBy&&(d.slideBy=Math.min(d.slideBy,d.items)),d.dots||"page"==d.slideBy)for(this._pages=[],a=e,b=0,c=0;f>a;a++)(b>=g||0===b)&&(this._pages.push({start:a-e,end:a-e+g-1}),b=0,++c),b+=this._core.mergers(this._core.relative(a))},b.prototype.draw=function(){var b,c,d="",e=this._core.settings,f=(this._core.$stage.children(),this._core.relative(this._core.current()));if(!e.nav||e.loop||e.navRewind||(this._controls.$previous.toggleClass("disabled",0>=f),this._controls.$next.toggleClass("disabled",f>=this._core.maximum())),this._controls.$previous.toggle(e.nav),this._controls.$next.toggle(e.nav),e.dots){if(b=this._pages.length-this._controls.$indicators.children().length,e.dotData&&0!==b){for(c=0;c<this._controls.$indicators.children().length;c++)d+=this._templates[this._core.relative(c)];this._controls.$indicators.html(d)}else b>0?(d=new Array(b+1).join(this._templates[0]),this._controls.$indicators.append(d)):0>b&&this._controls.$indicators.children().slice(b).remove();this._controls.$indicators.find(".active").removeClass("active"),this._controls.$indicators.children().eq(a.inArray(this.current(),this._pages)).addClass("active")}this._controls.$indicators.toggle(e.dots)},b.prototype.onTrigger=function(b){var c=this._core.settings;b.page={index:a.inArray(this.current(),this._pages),count:this._pages.length,size:c&&(c.center||c.autoWidth||c.dotData?1:c.dotsEach||c.items)}},b.prototype.current=function(){var b=this._core.relative(this._core.current());return a.grep(this._pages,function(a){return a.start<=b&&a.end>=b}).pop()},b.prototype.getPosition=function(b){var c,d,e=this._core.settings;return"page"==e.slideBy?(c=a.inArray(this.current(),this._pages),d=this._pages.length,b?++c:--c,c=this._pages[(c%d+d)%d].start):(c=this._core.relative(this._core.current()),d=this._core.items().length,b?c+=e.slideBy:c-=e.slideBy),c},b.prototype.next=function(b){a.proxy(this._overrides.to,this._core)(this.getPosition(!0),b)},b.prototype.prev=function(b){a.proxy(this._overrides.to,this._core)(this.getPosition(!1),b)},b.prototype.to=function(b,c,d){var e;d?a.proxy(this._overrides.to,this._core)(b,c):(e=this._pages.length,a.proxy(this._overrides.to,this._core)(this._pages[(b%e+e)%e].start,c))},a.fn.owlCarousel.Constructor.Plugins.Navigation=b}(window.Zepto||window.jQuery,window,document),function(a,b){"use strict";var c=function(d){this._core=d,this._hashes={},this.$element=this._core.$element,this._handlers={"initialized.owl.carousel":a.proxy(function(){"URLHash"==this._core.settings.startPosition&&a(b).trigger("hashchange.owl.navigation")},this),"prepared.owl.carousel":a.proxy(function(b){var c=a(b.content).find("[data-hash]").andSelf("[data-hash]").attr("data-hash");this._hashes[c]=b.content},this)},this._core.options=a.extend({},c.Defaults,this._core.options),this.$element.on(this._handlers),a(b).on("hashchange.owl.navigation",a.proxy(function(){var a=b.location.hash.substring(1),c=this._core.$stage.children(),d=this._hashes[a]&&c.index(this._hashes[a])||0;return a?void this._core.to(d,!1,!0):!1},this))};c.Defaults={URLhashListener:!1},c.prototype.destroy=function(){var c,d;a(b).off("hashchange.owl.navigation");for(c in this._handlers)this._core.$element.off(c,this._handlers[c]);for(d in Object.getOwnPropertyNames(this))"function"!=typeof this[d]&&(this[d]=null)},a.fn.owlCarousel.Constructor.Plugins.Hash=c}(window.Zepto||window.jQuery,window,document);

//]]></script>
<b:if cond='data:view.isPost'>
<script>
//<![CDATA[
var randomRelatedIndex,showRelatedPost;(function(n,m,k){var d={widgetTitle:"<h4>Related Posts:</h4>",widgetStyle:1,homePage:"https://www.dte.web.id",numPosts:7,summaryLength:125,titleLength:"auto",thumbnailSize:200,noImage:"data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAIAAACQd1PeAAAAA3NCSVQICAjb4U/gAAAADElEQVQImWOor68HAAL+AX7vOF2TAAAAAElFTkSuQmCC",containerId:"related-post",newTabLink:false,moreText:"Baca Selengkapnya",callBack:function(){}};for(var f in relatedPostConfig){d[f]=(relatedPostConfig[f]=="undefined")?d[f]:relatedPostConfig[f]}var j=function(a){var b=m.createElement("script");b.type="text/javascript";b.src=a;k.appendChild(b)},o=function(b,a){return Math.floor(Math.random()*(a-b+1))+b},l=function(a){var p=a.length,c,b;if(p===0){return false}while(--p){c=Math.floor(Math.random()*(p+1));b=a[p];a[p]=a[c];a[c]=b}return a},e=(typeof labelArray=="object"&&labelArray.length>0)?"/-/"+l(labelArray)[0]:"",h=function(b){var c=b.feed.openSearch$totalResults.$t-d.numPosts,a=o(1,(c>0?c:1));j(d.homePage.replace(/\/$/,"")+"/feeds/posts/summary"+e+"?alt=json-in-script&orderby=updated&start-index="+a+"&max-results="+d.numPosts+"&callback=showRelatedPost")},g=function(z){var s=document.getElementById(d.containerId),x=l(z.feed.entry),A=d.widgetStyle,c=d.widgetTitle+'<ul class="related-post-style-'+A+'">',b=d.newTabLink?' target="noopener"':"",y='<span class="bg_overlay"></span>',v,t,w,r,u;if(!s){return}for(var q=0;q<d.numPosts;q++){if(q==x.length){break}t=x[q].title.$t;w=(d.titleLength!=="auto"&&d.titleLength<t.length)?t.substring(0,d.titleLength)+"&hellip;":t;r=("media$thumbnail"in x[q]&&d.thumbnailSize!==false)?x[q].media$thumbnail.url.replace(/.*?:\/\//g , "//").replace(/\/s[0-9]+(\-c)?/, "/s"+d.thumbnailSize):d.noImage;u=("summary"in x[q]&&d.summaryLength>0)?x[q].summary.$t.replace(/<br ?\/?>/g," ").replace(/<.*?>/g,"").replace(/[<>]/g,"").substring(0,d.summaryLength)+"&hellip;":"";for(var p=0,a=x[q].link.length;p<a;p++){v=(x[q].link[p].rel=="alternate")?x[q].link[p].href:"#"}if(A==2){c+='<li><div class="related-post-item-thumbnail"><img alt="" src="'+r+'" width="'+d.thumbnailSize+'" height="'+d.thumbnailSize+'"></div><div class="related-post-item-text"><a class="related-post-item-title" title="'+t+'" href="'+v+'"'+b+">"+w+'</a><span class="related-post-item-summary"><span class="related-post-item-summary-text">'+u+'</span> <a href="'+v+'" class="related-post-item-more"'+b+">"+d.moreText+"</a></span></div>"+y+"</li>"}else{if(A==3||A==4){c+='<li class="related-post-item" tabindex="0"><a class="related-post-item-title-thumb" href="'+v+'"'+b+'><div class="related-post-item-thumbnail"><img alt="" src="'+r+'" width="'+d.thumbnailSize+'" height="'+d.thumbnailSize+'"></a></div><div class="related-post-item-tooltip"><a class="related-post-item-title" title="'+t+'" href="'+v+'"'+b+">"+w+"</a><span>"+u+"</span></div>"+y+"</li>"}else{if(A==5){c+='<li class="related-post-item" tabindex="0"><a class="related-post-item-wrapper" href="'+v+'" title="'+t+'"'+b+'><div class="related-post-item-thumbnail"><img alt="" src="'+r+'" width="'+d.thumbnailSize+'" height="'+d.thumbnailSize+'"><span class="related-post-item-tooltip">'+w+"</span></a>"+y+"</li>"}else{if(A==6){c+='<li><div class="related-post-item-tooltip"><div class="related-post-item-thumbnail"><img alt="" src="'+r+'" width="'+d.thumbnailSize+'" height="'+d.thumbnailSize+'"></div><a class="related-post-item-title" title="'+t+'" href="'+v+'"'+b+">"+w+'</a><span class="related-post-item-summary"><span class="related-post-item-summary-text">'+u+"</span></span>"+y+"</div></li>"}else{c+='<li><a title="'+t+'" href="'+v+'"'+b+">"+w+"</a></li>"}}}}}s.innerHTML=c+="</ul>"+y;d.callBack()};randomRelatedIndex=h;showRelatedPost=g;j(d.homePage.replace(/\/$/,"")+"/feeds/posts/summary"+e+"?alt=json-in-script&orderby=updated&max-results=0&callback=randomRelatedIndex")})(window,document,document.getElementsByTagName("head")[0]);
//]]>         
</script>
</b:if>
<script>
$(window).scroll(function(){$(this).scrollTop()&gt;200?$(&quot;.back-to-top&quot;).fadeIn():$(&quot;.back-to-top&quot;).fadeOut()}),$(&quot;.back-to-top&quot;).hide().click(function(){return $(&quot;html, body&quot;).animate({scrollTop:0},1e3),!1});
//<![CDATA[
var no_image = "https://4.bp.blogspot.com/-SKh7CYM3lB0/WZlRLgH8wII/AAAAAAAACjQ/vx5PJdQYhSo136-Wg-A633KcElrfkHNNACLcBGAs/s1600/non.png",
month_format = [, "Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sept", "Oct", "Nov", "Dec"],
more_text = "See all projects";
eval(function(p,a,c,k,e,r){e=function(c){return(c<a?'':e(parseInt(c/a)))+((c=c%a)>35?String.fromCharCode(c+29):c.toString(36))};if(!''.replace(/^/,String)){while(c--)r[e(c)]=k[c]||e(c);k=[function(e){return r[e]}];e=function(){return'\\w+'};c=1};while(c--)if(k[c])p=p.replace(new RegExp('\\b'+e(c)+'\\b','g'),k[c]);return p}('$(".C-16 .17 .I-J").N(z(){A e=($(b).F("w").B("O-18"),$(b).F("w").B("O-19")),t=($(b).P("1a").1C(),$(b).Q().B("1b")),a=$(b).F("w").B("O-1c");a.1D("D")&&$.1E({R:"/1F/1G/1d/?1H=1I-1J-1K&S-T="+e,1c:"1L",1M:"1N",1O:z(e){1e(A a="",s=\'<j 9="1f-D">\',n=0;n<e.k.q.1g;n++){1e(A r=0;r<e.k.q[n].K.1g;r++)U("1P"==e.k.q[n].K[r].1Q){a=e.k.q[n].K[r].G;1R}A i=e.k.q[n].H.$t,o=e.k.q[n].1S[0].1T,l=e.k.q[n].1h[0].1U.$t,d=e.k.q[n].1V.$t,c=d.V(0,4),p=d.V(5,7),u=d.V(8,10),m=1W[1X(p,10)]+" "+u+", "+c,f=e.k.q[n].J.$t,h=$("<j>").1i(f);U(f.1j("//1Y.1Z.21/22/")>-1)A v=e.k.q[n].23$24.R,g=v;1k U(f.1j("<W")>-1)A y=h.F("W:25").B("26"),g=y;1k A g=27;s+=\'<1l 9="D-28"><j 9="D-W"><a 9="1m-1n" G="\'+a+\'" X="1o:R(\'+g+\') 19-29 1p 1p;1o-2a: 2b"></a><w 9="C-2c"><a H=\'+o+" "+o+\' G="/1q/18/\'+o+\'?&S-T=6">\'+o+\'</a></w></j><j 9="D-J"><1r 9="C-H"><a G="\'+a+\'">\'+i+\'</a></1r><j 9="C-2d"><w 9="C-1h">\'+l+\'</w><w 9="C-2e">\'+m+\'</w></2f></j><j 9="2g"/></1l>\'}s+="</j>",$(".C-16 .17 .I-J").N(z(){A e=$(b).Q().B("1b");e==t&&($(b).1i(s),$(b).Q().2h("D"),$(b).P("1a").2i(\'<j 9="I-H"></j>\'),$(b).P(".I-H").2j(\'<a 9="2k-K" G="/1q/S-T=6">\'+2l+"</a>"),$(".1f-D").Y({Z:11,L:!0,1s:2m,1t:["",""],M:!1,12:!0,13:14,E:!0,2n:!0,15:{0:{x:1,E:!1},2o:{x:2,E:!1},1u:{x:4,E:!0,M:!1}}}),$(b).F(".1m-1n").N(z(){$(b).B("X",z(e,t){1v t.1w("/1d.1x","/2p.1x")}).B("X",z(e,t){1v t.1w("2q-c","2r")})}))})}})}),$(1y).1z(z(){$(".2s").Y({x:1,Z:11,L:!0,1t:["",""],M:!0,12:!0,13:14,E:!1,1A:!0,2t:!0,2u:"2v",2w:"2x",15:{0:{x:1,L:!1},1B:{x:1,L:!0}}})}),$(1y).1z(z(){$(".2y-2z").Y({Z:11,M:!0,12:!0,13:14,E:!1,1s:20,1A:!0,15:{0:{x:2},1B:{x:3},1u:{x:5}}})});',62,160,'|||||||||class||this||||||||div|feed||||||entry||||||span|items||function|var|attr|recent|carousel|dots|find|href|title|widget|content|link|nav|loop|each|data|prev|parent|url|max|results|if|substring|img|style|owlCarousel|smartSpeed||550|autoplay|autoplaySpeed|800|responsive|boxes|HTML|label|no|h3|id|type|default|for|main|length|author|html|indexOf|else|li|box|image|background|center|search|h2|margin|navText|1e3|return|replace|jpg|document|ready|mouseDrag|601|text|match|ajax|feeds|posts|alt|json|in|script|get|dataType|jsonp|success|alternate|rel|break|category|term|name|published|month_format|parseInt|www|youtube||com|embed|media|thumbnail|first|src|no_image|item|repeat|size|cover|tag|meta|date|dan|clr|addClass|wrap|append|more|more_text|30|responsiveClass|600|mqdefault|s72|s1600|boxtestimonial|singleItem|animateIn|fadeIn|animateOut|fadeOut|customer|parnert'.split('|'),0,{}))

"use strict";$(function(){$("#load-grid").each(function(){var d=$(this),a=d.data("load");a&&$("#load-grid").show(),$("#load-grid").on("click",function(d){$("#load-grid").hide(),$.ajax({url:a,success:function(d){var o=$(d).find(".bxposts");o.find(".halaman-indeks").addClass("post-animated post-fadeInUp"),$(".bxposts").append(o.html()),a=$(d).find("#load-grid").data("load"),a?$("#load-grid").show():($("#load-grid").hide(),$("#blog-pager .endmore").addClass("show"))},beforeSend:function(){$("#blog-pager .loading").show()},complete:function(){$("#blog-pager .loading").hide()}}),d.preventDefault()})})});

//script to create sticky header 
"use strict";function createSticky(e){if("undefined"!=typeof e){var t=e.offset().top+50,c=jQuery(window);c.on("scroll",function(){c.scrollTop()>t?e.addClass("stickyhead"):e.removeClass("stickyhead")})}}jQuery(function(){createSticky(jQuery("#sticky-wrap"))});

// youtube
"use strict";!function(o){"use strict";var e=o(document),u=function(o){if(o.match(/(youtube.com)/))var e="v=",u=1;else if(o.match(/(youtu.be)/)||o.match(/(vimeo.com\/)+[0-9]/))var e="/",u=3;else if(o.match(/(vimeo.com\/)+[a-zA-Z]/))var e="/",u=5;return o=o.split(e)[u]};o.fn.YouTubePopUp=function(a){var p=o.extend({autoplay:1},a),t=o(this);t.on("click",function(a){a.preventDefault();var i=t.attr("href"),c=u(i),n=c.replace(/(&)+(.*)/,"");if(i.match(/(youtu.be)/)||i.match(/(youtube.com)/))var m="https://www.youtube.com/embed/"+n+"?autoplay="+p.autoplay;else if(i.match(/(vimeo.com\/)+[0-9]/)||i.match(/(vimeo.com\/)+[a-zA-Z]/))var m="https://player.vimeo.com/video/"+n+"?autoplay="+p.autoplay;var s='<div class="YouTubePopUp-Wrap YouTubePopUp-animation"><div class="YouTubePopUp-Content"><span class="YouTubePopUp-Close"></span><iframe src="'+m+'" allowfullscreen></iframe></div></div>';o("body").append(s),o(".YouTubePopUp-Wrap").hasClass("YouTubePopUp-animation")&&setTimeout(function(){o(".YouTubePopUp-Wrap").removeClass("YouTubePopUp-animation")},600),e.on("click",".YouTubePopUp-Wrap, .YouTubePopUp-Close",function(){o(".YouTubePopUp-Wrap").addClass("YouTubePopUp-Hide").delay(515).queue(function(){o(this).remove()})})}),e.on("keyup",function(e){27==e.keyCode&&o(".YouTubePopUp-Wrap:visible").click()})}}(jQuery),$(function(){$(".js-modal-video").YouTubePopUp()});

// accordion
"use strict";var accordion=function(){var o=$(".js-accordion"),c=o.find(".js-accordion-header"),e=($(".js-accordion-item"),{speed:400,oneOpen:!1});return{init:function(o){c.on("click",function(){accordion.toggle($(this))}),$.extend(e,o),e.oneOpen&&$(".js-accordion-item.active").length>1&&$(".js-accordion-item.active:not(:first)").removeClass("active"),$(".js-accordion-item.active").find("> .js-accordion-body").show()},toggle:function(o){e.oneOpen&&o[0]!=o.closest(".js-accordion").find("> .js-accordion-item.active > .js-accordion-header")[0]&&o.closest(".js-accordion").find("> .js-accordion-item").removeClass("active").find(".js-accordion-body").slideUp(),o.closest(".js-accordion-item").toggleClass("active"),o.next().stop().slideToggle(e.speed)}}}();$(document).ready(function(){accordion.init({speed:300,oneOpen:!0})});$("#toTop").click(function () {$("html,body").animate({scrollTop: 0}, 500);});

// Search
"use strict";function LMsearchForm(){for(var t=document.getElementById("searchcontainer"),n=document.getElementById("search-terms"),e=document.querySelectorAll(".iconsearch-label"),c=0;c<e.length;c++)e[c].addEventListener("click",function(e){t.classList.toggle("opensearch"),t.classList.contains("opensearch")||(n.blur(),e.preventDefault()),e.stopPropagation()},!1);n.addEventListener("click",function(e){e.stopPropagation()},!1),document.addEventListener("click",function(e){t.classList.remove("opensearch"),n.blur(),e.stopPropagation()},!1),document.addEventListener("keydown",function(e){"Escape"==e.key&&(t.classList.remove("opensearch"),n.blur())})}LMsearchForm();

"use strict";$(function(){$("#load-grid").each(function(){var d=$(this),a=d.data("load");a&&$("#load-grid").show(),$("#load-grid").on("click",function(d){$("#load-grid").hide(),$.ajax({url:a,success:function(d){var o=$(d).find(".bxposts");o.find(".halaman-indeks").addClass("post-animated post-fadeInUp"),$(".bxposts").append(o.html()),a=$(d).find("#load-grid").data("load"),a?$("#load-grid").show():($("#load-grid").hide(),$("#blog-pager .endmore").addClass("show"))},beforeSend:function(){$("#blog-pager .loading").show()},complete:function(){$("#blog-pager .loading").hide()}}),d.preventDefault()})})});

"use strict";$(function(){$("#main-menu").each(function(){for(var e=$(this).find(".LinkList ul > li").children("a"),a=e.length,n=0;a>n;n++){var t=e.eq(n),s=t.text();if("_"!==s.charAt(0)){var i=e.eq(n+1),l=i.text();if("_"===l.charAt(0)){var u=t.parent();u.append('<ul class="sub-menu m-sub"/>')}}"_"===s.charAt(0)&&(t.text(s.replace("_","")),t.parent().appendTo(u.children(".sub-menu")))}for(n=0;a>n;n++)t=e.eq(n),s=t.text(),"_"!==s.charAt(0)&&(i=e.eq(n+1),l=i.text(),"_"===l.charAt(0)&&(u=t.parent(),u.append('<ul class="sub-menu2 m-sub"/>'))),"_"===s.charAt(0)&&(t.text(s.replace("_","")),t.parent().appendTo(u.children(".sub-menu2")));$("#main-menu ul li ul").parent("li").addClass("has-sub"),$("#main-menu .widget").addClass("show-menu")}),$("#main-menu-nav").clone().appendTo(".mobile-menu"),$(".mobile-menu .has-sub").append('<div class="submenu-toggle"/>'),$(".mobile-menu ul > li a").each(function(){var e=$(this),a=e.attr("href").trim(),n=a.toLowerCase(),t=a.split("/"),s=t[0];n.match("mega-menu")&&e.attr("href","/search/label/"+s+"?&max-results="+postPerPage)}),$(".slide-menu-toggle").on("click",function(){$("body").toggleClass("nav-active")}),$(".mobile-menu ul li .submenu-toggle").on("click",function(e){$(this).parent().hasClass("has-sub")&&(e.preventDefault(),$(this).parent().hasClass("show")?$(this).parent().removeClass("show").find("> .m-sub").slideToggle(170):$(this).parent().addClass("show").children(".m-sub").slideToggle(170))}),$("#main-menu #main-menu-nav li").each(function(){var e=$(this),a=e.find("a").attr("href").trim(),n=e,t=a.toLowerCase(),s=a.split("/"),i=s[0];b(n,t,5,i)})});

"use strict";function toggleMenu(){overlay.classList.toggle("active"),menu.classList.toggle("active")}var overlay=document.querySelector(".overlay"),menu=document.querySelector(".menu");$(".sidebar-dropdown > a").click(function(){$(".sidebar-submenu").slideUp(200),$(this).parent().hasClass("active")?($(".sidebar-dropdown").removeClass("active"),$(this).parent().removeClass("active")):($(".sidebar-dropdown").removeClass("active"),$(this).next(".sidebar-submenu").slideDown(200),$(this).parent().addClass("active"))});

"use strict";!function(s){function e(){n(s(".cd-headline.letters").find("b")),t(s(".cd-headline"))}function n(e){e.each(function(){var e=s(this),n=e.text().split(""),t=e.hasClass("is-visible");for(i in n)e.parents(".rotate-2").length>0&&(n[i]="<em>"+n[i]+"</em>"),n[i]=t?'<i class="in">'+n[i]+"</i>":"<i>"+n[i]+"</i>";var a=n.join("");e.html(a).css("opacity",1)})}function t(i){var e=o;i.each(function(){var i=s(this);if(i.hasClass("clip")){var n=i.find(".cd-words-wrapper"),t=n.width()+10;n.css("width",t)}else if(!i.hasClass("type")){var d=i.find(".cd-words-wrapper b"),r=0;d.each(function(){var i=s(this).width();i>r&&(r=i)}),i.find(".cd-words-wrapper").css("width",r)}setTimeout(function(){a(i.find(".is-visible").eq(0))},e)})}function a(i){var s=r(i);i.parents(".cd-headline").hasClass("clip")?i.parents(".cd-words-wrapper").animate({width:"2px"},l,function(){c(i,s),d(s)}):(c(i,s),setTimeout(function(){a(s)},o))}function d(i){i.parents(".cd-headline").hasClass("clip")&&i.parents(".cd-words-wrapper").animate({width:i.width()+10},l,function(){setTimeout(function(){a(i)},h)})}function r(i){return i.is(":last-child")?i.parent().children().eq(0):i.next()}function c(i,s){i.removeClass("is-visible").addClass("is-hidden"),s.removeClass("is-hidden").addClass("is-visible")}var o=2e3,l=500,h=3e3;e()}(jQuery);

//]]>         
</script>
</b:includable>
<b:includable id='backtop'>
<div class='back-to-top'><a href='#' id='back-to-top' title='back to top'><i class='far fa-chevron-up'/></a></div>
</b:includable>
<b:includable id='creditall'>
<div class='credit-footer'>&#169; Copyright 2023 - <a expr:href='data:blog.homepageUrl' expr:title='data:blog.title'><data:blog.title/></a> - Todos los Derechos Reservados.
    </div>
</b:includable>
<b:includable id='adsjs'>
<b:if cond='data:view.isPost'>
<script>
//<![CDATA[
!function(){var e=document.querySelector(".post-body"),n=e.querySelectorAll("div > br, span > br, div > p, span > p"),t=Math.ceil(.2*n.length),l=Math.ceil(.5*n.length),o=document.querySelector("#Middle-Ad-Slot1 .widget-content"),i=document.querySelector("#Middle-Ad-Slot2 .widget-content"),r=document.querySelector("#top-Ad-Slots .widget-content"),d=document.querySelector("#Ad-Slots-below .widget-content"),c=document.getElementById("iklan1"),a=document.getElementById("iklan2");function u(e,n){n.parentNode.insertBefore(e,n.nextSibling)}null!=r&&"\n"!=r.innerHTML&&e.insertBefore(r,e.childNodes[0]),null!=d&&"\n"!=d.innerHTML&&e.appendChild(d),0<n.length?(null!=o&&"\n"!=o.innerHTML&&u(o,null!==c?c:n[t]),null!=i&&"\n"!=i.innerHTML&&u(i,null!==a?a:n[l])):(o.parentNode.removeChild(o),i.parentNode.removeChild(i))}();
//]]>
</script>
</b:if>
</b:includable>
</b:defaultmarkup>
<b:defaultmarkup type='PopularPosts'>
    <b:includable id='main' var='this'>
      <b:include name='widget-title'/>
      <div class='widget-content'>
        <b:loop values='data:posts' var='post'>
          <b:include data='post' name='postContent'/>
        </b:loop>
      </div>
    </b:includable>
    <b:includable id='postContent' var='post'>
      <div class='post'>
        <div class='post-content'>
          <a class='post-image-link' expr:href='data:post.url'>
            <b:if cond='data:post.featuredImage'>
              <img class='sizeimg' expr:alt='data:post.title' expr:src='data:post.featuredImage resizeImage 680' expr:title='data:post.title'/>
              <b:else/>
              <img class='sizeimg' expr:alt='data:post.title' expr:title='data:post.title' src='https://4.bp.blogspot.com/-SKh7CYM3lB0/WZlRLgH8wII/AAAAAAAACjQ/vx5PJdQYhSo136-Wg-A633KcElrfkHNNACLcBGAs/s1600/non.png'/>
            </b:if>
          </a>
          <div class='post-info'>
            <h2 class='post-title'>
              <a expr:href='data:post.url'><data:post.title/></a>
            </h2>
            <div class='post-meta'>
              <span class='post-date published' expr:datetime='data:post.date.iso8601'><data:post.date/></span>
            </div>
          </div>
        </div>
      </div>
    </b:includable>
  </b:defaultmarkup>
<b:defaultmarkup type='Header'>
<b:includable id='main' var='this'>
<div class='header-widget'>
<b:include cond='data:imagePlacement in {&quot;REPLACE&quot;, &quot;BEFORE_DESCRIPTION&quot;}' name='image'/>
<b:include cond='data:imagePlacement == &quot;BEHIND&quot;' name='title'/>
</div>
</b:includable>
    <b:includable id='image'>
      <a class='header-image-wrapper' expr:href='data:blog.homepageUrl'>
        <img expr:alt='data:blog.title.escaped' expr:data-height='data:height' expr:data-width='data:width' expr:src='data:image'/>
      </a>
    </b:includable>
  </b:defaultmarkup>
  <b:defaultmarkup type='Label'>
    <b:includable id='main' var='this'>
      <b:include name='widget-title'/>
      <b:include name='content'/>
    </b:includable>
    <b:includable id='content'>
      <div class='widget-content'>
        <b:class expr:name='data:this.display + &quot;-label&quot;'/>
        <b:include cond='data:this.display == &quot;list&quot;' name='list'/>
        <b:include cond='data:this.display == &quot;cloud&quot;' name='list'/>
      </div>
    </b:includable>
    <b:includable id='list'>
      <ul>
        <b:loop values='data:labels' var='label'>
          <li>
            <a class='label-name' expr:href='data:label.url'>
              <data:label.name/>
              <b:if cond='data:this.showFreqNumbers'>
                <span class='label-count'><data:label.count/></span>
              </b:if>
            </a>
          </li>
        </b:loop>
      </ul>
    </b:includable>
  </b:defaultmarkup>
</b:defaultmarkups>
<!-- Google Analytics -->
<b:include data='blog' name='google-analytics'/>
<b:include name='fontstyle'/>
</head>
<body expr:class='data:blog.pageType'>
  <b:class cond='data:view.isHomepage' name='home'/>
  <b:class cond='data:view.isPage' name='item'/>
  <b:class cond='data:view.isArchive' name='index'/>
  <b:class cond='data:view.isError' name='boxerror'/>
<b:section class='template-option' id='template-option' maxwidgets='1' showaddelement='no'>
  <b:widget id='HTML100' locked='true' title='Theme Options' type='HTML' visible='true'>
    <b:widget-settings>
      <b:widget-setting name='content'/>
    </b:widget-settings>
    <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
  </b:widget>
</b:section>
 <!-- Wrapper -->
<div class='boxhome'>
  <!-- Header Wrapper -->
<header id='sticky-wrap'>
<div class='header-wrapper'>
<!-- Main Top Bar -->
  <div id='top-bar'>
        <b:section class='top-bar-nav' id='top-bar-nav' maxwidgets='1' showaddelement='yes'>
          <b:widget id='LinkList111' locked='true' title='' type='LinkList' visible='false'>
            <b:widget-settings>
              <b:widget-setting name='sorting'>NONE</b:widget-setting>
              <b:widget-setting name='text-1'>Quienes Somos</b:widget-setting>
              <b:widget-setting name='link-1'>https://www.blogger.com/</b:widget-setting>
              <b:widget-setting name='text-0'>Inicio</b:widget-setting>
              <b:widget-setting name='link-2'>https://www.blogger.com/</b:widget-setting>
              <b:widget-setting name='link-0'>/</b:widget-setting>
              <b:widget-setting name='text-2'>Contactanos</b:widget-setting>
            </b:widget-settings>
            <b:includable id='main'>
  <b:include name='widget-title'/>
  <b:include name='content'/>
</b:includable>
            <b:includable id='content'>
 <div class='widget-content'>
   <ul>
     <b:loop values='data:links' var='link'>
       <li><a expr:href='data:link.target'><data:link.name/></a></li>
     </b:loop>
   </ul>
 </div>
</b:includable>
          </b:widget>
        </b:section>

      <!-- Top Social --> 
        <b:section class='top-bar-social social' id='top-bar-social' maxwidgets='1' showaddelement='yes'>
           <b:widget id='LinkList112' locked='true' title='' type='LinkList' visible='false'>
             <b:widget-settings>
               <b:widget-setting name='link-3'>https://www.blogger.com/</b:widget-setting>
               <b:widget-setting name='sorting'>NONE</b:widget-setting>
               <b:widget-setting name='text-1'>twitter</b:widget-setting>
               <b:widget-setting name='link-1'>#</b:widget-setting>
               <b:widget-setting name='text-0'>facebook</b:widget-setting>
               <b:widget-setting name='link-2'>https://www.blogger.com/</b:widget-setting>
               <b:widget-setting name='text-3'>pinterest</b:widget-setting>
               <b:widget-setting name='link-0'>/</b:widget-setting>
               <b:widget-setting name='text-2'>instagram</b:widget-setting>
             </b:widget-settings>
             <b:includable id='main'>
  <b:include name='widget-title'/>
  <b:include name='content'/>
</b:includable>
             <b:includable id='content'>
 <div class='widget-content'>
   <ul>
     <b:loop values='data:links' var='link'>
       <li><a expr:href='data:link.target'><data:link.name/></a></li>
     </b:loop>
   </ul>
 </div>
</b:includable>
           </b:widget>
         </b:section>
    </div>
  
  <b:section class='headblog' id='headblog' maxwidgets='1' showaddelement='yes'>
    <b:widget id='Header1' locked='true' title='Mr Renta (cabecera)' type='Header' visible='true'>
      <b:widget-settings>
        <b:widget-setting name='displayUrl'>https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi-8zJWbzihkNTt_NBeMFxsv5wlMxSJtKnCqjUw0LBjN5b7ntS81gthyphenhyphen9aHl08Ja2Ca3mIpoTpdli3gH4okUj-eZi8H0_xxqYr8JAvfsNx4KjYrh0qyBqmOxisNk_6QySNa7K0WJz_ZD6ttcoKafluuzQCd2ggTEJAUo6Qa0WBWuBvHaZyllGVvH7UeJy4/s310/820-22.png</b:widget-setting>
        <b:widget-setting name='displayHeight'>83</b:widget-setting>
        <b:widget-setting name='sectionWidth'>312</b:widget-setting>
        <b:widget-setting name='useImage'>true</b:widget-setting>
        <b:widget-setting name='shrinkToFit'>false</b:widget-setting>
        <b:widget-setting name='imagePlacement'>REPLACE</b:widget-setting>
        <b:widget-setting name='displayWidth'>310</b:widget-setting>
      </b:widget-settings>
      <b:includable id='main' var='this'>
<div class='header-widget'>
<b:include cond='data:imagePlacement in {&quot;REPLACE&quot;, &quot;BEFORE_DESCRIPTION&quot;}' name='image'/>
<b:include cond='data:imagePlacement == &quot;BEHIND&quot;' name='title'/>
</div>
</b:includable>
      <b:includable id='behindImageStyle'>
    <b:if cond='data:sourceUrl'>
      <b:include cond='data:this.image' data='{                    image: data:this.image,                    selector: &quot;.header-widget&quot;                  }' name='responsiveImageStyle'/>
      <style type='text/css'>
        .header-widget {
          background-position: <data:blog.locale.languageAlignment/>;
          background-repeat: no-repeat;
          background-size: cover;
        }
      </style>
    </b:if>
  </b:includable>
      <b:includable id='description'>
    <p>
      <data:this.description/>
    </p>
  </b:includable>
      <b:includable id='image'>
      <a class='header-image-wrapper' expr:href='data:blog.homepageUrl'>
        <img expr:alt='data:blog.title.escaped' expr:data-height='data:height' expr:data-width='data:width' expr:src='data:image'/>
      </a>
    </b:includable>
      <b:includable id='title'>
    <h1>
      <b:tag cond='data:view.url != data:blog.homepageUrl' expr:href='data:blog.homepageUrl' name='a'>
        <data:title/>
      </b:tag>
    </h1>
  </b:includable>
    </b:widget>
  </b:section>

<!-- Script para hacer scroll al clic en el logo -->
<script type='text/javascript'>
  // Obtiene el elemento del logo por su ID
  var logo = document.getElementById(&#39;blogLogo&#39;);

  // Agrega un evento de clic al logo
  logo.addEventListener(&#39;click&#39;, function(e) {
    e.preventDefault(); // Previene el comportamiento predeterminado del enlace

    // Obtiene la sección a la que deseas hacer scroll
    var sectionToScroll = document.getElementById(&#39;headblog&#39;);

    // Realiza el scroll suave hacia la sección
    sectionToScroll.scrollIntoView({ behavior: &#39;smooth&#39; });
  });
</script>
  
  
  
<b:include name='btnmenu'/>
<div class='overlay' onclick='toggleMenu()'/>
<div class='menu'>
<div class='page-wrapper chiller-theme toggled'>
    <div class='header-menu'>
      <div class='mobile-menu'/>
        <b:section class='main-menu' id='main-menu' maxwidgets='1' showaddelement='yes'>
          <b:widget id='LinkList113' locked='true' title='Link List' type='LinkList' visible='true'>
            <b:widget-settings>
              <b:widget-setting name='link-5'>#</b:widget-setting>
              <b:widget-setting name='link-3'>#Testimonios</b:widget-setting>
              <b:widget-setting name='link-4'>#</b:widget-setting>
              <b:widget-setting name='text-1'>Quién soy</b:widget-setting>
              <b:widget-setting name='text-0'>Inicio</b:widget-setting>
              <b:widget-setting name='text-3'>Testimonios</b:widget-setting>
              <b:widget-setting name='text-2'>Servicios</b:widget-setting>
              <b:widget-setting name='text-5'>Contacto</b:widget-setting>
              <b:widget-setting name='text-4'>Pagos</b:widget-setting>
              <b:widget-setting name='sorting'>NONE</b:widget-setting>
              <b:widget-setting name='link-1'>#quiensoy</b:widget-setting>
              <b:widget-setting name='link-2'>#Servicios</b:widget-setting>
              <b:widget-setting name='link-0'>#Inicio</b:widget-setting>
            </b:widget-settings>
            <b:includable id='main'>
  <b:include name='widget-title'/>
  <b:include name='content'/>
</b:includable>
            <b:includable id='content'>
 <div class='widget-content'>
   <ul>
     <b:loop values='data:links' var='link'>
       <li><a expr:href='data:link.target'><data:link.name/></a></li>
     </b:loop>
   </ul>
 </div>
</b:includable>
          </b:widget>
        </b:section>
<b:include name='searchdesktop'/>
<b:include name='searchFormContainer'/>
</div>
    </div>
  </div>
<b:include name='searchmobile'/>
</div>
  </header>

<div class='clr'/>
<b:if cond='data:view.isHomepage'>
<div id='outer-wrapper'>
  <b:section class='digital-wrapper' id='Inicio' maxwidgets='1' showaddelement='yes'>
    <b:widget id='HTML17' locked='false' title='Réntame' type='HTML' visible='true'>
      <b:widget-settings>
        <b:widget-setting name='content'><![CDATA[<div class='boxcontent'>
          <div class='box-left'>
            <section class='cd-wrapper'>
              <div class='cd-headline clip'>
                <span class='cd-words-wrapper'>
                  <b class='is-visible'>para escucharte</b>
                  <b>para verte</b>
					<b>y caminar juntos</b>
                </span>
              </div>
            </section>
            <p>Mi objetivo va más allá de ofrecer tiempo; quiero ser un recordatorio de que el valor humano trasciende las métricas de productividad, incluso en el mundo virtual.</p>
            <div class='wpbtn'>
              <a class='btn-wite' href='#'>Réntame Ahora</a>
              
            </div>
          </div>
          <div class='box-right'><img src=''/>
          </div>
        </div>]]></b:widget-setting>
      </b:widget-settings>
      <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
    </b:widget>
  </b:section>
</div>
</b:if>
</div>

<script>
  // JavaScript para scroll suave al hacer clic en el botón de &quot;Inicio&quot;
  document.querySelector(&#39;a[href=&quot;#Inicio&quot;]&#39;).addEventListener(&#39;click&#39;, function(event) {
    event.preventDefault(); // Evitar el comportamiento predeterminado del enlace

    // Calcular el desplazamiento al elemento de inicio
    const inicioElement = document.getElementById(&#39;Inicio&#39;);
    const yOffset = -100; // Ajusta el desplazamiento según sea necesario
    const y = inicioElement.getBoundingClientRect().top + window.pageYOffset + yOffset;

    // Desplazarse suavemente al elemento de inicio
    window.scrollTo({ top: y, behavior: &#39;smooth&#39; });
  });
</script>
  
<div class='clr'/>
<b:if cond='data:view.isHomepage'>
<div class='boxmarket'>
<div id='outer-wrapper'>
<div class='marketblog'>
<div class='boxwrap-text'>
<b:section class='boxwrap-text' id='quiensoy' maxwidgets='1' showaddelement='yes'>
  <b:widget id='HTML10' locked='false' title='Sobre Mí' type='HTML' visible='true'>
    <b:widget-settings>
      <b:widget-setting name='content'><![CDATA[<div class='marketleft'>
          <h2>¡Hola a todos! <span>Soy Ozz</span></h2>

          <p>A mis 30 años, me considero amigable, social, serio cuando se requiere y siempre con una sonrisa lista para alegrar el día. Utilizo las redes sociales y plataformas virtuales como Blogger para brindar importancia de detenernos y valorar el simple hecho de estar juntos, incluso a distancia. No todo se trata de productividad; compartir momentos, aunque no impliquen "hacer" algo en el sentido convencional, también tiene un valor significativo en nuestras vidas. En un mundo donde la constante ocupación parece ser la medida del éxito, es esencial recordar que el simple acto de estar presente, aunque sea en una pantalla, tiene su propio valor.
La compañía humana es un regalo invaluable que puede hacernos sentir conectados, apoyados y amados, ¡incluso a través de la tecnología! Si te sientes solo o necesitas compañía virtual, estoy aquí para ti. ¡Será un placer compartir tiempo contigo a través de la pantalla!
Mi objetivo va más allá de ofrecer tiempo; quiero ser un recordatorio de que el valor humano trasciende las métricas de productividad, incluso en el mundo virtual.
Valoremos cada momento, incluso en la simple conexión humana a través de las pantallas.</p>

        </div>

        <div class='marketright'>
          <img alt='' src='https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEinQ4jSZLQx2LB8VLZ_rcC7LG31gYPALwfPT9s6dkKsSqBBSMVuZOIY2CGALMlt7bjahSWuRNZZhTJ8tSYD6I36B8z6f-VokKIFSVVt7n1D_ZSZXbj1m8c3Dw6uoNFnDNKdgu5nz8WfX_Z65Djl-WGteBHtTAKOHs_gItaSruttKV7WgqssMewEQjNr4d0/s16000/IMG_5037.jpg'/>
        </div>]]></b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
  </b:widget>
</b:section>

</div>
</div>
</div>
</div>
<script>
  document.addEventListener(&quot;DOMContentLoaded&quot;, function() {
    const links = document.querySelectorAll(&#39;a[href^=&quot;#&quot;]&#39;);
    links.forEach(link =&gt; {
      link.addEventListener(&quot;click&quot;, scrollToSection);
    });

    function scrollToSection(event) {
      event.preventDefault();
      const targetId = this.getAttribute(&quot;href&quot;);
      const targetSection = document.querySelector(targetId);

      const menuHeight = 80; // Altura del menú en píxeles

      if (targetSection) {
        const targetPosition = targetSection.getBoundingClientRect().top + window.pageYOffset - menuHeight;
        window.scrollTo({
          top: targetPosition,
          behavior: &quot;smooth&quot;
        });
      }
    }
  });
</script>

<div class='clr'/>
<div class='statiswrap'>
<div id='outer-wrapper'>
<div class='boxwrap-text'>
  
<b:section class='boxwrap-text' id='Servicios' maxwidgets='1' showaddelement='yes'>
  <b:widget id='HTML11' locked='false' title='Servicioz' type='HTML' visible='true'>
    <b:widget-settings>
      <b:widget-setting name='content'><![CDATA[<div class='boxwrap-wrap'>
<div class='boxwrap-os-left'>
  <h2>Mi enfoque es simple: <span>estar presente para ti</span></h2>
</div>
<div class='boxwrap-os-right'>
  <p>Ofrezco un espacio de escucha y acompañamiento, tanto por teléfono como en video llamadas, donde te brindo atención amable y libre de juicios. Además, estoy disponible para encuentros presenciales donde podemos compartir momentos y conversaciones enriquecedoras, todo con el objetivo de recordarte el valor humano más allá de las métricas de productividad. Sin imponer opiniones, y valorar cada momento de conexión humana, incluso a través de las pantallas.</p>
</div>
</div>
<div class='tabs'>
  <input checked='' id='tab1' name='tab-control' type='radio'/>
  <input id='tab2' name='tab-control' type='radio'/>
  <input id='tab3' name='tab-control' type='radio'/>
  <input id='tab4' name='tab-control' type='radio'/>
  <input id='tab5' name='tab-control' type='radio'/>
<ul>
<li title=''><label class='color1' for='tab1' role='button'><i class='fad fa-mobile-alt'></i><span>Llamadas telefónicas</span></label></li>
<li title=''><label class='color2' for='tab2' role='button'><i class='fad fa-video'></i><span>Video llamadas</span></label></li>
<li title=''><label class='color3' for='tab3' role='button'><i class='fad fa-user-friends'></i><span>Presencial</span></label></li> 
</ul>

<div class='content'>
<section>
<div class='content-left'>
<div class='serviceimg'> 
<img alt='' src='https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEitfCYWEUfK1WETld9Vr3YUTzsEqCXDi6qLLtbz0ek88AC8mgVKMLIGFRZLkUR3lnjyqYMD76zZcTn0V4bfNH3aszETith5RuU0XMrw6feYHuPTItkWHnL8utGkSx-SPfaQOh9i29k6eADEFYMHFY0cRJp26qwPjVCwC_IeH6o4HcIfwrIVcbxLKlEs3Os/s1600/Llamda-t%C3%A9lefonica.png'/></div>
</div>
<div class='content-right'>
<h3>Llamadas telefónicas</h3>
<h>Escucharte de manera amable y sin prejuicios</h>
<h>Si necesitas un espacio para hablar sin restricciones ni juicios, estoy aquí para ti</h>
<h>No estoy obligado a dar una opinión concreta para evitar influir en tus decisiones</h>

<ul>
<li><i class="fas fa-heart blue-heart"></i>
<style>
.blue-heart {
    color: blue;
}
</style><span>Valoremos cada momento, incluso en la simple conexión humana a través de las pantallas.</span></li>
</ul>

<a class='octf-btn btnfont btncolor' href='#'>Quiero rentarte 🙈</a>
</div>
</section>

<section>
<div class='content-left'>
<div class='serviceimg'> 
<img alt='' src='https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgwx0NxOIH8YTdhhIFjyBR5nAZa7wYj8IWSjBKLiwWWnXs9ht8t7fG2PuHXd17JSeE29I4ymFsijfUo8zsJtyO9GIM5omjMTfi3c-xhd_VNeDHEtpLeaNWsAgqQm-XYsrzTFvEny3lKmL-oIYlihplGquCMEHcCyRVkDX4irD47xNcMCwa3PyEmzbvlV98/s1600/video-llamda.png'/></div>
</div>
<div class='content-right'>
<h3>Video llamadas</h3>
<h>Simplemente verte y escucharte de la manera más simple y amable.</h>
<h>No estoy obligado a dar una opinión en concreto ya que puede incurrir en no tener el resultado que alguien desee</h>
<h>y si la persona quiere una opinion que no este sujeta al  cambio o resultado</h>
<ul>
<li><i class="fas fa-heart blue-heart"></i>
<style>
.blue-heart {
    color: blue;
}
</style><span>Valoremos cada momento, incluso en la simple conexión humana a través de las pantallas.</span></li>
</ul>

<a class='octf-btn btnfont btncolor' href='#'>Quiero rentarte 🙈</a>
</div>
</section>

<section>
<div class='content-left'>
<div class='serviceimg'> 
<img alt='' src='https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi0WbRYUfOaef1TagFLh1x9_Q1H6G77W11HVIBPhNA8rT1tLAswUc4CI_uARto6E3uVAo95BZkYu0FjoqP7uWNCALhbYl2N9dSnrUBmnU0Bjy4hV1vKFzDbko7tObYfYhQWfzZeZLkcbVrig73kVVWd9FZFLcHUPmAa7VTUhkAtUv-DqB5mb03fa24bm6o/s1600/Servicio-presencial.png'/></div>
</div>
<div class='content-right'>
<h3>Presencial</h3>
<h>Tener una conversación, común o interesante,</h>
<h>quiero escucharte de la manera más simple y amable.</h>

<ul>
<li><i class="fas fa-heart blue-heart"></i>
<style>
.blue-heart {
    color: blue;
}
</style><span>Valoremos cada momento, incluso en la simple conexión humana a través de las pantallas.</span></li>
</ul>

<a class='octf-btn btnfont btncolor' href='#'>Quiero rentarte 🙈</a>
</div>
</section>
<section>
<div class='content-left'>
<div class='serviceimg'>
 
<img alt='' src='https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi0WbRYUfOaef1TagFLh1x9_Q1H6G77W11HVIBPhNA8rT1tLAswUc4CI_uARto6E3uVAo95BZkYu0FjoqP7uWNCALhbYl2N9dSnrUBmnU0Bjy4hV1vKFzDbko7tObYfYhQWfzZeZLkcbVrig73kVVWd9FZFLcHUPmAa7VTUhkAtUv-DqB5mb03fa24bm6o/s1600/Servicio-presencial.png'/></div>
</div>

<div class='content-right'>
<h3>Social Media</h3>
<p>Crearemos un plan, aplicando el marketing de contenidos enfocado en potenciar tu presencia en redes sociales. Realizaremos campañas efectivas para que llegues a clientes potencial y obtengan tu producto y/o servicio.</p>
<ul>
<li><i class='fad icon1 fa-analytics'></i><span>te ofrecemos la mejor solución de acuerdo a tus necesidades</span></li>
<li><i class='fab icon2 fa-accusoft'></i><span>Para mejorar los resultados para tu negocio</span></li>
</ul>
<a class='octf-btn btnfont btncolor' href='#'>Elegir Planes</a>
</div>
</section>
<section>
<div class='content-left'>
<div class='serviceimg'> 
<img alt='' src='https://1.bp.blogspot.com/-cdaYetQIMPE/Xu3Caqq4r5I/AAAAAAAAALo/sUIpfpmyWzYOpcJm9hzNIX1yKjicRcBqACLcBGAsYHQ/s1600/dg_web.png'/></div>
</div>
<div class='content-right'>
<h3>Diseño Web</h3>
<p>Desarrollaremos la página web que necesita tu empresa para estar en las primeras posiciones de los buscadores. Te garantizamos una buena experiencia del usuario para que se conviertan en potenciales clientes.</p>
<ul>
<li><i class='fad icon1 fa-analytics'></i><span>te ofrecemos la mejor solución de acuerdo a tus necesidades</span></li>
<li><i class='fab icon2 fa-accusoft'></i><span>Para mejorar los resultados para tu negocio</span></li>
</ul>
<a class='octf-btn btnfont btncolor' href='#'>Elegir Planes</a>
</div>
</section>
</div>
</div>]]></b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
  </b:widget>
</b:section>
</div>
</div>
</div>
  
  
  
  
  
  
<div class='clr'/>
 <div class='recent-warpper'>   
   <div class='recent-boxes'> 
     <b:section class='RecentNew' id='RecentNew' maxwidgets='1' showaddelement='yes'>
        <b:widget id='HTML4' locked='false' title='Pago' type='HTML' visible='true'>
          <b:widget-settings>
            <b:widget-setting name='content'/>
          </b:widget-settings>
          <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
        </b:widget>
      </b:section>
     </div>
</div>
<div class='clr'/>
<b:section class='box-convert' id='box-convert' maxwidgets='1' showaddelement='yes'/>
</b:if>
    
<!-- Outer Wrapper -->
<div id='outer-wrapper'>
  <!-- Content Wrapper -->
  <div id='content-wrapper'>
    <div class='container'>
      <!-- Main Wrapper -->
      <main class='main-wrapper'>
        <b:section class='main' id='main' maxwidgets='1' showaddelement='yes'>
          <b:widget id='Blog1' locked='true' title='Entradas del blog' type='Blog' visible='true'>
            <b:widget-settings>
              <b:widget-setting name='showDateHeader'>false</b:widget-setting>
              <b:widget-setting name='commentLabel'>Comments</b:widget-setting>
              <b:widget-setting name='style.textcolor'>#ffffff</b:widget-setting>
              <b:widget-setting name='showShareButtons'>true</b:widget-setting>
              <b:widget-setting name='authorLabel'>by</b:widget-setting>
              <b:widget-setting name='showCommentLink'>true</b:widget-setting>
              <b:widget-setting name='style.urlcolor'>#ffffff</b:widget-setting>
              <b:widget-setting name='showAuthor'>true</b:widget-setting>
              <b:widget-setting name='style.linkcolor'>#ffffff</b:widget-setting>
              <b:widget-setting name='style.unittype'>TextAndImage</b:widget-setting>
              <b:widget-setting name='style.bgcolor'>#ffffff</b:widget-setting>
              <b:widget-setting name='timestampLabel'/>
              <b:widget-setting name='reactionsLabel'/>
              <b:widget-setting name='showAuthorProfile'>true</b:widget-setting>
              <b:widget-setting name='style.layout'>1x1</b:widget-setting>
              <b:widget-setting name='showLabels'>true</b:widget-setting>
              <b:widget-setting name='showLocation'>false</b:widget-setting>
              <b:widget-setting name='postLabelsLabel'>Tags</b:widget-setting>
              <b:widget-setting name='showTimestamp'>true</b:widget-setting>
              <b:widget-setting name='postsPerAd'>1</b:widget-setting>
              <b:widget-setting name='showBacklinks'>false</b:widget-setting>
              <b:widget-setting name='style.bordercolor'>#ffffff</b:widget-setting>
              <b:widget-setting name='showInlineAds'>false</b:widget-setting>
              <b:widget-setting name='showReactions'>false</b:widget-setting>
            </b:widget-settings>
            <b:includable id='main' var='this'>
  <div class='blog-posts hfeed container'>
    <b:loop index='i' values='data:posts' var='post'>
      <b:include data='post' name='postCommentsAndAd'/>
    </b:loop>
  </div>
  <b:include cond='data:view.isMultipleItems' name='postPagination'/>
  <b:include name='feedLinks'/>
</b:includable>
            <b:includable id='aboutPostAuthor'>
  <div class='author-name'>
    <a class='g-profile' expr:href='data:post.author.profileUrl' rel='author' title='author profile'>
      <span>
        <data:post.author.name/>
      </span>
    </a>
  </div>
  <div>
    <span class='author-desc'>
      <data:post.author.aboutMe/>
    </span>
  </div>
</b:includable>
            <b:includable id='addComments'>
  <a expr:href='data:post.commentsUrl' expr:onclick='data:post.commentsUrlOnclick'>
    <b:message name='messages.postAComment'/>
  </a>
</b:includable>
            <b:includable id='blogThisShare'>
  <b:with value='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=270,width=475\&quot;); return false;&quot;' var='onclick'>
    <b:include name='platformShare'/>
  </b:with>
</b:includable>
            <b:includable id='bylineByName' var='byline'>
  <b:switch var='data:byline.name'>
  <b:case value='share'/>
    <b:include cond='data:post.shareUrl' name='postShareButtons'/>
  <b:case value='comments'/>
    <b:include cond='data:post.allowComments' name='postCommentsLink'/>
  <b:case value='location'/>
    <b:include cond='data:post.location' name='postLocation'/>
  <b:case value='timestamp'/>
    <b:include cond='not data:view.isPage' name='postTimestamp'/>
  <b:case value='author'/>
    <b:include name='postAuthor'/>
  <b:case value='labels'/>
    <b:include cond='data:post.labels' name='postLabels'/>
  <b:case value='icons'/>
    <b:include cond='data:post.emailPostUrl' name='emailPostIcon'/>
  </b:switch>
</b:includable>
            <b:includable id='bylineRegion' var='regionItems'>
  <b:loop values='data:regionItems' var='byline'>
    <b:include data='byline' name='bylineByName'/>
  </b:loop>
</b:includable>
            <b:includable id='commentAuthorAvatar'>
  <div class='avatar-image-container'>
    <img class='author-avatar' expr:src='data:comment.authorAvatarSrc' height='35' width='35'/>
  </div>
</b:includable>
            <b:includable id='commentDeleteIcon' var='comment'>
  <span expr:class='&quot;item-control &quot; + data:comment.adminClass'>
    <b:if cond='data:showCmtPopup'>
      <div class='goog-toggle-button'>
        <div class='goog-inline-block comment-action-icon'/>
      </div>
    <b:else/>
      <a class='comment-delete' expr:href='data:comment.deleteUrl' expr:title='data:messages.deleteComment'>
        <img src='https://resources.blogblog.com/img/icon_delete13.gif'/>
      </a>
    </b:if>
  </span>
</b:includable>
            <b:includable id='commentForm' var='post'>
  <div class='comment-form'>
    <a name='comment-form'/>
    <h4 id='comment-post-message'><data:messages.postAComment/></h4>
    <b:if cond='data:this.messages.blogComment != &quot;&quot;'>
      <p><data:this.messages.blogComment/></p>
    </b:if>
    <b:include data='post' name='commentFormIframeSrc'/>
    <iframe allowtransparency='allowtransparency' class='blogger-iframe-colorize blogger-comment-from-post' expr:height='data:cmtIframeInitialHeight ?: &quot;90px&quot;' frameborder='0' id='comment-editor' name='comment-editor' src='' width='100%'/>
    <data:post.cmtfpIframe/>
    <script type='text/javascript'>
      BLOG_CMT_createIframe(&#39;<data:post.appRpcRelayPath/>&#39;);
    </script>
  </div>
</b:includable>
            <b:includable id='commentFormIframeSrc' var='post'>
  <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
</b:includable>
            <b:includable id='commentItem' var='comment'>
  <div class='comment' expr:id='&quot;c&quot; + data:comment.id'>
    <b:include cond='data:blog.enabledCommentProfileImages' name='commentAuthorAvatar'/>

    <div class='comment-block'>
      <div class='comment-author'>
        <b:if cond='data:comment.authorUrl'>
          <b:message name='messages.authorSaidWithLink'>
            <b:param expr:value='data:comment.author' name='authorName'/>
            <b:param expr:value='data:comment.authorUrl' name='authorUrl'/>
          </b:message>
        <b:else/>
          <b:message name='messages.authorSaid'>
            <b:param expr:value='data:comment.author' name='authorName'/>
          </b:message>
        </b:if>
      </div>
      <div expr:class='&quot;comment-body&quot; + (data:comment.isDeleted ? &quot; deleted&quot; : &quot;&quot;)'>
        <data:comment.body/>
      </div>
      <div class='comment-footer'>
        <span class='comment-timestamp'>
          <a expr:href='data:comment.url' title='comment permalink'>
            <data:comment.timestamp/>
          </a>
          <b:include data='comment' name='commentDeleteIcon'/>
        </span>
      </div>
    </div>
  </div>
</b:includable>
            <b:includable id='commentList' var='comments'>
  <div id='comments-block'>
    <b:loop values='data:comments' var='comment'>
      <b:include data='comment' name='commentItem'/>
    </b:loop>
  </div>
</b:includable>
            <b:includable id='commentPicker' var='post'>
  <b:if cond='data:post.showThreadedComments'>
    <b:include data='post' name='threadedComments'/>
  <b:else/>
    <b:include data='post' name='comments'/>
  </b:if>
</b:includable>
            <b:includable id='comments' var='post'>
  <section expr:class='&quot;comments&quot; + (data:post.embedCommentForm ? &quot; embed&quot; : &quot;&quot;)' expr:data-num-comments='data:post.numberOfComments' id='comments'>
    <a name='comments'/>
    <b:if cond='data:post.allowComments'>

      <b:include name='commentsTitle'/>

      <div expr:id='data:widget.instanceId + &quot;_comments-block-wrapper&quot;'>
        <b:include cond='data:post.comments' data='post.comments' name='commentList'/>
      </div>

      <b:if cond='data:post.commentPagingRequired'>
        <div class='paging-control-container'>
          <b:if cond='data:post.hasOlderLinks'>
            <a expr:class='data:post.oldLinkClass' expr:href='data:post.oldestLinkUrl'>
              <data:messages.oldest/>
            </a>
            <a expr:class='data:post.oldLinkClass' expr:href='data:post.olderLinkUrl'>
              <data:messages.older/>
            </a>
          </b:if>

          <span class='comment-range-text'>
            <data:post.commentRangeText/>
          </span>

          <b:if cond='data:post.hasNewerLinks'>
            <a expr:class='data:post.newLinkClass' expr:href='data:post.newerLinkUrl'>
              <data:messages.newer/>
            </a>
            <a expr:class='data:post.newLinkClass' expr:href='data:post.newestLinkUrl'>
              <data:messages.newest/>
            </a>
          </b:if>
        </div>
      </b:if>

      <div class='footer'>
        <b:if cond='data:post.embedCommentForm'>
          <b:if cond='data:post.allowNewComments'>
            <b:include data='post' name='commentForm'/>
          <b:else/>
            <data:post.noNewCommentsText/>
          </b:if>
        <b:else/>
          <b:if cond='data:post.allowComments'>
            <b:include data='post' name='addComments'/>
          </b:if>
        </b:if>
      </div>
    </b:if>
    <b:if cond='data:showCmtPopup'>
      <div id='comment-popup'>
        <iframe allowtransparency='allowtransparency' frameborder='0' id='comment-actions' name='comment-actions' scrolling='no'>
        </iframe>
      </div>
    </b:if>
  </section>
</b:includable>
            <b:includable id='commentsLink'>
  <a class='comment-link' expr:href='data:post.commentsUrl' expr:onclick='data:post.commentsUrlOnclick'>
    <b:if cond='data:post.numberOfComments &gt; 0'>
      <b:message name='messages.numberOfComments'>
        <b:param expr:value='data:post.numberOfComments' name='numComments'/>
      </b:message>
    <b:else/>
      <data:messages.postAComment/>
    </b:if>
  </a>
</b:includable>
            <b:includable id='commentsLinkIframe'>
  <!-- G+ comments, no longer available. The includable is retained for backwards-compatibility. -->
</b:includable>
            <b:includable id='commentsTitle'>
  <h3 class='title'><data:messages.comments/></h3>
</b:includable>
            <b:includable id='defaultAdUnit'>
  <ins class='adsbygoogle' data-ad-format='auto' expr:data-ad-client='data:adClientId ?: data:blog.adsenseClientId' expr:data-ad-host='data:blog.adsenseHostId' expr:style='data:style ?: &quot;display: block;&quot;'>
    <b:attr cond='not data:blog.analytics4' expr:value='data:blog.analyticsAccountNumber' name='data-analytics-uacct'/>
  </ins>
  <script>
   (adsbygoogle = window.adsbygoogle || []).push({});
  </script>
</b:includable>
            <b:includable id='emailPostIcon'>
  <span class='byline post-icons'>
    <!-- email post links -->
    <span class='item-action'>
      <a expr:href='data:post.emailPostUrl' expr:title='data:messages.emailPost'>
        <b:include data='{ iconClass: &quot;touch-icon sharing-icon&quot; }' name='emailIcon'/>
      </a>
    </span>
  </span>
</b:includable>
            <b:includable id='facebookShare'>
  <b:with value='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=430,width=640\&quot;); return false;&quot;' var='onclick'>
    <b:include name='platformShare'/>
  </b:with>
</b:includable>
            <b:includable id='feedLinks'>
  <b:if cond='!data:view.isPost'> <!-- Blog feed links -->
    <b:if cond='data:feedLinks'>
      <div class='blog-feeds'>
        <b:include data='feedLinks' name='feedLinksBody'/>
      </div>
    </b:if>
  <b:else/> <!--Post feed links -->
    <div class='post-feeds'>
      <b:loop values='data:posts' var='post'>
        <b:if cond='data:post.allowComments and data:post.feedLinks'>
          <b:include data='post.feedLinks' name='feedLinksBody'/>
        </b:if>
      </b:loop>
    </div>
  </b:if>
</b:includable>
            <b:includable id='feedLinksBody' var='links'>
  <div class='feed-links'>
  <data:messages.subscribeTo/>
  <b:loop values='data:links' var='f'>
     <a class='feed-link' expr:href='data:f.url' expr:type='data:f.mimeType' target='_blank'><data:f.name/> (<data:f.feedType/>)</a>
  </b:loop>
  </div>
</b:includable>
            <b:includable id='footerBylines'>
  <b:if cond='data:widgets.Blog.first.footerBylines'>
    <b:loop index='i' values='data:widgets.Blog.first.footerBylines' var='region'>
      <b:if cond='not data:region.items.empty'>
        <div expr:class='&quot;post-footer-line post-footer-line-&quot; + (data:i + 1)'>
          <b:with value='&quot;footer-&quot; + (data:i + 1)' var='regionName'>
            <b:include data='region.items' name='bylineRegion'/>
          </b:with>
        </div>
      </b:if>
    </b:loop>
  </b:if>
</b:includable>
            <b:includable id='googlePlusShare'>
</b:includable>
            <b:includable id='headerByline'>
  <b:if cond='data:widgets.Blog.first.headerByline'>
    <div class='post-header'>
      <div class='post-header-line-1'>
        <b:with value='&quot;header-1&quot;' var='regionName'>
          <b:include data='data:widgets.Blog.first.headerByline.items' name='bylineRegion'/>
        </b:with>
      </div>
    </div>
  </b:if>
</b:includable>
            <b:includable id='homePageLink'>
  <a class='home-link' expr:href='data:blog.homepageUrl'>
    <data:messages.home/>
  </a>
</b:includable>
            <b:includable id='iframeComments' var='post'>
  <!-- G+ comments, no longer available. The includable is retained for backwards-compatibility. -->
</b:includable>
            <b:includable id='inlineAd' var='post'>
  <b:if cond='!data:view.isPreview'>
    <b:if cond='data:this.adCode or data:this.adClientId or data:blog.adsenseClientId'>
      <!-- Ad -->
      <div class='inline-ad'>
        <b:if cond='data:this.adCode != &quot;&quot;'>
          <data:this.adCode/>
        <b:else/>
          <b:include cond='data:this.adClientId or data:blog.adsenseClientId' name='defaultAdUnit'/>
        </b:if>
      </div>
    </b:if>
  <b:else/>
    <div class='inline-ad'>
      <div class='inline-ad-placeholder'>
        <span><b:message name='messages.adsGoHere'/></span>
      </div>
    </div>
  </b:if>
</b:includable>
            <b:includable id='linkShare'>
  <b:with value='&quot;window.prompt(\&quot;Copy to clipboard: Ctrl+C, Enter\&quot;, \&quot;&quot; + data:originalUrl + &quot;\&quot;); return false;&quot;' var='onclick'>
    <b:include name='platformShare'/>
  </b:with>
</b:includable>
            <b:includable id='nextPageLink'>
  <a class='blog-pager-older-link' expr:href='data:olderPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-older-link&quot;' expr:title='data:messages.olderPosts'>
    <data:messages.olderPosts/>
  </a>
</b:includable>
            <b:includable id='otherSharingButton'>
  <span class='sharing-platform-button sharing-element-other' expr:aria-label='data:messages.shareToOtherApps.escaped' expr:data-url='data:originalUrl' expr:title='data:messages.shareToOtherApps.escaped' role='menuitem' tabindex='-1'>
    <b:with value='{key: &quot;sharingOther&quot;}' var='platform'>
      <b:include name='sharingPlatformIcon'/>
    </b:with>
    <span class='platform-sharing-text'><data:messages.shareOtherApps.escaped/></span>
  </span>
</b:includable>
            <b:includable id='platformShare'>
  <a expr:class='&quot;goog-inline-block sharing-&quot; + data:platform.key' expr:data-url='data:originalUrl' expr:href='data:shareUrl + &quot;&amp;target=&quot; + data:platform.target' expr:onclick='data:onclick ? data:onclick : &quot;&quot;' expr:title='data:platform.shareMessage' target='_blank'>
    <span class='share-button-link-text'>
      <data:platform.shareMessage/>
    </span>
  </a>
</b:includable>
            <b:includable id='post' var='post'>
  <div class='post'>
    <b:include data='post' name='postMeta'/>
    <b:include data='post' name='postTitle'/>
    <b:include name='headerByline'/>
    <b:if cond='data:view.isSingleItem'>
      <b:include data='post' name='postBody'/>
    <b:else/>
      <b:include data='post' name='postBodySnippet'/>
      <b:include data='post' name='postJumpLink'/>
    </b:if>
    <b:include data='post' name='postFooter'/>
  </div>
</b:includable>
            <b:includable id='postAuthor'>
  <span class='byline post-author vcard'>
    <span class='post-author-label'>
      <data:byline.label/>
    </span>
    <span class='fn'>
      <b:if cond='data:post.author.profileUrl'>
        <meta expr:content='data:post.author.profileUrl'/>
        <a class='g-profile' expr:href='data:post.author.profileUrl' rel='author' title='author profile'>
          <span><data:post.author.name/></span>
        </a>
      <b:else/>
        <span><data:post.author.name/></span>
      </b:if>
    </span>
  </span>
</b:includable>
            <b:includable id='postBody' var='post'>
  <!-- If metaDescription is empty, use the post body as the schema.org description too, for G+/FB snippeting. -->
  <div class='post-body entry-content float-container' expr:id='&quot;post-body-&quot; + data:post.id'>
    <data:post.body/>
  </div>
</b:includable>
            <b:includable id='postBodySnippet' var='post'>
  <b:include data='post' name='postBody'/>
</b:includable>
            <b:includable id='postCommentsAndAd' var='post'>
  <article class='post-outer-container'>
    <!-- Post title and body -->
    <div class='post-outer'>
      <b:include data='post' name='post'/>
    </div>

    <!-- Comments -->
    <b:include cond='data:view.isSingleItem' data='post' name='commentPicker'/>

    <!-- Show ad inside post container, after comments, if single item. -->
    <b:include cond='data:view.isSingleItem and data:post.includeAd' data='post' name='inlineAd'/>
  </article>

  <!-- Show ad outside post container (between posts) for feed pages. -->
  <b:include cond='data:view.isMultipleItems and data:post.includeAd' data='post' name='inlineAd'/>
</b:includable>
            <b:includable id='postCommentsLink'>
  <b:if cond='data:view.isMultipleItems'>
    <span class='byline post-comment-link container'>
      <b:include cond='data:post.commentSource != 1' name='commentsLink'/>
    </span>
  </b:if>
</b:includable>
            <b:includable id='postFooter' var='post'>
  <div class='post-footer'>
    <b:include name='footerBylines'/>
    <b:include data='post' name='postFooterAuthorProfile'/>
  </div>
</b:includable>
            <b:includable id='postFooterAuthorProfile' var='post'>
  <b:if cond='data:post.author.aboutMe and data:view.isPost'>
    <div class='author-profile'>
      <b:if cond='data:post.author.authorPhoto.url'>
        <img class='author-image' expr:src='data:post.author.authorPhoto.url' width='50px'/>
        <div class='author-about'>
          <b:include data='post' name='aboutPostAuthor'/>
        </div>
      <b:else/>
        <b:include data='post' name='aboutPostAuthor'/>
      </b:if>
    </div>
  </b:if>
</b:includable>
            <b:includable id='postHeader' var='post'>
  <b:include name='headerByline'/>
</b:includable>
            <b:includable id='postJumpLink' var='post'>
  <div class='jump-link flat-button'>
    <a expr:href='data:post.url fragment &quot;more&quot;' expr:title='data:post.title'>
      <b:eval expr='data:blog.jumpLinkMessage'/>
    </a>
  </div>
</b:includable>
            <b:includable id='postLabels'>
  <span class='byline post-labels'>
    <span class='byline-label'><data:byline.label/></span>
    <b:loop index='i' values='data:post.labels' var='label'>
      <a expr:href='data:label.url' rel='tag'>
        <data:label.name/>
      </a>
    </b:loop>
  </span>
</b:includable>
            <b:includable id='postLocation'>
  <span class='byline post-location'>
    <data:byline.label/>
    <a expr:href='data:post.location.mapsUrl' target='_blank'><data:post.location.name/></a>
  </span>
</b:includable>
            <b:includable id='postMeta' var='post'>
  <b:include data='post' name='postMetadataJSON'/>
</b:includable>
            <b:includable id='postMetadataJSONImage'>
  &quot;image&quot;: {
    &quot;@type&quot;: &quot;ImageObject&quot;,
    <b:if cond='data:post.featuredImage.isResizable'>
    &quot;url&quot;: &quot;<b:eval expr='resizeImage(data:post.featuredImage, 1200, &quot;1200:630&quot;)'/>&quot;,
    &quot;height&quot;: 630,
    &quot;width&quot;: 1200
    <b:else/>
    &quot;url&quot;: &quot;https://blogger.googleusercontent.com/img/b/U2hvZWJveA/AVvXsEgfMvYAhAbdHksiBA24JKmb2Tav6K0GviwztID3Cq4VpV96HaJfy0viIu8z1SSw_G9n5FQHZWSRao61M3e58ImahqBtr7LiOUS6m_w59IvDYwjmMcbq3fKW4JSbacqkbxTo8B90dWp0Cese92xfLMPe_tg11g/w1200/&quot;,
    &quot;height&quot;: 348,
    &quot;width&quot;: 1200
    </b:if>
  },
</b:includable>
            <b:includable id='postMetadataJSONPublisher'>
 &quot;publisher&quot;: {
    &quot;@type&quot;: &quot;Organization&quot;,
    &quot;name&quot;: &quot;Blogger&quot;,
    &quot;logo&quot;: {
      &quot;@type&quot;: &quot;ImageObject&quot;,
      &quot;url&quot;: &quot;https://blogger.googleusercontent.com/img/b/U2hvZWJveA/AVvXsEgfMvYAhAbdHksiBA24JKmb2Tav6K0GviwztID3Cq4VpV96HaJfy0viIu8z1SSw_G9n5FQHZWSRao61M3e58ImahqBtr7LiOUS6m_w59IvDYwjmMcbq3fKW4JSbacqkbxTo8B90dWp0Cese92xfLMPe_tg11g/h60/&quot;,
      &quot;width&quot;: 206,
      &quot;height&quot;: 60
    }
  },
</b:includable>
            <b:includable id='postPagination'>
  <div class='blog-pager container' id='blog-pager'>
    <b:include cond='data:newerPageUrl' name='previousPageLink'/>
    <b:include cond='data:olderPageUrl' name='nextPageLink'/>
    <b:include cond='data:view.url != data:blog.homepageUrl' name='homePageLink'/>
  </div>
</b:includable>
            <b:includable id='postReactions'>
  <!-- Reaction feature no longer available. The includable is retained for backwards-compatibility. -->
</b:includable>
            <b:includable id='postShareButtons'>
  <div class='byline post-share-buttons goog-inline-block'>
    <b:with value='data:sharingId ?: ((data:widget.instanceId ?: &quot;sharing&quot;) + &quot;-&quot; + (data:regionName ?: &quot;byline&quot;) + &quot;-&quot; + data:post.id)' var='sharingId'>
      <!-- Note: 'sharingButtons' includable is from the default Sharing widget markup. -->
      <b:include data='{                                                sharingId: data:sharingId,                                                originalUrl: data:post.url,                                                platforms: data:this.sharing.platforms,                                                shareUrl: data:post.shareUrl,                                                shareTitle: data:post.title,                                              }' name='sharingButtons'/>
    </b:with>
  </div>
</b:includable>
            <b:includable id='postTimestamp'>
  <span class='byline post-timestamp'>
    <data:byline.label/>
    <b:if cond='data:post.url'>
      <meta expr:content='data:post.url.canonical'/>
      <a class='timestamp-link' expr:href='data:post.url' rel='bookmark' title='permanent link'>
        <time class='published' expr:datetime='data:post.date.iso8601' expr:title='data:post.date.iso8601'>
          <data:post.date/>
        </time>
      </a>
    </b:if>
  </span>
</b:includable>
            <b:includable id='postTitle' var='post'>
  <a expr:name='data:post.id'/>
  <b:if cond='data:post.title != &quot;&quot;'>
    <h3 class='post-title entry-title'>
      <b:if cond='data:post.link or (data:post.url and data:view.url != data:post.url)'>
        <a expr:href='data:post.link ?: data:post.url'><data:post.title/></a>
      <b:else/>
        <data:post.title/>
      </b:if>
    </h3>
  </b:if>
</b:includable>
            <b:includable id='previousPageLink'>
  <a class='blog-pager-newer-link' expr:href='data:newerPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-newer-link&quot;' expr:title='data:messages.newerPosts'>
    <data:messages.newerPosts/>
  </a>
</b:includable>
            <b:includable id='sharingButton'>
  <span expr:aria-label='data:platform.shareMessage' expr:class='&quot;sharing-platform-button sharing-element-&quot; + data:platform.key' expr:data-href='data:shareUrl + &quot;&amp;target=&quot; + data:platform.target' expr:data-url='data:originalUrl' expr:title='data:platform.shareMessage' role='menuitem' tabindex='-1'>
    <b:include name='sharingPlatformIcon'/>
    <span class='platform-sharing-text'><data:platform.name/></span>
  </span>
</b:includable>
            <b:includable id='sharingButtonContent'>
  <div class='flat-icon-button ripple'>
    <b:include name='shareIcon'/>
  </div>
</b:includable>
            <b:includable id='sharingButtons'>
  <div class='sharing' expr:aria-owns='&quot;sharing-popup-&quot; + data:sharingId' expr:data-title='data:shareTitle'>
    <button class='sharing-button touch-icon-button' expr:aria-controls='&quot;sharing-popup-&quot; + data:sharingId' expr:aria-label='data:messages.share.escaped' expr:id='&quot;sharing-button-&quot; + data:sharingId' role='button'>
      <b:include name='sharingButtonContent'/>
    </button>
    <b:include name='sharingButtonsMenu'/>
  </div>
</b:includable>
            <b:includable id='sharingButtonsMenu'>
  <div class='share-buttons-container'>
    <ul aria-hidden='true' class='share-buttons hidden' expr:aria-label='data:messages.share.escaped' expr:id='&quot;sharing-popup-&quot; + data:sharingId' role='menu'>
      <b:loop values='(data:platforms ?: data:blog.sharing.platforms) filter (p =&gt; p.key not in {&quot;blogThis&quot;})' var='platform'>
        <li>
          <b:include name='sharingButton'/>
        </li>
      </b:loop>
      <li aria-hidden='true' class='hidden'>
        <b:include name='otherSharingButton'/>
      </li>
    </ul>
  </div>
</b:includable>
            <b:includable id='sharingPlatformIcon'>
  <b:include data='{ iconClass: (&quot;touch-icon sharing-&quot; + data:platform.key) }' expr:name='data:platform.key + &quot;Icon&quot;'/>
</b:includable>
            <b:includable id='threadedCommentForm' var='post'>
  <div class='comment-form'>
    <a name='comment-form'/>
    <h4 id='comment-post-message'><data:messages.postAComment/></h4>
    <b:if cond='data:this.messages.blogComment != &quot;&quot;'>
      <p><data:this.messages.blogComment/></p>
    </b:if>
    <b:include data='post' name='commentFormIframeSrc'/>
    <iframe allowtransparency='allowtransparency' class='blogger-iframe-colorize blogger-comment-from-post' expr:height='data:cmtIframeInitialHeight ?: &quot;90px&quot;' frameborder='0' id='comment-editor' name='comment-editor' src='' width='100%'/>
    <data:post.cmtfpIframe/>
    <script type='text/javascript'>
      BLOG_CMT_createIframe(&#39;<data:post.appRpcRelayPath/>&#39;);
    </script>
  </div>
</b:includable>
            <b:includable id='threadedCommentJs' var='post'>
  <script async='async' expr:src='data:post.commentSrc' type='text/javascript'/>
  <b:template-script inline='true' name='threaded_comments'/>
  <script type='text/javascript'>
    blogger.widgets.blog.initThreadedComments(
        <data:post.commentJso/>,
        <data:post.commentMsgs/>,
        <data:post.commentConfig/>);
  </script>
</b:includable>
            <b:includable id='threadedComments' var='post'>
  <section class='comments threaded' expr:data-embed='data:post.embedCommentForm' expr:data-num-comments='data:post.numberOfComments' id='comments'>
    <a name='comments'/>

    <b:include name='commentsTitle'/>

    <div class='comments-content'>
      <b:if cond='data:post.embedCommentForm'>
        <b:include data='post' name='threadedCommentJs'/>
      </b:if>
      <div id='comment-holder'>
         <data:post.commentHtml/>
      </div>
    </div>

    <p class='comment-footer'>
      <b:if cond='data:post.allowNewComments'>
        <b:include data='post' name='threadedCommentForm'/>
      <b:else/>
        <data:post.noNewCommentsText/>
      </b:if>
      <b:if cond='data:post.showManageComments'>
        <b:include data='post' name='manageComments'/>
      </b:if>
    </p>

    <b:if cond='data:showCmtPopup'>
      <div id='comment-popup'>
        <iframe allowtransparency='allowtransparency' frameborder='0' id='comment-actions' name='comment-actions' scrolling='no'>
        </iframe>
      </div>
    </b:if>
  </section>
</b:includable>
          </b:widget>
        </b:section> 
<b:if cond='data:view.isLayoutMode or data:view.isPost'>
              <b:section class='top-Ad-Slots' id='top-Ad-Slots' maxwidgets='1' name='Ads Appear Above the Article' showaddelement='no'>
                <b:widget id='HTML76' locked='true' title='Ad Code' type='HTML' visible='false'>
                  <b:widget-settings>
                    <b:widget-setting name='content'/>
                  </b:widget-settings>
                  <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
                </b:widget>
              </b:section>  
              <b:section class='Middle-Ad-Slot1' id='Middle-Ad-Slot1' maxwidgets='1' name='Ads Appear in the Middle of the Article' showaddelement='no'>
                  <b:widget id='HTML77' locked='true' title='Ad Code' type='HTML' visible='false'>
                    <b:widget-settings>
                      <b:widget-setting name='content'><![CDATA[<a href="https://www.blogger.com/" target='noopener'><img src="https://1.bp.blogspot.com/-7Q2ijJWHll0/XsOqo6RV8SI/AAAAAAAAAGo/PIrILeuAlkYbxDAHa60E_mo8UR0VofRMgCLcBGAsYHQ/s1600/bnr.png" alt="advertise"/></a>]]></b:widget-setting>
                    </b:widget-settings>
                    <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
                  </b:widget>
                </b:section>
              <b:section class='Middle-Ad-Slot2' id='Middle-Ad-Slot2' maxwidgets='1' name='Ads Appear in the Middle of the Article' showaddelement='no'>
                <b:widget id='HTML78' locked='true' title='Ad Code' type='HTML' visible='false'>
                  <b:widget-settings>
                    <b:widget-setting name='content'/>
                  </b:widget-settings>
                  <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
                </b:widget>
              </b:section>
              <b:section class='Ad-Slots-below' id='Ad-Slots-below' maxwidgets='1' name='Ads Appear Under the Article' showaddelement='no'>
                <b:widget id='HTML79' locked='true' title='Ad Code' type='HTML' visible='false'>
                  <b:widget-settings>
                    <b:widget-setting name='content'/>
                  </b:widget-settings>
                  <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
                </b:widget>
              </b:section>
<b:include name='adsjs'/>    
</b:if>       
<div class='related-posts-widget' id='related-posts-widget'>
  <div class='notex'/>
  <b:section class='relatedPost' id='related-post-set-desktop' maxwidgets='1' name='Related Post Setting (Desktop &amp; Tablet)' preferred='yes' showaddelement='no'>
    <b:widget id='HTML9' locked='false' title='Related Posts' type='HTML' visible='true'>
      <b:widget-settings>
        <b:widget-setting name='content'>widgetStyle:3,
numPosts:3,
summaryLength:101,</b:widget-setting>
      </b:widget-settings>
      <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
    </b:widget>
  </b:section>
  <b:section class='relatedPost' id='related-post-set-mobile' maxwidgets='1' mobile='yes' name='Related Post Setting (Mobile)' preferred='yes' showaddelement='no'>
    <b:widget id='HTML8' locked='false' title='Related Posts' type='HTML' visible='true'>
      <b:widget-settings>
        <b:widget-setting name='content'>widgetStyle:1,
numPosts:5,
summaryLength:60,</b:widget-setting>
      </b:widget-settings>
      <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
    </b:widget>
  </b:section>
    </div>
      </main>
      <!-- Sidebar Wrapper -->
      <aside class='sidebar-wrapper'>
        <b:section class='sidebar common-widget' id='sidebar' showaddelement='yes'>
          <b:widget id='HTML6' locked='false' title='All Settings (Pengaturan)' type='HTML' visible='false'>
            <b:widget-settings>
              <b:widget-setting name='content'><![CDATA[<img alt="advertise" src="https://1.bp.blogspot.com/-Sj7vpKOygV0/Xu-YjruJjvI/AAAAAAAAAL4/oTfSGJHNBZ4PRcY7wn4AdnMIIUdpq-3hwCLcBGAsYHQ/s1600/bnr2.jpg" title="advertise"/>]]></b:widget-setting>
            </b:widget-settings>
            <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
          </b:widget>
          <b:widget id='PopularPosts1' locked='false' title='Popular Post' type='PopularPosts' visible='true'>
            <b:widget-settings>
              <b:widget-setting name='numItemsToShow'>10</b:widget-setting>
              <b:widget-setting name='showThumbnails'>true</b:widget-setting>
              <b:widget-setting name='showSnippets'>true</b:widget-setting>
              <b:widget-setting name='timeRange'>LAST_YEAR</b:widget-setting>
            </b:widget-settings>
            <b:includable id='main' var='this'>
      <b:include name='widget-title'/>
      <div class='widget-content'>
        <b:loop values='data:posts' var='post'>
          <b:include data='post' name='postContent'/>
        </b:loop>
      </div>
    </b:includable>
            <b:includable id='blogThisShare'>
  <b:with value='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=270,width=475\&quot;); return false;&quot;' var='onclick'>
    <b:include name='platformShare'/>
  </b:with>
</b:includable>
            <b:includable id='bylineByName' var='byline'>
  <b:switch var='data:byline.name'>
  <b:case value='share'/>
    <b:include cond='data:post.shareUrl' name='postShareButtons'/>
  <b:case value='comments'/>
    <b:include cond='data:post.allowComments' name='postCommentsLink'/>
  <b:case value='location'/>
    <b:include cond='data:post.location' name='postLocation'/>
  <b:case value='timestamp'/>
    <b:include cond='not data:view.isPage' name='postTimestamp'/>
  <b:case value='author'/>
    <b:include name='postAuthor'/>
  <b:case value='labels'/>
    <b:include cond='data:post.labels' name='postLabels'/>
  <b:case value='icons'/>
    <b:include cond='data:post.emailPostUrl' name='emailPostIcon'/>
  </b:switch>
</b:includable>
            <b:includable id='bylineRegion' var='regionItems'>
  <b:loop values='data:regionItems' var='byline'>
    <b:include data='byline' name='bylineByName'/>
  </b:loop>
</b:includable>
            <b:includable id='commentsLink'>
  <a class='comment-link' expr:href='data:post.commentsUrl' expr:onclick='data:post.commentsUrlOnclick'>
    <b:if cond='data:post.numberOfComments &gt; 0'>
      <b:message name='messages.numberOfComments'>
        <b:param expr:value='data:post.numberOfComments' name='numComments'/>
      </b:message>
    <b:else/>
      <data:messages.postAComment/>
    </b:if>
  </a>
</b:includable>
            <b:includable id='commentsLinkIframe'>
  <!-- G+ comments, no longer available. The includable is retained for backwards-compatibility. -->
</b:includable>
            <b:includable id='emailPostIcon'>
  <span class='byline post-icons'>
    <!-- email post links -->
    <span class='item-action'>
      <a expr:href='data:post.emailPostUrl' expr:title='data:messages.emailPost'>
        <b:include data='{ iconClass: &quot;touch-icon sharing-icon&quot; }' name='emailIcon'/>
      </a>
    </span>
  </span>
</b:includable>
            <b:includable id='facebookShare'>
  <b:with value='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=430,width=640\&quot;); return false;&quot;' var='onclick'>
    <b:include name='platformShare'/>
  </b:with>
</b:includable>
            <b:includable id='footerBylines'>
  <b:if cond='data:widgets.Blog.first.footerBylines'>
    <b:loop index='i' values='data:widgets.Blog.first.footerBylines' var='region'>
      <b:if cond='not data:region.items.empty'>
        <div expr:class='&quot;post-footer-line post-footer-line-&quot; + (data:i + 1)'>
          <b:with value='&quot;footer-&quot; + (data:i + 1)' var='regionName'>
            <b:include data='region.items' name='bylineRegion'/>
          </b:with>
        </div>
      </b:if>
    </b:loop>
  </b:if>
</b:includable>
            <b:includable id='googlePlusShare'>
</b:includable>
            <b:includable id='headerByline'>
  <b:if cond='data:widgets.Blog.first.headerByline'>
    <div class='post-header'>
      <div class='post-header-line-1'>
        <b:with value='&quot;header-1&quot;' var='regionName'>
          <b:include data='data:widgets.Blog.first.headerByline.items' name='bylineRegion'/>
        </b:with>
      </div>
    </div>
  </b:if>
</b:includable>
            <b:includable id='linkShare'>
  <b:with value='&quot;window.prompt(\&quot;Copy to clipboard: Ctrl+C, Enter\&quot;, \&quot;&quot; + data:originalUrl + &quot;\&quot;); return false;&quot;' var='onclick'>
    <b:include name='platformShare'/>
  </b:with>
</b:includable>
            <b:includable id='otherSharingButton'>
  <span class='sharing-platform-button sharing-element-other' expr:aria-label='data:messages.shareToOtherApps.escaped' expr:data-url='data:originalUrl' expr:title='data:messages.shareToOtherApps.escaped' role='menuitem' tabindex='-1'>
    <b:with value='{key: &quot;sharingOther&quot;}' var='platform'>
      <b:include name='sharingPlatformIcon'/>
    </b:with>
    <span class='platform-sharing-text'><data:messages.shareOtherApps.escaped/></span>
  </span>
</b:includable>
            <b:includable id='platformShare'>
  <a expr:class='&quot;goog-inline-block sharing-&quot; + data:platform.key' expr:data-url='data:originalUrl' expr:href='data:shareUrl + &quot;&amp;target=&quot; + data:platform.target' expr:onclick='data:onclick ? data:onclick : &quot;&quot;' expr:title='data:platform.shareMessage' target='_blank'>
    <span class='share-button-link-text'>
      <data:platform.shareMessage/>
    </span>
  </a>
</b:includable>
            <b:includable id='postAuthor'>
  <span class='byline post-author vcard'>
    <span class='post-author-label'>
      <data:byline.label/>
    </span>
    <span class='fn'>
      <b:if cond='data:post.author.profileUrl'>
        <meta expr:content='data:post.author.profileUrl'/>
        <a class='g-profile' expr:href='data:post.author.profileUrl' rel='author' title='author profile'>
          <span><data:post.author.name/></span>
        </a>
      <b:else/>
        <span><data:post.author.name/></span>
      </b:if>
    </span>
  </span>
</b:includable>
            <b:includable id='postCommentsLink'>
  <span class='byline post-comment-link container'>
    <b:include cond='data:post.commentSource != 1' name='commentsLink'/>
  </span>
</b:includable>
            <b:includable id='postContent' var='post'>
      <div class='post'>
        <div class='post-content'>
          <a class='post-image-link' expr:href='data:post.url'>
            <b:if cond='data:post.featuredImage'>
              <img class='sizeimg' expr:alt='data:post.title' expr:src='data:post.featuredImage resizeImage 680' expr:title='data:post.title'/>
              <b:else/>
              <img class='sizeimg' expr:alt='data:post.title' expr:title='data:post.title' src='https://4.bp.blogspot.com/-SKh7CYM3lB0/WZlRLgH8wII/AAAAAAAACjQ/vx5PJdQYhSo136-Wg-A633KcElrfkHNNACLcBGAs/s1600/non.png'/>
            </b:if>
          </a>
          <div class='post-info'>
            <h2 class='post-title'>
              <a expr:href='data:post.url'><data:post.title/></a>
            </h2>
            <div class='post-meta'>
              <span class='post-date published' expr:datetime='data:post.date.iso8601'><data:post.date/></span>
            </div>
          </div>
        </div>
      </div>
    </b:includable>
            <b:includable id='postJumpLink' var='post'>
  <div class='jump-link flat-button'>
    <a expr:href='data:post.url fragment &quot;more&quot;' expr:title='data:post.title'>
      <b:eval expr='data:blog.jumpLinkMessage'/>
    </a>
  </div>
</b:includable>
            <b:includable id='postLabels'>
  <span class='byline post-labels'>
    <span class='byline-label'><data:byline.label/></span>
    <b:loop index='i' values='data:post.labels' var='label'>
      <a expr:href='data:label.url' rel='tag'>
        <data:label.name/>
      </a>
    </b:loop>
  </span>
</b:includable>
            <b:includable id='postLocation'>
  <span class='byline post-location'>
    <data:byline.label/>
    <a expr:href='data:post.location.mapsUrl' target='_blank'><data:post.location.name/></a>
  </span>
</b:includable>
            <b:includable id='postReactions'>
  <!-- Reaction feature no longer available. The includable is retained for backwards-compatibility. -->
</b:includable>
            <b:includable id='postShareButtons'>
  <div class='byline post-share-buttons goog-inline-block'>
    <b:with value='data:sharingId ?: ((data:widget.instanceId ?: &quot;sharing&quot;) + &quot;-&quot; + (data:regionName ?: &quot;byline&quot;) + &quot;-&quot; + data:post.id)' var='sharingId'>
      <!-- Note: 'sharingButtons' includable is from the default Sharing widget markup. -->
      <b:include data='{                                                sharingId: data:sharingId,                                                originalUrl: data:post.url,                                                platforms: data:this.sharing.platforms,                                                shareUrl: data:post.shareUrl,                                                shareTitle: data:post.title,                                              }' name='sharingButtons'/>
    </b:with>
  </div>
</b:includable>
            <b:includable id='postTimestamp'>
  <span class='byline post-timestamp'>
    <data:byline.label/>
    <b:if cond='data:post.url'>
      <meta expr:content='data:post.url.canonical'/>
      <a class='timestamp-link' expr:href='data:post.url' rel='bookmark' title='permanent link'>
        <time class='published' expr:datetime='data:post.date.iso8601' expr:title='data:post.date.iso8601'>
          <data:post.date/>
        </time>
      </a>
    </b:if>
  </span>
</b:includable>
            <b:includable id='sharingButton'>
  <span expr:aria-label='data:platform.shareMessage' expr:class='&quot;sharing-platform-button sharing-element-&quot; + data:platform.key' expr:data-href='data:shareUrl + &quot;&amp;target=&quot; + data:platform.target' expr:data-url='data:originalUrl' expr:title='data:platform.shareMessage' role='menuitem' tabindex='-1'>
    <b:include name='sharingPlatformIcon'/>
    <span class='platform-sharing-text'><data:platform.name/></span>
  </span>
</b:includable>
            <b:includable id='sharingButtonContent'>
  <div class='flat-icon-button ripple'>
    <b:include name='shareIcon'/>
  </div>
</b:includable>
            <b:includable id='sharingButtons'>
  <div class='sharing' expr:aria-owns='&quot;sharing-popup-&quot; + data:sharingId' expr:data-title='data:shareTitle'>
    <button class='sharing-button touch-icon-button' expr:aria-controls='&quot;sharing-popup-&quot; + data:sharingId' expr:aria-label='data:messages.share.escaped' expr:id='&quot;sharing-button-&quot; + data:sharingId' role='button'>
      <b:include name='sharingButtonContent'/>
    </button>
    <b:include name='sharingButtonsMenu'/>
  </div>
</b:includable>
            <b:includable id='sharingButtonsMenu'>
  <div class='share-buttons-container'>
    <ul aria-hidden='true' class='share-buttons hidden' expr:aria-label='data:messages.share.escaped' expr:id='&quot;sharing-popup-&quot; + data:sharingId' role='menu'>
      <b:loop values='(data:platforms ?: data:blog.sharing.platforms) filter (p =&gt; p.key not in {&quot;blogThis&quot;})' var='platform'>
        <li>
          <b:include name='sharingButton'/>
        </li>
      </b:loop>
      <li aria-hidden='true' class='hidden'>
        <b:include name='otherSharingButton'/>
      </li>
    </ul>
  </div>
</b:includable>
            <b:includable id='sharingPlatformIcon'>
  <b:include data='{ iconClass: (&quot;touch-icon sharing-&quot; + data:platform.key) }' expr:name='data:platform.key + &quot;Icon&quot;'/>
</b:includable>
            <b:includable id='snippetedPostByline'>
  <b:with value='(data:widgets first (w =&gt; w.type == &quot;Blog&quot;)).allBylineItems' var='blogBylines'>
    <div class='item-byline'>
      <b:with value='data:blogBylines first (i =&gt; i.name == &quot;author&quot;)' var='byline'>
        <b:include cond='data:byline and data:this.postDisplay.showAuthor' data='post' name='postAuthor'/>
      </b:with>
      <b:with value='data:blogBylines first (i =&gt; i.name == &quot;timestamp&quot;)' var='byline'>
        <b:include cond='data:byline and data:this.postDisplay.showDate' data='post' name='postTimestamp'/>
      </b:with>
    </div>
  </b:with>
</b:includable>
            <b:includable id='snippetedPostContent'>
  <div class='post-content'>
    <b:include cond='data:this.postDisplay.showTitle' name='snippetedPostTitle'/>
    <b:include cond='data:this.postDisplay.showDate or data:this.postDisplay.showAuthor' name='snippetedPostByline'/>
    <b:include cond='data:this.postDisplay.showSnippet' data='post' name='postSnippet'/>
    <b:include cond='data:this.postDisplay.showFeaturedImage and data:post.featuredImage' name='snippetedPostThumbnail'/>
  </div>
</b:includable>
            <b:includable id='snippetedPostThumbnail'>
  <div class='item-thumbnail'>
    <a expr:href='data:post.url'>
      <b:include data='{                         image: data:post.featuredImage,                         imageSizes: [72, 144],                         imageRatio: &quot;1:1&quot;,                         sourceSizes: &quot;72px&quot;                        }' name='responsiveImage'/>
    </a>
  </div>
</b:includable>
            <b:includable id='snippetedPostTitle'>
  <b:if cond='data:post.title != &quot;&quot;'>
    <h3 class='post-title'><a expr:href='data:post.url'><data:post.title/></a></h3>
  </b:if>
</b:includable>
            <b:includable id='snippetedPosts'>
  <div role='feed'>
    <!-- Don't render the post that we're currently already looking at. -->
    <b:loop values='data:posts filter (p =&gt; p.id != data:view.postId)' var='post'>
      <article class='post' role='article'>
        <b:include name='snippetedPostContent'/>
      </article>
    </b:loop>
  </div>
</b:includable>
          </b:widget>
        </b:section>
        </aside>
      </div>
  </div>
<div class='clr'/>
</div>

<b:if cond='data:view.isHomepage'>
<div class='boxwrap'>
<div id='outer-wrapper'>
<div class='boxwrap-left font-small'>
<b:section class='boxwrap-text' id='boxwrap3' maxwidgets='1' showaddelement='yes'/>
</div>
<div class='boxwrap-right'>
<b:section class='boxwrap-text font-big' id='boxwrap4' maxwidgets='1' showaddelement='yes'/>
</div>
</div>
</div>
<div class='clr'/>
<div class='boxpixal'>
<div id='outer-wrapper'>
<b:section class='boxwrap-text center-text' id='boxwrap5' maxwidgets='1' showaddelement='yes'/>
</div>
</div>
  
<div class='clr'/>
<div class='testi-wrap'>
<div id='outer-wrapper'>
<b:section class='boxwrap-text center-text' id='Testimonios' maxwidgets='1' showaddelement='yes'>
  <b:widget id='HTML16' locked='false' title='TESTIMONIOS' type='HTML' visible='true'>
    <b:widget-settings>
      <b:widget-setting name='content'><![CDATA[<h2>Clientes Sastifechos</h2>
<div class='boxtestimonial'>
<div class='ithemonial'>
<div class='ithemonialicon'></div>
<p>Recomendamos encarecidamente  a cualquier empresa que quiera mejorar su presencia en línea.</p>
<div class='monialimg'>
<img alt='Education Career' src='https://1.bp.blogspot.com/-UEVKyM5bzmY/XuySBpuAAVI/AAAAAAAAAJw/Gy6nDQz3qTIgxHbH2H5Nq6uIlPLz0kBfQCLcBGAsYHQ/s1600/mo1.jpg'/>
<h4>Jhon Wick, <span>Cliente</span></h4>
</div>
</div>
<div class='ithemonial'>
<div class='ithemonialicon'></div>
<p>El equipo de es muy profesional y está siempre atento a nuestras necesidades. Nos ofrecen un servicio personalizado y adaptado a nuestro negocio&#39;t look even slightly believable.</p>
<div class='monialimg'>
<img alt='Education Career' src='https://1.bp.blogspot.com/-lNyH8k7Lntc/XuySBwOnvNI/AAAAAAAAAJ0/9X0ojZeQJAMvWoj-obWaunU6T3z_KPGFACLcBGAsYHQ/s1600/mo2.jpg'/>
<h4>Kaptain Amerika, <span>Cliente</span></h4>
</div>
</div>
<div class='ithemonial'>
<div class='ithemonialicon'></div>
<p>Trabajamos desde hace dos años y estamos muy satisfechos con los resultados que hemos obtenido. Han ayudado a aumentar nuestra visibilidad en línea, mejorar el tráfico a nuestro sitio web y aumentar las conversiones.</p>
<div class='monialimg'>
<img alt='Education Career' src='https://1.bp.blogspot.com/-YeNgY4KiWYQ/XuySBv203rI/AAAAAAAAAJs/9KuOWuXD7JIEmFdWGKkF6DVmjDbCYQO7wCLcBGAsYHQ/s1600/mo3.jpg'/>
<h4>Mark Warren, <span>Cliente</span></h4>
</div>
</div>
</div>]]></b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
  </b:widget>
</b:section>
<div class='clr'/>
<script src='https://raw.githack.com/ililio/i/main/i.js' type='text/javascript'/>
<div class='boxwrap-text center-text'>
<h3>Siguenos</h3>
<h2>Suscríbete al boletín</h2>
</div>
<div class='subs-wrapper'>
<b:section class='subs' id='Subscribe' maxwidgets='1' showaddelement='yes'/>
</div>
<div class='clr'/>
<div class='parnert-wrapper'>
<div id='outer-wrapper'>
<div class='boxwrap-text center-text'>
<h2>Aliados Estratégicos</h2>
</div>
  
<b:section class='parnert' id='Slider Parnert' maxwidgets='1' showaddelement='yes'>
  <b:widget id='HTML5' locked='false' title='Slider Parnert' type='HTML' visible='false'>
    <b:widget-settings>
      <b:widget-setting name='content'><![CDATA[<div class='customer-parnert'>
<div class='brand-box'>
<img alt='' src='https://1.bp.blogspot.com/-drjx77NQDD0/XuyNfsahL5I/AAAAAAAAAII/0OAS7hIx6KU_3aYq5tEuDJn3WQuA0zDGwCLcBGAsYHQ/s1600/a1.png' title=''/>
</div>
<div class='brand-box'>
<img alt='' src='https://1.bp.blogspot.com/-o7V1EdTrsMw/XuyNfuj25AI/AAAAAAAAAIE/x-nr4FIAm8wqTi2O_CPuHBVWCFWOVmJYACLcBGAsYHQ/s1600/a2.png' title=''/>
</div>
<div class='brand-box'>
<img alt='' src='https://1.bp.blogspot.com/-FRwbzLeXjh0/XuyNfpnHq9I/AAAAAAAAAIA/BdRk5iRZ76wiTJ35HKFw0V_8TTY1jTL-wCLcBGAsYHQ/s1600/a3.png' title=''/>
</div>
<div class='brand-box'>
<img alt='' src='https://1.bp.blogspot.com/-AN9ph7hPSbo/XuyNgUZ7w1I/AAAAAAAAAIM/J6iM7rIGQsYLO9IID7OOGHF_Icq1ACDiwCLcBGAsYHQ/s1600/a4.png' title=''/>
</div>
<div class='brand-box'>
<img alt='' src='https://1.bp.blogspot.com/-NQG8__SPqPk/XuyNg6QRmuI/AAAAAAAAAIQ/n2-txftKX40t_tJsFdFnxAJ1Q0BXiIo6gCLcBGAsYHQ/s1600/a5.png' title=''/>
</div>
<div class='brand-box'>
<img alt='' src='https://1.bp.blogspot.com/-FKZRq85m8lg/XuyNhOvmErI/AAAAAAAAAIU/1QQ5LjlNP3wAgvJhWQWZ09u74FKwOriFwCLcBGAsYHQ/s1600/a6.png' title=''/>
</div>
</div>]]></b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
  </b:widget>
</b:section>
</div>
</div>
</div>
</div>
</b:if>



<footer id='footer-wrapper'>
<div class='lay'>
<div id='outer-wrapper'>
<b:section class='boxwrap-text' id='boxwrap7' maxwidgets='1' showaddelement='yes'>
  <b:widget id='HTML18' locked='false' title='' type='HTML' visible='true'>
    <b:widget-settings>
      <b:widget-setting name='content'><![CDATA[<div class='map-wrapper'>
<div class='map-wrapper-left'>
<div class='mplogo'>
<a href='/'><img alt='' src='https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi-8zJWbzihkNTt_NBeMFxsv5wlMxSJtKnCqjUw0LBjN5b7ntS81gthyphenhyphen9aHl08Ja2Ca3mIpoTpdli3gH4okUj-eZi8H0_xxqYr8JAvfsNx4KjYrh0qyBqmOxisNk_6QySNa7K0WJz_ZD6ttcoKafluuzQCd2ggTEJAUo6Qa0WBWuBvHaZyllGVvH7UeJy4/s310/820-22.png' title='Mr Renta'/></a>
</div>
</div>
<div class='map-wrapper-right'>
<div class='elementor-map'>
<div class='icon-box'>
<i class='far fa-map-marker-alt'></i>
<div class='icon-box__text'>
<span class='icon-box__title'>Dirección</span>
<span class='icon-box__subtitle'>Valledupar - Cesar, Colombia</span>
</div>
</div>
<div class='icon-box'>
<i class='fal fa-envelope'></i>
<div class='icon-box__text'>
<span class='icon-box__title'>E-Mail</span>
<span class='icon-box__subtitle'>Aún no disponible</span>
</div>
</div>
<div class='icon-box'>


</div>
</div>
</div>
</div>]]></b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
  </b:widget>
</b:section>
  
  
  
  

<div class='footer-box'>
<b:section class='footer' id='footer1' showaddelement='yes'>
  <b:widget id='HTML1' locked='false' title='Nosotros' type='HTML' visible='true'>
    <b:widget-settings>
      <b:widget-setting name='content'><![CDATA[A mis 30 años, me considero amigable, social, serio cuando se requiere y siempre con una sonrisa lista para alegrar el día.
<ul class="iconfit">
<li><a href="https://www.facebook.com/OzzFlorezMendoza/" target="_blank" title="Facebook Ozz"><i class="fab fa-facebook-f"></i></a></li>
<li><a href="https://twitter.com/Ozznyder" target="_blank" title="Twitter Ozz"><i class="fab fa-twitter"></i></a></li>
<li><a href="https://www.instagram.com/osny.der/" target="_blank" title="Instagram Ozz"><i class="fab fa-instagram"></i></a></li>
<li><a href="https://www.youtube.com/@osnyder/" target="_blank" title="Youtube Ozz"><i class="fab fa-youtube"></i></a></li>
</ul>]]></b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
  </b:widget>
</b:section>
<b:section class='footer' id='footer2' showaddelement='yes'>
  <b:widget id='HTML2' locked='false' title='Servicios' type='HTML' visible='true'>
    <b:widget-settings>
      <b:widget-setting name='content'><![CDATA[<ul>
<li><a href="#">Marketing Digital</a></li>
<li><a href="#">SEO Posicionamiento Web</a></li>
<li><a href="#">Email Marketing</a></li>
<li><a href="#">Social Media &amp; Planning</a></li>
<li><a href="#">Desarrollo Web</a></li>
</ul>]]></b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
  </b:widget>
</b:section>
<b:section class='footer' id='footer3' showaddelement='yes'>
  <b:widget id='HTML3' locked='false' title='Cursos' type='HTML' visible='true'>
    <b:widget-settings>
      <b:widget-setting name='content'><![CDATA[<ul>
<li><a href="#">Marketing Digital</a></li>
<li><a href="#">Google Analytics</a></li>
<li><a href="#">Facebook e Instagram Ads</a></li>
<li><a href="#">SEO Posicionamiento Web</a></li>
<li><a href="#">Marketing de contenidos</a></li>
</ul>]]></b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
  </b:widget>
</b:section>
<b:section class='footer' id='footer4' showaddelement='yes'>
  <b:widget id='HTML7' locked='false' title='Enlaces rápidos' type='HTML' visible='true'>
    <b:widget-settings>
      <b:widget-setting name='content'><![CDATA[<ul>
<li><a href="#">Google Search Console</a></li>
<li><a href="#">Google Analitycs</a></li>
<li><a href="#">Google Maps</a></li>
<li><a href="#">Test de velocidad&amp; Planning</a></li>
<li><a href="#">Generador de Sitemap</a></li>
</ul>]]></b:widget-setting>
    </b:widget-settings>
    <b:includable id='main'>
  <b:include name='widget-title'/>
  <div class='widget-content'>
    <data:content/>
  </div>
</b:includable>
  </b:widget>
</b:section>
</div>
<b:include name='creditall'/>
</div>
</div>
</footer>
 <b:include name='backtop'/>
 <b:include name='jsall'/>
</body>
</html>
