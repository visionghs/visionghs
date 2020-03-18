<!--DOCTYPE html-->
<!--<html lang="en" dir="ltr" prefix="content: http://purl.org/rss/1.0/modules/content/  dc: http://purl.org/dc/terms/  foaf: http://xmlns.com/foaf/0.1/  og: http://ogp.me/ns#  rdfs: http://www.w3.org/2000/01/rdf-schema#  schema: http://schema.org/  sioc: http://rdfs.org/sioc/ns#  sioct: http://rdfs.org/sioc/types#  skos: http://www.w3.org/2004/02/skos/core#  xsd: http://www.w3.org/2001/XMLSchema# ">
 -->
 <head>
    <meta charset="utf-8" /><script type="text/javascript">(window.NREUM||(NREUM={})).loader_config={licenseKey:"006b5744c1",applicationID:"115598855"};window.NREUM||(NREUM={}),__nr_require=function(e,n,t){function r(t){if(!n[t]){var i=n[t]={exports:{}};e[t][0].call(i.exports,function(n){var i=e[t][1][n];return r(i||n)},i,i.exports)}return n[t].exports}if("function"==typeof __nr_require)return __nr_require;for(var i=0;i<t.length;i++)r(t[i]);return r}({1:[function(e,n,t){function r(){}function i(e,n,t){return function(){return o(e,[u.now()].concat(f(arguments)),n?null:this,t),n?void 0:this}}var o=e("handle"),a=e(4),f=e(5),c=e("ee").get("tracer"),u=e("loader"),s=NREUM;"undefined"==typeof window.newrelic&&(newrelic=s);var p=["setPageViewName","setCustomAttribute","setErrorHandler","finished","addToTrace","inlineHit","addRelease"],l="api-",d=l+"ixn-";a(p,function(e,n){s[n]=i(l+n,!0,"api")}),s.addPageAction=i(l+"addPageAction",!0),s.setCurrentRouteName=i(l+"routeName",!0),n.exports=newrelic,s.interaction=function(){return(new r).get()};var m=r.prototype={createTracer:function(e,n){var t={},r=this,i="function"==typeof n;return o(d+"tracer",[u.now(),e,t],r),function(){if(c.emit((i?"":"no-")+"fn-start",[u.now(),r,i],t),i)try{return n.apply(this,arguments)}catch(e){throw c.emit("fn-err",[arguments,this,e],t),e}finally{c.emit("fn-end",[u.now()],t)}}}};a("actionText,setName,setAttribute,save,ignore,onEnd,getContext,end,get".split(","),function(e,n){m[n]=i(d+n)}),newrelic.noticeError=function(e,n){"string"==typeof e&&(e=new Error(e)),o("err",[e,u.now(),!1,n])}},{}],2:[function(e,n,t){function r(e,n){var t=e.getEntries();t.forEach(function(e){"first-paint"===e.name?c("timing",["fp",Math.floor(e.startTime)]):"first-contentful-paint"===e.name&&c("timing",["fcp",Math.floor(e.startTime)])})}function i(e,n){var t=e.getEntries();t.length>0&&c("lcp",[t[t.length-1]])}function o(e){if(e instanceof s&&!l){var n,t=Math.round(e.timeStamp);n=t>1e12?Date.now()-t:u.now()-t,l=!0,c("timing",["fi",t,{type:e.type,fid:n}])}}if(!("init"in NREUM&&"page_view_timing"in NREUM.init&&"enabled"in NREUM.init.page_view_timing&&NREUM.init.page_view_timing.enabled===!1)){var a,f,c=e("handle"),u=e("loader"),s=NREUM.o.EV;if("PerformanceObserver"in window&&"function"==typeof window.PerformanceObserver){a=new PerformanceObserver(r),f=new PerformanceObserver(i);try{a.observe({entryTypes:["paint"]}),f.observe({entryTypes:["largest-contentful-paint"]})}catch(p){}}if("addEventListener"in document){var l=!1,d=["click","keydown","mousedown","pointerdown","touchstart"];d.forEach(function(e){document.addEventListener(e,o,!1)})}}},{}],3:[function(e,n,t){function r(e,n){if(!i)return!1;if(e!==i)return!1;if(!n)return!0;if(!o)return!1;for(var t=o.split("."),r=n.split("."),a=0;a<r.length;a++)if(r[a]!==t[a])return!1;return!0}var i=null,o=null,a=/Version\/(\S+)\s+Safari/;if(navigator.userAgent){var f=navigator.userAgent,c=f.match(a);c&&f.indexOf("Chrome")===-1&&f.indexOf("Chromium")===-1&&(i="Safari",o=c[1])}n.exports={agent:i,version:o,match:r}},{}],4:[function(e,n,t){function r(e,n){var t=[],r="",o=0;for(r in e)i.call(e,r)&&(t[o]=n(r,e[r]),o+=1);return t}var i=Object.prototype.hasOwnProperty;n.exports=r},{}],5:[function(e,n,t){function r(e,n,t){n||(n=0),"undefined"==typeof t&&(t=e?e.length:0);for(var r=-1,i=t-n||0,o=Array(i<0?0:i);++r<i;)o[r]=e[n+r];return o}n.exports=r},{}],6:[function(e,n,t){n.exports={exists:"undefined"!=typeof window.performance&&window.performance.timing&&"undefined"!=typeof window.performance.timing.navigationStart}},{}],ee:[function(e,n,t){function r(){}function i(e){function n(e){return e&&e instanceof r?e:e?c(e,f,o):o()}function t(t,r,i,o){if(!l.aborted||o){e&&e(t,r,i);for(var a=n(i),f=v(t),c=f.length,u=0;u<c;u++)f[u].apply(a,r);var p=s[y[t]];return p&&p.push([b,t,r,a]),a}}function d(e,n){h[e]=v(e).concat(n)}function m(e,n){var t=h[e];if(t)for(var r=0;r<t.length;r++)t[r]===n&&t.splice(r,1)}function v(e){return h[e]||[]}function g(e){return p[e]=p[e]||i(t)}function w(e,n){u(e,function(e,t){n=n||"feature",y[t]=n,n in s||(s[n]=[])})}var h={},y={},b={on:d,addEventListener:d,removeEventListener:m,emit:t,get:g,listeners:v,context:n,buffer:w,abort:a,aborted:!1};return b}function o(){return new r}function a(){(s.api||s.feature)&&(l.aborted=!0,s=l.backlog={})}var f="nr@context",c=e("gos"),u=e(4),s={},p={},l=n.exports=i();l.backlog=s},{}],gos:[function(e,n,t){function r(e,n,t){if(i.call(e,n))return e[n];var r=t();if(Object.defineProperty&&Object.keys)try{return Object.defineProperty(e,n,{value:r,writable:!0,enumerable:!1}),r}catch(o){}return e[n]=r,r}var i=Object.prototype.hasOwnProperty;n.exports=r},{}],handle:[function(e,n,t){function r(e,n,t,r){i.buffer([e],r),i.emit(e,n,t)}var i=e("ee").get("handle");n.exports=r,r.ee=i},{}],id:[function(e,n,t){function r(e){var n=typeof e;return!e||"object"!==n&&"function"!==n?-1:e===window?0:a(e,o,function(){return i++})}var i=1,o="nr@id",a=e("gos");n.exports=r},{}],loader:[function(e,n,t){function r(){if(!x++){var e=E.info=NREUM.info,n=d.getElementsByTagName("script")[0];if(setTimeout(s.abort,3e4),!(e&&e.licenseKey&&e.applicationID&&n))return s.abort();u(y,function(n,t){e[n]||(e[n]=t)}),c("mark",["onload",a()+E.offset],null,"api");var t=d.createElement("script");t.src="https://"+e.agent,n.parentNode.insertBefore(t,n)}}function i(){"complete"===d.readyState&&o()}function o(){c("mark",["domContent",a()+E.offset],null,"api")}function a(){return O.exists&&performance.now?Math.round(performance.now()):(f=Math.max((new Date).getTime(),f))-E.offset}var f=(new Date).getTime(),c=e("handle"),u=e(4),s=e("ee"),p=e(3),l=window,d=l.document,m="addEventListener",v="attachEvent",g=l.XMLHttpRequest,w=g&&g.prototype;NREUM.o={ST:setTimeout,SI:l.setImmediate,CT:clearTimeout,XHR:g,REQ:l.Request,EV:l.Event,PR:l.Promise,MO:l.MutationObserver};var h=""+location,y={beacon:"bam.nr-data.net",errorBeacon:"bam.nr-data.net",agent:"js-agent.newrelic.com/nr-1167.min.js"},b=g&&w&&w[m]&&!/CriOS/.test(navigator.userAgent),E=n.exports={offset:f,now:a,origin:h,features:{},xhrWrappable:b,userAgent:p};e(1),e(2),d[m]?(d[m]("DOMContentLoaded",o,!1),l[m]("load",r,!1)):(d[v]("onreadystatechange",i),l[v]("onload",r)),c("mark",["firstbyte",f],null,"api");var x=0,O=e(6)},{}],"wrap-function":[function(e,n,t){function r(e){return!(e&&e instanceof Function&&e.apply&&!e[a])}var i=e("ee"),o=e(5),a="nr@original",f=Object.prototype.hasOwnProperty,c=!1;n.exports=function(e,n){function t(e,n,t,i){function nrWrapper(){var r,a,f,c;try{a=this,r=o(arguments),f="function"==typeof t?t(r,a):t||{}}catch(u){l([u,"",[r,a,i],f])}s(n+"start",[r,a,i],f);try{return c=e.apply(a,r)}catch(p){throw s(n+"err",[r,a,p],f),p}finally{s(n+"end",[r,a,c],f)}}return r(e)?e:(n||(n=""),nrWrapper[a]=e,p(e,nrWrapper),nrWrapper)}function u(e,n,i,o){i||(i="");var a,f,c,u="-"===i.charAt(0);for(c=0;c<n.length;c++)f=n[c],a=e[f],r(a)||(e[f]=t(a,u?f+i:i,o,f))}function s(t,r,i){if(!c||n){var o=c;c=!0;try{e.emit(t,r,i,n)}catch(a){l([a,t,r,i])}c=o}}function p(e,n){if(Object.defineProperty&&Object.keys)try{var t=Object.keys(e);return t.forEach(function(t){Object.defineProperty(n,t,{get:function(){return e[t]},set:function(n){return e[t]=n,n}})}),n}catch(r){l([r])}for(var i in e)f.call(e,i)&&(n[i]=e[i]);return n}function l(n){try{e.emit("internal-error",n)}catch(t){}}return e||(e=i),t.inPlace=u,t.flag=a,t}},{}]},{},["loader"]);</script>
<link rel="shortlink" href="https://visionghs.github.io//" />
<link rel="canonical" href="https://visionghs.github.io//" />
<meta name="Generator" content="Drupal 8 (https://www.drupal.org)" />
<meta name="MobileOptimized" content="width" />
<meta name="HandheldFriendly" content="true" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<link rel="shortcut icon" href="https://visionghs.github.io//favicon.png" type="image/png" />
<link rel="alternate" hreflang="en" href="https://visionghs.github.io//" />
<link rel="alternate" hreflang="fr" href="https://visionghs.github.io//" />
<link rel="alternate" hreflang="es" href="https://visionghs.github.io//" />
<link rel="revision" href="https://visionghs.github.io//" />
<script src="https://visionghs.github.io//google_tag/drupal_gtm_container/google_tag.script.js?q71t5h" defer></script>

  
 <title>Vision | Global Health Leadership</title>
<link rel="stylesheet" media="all" href="https://visionghs.github.io//css/styleset1.css">
<link rel="stylesheet" media="all" href="https://visionghs.github.io//css/styleset2.css">
<link rel="stylesheet" media="all" href="//fonts.googleapis.com/css?family=Lato:400,700,900" />

    
<!--[if lte IE 8]>
<script src="https://visionghs.github.io//js/js_VtafjXmRvoUgAzqzYTA3Wrjkx9wcWhjP0G4ZnnqRamA.js"></script>
<![endif]-->

  </head>
  <body class="page--front">
        <a href="#main-content" class="visually-hidden focusable">
      Skip to main content
    </a>
   <!-- <noscript aria-hidden="true"><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-WCWLCJ8" height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript> -->
      <div class="dialog-off-canvas-main-canvas" data-off-canvas-main-canvas>
    
  <div class="region region-alert">
    <div class="views-element-container block block-views block-views-blockalert-block-1 block--views-block-alert-block-1" id="block-views-block-alert-block-1">
  
    
      <div><div class="js-view-dom-id-a74d360a73b24ddb8b44f269cc58bc6e49deffe4b98bb6b82ea64fc72a19d140 views-view--alert views-view--alert--">
  
  
  

  
  
  

      <div class="views-row">


<input  type="checkbox" checked="checked" id="visionghs-alert-1-26-toggle" class="visionghs-alert--toggle hidden">
<label  class="visionghs-alert" id="visionghs-alert-1-26" for="visionghs-alert-1-26-toggle">
  <span class="content">
          <a href="https://www.cdc.gov/coronavirus/2019-ncov/index.html" class="field--name-message">The 2020 conference has gone virtual due to the Coronavirus. Check out CDC for information</a>
        <div class="close">✕</div>
  </span>
</label>
</div>


  
  

  
  

  
  
</div>
</div>

  </div>

  </div>


  <div class="region region-topnav">
    <div class="container">
      <div id="block-sitebranding" class="block block-system block-system-branding-block block--sitebranding">
  
    
              <a class="topnav__logo" href="/" title="Home" rel="home">
        <img src="https://visionghs.github.io//images/logo.png" alt="Home"/>
      </a>
          
</div>
      <div class="show-menu" aria-label="Show Menu" aria-controls="menu-level-0"></div>
  <nav role="navigation" aria-labelledby="block-mainnavigation-menu" id="block-mainnavigation" class="block block-menu navigation menu--main region-topnav__menu--main">
                      
    <h2 class="visually-hidden" id="block-mainnavigation-menu">Main navigation</h2>
    

              
<ul class="menu menu-level-0">
  
  <li class="menu-item menu-item--expanded menu-item--our-work">
    <div class="menu_link_title"><a href="https://visionghs.github.io//About" class="our-work" data-drupal-link-system-path="node/72681">About Us</a></div>
              
    
  <div class="menu_link_content menu-link-contentmain view-mode-default menu-dropdown menu-dropdown-0 menu-type-default">
              
    <ul class="menu menu-level-1">
      
    <li class="menu-item">
      <a href="https://visionghs.github.io//About/Vision" class="impact">Our Vision & Values</a>
                        <img src="https://visionghs.github.io//images/menu1.jpg" alt="A girl smiles in Ghana" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="https://visionghs.github.io//About/History" data-drupal-link-system-path="group/641">History</a>
                        <img src="https://visionghs.github.io//images/menu2.jpg" alt="A Cambodian girl smiles" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="https://visionghs.github.io//About/Conference" class="dis-man" data-drupal-link-system-path="group/606">Conference</a>
                        <img src="https://visionghs.github.io//images/menu3.jpg" alt="woman standing outside " typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="https://visionghs.github.io//About/Partners" class="econ-dev" data-drupal-link-system-path="group/651">Partners</a>
                        <img src="https://visionghs.github.io//images/menu4.jpg" alt="Young boy" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="https://visionghs.github.io//About/Mentoring" data-drupal-link-system-path="group/586">Mentoring</a>
                        <img src="https://visionghs.github.io//images/menu5.jpg" alt="A young girl writes on a chalkboard" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="https://visionghs.github.io//About/Projects">Projects</a>
                        <img src="https://visionghs.github.io//images/menu6.jpg" alt="A pastor and child in a church" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="https://visionghs.github.io//About/CaseStudies" data-drupal-link-system-path="group/646">Case Studies</a>
                        <img src="https://visionghs.github.io//images/menu7.jpg" alt="A Healthy Baby" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="https://visionghs.github.io//About/Team" data-drupal-link-system-path="group/576">Our Team</a>
                        <img src="https://visionghs.github.io//images/menu8.jpg" alt="A Colombian boy has clean water" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="https://visionghs.github.io//About" class="show-more">View All</a>
                      

          </li>
    </ul>



      </div>



      </li>
  
  <li class="menu-item menu-item--expanded menu-item--where-we-work">
    <div class="menu_link_title"><a href="https://visionghs.github.io//GHLC" class="where-work" data-drupal-link-system-path="node/72811">Conferences</a></div>
              
    
  <div class="menu_link_content menu-link-contentmain view-mode-default menu-dropdown menu-dropdown-0 menu-type-default">
              
    <ul class="menu menu-level-1">
      
    <li class="menu-item">
      <a href="https://visionghs.github.io//GHLC/Apply" class="africa" data-drupal-link-system-path="node/72761">Apply</a>
                        <img src="https://visionghs.github.io//images/menu9.jpg" alt="An African woman holds her child" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="https://visionghs.github.io//GHLC/Locations" class="amer-carib" data-drupal-link-system-path="node/72766">Locations</a>
                        <img src="https://visionghs.github.io//images/menu10.jpg" alt="A boy in Mexico smiles while sitting in a hammock" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="https://visionghs.github.io//GHLC/Speakers" class="asia-pacific" data-drupal-link-system-path="node/72771">Speakers</a>
                        <img src="https://visionghs.github.io//images/menu12.jpg" alt="A group of children jump into the ocean in the Philippines" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="https://visionghs.github.io//GHLC/Schedule" class="europe" data-drupal-link-system-path="node/72806">Schedule</a>
                        <img src="https://visionghs.github.io//images/menu11.jpg" alt="A girl makes a heart shape with her hands" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="https://visionghs.github.io//GHLC/FAQS" class="middle-east" data-drupal-link-system-path="node/72796">FAQS</a>
                        <img src="https://visionghs.github.io//images/menu13.jpg" alt="A boy holds a blanket in Eastern Europe" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="https://visionghs.github.io//GHLC" class="show-more" data-drupal-link-system-path="node/72811">See All</a>
                      

          </li>
    </ul>



      </div>



      </li>
  
  <li class="menu-item menu-item--expanded menu-item--resources">
    <div class="menu_link_title"><a href="https://visionghs.github.io//GetInvolved" class="resources" data-drupal-link-system-path="node/72561">Get Involved</a></div>
              
    
  <div class="menu_link_content menu-link-contentmain view-mode-default menu-dropdown menu-dropdown-0 menu-type-default">
              
    <ul class="menu menu-level-1">
      
    <li class="menu-item">
      <a href="https://visionghs.github.io//GetInvolved/College" class="stories" data-drupal-link-system-path="stories">College & Graduate Students</a>
                        <img src="https://visionghs.github.io//images/menu14.jpg" alt="A Peru woman stands in her home" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="https://visionghs.github.io//GetInvolved/Highschool" class="newsroom" data-drupal-link-system-path="newsroom">High School Students</a>
                        <img src="https://visionghs.github.io//images/menu15.jpg" alt="A man reads the newspaper" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="https://visionghs.github.io//GetInvolved/Middleschool" class="publications" data-drupal-link-system-path="publications">Middle School Students</a>
                        <img src="https://visionghs.github.io//images/menu16.jpg" alt="A Chinese boy at school" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="https://visionghs.github.io//GetInvolved/Professionals" class="thought-leader" data-drupal-link-system-path="node/72831">Postgrad & Professionals</a>
                        <img src="https://visionghs.github.io//images/menu17.jpg" alt="A man walks through a field" typeof="foaf:Image" />




          </li>
    </ul>



      </div>



      </li>
</ul>

      </nav>
  <div id="overlay--dropdown" class="overlay--dropdown"></div>
<nav role="navigation" aria-labelledby="block-getinvolved-menu" id="block-getinvolved" class="block block-menu navigation menu--get-involved">
            
  <h2 class="visually-hidden" id="block-getinvolved-menu">More</h2>
  

        
              <ul data-region="topnav">
                    <li class="menu-item--get-involved menu-item--expandable">
        <a href="/More" class="get-involved" data-drupal-link-system-path="node/72911">More</a>
                                <ul>
                    <li class="menu-item--sponsor-a-child">
        <a href="https://visionghs.github.io//GHLC/Apply" class="sponsor" data-drupal-link-system-path="node/72686">Apply to Conference</a>
              </li>
                <li class="menu-item--emergency-support">
        <a href="https://visionghs.github.io//Contact" class="emergency">Contact Us</a>
              </li>
                <li class="menu-item--donate">
        <a href="https://www.paypal.com/paypalme2/HarvardVISION" class="donate" data-drupal-link-system-path="node/72886">Donate</a>
              </li>
                <li class="menu-item--pray-with-us">
        <a href="https://visionghs.github.io//About/Partners" class="prayer" data-drupal-link-system-path="node/72891">Partner with Us</a>
              </li>
                <li class="menu-item--campaign-with-us">
        <a href="https://visionghs.github.io//GetInvolved" class="work-with-us" data-drupal-link-system-path="group/1">Get Involved</a>
              </li>
        </ul>
  
              </li>
        </ul>
  


  </nav>


    </div>
  </div>


  <div class="region region-preheader">
    <div data-drupal-messages-fallback class="hidden"></div>

  </div>

<header>
    <div class="region region-header">
    
  </div>

    
</header>

<main role="main" id="main-content" tabindex="-1" class="body-wrapper">
    <div class="region region-content">
    <div id="block-visionghs-2018-content" class="block block-system block-system-main-block block--visionghs-2018-content">
  
    
      
<article role="article" about="/homepage" class="node--landing-page page--homepage">

  <div class="hero-overlap">
          <div class="eck-entity component--container container--hero not-slider">
    <div class="container__components__hero">
    <div class="views-element-container"><div class="js-view-dom-id-6ae94b31c29563a793f42999a5e345204f59b97a9b30aef8902e65d8f52dec18 views-view--random-hero views-view--random-hero--">
  
  
  

  
  
  

      <div class="views-row">

  <div class="eck-entity hero--default component-hero image-align-bottom text-align-right text-color-white">
    <div class="hero__background">
      <div>
  
  
            <div class="field field--name-thumbnail field--type-image field--label-hidden">    <picture>
  
            <img src="https://visionghs.github.io//images/hopkinton.jpg" alt="Hopkinton" typeof="foaf:Image" />

  </picture>

</div>
      
</div>

    </div>
    <div class="hero__content">
      <div class="hero__content--inner">
                  <div class="hero__subtitle">
            Each year we mentor students to
          </div>
                          <div class="hero__title">
            Create Community Interventions, Learn to Research an Issue, Write a Report, and Become Civically Minded Leaders!
          </div>
                                  <a href="https://visionghs.github.io//About" class="btn btn--lg btn--primary--orange">Learn More</a>
              </div>
    </div>
  </div>

</div>


  
  

  
  

  
  
</div>
</div>

  </div>
  </div>

        <div class="eck-entity component--container container--claim not-slider">
  <div class="container--inner">
            <div class="container__components ">
            <div class="eck-entity component-claim">
    <div class="claim__title">
  <p>500+</p>

  </div>
      <div class="claim__subtitle">
  Students Mentored
  </div>
      <a href="https://visionghs.github.io//About/Mentoring" class="btn btn--secondary--blue">learn more</a>
  </div>
        <div class="eck-entity component-claim">
    <div class="claim__title">
  <p>4</p>

  </div>
      <div class="claim__subtitle">
  Years of Holding Conferences
  </div>
      <a href="https://visionghs.github.io//About/Conference" class="btn btn--secondary--blue">learn more</a>
  </div>
        <div class="eck-entity component-claim">
    <div class="claim__title">
  <p>100+</p>

  </div>
      <div class="claim__subtitle">
  Community Projects
  </div>
      <a href="https://visionghs.github.io//About/Projects" class="btn btn--secondary--blue">learn more</a>
  </div>
  
    </div>
          <div class="container__footer"><p><em>*Vision was founded in 2014 by Paul Lewis'18 at Harvard College and the first conference was held in 2017. Harvard College Vision is an officially recognized organization at Harvard College that runs the annual Global Health and Leadership Conference.</em></p></div>
        
  </div>
</div>

        
  <div class="eck-entity component--view component--view--locations">
          <div class="view__header"><div class="hero__title">3 sites</div></div>
        <div class="view__content">
   
  
  

      <header>
      <span class="legend legend--global-center">Harvard College</span><span class="legend legend--field-office">Columbia University</span><span class="legend legend--support-office">Johns Hopkins University</span>
    </header>
  
  
  
    </div>
  </div>

        <div class="eck-entity component-cta background-color-white accent-color-orange image-align-right layout-card">
  <div class="cta__image"><div>
  
  
            <div class="field field--name-field-media-image field--type-image field--label-hidden">  <img src="https://visionghs.github.io//images/Taiki1.jpg" alt="COVID-19-Masks" typeof="foaf:Image" />

</div>
      
</div>
</div>
  <div class="cta__content">
    <div class="cta__content--inner">
    <div class="cta__icon"></div>
              <h3 class="cta__title">
        <p>Global Health and Leadership Conference:</p>

        </h3>
                    <div class="cta__subtitle">
        Join a Tranformative Experience
        </div>
                    <div class="cta__description">
        
            <div class="field field--name-field-component-description field--type-text-long field--label-hidden"><p>Conduct Projects, Give Presentations, Impact Communities, and Make Friends around the World! </p></div>
      
        </div>
                    <div class="cta__btns">
          <a href="https://visionghs.github.io//GHLC" class="cta__btn">Learn More</a>
        </div>
          </div>
  </div>
</div>

        <div class="eck-entity component--container container--icon not-slider">
  <div class="container--inner">
          <h2 class="container__title">Our students impact their communities in various ways</h2>
              <div class="container__header"><p class="text--emphasis"><a href="https://visionghs.github.io//About/Projects">Project Examples </a></p></div>
        <div class="container__components ">
            <div  class="eck-entity component-icon">
    <a class="icon__wrapper" href="https://visionghs.github.io//About/Projects/IsabellaCarlo">
      <div class="icon__image">  <img src="https://visionghs.github.io//images/Asset2.png" alt="Child protection icon" typeof="foaf:Image" />

</div>
    <div class="icon__subtitle">Physical Health</div>
    </a>
  </div>

        <div  class="eck-entity component-icon">
    <a class="icon__wrapper" href="https://visionghs.github.io//About/Projects/TaikiYamamoto">
      <div class="icon__image">  <img src="https://visionghs.github.io//images/Asset3.png" alt="Disaster Management Icon" typeof="foaf:Image" />

</div>
    <div class="icon__subtitle">Mental Health</div>
    </a>
  </div>

        <div  class="eck-entity component-icon">
    <a class="icon__wrapper" href="https://visionghs.github.io//About/Projects/GabriellaSpina">
      <div class="icon__image">  <img src="https://visionghs.github.io//images/Asset2.png" alt="Education icon" typeof="foaf:Image" />

</div>
    <div class="icon__subtitle">Women's Health</div>
    </a>
  </div>

        <div  class="eck-entity component-icon">
    <a class="icon__wrapper" href="https://visionghs.github.io//About/Projects/">
      <div class="icon__image">  <img src="https://visionghs.github.io//images/Asset3.png" alt="Health Icon" typeof="foaf:Image" />

</div>
    <div class="icon__subtitle">Social Health</div>
    </a>
  </div>

        <div  class="eck-entity component-icon">
    <a class="icon__wrapper" href="https://visionghs.github.io//About/Projects/">
      <div class="icon__image">  <img src="https://visionghs.github.io//images/Asset2.png" alt="Faith and Development icon" typeof="foaf:Image" />

</div>
    <div class="icon__subtitle">Education</div>
    </a>
  </div>

        <div  class="eck-entity component-icon">
    <a class="icon__wrapper" href="https://visionghs.github.io//About/Projects/">
      <div class="icon__image">  <img src="https://visionghs.github.io//images/Asset3.png" alt="Nutrition Icon" typeof="foaf:Image" />

</div>
    <div class="icon__subtitle">Nutrition</div>
    </a>
  </div>

        <div  class="eck-entity component-icon">
    <a class="icon__wrapper" href="https://visionghs.github.io//About/Projects/">
      <div class="icon__image">  <img src="https://visionghs.github.io//images/Asset2.png" alt="Economic Development Icon" typeof="foaf:Image" />

</div>
    <div class="icon__subtitle">Medical</div>
    </a>
  </div>

        <div  class="eck-entity component-icon">
    <a class="icon__wrapper" href="https://visionghs.github.io//About/Projects/">
      <div class="icon__image">  <img src="https://visionghs.github.io//images/Asset3.png" alt="Water Icon" typeof="foaf:Image" />

</div>
    <div class="icon__subtitle">Caregiving</div>
    </a>
  </div>

  
    </div>
          <div class="container__footer"><p><a class="btn--primary--orange" href="https://visionghs.github.io//About/Projects/All">SEE ALL</a></p></div>
        
  </div>
</div>

        <div class="eck-entity component--media background-color-white accent-color-orange single-item">
    
            <div class="field field--name-field-component-heading field--type-text-long field--label-hidden"><p><strong>Meet Our Team</strong></p>

<p>Katrina was a Vision Volunteer in high school and attended our 2017 & 2018 conferences. She is entering her junior year at Harvard for the 2020-2021 school year and is a leader of Vision and the Global Health and Leadership Conference at Harvard College.</p></div>
      
      <div class="field field--name-field-component-media field--type-entity-reference field--label-hidden">
              <div><div>
    <img src="https://visionghs.github.io//images/Katrina.jpg" alt="Katrina" typeof="foaf:Image" />
  
 <!--           <div class="field field--name-field-media-oembed-video field--type-string field--label-hidden"><iframe src="/media/oembed?url=https%3A//www.youtube.com/watch%3Fv%3DRR6doOwK2wc&amp;max_width=0&amp;max_height=0&amp;hash=9gLU7b7g0n8rDjG_jELeWcsixSdjf18eg9izOoCQ6KI" frameborder="0" allowtransparency width="480" height="270" class="media-oembed-content" title="The Impact of Child Sponsorship - Meet Nancy (60 sec)"></iframe>
</div> --> 
      
</div>
</div>
          </div>
  
</div>

        <div class="eck-entity component--container container--card js-slider">
  <div class="container--inner">
            <div class="container__slider">
            <div  class="eck-entity component-card">
    <a href="https://visionghs.github.io//GHLC">
      <div class="card__image"><div>
  
  
            <div class="field field--name-field-media-image field--type-image field--label-hidden">    <picture>
           <img src="https://visionghs.github.io//images/Digital.jpg" alt="A group of students using ipad" typeof="foaf:Image" />

  </picture>

</div>
      
</div>
</div>
    <div class="card__content">
            <div class="card__subtitle">
      Featured
      </div>
                  <div class="card__title">
      4th annual conference moved online
      </div>
                  <div class="card__description">
      
            <div class="field field--name-field-component-description field--type-text-long field--label-hidden"><p dir="ltr">With the coronavirus pandemic and the announcement of Harvard College sending students home, the 4th annual conference moves to an online format.</p></div>
      
      </div>
                  <span class="card__btn">Learn More </span>
          </div>
    </a>
  </div>

        <div  class="eck-entity component-card">
    <a href="https://www.the-iyrc.org/">
      <div class="card__image"><div>
  
  
            <div class="field field--name-field-media-image field--type-image field--label-hidden">    <picture>
           <img src="https://visionghs.github.io//images/iyrc.jpg" alt="IYRC 2019" typeof="foaf:Image" />

  </picture>

</div>
      
</div>
</div>
    <div class="card__content">
                  <div class="card__title">
      International Young Researchers' Conference (IYRC)
      </div>
                  <div class="card__description">
      
            <div class="field field--name-field-component-description field--type-text-long field--label-hidden"><p>We began collaborating with IYRC when our founder helped with their first conference in 2018 in Japan.</p></div>
      
      </div>
                  <span class="card__btn">Learn More</span>
          </div>
    </a>
  </div>

        <div  class="eck-entity component-card">
    <a href="https://visionghs.github.io//About/Mentoring">
      <div class="card__image"><div>
  
  
            <div class="field field--name-field-media-image field--type-image field--label-hidden">    <picture>
            <img src="https://visionghs.github.io//images/winner.jpg" alt="case study winners 2019" typeof="foaf:Image" />

  </picture>

</div>
      
</div>
</div>
    <div class="card__content">
            <div class="card__subtitle">
      Transformative experiences
      </div>
                  <div class="card__title">
      Work with Students Around the World
      </div>
                  <div class="card__description">
      
            <div class="field field--name-field-component-description field--type-text-long field--label-hidden"><p>Each year, we encourage students to step outside their comfort zone to grow as civically minded leaders</p></div>
      
      </div>
                  <span class="card__btn">Learn More</span>
          </div>
    </a>
  </div>

  
    </div>
            
  </div>
</div>

        <div class="eck-entity component-cta background-color-offwhite accent-color-green image-align-left layout-card">
  <div class="cta__image"><div>
  
  
            <div class="field field--name-field-media-image field--type-image field--label-hidden">  <img src="https://visionghs.github.io//images/GHLC2018.png" alt="ghlc 2018" typeof="foaf:Image" />

</div>
      
</div>
</div>
  <div class="cta__content">
    <div class="cta__content--inner">
    
              <h3 class="cta__title">
        <p>Become a Vision Global Health Scholar</p>

        </h3>
                    <div class="cta__subtitle">
        Engage with global health in a deeper way.
        </div>
                    <div class="cta__description">
        
            <div class="field field--name-field-component-description field--type-text-long field--label-hidden"><p>Students interested in continuing the work developed in the Global Health and Leadership Conference may apply to be a Vision Global Health Scholar. Selected Fellows work closely with the Vision team to improve on annual programming. They improve the original project design, receive special training in the topic of interest, collect data, discuss findings, and prepare a presentation for the annual Global Health and Leadership Conference hosted at Columbia, Harvard, and Johns Hopkins.</p></div>
      
        </div>
                    <div class="cta__btns">
          <a href="https://visionghs.github.io//Highschool/Scholars" class="cta__btn">Learn More</a>
        </div>
          </div>
  </div>
</div>

          <div class="eck-entity component-cta background-color-orange accent-color-orange image-align-left layout-full-width same-color">
  <div class="cta__image"><div>
  
  
            <div class="field field--name-field-media-image field--type-image field--label-hidden">  <img src="https://visionghs.github.io//images/team.png" alt="team" typeof="foaf:Image" />

</div>
      
</div>
</div>
  <div class="cta__content">
    <div class="cta__content--inner">
    <div class="cta__icon"></div>
              <h3 class="cta__title">
        <p>Meet our team!</p>

        </h3>
                                <div class="cta__btns">
          <a href="https://visionghs.github.io//About/Team" class="cta__btn">Learn More </a>
        </div>
          </div>
  </div>
</div>

  
  </div>

</article>

  </div>

  </div>

</main>

<footer>
    <div class="region region-footer">
    <div class="container footer__container">
      <div id="block-footerlogo" class="block block-block-content block-block-contentcf8031b4-74c0-48cd-bae0-c967ac240c33 block--footerlogo">
  
    
      
            <div class="field field--name-body field--type-text-with-summary field--label-hidden"><p><a href="/"><img alt="World Vision" data-entity-type="file" data-entity-uuid="3065fa6b-85d7-4b26-848a-5843989552c8" src="https://visionghs.github.io//images/logo--white-rgb_13.png" /></a></p></div>
      
  </div>
<nav role="navigation" aria-labelledby="block-footer-menu" id="block-footer" class="block block-menu navigation menu--footer">
            
  <h2 class="visually-hidden" id="block-footer-menu">Footer</h2>
  

        
              <ul data-region="footer">
                    <li class="menu-item--about-us menu-item--expandable">
        <a href="https://visionghs.github.io//About" data-drupal-link-system-path="node/72551">About Us</a>
                                <ul>
                    <li class="menu-item--our-vision--values">
        <a href="https://visionghs.github.io//About/Vision">Our Vision &amp; Values</a>
              </li>
                <li class="menu-item--our-history">
        <a href="https://visionghs.github.io//About/History" data-drupal-link-system-path="node/72646">Our History</a>
              </li>
                <li class="menu-item--our-leadership">
        <a href="https://visionghs.github.io//About/Team">Our Leadership</a>
              </li>
                <li class="menu-item--our-structure">
        <a href="https://visionghs.github.io//About/Conference">Our Conference</a>
              </li>
                <li class="menu-item--our-partners">
        <a href="https://visionghs.github.io//About/Partners" data-drupal-link-system-path="group/1026">Our Partners</a>
              </li>
                <li class="menu-item--accountability">
        <a href="https://visionghs.github.io//About/Mentoring" data-drupal-link-system-path="node/72741">Mentoring</a>
              </li>
                <li class="menu-item--faq">
        <a href="https://visionghs.github.io//Highschool/Scholars">Scholars</a>
              </li>
        </ul>
  
              </li>
                <li class="menu-item--our-approaches-to-change menu-item--expandable">
        <a href="https://visionghs.github.io//GHLC" data-drupal-link-system-path="node/72731">Global Health and Leadership Conference</a>
                                <ul>
                    <li class="menu-item--our-global-strategy">
        <a href="https://visionghs.github.io//GHLC/Apply" data-drupal-link-system-path="node/72696">Apply</a>
              </li>
                <li class="menu-item--the-role-of-faith">
        <a href="https://visionghs.github.io//GHLC/Speakers" data-drupal-link-system-path="node/72726">Speakers</a>
              </li>
                <li class="menu-item--global-campaign">
        <a href="https://visionghs.github.io//GHLC/Schedule" data-drupal-link-system-path="group/1">Schedule</a>
              </li>
                <li class="menu-item--work-in-fragile-places">
        <a href="https://visionghs.github.io//GHLC/FAQS"></a> FAQS
              </li>
        </ul>
  
              </li>
                <li class="menu-item--careers--internships menu-item--expandable">
        <a href="https://visionghs.github.io//GetInvolved"> Join Our Mission</a>
                                <ul>
                    <li class="menu-item--open-positions">
        <a href="https://visionghs.github.io//GetInvolved/College">College & Graduate Students</a>
              </li>
                <li class="menu-item--explore-teams">
        <a href="https://visionghs.github.io//GetInvolved/Highschool">High School Students</a>
              </li>
                <li class="menu-item--explore-locations">
        <a href="https://visionghs.github.io//GetInvolved/Middleschool">Middle School Students</a>
              </li>
                <li class="menu-item--our-culture">
        <a href="https://visionghs.github.io//GetInvolved/Professionals">Postgraduate & Professionals</a>
              </li>
        </ul>
  
              </li>
                <li class="menu-item--connect-with-us menu-item--expandable">
        <a href="https://visionghs.github.io//Contact" data-drupal-link-system-path="node/72846">Connect With Us</a>
                                <ul>
                    <li class="menu-item--facebook">
        <a href="https://www.facebook.com/HarvardVision/" class="facebook-link" target="_blank">Facebook</a>
              </li>
                <li class="menu-item--youtube">
        <a href="https://www.youtube.com/" class="youtube-link" target="_blank">Youtube</a>
              </li>
                <li class="menu-item--twitter">
        <a href="https://twitter.com/Harvard_Vision" class="twitter-link" target="_blank">Twitter</a>
              </li>
                <li class="menu-item--instagram">
        <a href="https://www.instagram.com/harvardcollegevision/" class="instagram-link" target="_blank">Instagram</a>
              </li>
                <li class="menu-item--linkedin">
        <a href="https://www.linkedin.com/in/paulmatthewlewis/" class="linkedin-link" target="_blank">LinkedIn</a>
              </li>
                <li class="menu-item--contact-us">
        <a href="https://visionghs.github.io//Contact" data-drupal-link-system-path="node/72846">Contact Us</a>
              </li>
                <li class="menu-item--world-vision-in-your-country">
        <a href="mailto:info@harvardcollegevision.org" data-drupal-link-system-path="node/72811">Email</a>
              </li>
                <li class="menu-item--report-a-concern">
        <a href="https://www.messenger.com/t/HarvardVision">Facebook Messenger</a>
              </li>
        </ul>
  
              </li>
        </ul>
  


  </nav>

<div id="block-accountablenowlogo" class="block block-block-content block-block-contentc32d35ab-86e0-4257-b5df-c684ffe90575 block--accountablenowlogo">
  
    
      
            <div class="field field--name-body field--type-text-with-summary field--label-hidden"><p> </p>

<!--<p><a href="https://accountablenow.org/"><img alt="Accountable Now" data-entity-type="file" data-entity-uuid="fdc87d61-f207-4043-8d97-37814a46bb97" src="https://visionghs.github.io//images/logo--accountable-now_11.png" /></a></p></div>
    -->  
  </div>
<nav role="navigation" aria-labelledby="block-footerlegal-menu" id="block-footerlegal" class="block block-menu navigation menu--footer-legal">
            
  <h2 class="visually-hidden" id="block-footerlegal-menu">Footer Legal</h2>
  

        
              <ul data-region="footer">
          <li class='copyright'>&copy; 2020 Vision Global Health Society</li>
          <li>
        <a href="https://visionghs.github.io//History" data-drupal-link-system-path="node/41736">Founded: 2014</a>
              </li>
          <li>
        <a href="https://college.harvard.edu/" data-drupal-link-system-path="node/45251">Harvard College</a>
              </li>
        </ul>
  


  </nav>

    </div>
  </div>

<!--</footer> -->

  </div>

    
<!--    <script type="application/json" data-drupal-selector="drupal-settings-json">{"path":{"baseUrl":"\/","scriptPath":null,"pathPrefix":"","currentPath":"node\/72661","currentPathIsAdmin":false,"isFront":true,"currentLanguage":"en"},"pluralDelimiter":"\u0003","suppressDeprecationErrors":true,"ajaxPageState":{"libraries":"anchor_link\/drupal.anchor_link,core\/html5shiv,core\/picturefill,eu_cookie_compliance\/eu_cookie_compliance_bare,media\/oembed.formatter,system\/base,views\/views.module,visionghs_2018\/fonts,visionghs_2018\/global-scripts,visionghs_2018\/global-styling,visionghs_maps\/locations_view","theme":"visionghs_2018","theme_token":null},"ajaxTrustedUrl":{"form_action_p_pvdeGsVG5zNF_XLGPTvYSKCf43t8qZYSwcfZl2uzM":true},"eu_cookie_compliance":{"popup_enabled":true,"popup_agreed_enabled":false,"popup_hide_agreed":false,"popup_clicking_confirmation":false,"popup_scrolling_confirmation":false,"popup_html_info":"\u003Cdiv class=\u0022eu-cookie-compliance-banner eu-cookie-compliance-banner-info\u0022\u003E\n  \u003Cdiv class=\u0022popup-content info eu-cookie-compliance-content\u0022\u003E\n    \u003Cdiv id=\u0022popup-text\u0022 class=\u0022eu-cookie-compliance-message\u0022\u003E\n      \u003Cp\u003EThis site uses cookie to store information on your computer. By using this site you agree to our use of cookies. For More information see our \u003Ca href=\u0022\/privacy-policy\u0022\u003EPrivacy Policy\u003C\/a\u003E.\u003C\/p\u003E\n    \u003C\/div\u003E\n    \u003Cdiv id=\u0022popup-buttons\u0022 class=\u0022eu-cookie-compliance-buttons\u0022\u003E\n              \u003Cbutton type=\u0022button\u0022 class=\u0022decline-button eu-cookie-compliance-default-button btn--secondary--orange\u0022 \u003EDeny\u003C\/button\u003E\n            \u003Cbutton type=\u0022button\u0022 class=\u0022agree-button eu-cookie-compliance-secondary-button btn--primary--orange\u0022\u003EAccept\u003C\/button\u003E\n    \u003C\/div\u003E\n  \u003C\/div\u003E\n\u003C\/div\u003E","use_mobile_message":false,"mobile_popup_html_info":"\u003Cdiv class=\u0022eu-cookie-compliance-banner eu-cookie-compliance-banner-info\u0022\u003E\n  \u003Cdiv class=\u0022popup-content info eu-cookie-compliance-content\u0022\u003E\n    \u003Cdiv id=\u0022popup-text\u0022 class=\u0022eu-cookie-compliance-message\u0022\u003E\n      \n    \u003C\/div\u003E\n    \u003Cdiv id=\u0022popup-buttons\u0022 class=\u0022eu-cookie-compliance-buttons\u0022\u003E\n              \u003Cbutton type=\u0022button\u0022 class=\u0022decline-button eu-cookie-compliance-default-button btn--secondary--orange\u0022 \u003EDeny\u003C\/button\u003E\n            \u003Cbutton type=\u0022button\u0022 class=\u0022agree-button eu-cookie-compliance-secondary-button btn--primary--orange\u0022\u003EAccept\u003C\/button\u003E\n    \u003C\/div\u003E\n  \u003C\/div\u003E\n\u003C\/div\u003E","mobile_breakpoint":768,"popup_html_agreed":false,"popup_use_bare_css":true,"popup_height":"auto","popup_width":"100%","popup_delay":1000,"popup_link":"\/privacy-policy","popup_link_new_window":true,"popup_position":false,"fixed_top_position":true,"popup_language":"en","store_consent":false,"better_support_for_screen_readers":false,"cookie_name":"","reload_page":false,"domain":"","domain_all_sites":null,"popup_eu_only_js":false,"cookie_lifetime":100,"cookie_session":0,"disagree_do_not_show_popup":false,"method":"opt_in","whitelisted_cookies":"","withdraw_markup":"\u003Cbutton type=\u0022button\u0022 class=\u0022eu-cookie-withdraw-tab\u0022\u003EPrivacy settings\u003C\/button\u003E\n\u003Cdiv class=\u0022eu-cookie-withdraw-banner\u0022\u003E\n  \u003Cdiv class=\u0022popup-content info eu-cookie-compliance-content\u0022\u003E\n    \u003Cdiv id=\u0022popup-text\u0022 class=\u0022eu-cookie-compliance-message\u0022\u003E\n      \u003Ch2\u003EWe use cookies on this site to enhance your user experience\u003C\/h2\u003E\u003Cp\u003EYou have given your consent for us to set cookies.\u003C\/p\u003E\n    \u003C\/div\u003E\n    \u003Cdiv id=\u0022popup-buttons\u0022 class=\u0022eu-cookie-compliance-buttons\u0022\u003E\n      \u003Cbutton type=\u0022button\u0022 class=\u0022eu-cookie-withdraw-button\u0022\u003EWithdraw consent\u003C\/button\u003E\n    \u003C\/div\u003E\n  \u003C\/div\u003E\n\u003C\/div\u003E","withdraw_enabled":false,"withdraw_button_on_info_popup":null,"cookie_categories":[],"enable_save_preferences_button":null,"fix_first_cookie_category":null,"select_all_categories_by_default":null},"geolocation":{"commonMap":{"8e368c99890fc2c6d615cb057996bb97b3d3fab910830b5dcc1887b047d90ff0":{"settings":{"google_map_settings":{"type":"ROADMAP","zoom":"3","minZoom":0,"maxZoom":4,"rotateControl":0,"mapTypeControl":0,"streetViewControl":0,"zoomControl":1,"fullscreenControl":0,"scrollwheel":0,"disableDoubleClickZoom":0,"draggable":1,"height":"820px","width":"100%","info_auto_display":0,"marker_icon_path":"themes\/custom\/visionghs_2018\/images\/markers\/visionghs_marker_{{ type }}.png","disableAutoPan":0,"style":[{"featureType":"all","elementType":"labels","stylers":[{"visibility":"off"}]},{"featureType":"administrative","elementType":"geometry.fill","stylers":[{"color":"#fefefe"},{"lightness":20},{"visibility":"off"}]},{"featureType":"administrative","elementType":"geometry.stroke","stylers":[{"color":"#fefefe"},{"lightness":17},{"weight":1.2}]},{"featureType":"administrative","elementType":"labels","stylers":[{"visibility":"off"}]},{"featureType":"administrative.country","elementType":"geometry.stroke","stylers":[{"weight":"0.75"},{"color":"#dadada"},{"lightness":"0"}]},{"featureType":"administrative.province","elementType":"all","stylers":[{"visibility":"off"}]},{"featureType":"administrative.locality","elementType":"all","stylers":[{"visibility":"off"}]},{"featureType":"administrative.neighborhood","elementType":"all","stylers":[{"visibility":"off"}]},{"featureType":"administrative.land_parcel","elementType":"all","stylers":[{"visibility":"off"}]},{"featureType":"landscape","elementType":"geometry","stylers":[{"color":"#dadada"},{"visibility":"on"}]},{"featureType":"poi","elementType":"all","stylers":[{"visibility":"off"}]},{"featureType":"road","elementType":"all","stylers":[{"visibility":"off"}]},{"featureType":"water","elementType":"geometry","stylers":[{"color":"#f8f8f8"},{"lightness":17}]},{"featureType":"water","elementType":"labels","stylers":[{"visibility":"off"}]}],"preferScrollingToZooming":0,"gestureHandling":"cooperative"}}}},"google_map_url":"https:\/\/maps.googleapis.com\/maps\/api\/js?libraries=\u0026region=\u0026language=\u0026v=\u0026client=\u0026callback=Drupal.geolocation.googleCallback\u0026key=AIzaSyA8JO4Fet1f9TI0aW5n2YPs79geVEdUqMk"},"user":{"uid":0,"permissionsHash":"108ffe1feb20c047c66014a7d38f66d93fb5e11491fb28d60f0d65ac7f59da3e"}}</script>
-->
<script src="https://visionghs.github.io//js/js_BAqaKhzdQpF_4bl5P0uflguXHhjaa6x5RJiqg5l-nmo.js"></script>

  <script type="text/javascript">window.NREUM||(NREUM={});NREUM.info={"beacon":"bam.nr-data.net","licenseKey":"006b5744c1","applicationID":"115598855","transactionName":"MVwHZkMDWxBSVhUPDQgWJFFFC1oNHHETExIHVTlxXhBQP3VaEws+IFYXX3MXXA9XUBNLXBRcC1ZUEGUPUlYEDg0KXQBAdw1HDnJWFQ8NCA==","queueTime":0,"applicationTime":311,"atts":"HRsEEAsZSB4=","errorBeacon":"bam.nr-data.net","agent":""}</script>
 <!-- </body>
</html> -->
