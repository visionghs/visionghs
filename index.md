<!DOCTYPE html>
<html lang="en" dir="ltr" prefix="content: http://purl.org/rss/1.0/modules/content/  dc: http://purl.org/dc/terms/  foaf: http://xmlns.com/foaf/0.1/  og: http://ogp.me/ns#  rdfs: http://www.w3.org/2000/01/rdf-schema#  schema: http://schema.org/  sioc: http://rdfs.org/sioc/ns#  sioct: http://rdfs.org/sioc/types#  skos: http://www.w3.org/2004/02/skos/core#  xsd: http://www.w3.org/2001/XMLSchema# ">
  <head>
    <meta charset="utf-8" /><script type="text/javascript">(window.NREUM||(NREUM={})).loader_config={licenseKey:"006b5744c1",applicationID:"115598855"};window.NREUM||(NREUM={}),__nr_require=function(e,n,t){function r(t){if(!n[t]){var i=n[t]={exports:{}};e[t][0].call(i.exports,function(n){var i=e[t][1][n];return r(i||n)},i,i.exports)}return n[t].exports}if("function"==typeof __nr_require)return __nr_require;for(var i=0;i<t.length;i++)r(t[i]);return r}({1:[function(e,n,t){function r(){}function i(e,n,t){return function(){return o(e,[u.now()].concat(f(arguments)),n?null:this,t),n?void 0:this}}var o=e("handle"),a=e(4),f=e(5),c=e("ee").get("tracer"),u=e("loader"),s=NREUM;"undefined"==typeof window.newrelic&&(newrelic=s);var p=["setPageViewName","setCustomAttribute","setErrorHandler","finished","addToTrace","inlineHit","addRelease"],l="api-",d=l+"ixn-";a(p,function(e,n){s[n]=i(l+n,!0,"api")}),s.addPageAction=i(l+"addPageAction",!0),s.setCurrentRouteName=i(l+"routeName",!0),n.exports=newrelic,s.interaction=function(){return(new r).get()};var m=r.prototype={createTracer:function(e,n){var t={},r=this,i="function"==typeof n;return o(d+"tracer",[u.now(),e,t],r),function(){if(c.emit((i?"":"no-")+"fn-start",[u.now(),r,i],t),i)try{return n.apply(this,arguments)}catch(e){throw c.emit("fn-err",[arguments,this,e],t),e}finally{c.emit("fn-end",[u.now()],t)}}}};a("actionText,setName,setAttribute,save,ignore,onEnd,getContext,end,get".split(","),function(e,n){m[n]=i(d+n)}),newrelic.noticeError=function(e,n){"string"==typeof e&&(e=new Error(e)),o("err",[e,u.now(),!1,n])}},{}],2:[function(e,n,t){function r(e,n){var t=e.getEntries();t.forEach(function(e){"first-paint"===e.name?c("timing",["fp",Math.floor(e.startTime)]):"first-contentful-paint"===e.name&&c("timing",["fcp",Math.floor(e.startTime)])})}function i(e,n){var t=e.getEntries();t.length>0&&c("lcp",[t[t.length-1]])}function o(e){if(e instanceof s&&!l){var n,t=Math.round(e.timeStamp);n=t>1e12?Date.now()-t:u.now()-t,l=!0,c("timing",["fi",t,{type:e.type,fid:n}])}}if(!("init"in NREUM&&"page_view_timing"in NREUM.init&&"enabled"in NREUM.init.page_view_timing&&NREUM.init.page_view_timing.enabled===!1)){var a,f,c=e("handle"),u=e("loader"),s=NREUM.o.EV;if("PerformanceObserver"in window&&"function"==typeof window.PerformanceObserver){a=new PerformanceObserver(r),f=new PerformanceObserver(i);try{a.observe({entryTypes:["paint"]}),f.observe({entryTypes:["largest-contentful-paint"]})}catch(p){}}if("addEventListener"in document){var l=!1,d=["click","keydown","mousedown","pointerdown","touchstart"];d.forEach(function(e){document.addEventListener(e,o,!1)})}}},{}],3:[function(e,n,t){function r(e,n){if(!i)return!1;if(e!==i)return!1;if(!n)return!0;if(!o)return!1;for(var t=o.split("."),r=n.split("."),a=0;a<r.length;a++)if(r[a]!==t[a])return!1;return!0}var i=null,o=null,a=/Version\/(\S+)\s+Safari/;if(navigator.userAgent){var f=navigator.userAgent,c=f.match(a);c&&f.indexOf("Chrome")===-1&&f.indexOf("Chromium")===-1&&(i="Safari",o=c[1])}n.exports={agent:i,version:o,match:r}},{}],4:[function(e,n,t){function r(e,n){var t=[],r="",o=0;for(r in e)i.call(e,r)&&(t[o]=n(r,e[r]),o+=1);return t}var i=Object.prototype.hasOwnProperty;n.exports=r},{}],5:[function(e,n,t){function r(e,n,t){n||(n=0),"undefined"==typeof t&&(t=e?e.length:0);for(var r=-1,i=t-n||0,o=Array(i<0?0:i);++r<i;)o[r]=e[n+r];return o}n.exports=r},{}],6:[function(e,n,t){n.exports={exists:"undefined"!=typeof window.performance&&window.performance.timing&&"undefined"!=typeof window.performance.timing.navigationStart}},{}],ee:[function(e,n,t){function r(){}function i(e){function n(e){return e&&e instanceof r?e:e?c(e,f,o):o()}function t(t,r,i,o){if(!l.aborted||o){e&&e(t,r,i);for(var a=n(i),f=v(t),c=f.length,u=0;u<c;u++)f[u].apply(a,r);var p=s[y[t]];return p&&p.push([b,t,r,a]),a}}function d(e,n){h[e]=v(e).concat(n)}function m(e,n){var t=h[e];if(t)for(var r=0;r<t.length;r++)t[r]===n&&t.splice(r,1)}function v(e){return h[e]||[]}function g(e){return p[e]=p[e]||i(t)}function w(e,n){u(e,function(e,t){n=n||"feature",y[t]=n,n in s||(s[n]=[])})}var h={},y={},b={on:d,addEventListener:d,removeEventListener:m,emit:t,get:g,listeners:v,context:n,buffer:w,abort:a,aborted:!1};return b}function o(){return new r}function a(){(s.api||s.feature)&&(l.aborted=!0,s=l.backlog={})}var f="nr@context",c=e("gos"),u=e(4),s={},p={},l=n.exports=i();l.backlog=s},{}],gos:[function(e,n,t){function r(e,n,t){if(i.call(e,n))return e[n];var r=t();if(Object.defineProperty&&Object.keys)try{return Object.defineProperty(e,n,{value:r,writable:!0,enumerable:!1}),r}catch(o){}return e[n]=r,r}var i=Object.prototype.hasOwnProperty;n.exports=r},{}],handle:[function(e,n,t){function r(e,n,t,r){i.buffer([e],r),i.emit(e,n,t)}var i=e("ee").get("handle");n.exports=r,r.ee=i},{}],id:[function(e,n,t){function r(e){var n=typeof e;return!e||"object"!==n&&"function"!==n?-1:e===window?0:a(e,o,function(){return i++})}var i=1,o="nr@id",a=e("gos");n.exports=r},{}],loader:[function(e,n,t){function r(){if(!x++){var e=E.info=NREUM.info,n=d.getElementsByTagName("script")[0];if(setTimeout(s.abort,3e4),!(e&&e.licenseKey&&e.applicationID&&n))return s.abort();u(y,function(n,t){e[n]||(e[n]=t)}),c("mark",["onload",a()+E.offset],null,"api");var t=d.createElement("script");t.src="https://"+e.agent,n.parentNode.insertBefore(t,n)}}function i(){"complete"===d.readyState&&o()}function o(){c("mark",["domContent",a()+E.offset],null,"api")}function a(){return O.exists&&performance.now?Math.round(performance.now()):(f=Math.max((new Date).getTime(),f))-E.offset}var f=(new Date).getTime(),c=e("handle"),u=e(4),s=e("ee"),p=e(3),l=window,d=l.document,m="addEventListener",v="attachEvent",g=l.XMLHttpRequest,w=g&&g.prototype;NREUM.o={ST:setTimeout,SI:l.setImmediate,CT:clearTimeout,XHR:g,REQ:l.Request,EV:l.Event,PR:l.Promise,MO:l.MutationObserver};var h=""+location,y={beacon:"bam.nr-data.net",errorBeacon:"bam.nr-data.net",agent:"js-agent.newrelic.com/nr-1167.min.js"},b=g&&w&&w[m]&&!/CriOS/.test(navigator.userAgent),E=n.exports={offset:f,now:a,origin:h,features:{},xhrWrappable:b,userAgent:p};e(1),e(2),d[m]?(d[m]("DOMContentLoaded",o,!1),l[m]("load",r,!1)):(d[v]("onreadystatechange",i),l[v]("onload",r)),c("mark",["firstbyte",f],null,"api");var x=0,O=e(6)},{}],"wrap-function":[function(e,n,t){function r(e){return!(e&&e instanceof Function&&e.apply&&!e[a])}var i=e("ee"),o=e(5),a="nr@original",f=Object.prototype.hasOwnProperty,c=!1;n.exports=function(e,n){function t(e,n,t,i){function nrWrapper(){var r,a,f,c;try{a=this,r=o(arguments),f="function"==typeof t?t(r,a):t||{}}catch(u){l([u,"",[r,a,i],f])}s(n+"start",[r,a,i],f);try{return c=e.apply(a,r)}catch(p){throw s(n+"err",[r,a,p],f),p}finally{s(n+"end",[r,a,c],f)}}return r(e)?e:(n||(n=""),nrWrapper[a]=e,p(e,nrWrapper),nrWrapper)}function u(e,n,i,o){i||(i="");var a,f,c,u="-"===i.charAt(0);for(c=0;c<n.length;c++)f=n[c],a=e[f],r(a)||(e[f]=t(a,u?f+i:i,o,f))}function s(t,r,i){if(!c||n){var o=c;c=!0;try{e.emit(t,r,i,n)}catch(a){l([a,t,r,i])}c=o}}function p(e,n){if(Object.defineProperty&&Object.keys)try{var t=Object.keys(e);return t.forEach(function(t){Object.defineProperty(n,t,{get:function(){return e[t]},set:function(n){return e[t]=n,n}})}),n}catch(r){l([r])}for(var i in e)f.call(e,i)&&(n[i]=e[i]);return n}function l(n){try{e.emit("internal-error",n)}catch(t){}}return e||(e=i),t.inPlace=u,t.flag=a,t}},{}]},{},["loader"]);</script>
<link rel="shortlink" href="https://visionghs.github.io//" />
<link rel="canonical" href="https://visionghs.github.io//" />
<meta name="Generator" content="Drupal 8 (https://www.drupal.org)" />
<meta name="MobileOptimized" content="width" />
<meta name="HandheldFriendly" content="true" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<link rel="shortcut icon" href="https://visionghs.github.io//favicon.png" type="image/png" />
<link rel="alternate" hreflang="en" href="https://visionghs.github.io//homepage" />
<link rel="alternate" hreflang="fr" href="https://visionghs.github.io//fr/homepage" />
<link rel="alternate" hreflang="es" href="https://visionghs.github.io//es/homepage" />
<link rel="revision" href="https://visionghs.github.io//homepage" />
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
    <noscript aria-hidden="true"><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-WCWLCJ8" height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>
      <div class="dialog-off-canvas-main-canvas" data-off-canvas-main-canvas>
    
  <div class="region region-alert">
    <div class="views-element-container block block-views block-views-blockalert-block-1 block--views-block-alert-block-1" id="block-views-block-alert-block-1">
  
    
      <div><div class="js-view-dom-id-a74d360a73b24ddb8b44f269cc58bc6e49deffe4b98bb6b82ea64fc72a19d140 views-view--alert views-view--alert--">
  
  
  

  
  
  

      <div class="views-row">


<input  type="checkbox" checked="checked" id="wvi-alert-1-26-toggle" class="wvi-alert--toggle hidden">
<label  class="wvi-alert" id="wvi-alert-1-26" for="wvi-alert-1-26-toggle">
  <span class="content">
          <a href="https://visionghs.github.io//emergencies/coronavirus-health-crisis" class="field--name-message">Help stop the spread of the coronavirus and support those impacted</a>
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
        <img src="https://visionghs.github.io//images/logo.jpg" alt="Home"/>
      </a>
          
</div>
      <div class="show-menu" aria-label="Show Menu" aria-controls="menu-level-0"></div>
  <nav role="navigation" aria-labelledby="block-mainnavigation-menu" id="block-mainnavigation" class="block block-menu navigation menu--main region-topnav__menu--main">
                      
    <h2 class="visually-hidden" id="block-mainnavigation-menu">Main navigation</h2>
    

              
<ul class="menu menu-level-0">
  
  <li class="menu-item menu-item--expanded menu-item--our-work">
    <div class="menu_link_title"><a href="/our-work" class="our-work" data-drupal-link-system-path="node/72681">Our Work</a></div>
              
    
  <div class="menu_link_content menu-link-contentmain view-mode-default menu-dropdown menu-dropdown-0 menu-type-default">
              
    <ul class="menu menu-level-1">
      
    <li class="menu-item">
      <a href="/our-impact" class="impact">Our Impact</a>
                        <img src="https://visionghs.github.io//styles/medium_square/public/2019-02/menu--our-impact_11.jpg?itok=Fih-eKED" alt="A girl smiles in Ghana" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="/child-protection" data-drupal-link-system-path="group/641">Child Protection</a>
                        <img src="https://visionghs.github.io//styles/medium_square/public/2019-04/D055-0626-234.jpg_394905_0.jpg?itok=ZCizxXUN" alt="A Cambodian girl smiles" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="/disaster-management" class="dis-man" data-drupal-link-system-path="group/606">Disaster Management</a>
                        <img src="https://visionghs.github.io//styles/medium_square/public/2019-02/menu--disaster-management_11.jpg?itok=qOQNyA3N" alt="woman standing outside " typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="/economic-development" class="econ-dev" data-drupal-link-system-path="group/651">Economic Development</a>
                        <img src="https://visionghs.github.io//styles/medium_square/public/2019-02/menu--economic-development_11.jpg?itok=2V2cDB2e" alt="Young boy" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="/education" data-drupal-link-system-path="group/586">Education</a>
                        <img src="https://visionghs.github.io//styles/medium_square/public/2019-04/D256-0318-32_697779-web2.jpg?itok=Gikd_uTG" alt="A young girl writes on a chalkboard" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="/faithanddevelopment">Faith &amp; Development</a>
                        <img src="https://visionghs.github.io//styles/medium_square/public/2019-04/Ghana_Day1_201-web.jpg?itok=26dKzJgl" alt="A pastor and child in a church" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="/health" data-drupal-link-system-path="group/646">Health &amp; Nutrition</a>
                        <img src="https://visionghs.github.io//styles/medium_square/public/2019-04/D485-0571-61_481434-web.jpg?itok=0qx4rP7w" alt="A Healthy Baby" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="/cleanwater" data-drupal-link-system-path="group/576">Water</a>
                        <img src="https://visionghs.github.io//styles/medium_square/public/2019-04/Colombia_Day3_261-header.jpg?itok=EyqXpgDW" alt="A Colombian boy has clean water" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="/see-all-sectors" class="show-more">View All Sectors</a>
                      

          </li>
    </ul>



      </div>



      </li>
  
  <li class="menu-item menu-item--expanded menu-item--where-we-work">
    <div class="menu_link_title"><a href="/locations" class="where-work" data-drupal-link-system-path="node/72811">Where We Work</a></div>
              
    
  <div class="menu_link_content menu-link-contentmain view-mode-default menu-dropdown menu-dropdown-0 menu-type-default">
              
    <ul class="menu menu-level-1">
      
    <li class="menu-item">
      <a href="/africa" class="africa" data-drupal-link-system-path="node/72761">Africa</a>
                        <img src="https://visionghs.github.io//styles/medium_square/public/2019-02/menu--africa_11.jpg?itok=XgffMtyH" alt="An African woman holds her child" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="/americas" class="amer-carib" data-drupal-link-system-path="node/72766">Americas</a>
                        <img src="https://visionghs.github.io//styles/medium_square/public/2019-02/menu--americas-and-caribbean_11.jpg?itok=b8USpYSR" alt="A boy in Mexico smiles while sitting in a hammock" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="/where-we-work/asia-pacific" class="asia-pacific" data-drupal-link-system-path="node/72771">Asia Pacific</a>
                        <img src="https://visionghs.github.io//styles/medium_square/public/2019-04/2015-Philippines-Final-%2889-of-133%29.jpg?itok=8E4TN_5A" alt="A group of children jump into the ocean in the Philippines" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="/europe" class="europe" data-drupal-link-system-path="node/72806">Europe</a>
                        <img src="https://visionghs.github.io//styles/medium_square/public/2019-02/menu--europe_11.jpg?itok=ir6vNxgk" alt="A girl makes a heart shape with her hands" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="/where-we-work/middle-east" class="middle-east" data-drupal-link-system-path="node/72796">Middle East</a>
                        <img src="https://visionghs.github.io//styles/medium_square/public/2019-04/WV262015.jpg?itok=B2_soTjg" alt="A boy holds a blanket in Eastern Europe" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="/locations" class="show-more" data-drupal-link-system-path="node/72811">See All Locations</a>
                      

          </li>
    </ul>



      </div>



      </li>
  
  <li class="menu-item menu-item--expanded menu-item--resources">
    <div class="menu_link_title"><a href="/resources" class="resources" data-drupal-link-system-path="node/72561">Resources</a></div>
              
    
  <div class="menu_link_content menu-link-contentmain view-mode-default menu-dropdown menu-dropdown-0 menu-type-default">
              
    <ul class="menu menu-level-1">
      
    <li class="menu-item">
      <a href="/stories" class="stories" data-drupal-link-system-path="stories">Stories</a>
                        <img src="https://visionghs.github.io//styles/medium_square/public/2019-02/menu--stories_11.jpg?itok=wsXjT-QE" alt="A Peru woman stands in her home" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="/newsroom" class="newsroom" data-drupal-link-system-path="newsroom">Newsroom</a>
                        <img src="https://visionghs.github.io//styles/medium_square/public/2019-02/menu--newsroom_11.jpg?itok=KS0OfNt_" alt="A man reads the newspaper" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="/publications" class="publications" data-drupal-link-system-path="publications">Publications</a>
                        <img src="https://visionghs.github.io//styles/medium_square/public/2019-02/menu--publications_11.jpg?itok=0HKOwhe3" alt="A Chinese boy at school" typeof="foaf:Image" />




          </li>
      
    <li class="menu-item">
      <a href="/view" class="thought-leader" data-drupal-link-system-path="node/72831">World Vision View</a>
                        <img src="https://visionghs.github.io//styles/medium_square/public/2019-02/menu--thought-leadership_11.jpg?itok=aXMez7on" alt="A man walks through a field" typeof="foaf:Image" />




          </li>
    </ul>



      </div>



      </li>
</ul>

      </nav>
  <div id="overlay--dropdown" class="overlay--dropdown"></div>
<nav role="navigation" aria-labelledby="block-getinvolved-menu" id="block-getinvolved" class="block block-menu navigation menu--get-involved">
            
  <h2 class="visually-hidden" id="block-getinvolved-menu">Get Involved</h2>
  

        
              <ul data-region="topnav">
                    <li class="menu-item--get-involved menu-item--expandable">
        <a href="/get-involved" class="get-involved" data-drupal-link-system-path="node/72911">Get Involved</a>
                                <ul>
                    <li class="menu-item--sponsor-a-child">
        <a href="/child-sponsorship" class="sponsor" data-drupal-link-system-path="node/72686">Sponsor a Child</a>
              </li>
                <li class="menu-item--emergency-support">
        <a href="/emergencies" class="emergency">Emergency Support</a>
              </li>
                <li class="menu-item--donate">
        <a href="/donate" class="donate" data-drupal-link-system-path="node/72886">Donate</a>
              </li>
                <li class="menu-item--pray-with-us">
        <a href="/prayer" class="prayer" data-drupal-link-system-path="node/72891">Pray With Us</a>
              </li>
                <li class="menu-item--campaign-with-us">
        <a href="/ittakesaworld" class="work-with-us" data-drupal-link-system-path="group/1">Campaign With Us</a>
              </li>
        </ul>
  
              </li>
        </ul>
  


  </nav>
<div class="language-switcher-language-url block block-language block-language-blocklanguage-interface block--anguageswitcher" id="block-languageswitcher" role="navigation">
  
    
      <a href="/" class="language-link is-active" hreflang="en" data-drupal-link-system-path="&lt;front&gt;"><span class="language-switcher__option-text">English</span>
</a><ul class="links language-switcher__options"><li hreflang="fr" data-drupal-link-system-path="&lt;front&gt;"><a href="/fr" class="language-link" hreflang="fr" data-drupal-link-system-path="&lt;front&gt;"><span class="language-switcher__option-text">French</span>
</a></li><li hreflang="es" data-drupal-link-system-path="&lt;front&gt;"><a href="/es" class="language-link" hreflang="es" data-drupal-link-system-path="&lt;front&gt;"><span class="language-switcher__option-text">Spanish</span>
</a></li></ul>
  </div>

      <div class="region-topnav__search">
        <div class="topnav__search-wrapper">
          <form class="region-topnav__search-form" action="/search">
            <div>
              <a class="region-topnav__search-icon" href="/search"></a>
              <input class="region-topnav__search-input" type="text" name="search" value="" placeholder="Search WVI.ORG">
              <input class="region-topnav__search-submit" type="submit" value="Search">
              <div class="hide-search" aria-label="Close Search"></div>
            </div>
          </form>
          <div class="show-search" aria-label="Search Site" aria-controls="region-topnav__search"></div>
        </div>
      </div>
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
    <div id="block-wvi-2018-content" class="block block-system block-system-main-block block--wvi-2018-content">
  
    
      
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
                <!--[if IE 9]><video style="display: none;"><![endif]-->
              <source srcset="https://visionghs.github.io//styles/hero_rectangle/public/2020-01/W140-0024-088.jpg?itok=U6rvZ-q_ 1x, /sites/default/files/styles/hero_rectangle/public/2020-01/W140-0024-088.jpg?itok=U6rvZ-q_ 2x" media="(min-width: 1500px)" type="image/jpeg"/>
              <source srcset="https://visionghs.github.io//styles/hero_rectangle/public/2020-01/W140-0024-088.jpg?itok=U6rvZ-q_ 1x, /sites/default/files/styles/hero_rectangle/public/2020-01/W140-0024-088.jpg?itok=U6rvZ-q_ 2x" media="(min-width: 960px)" type="image/jpeg"/>
              <source srcset="https://visionghs.github.io//styles/hero_rectangle/public/2020-01/W140-0024-088.jpg?itok=U6rvZ-q_ 1x, /sites/default/files/styles/hero_rectangle/public/2020-01/W140-0024-088.jpg?itok=U6rvZ-q_ 2x" media="(min-width: 768px)" type="image/jpeg"/>
              <source srcset="https://visionghs.github.io//styles/large_landscape/public/2020-01/W140-0024-088.jpg?itok=P6y2H1Dt 1x, /sites/default/files/styles/large_landscape/public/2020-01/W140-0024-088.jpg?itok=P6y2H1Dt 2x" media="(min-width: 480px)" type="image/jpeg"/>
              <source srcset="https://visionghs.github.io//styles/medium_portrait/public/2020-01/W140-0024-088.jpg?itok=3vs9Mbw_ 1x, /sites/default/files/styles/medium_portrait/public/2020-01/W140-0024-088.jpg?itok=3vs9Mbw_ 2x" type="image/jpeg"/>
            <!--[if IE 9]></video><![endif]-->
            <img src="https://visionghs.github.io//styles/medium_portrait/public/2020-01/W140-0024-088.jpg?itok=3vs9Mbw_" alt="Child splashing clean water" typeof="foaf:Image" />

  </picture>

</div>
      
</div>

    </div>
    <div class="hero__content">
      <div class="hero__content--inner">
                  <div class="hero__subtitle">
            Every 60 seconds
          </div>
                          <div class="hero__title">
            a family gets water… a hungry child is fed… a family receives the tools to overcome poverty
          </div>
                                  <a href="/cleanwater" class="btn btn--lg btn--primary--orange">Learn More</a>
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
  <p>3M+</p>

  </div>
      <div class="claim__subtitle">
  Children Sponsored
  </div>
      <a href="/child-sponsorship" class="btn btn--secondary--blue">learn more</a>
  </div>
        <div class="eck-entity component-claim">
    <div class="claim__title">
  <p>3.2M</p>

  </div>
      <div class="claim__subtitle">
  People Gained Clean Water
  </div>
      <a href="/cleanwater" class="btn btn--secondary--blue">learn more</a>
  </div>
        <div class="eck-entity component-claim">
    <div class="claim__title">
  <p>170</p>

  </div>
      <div class="claim__subtitle">
  Emergency Responses
  </div>
      <a href="/get-involved/emergencies" class="btn btn--secondary--blue">learn more</a>
  </div>
  
    </div>
          <div class="container__footer"><p><em>*Facts and figures based on 2017 data</em></p></div>
        
  </div>
</div>

        
  <div class="eck-entity component--view component--view--locations">
          <div class="view__header"><h2>37,000+ staff in nearly 100 countries.</h2></div>
        <div class="view__content">
      <div class="views-element-container"><div class="js-view-dom-id-8e368c99890fc2c6d615cb057996bb97b3d3fab910830b5dcc1887b047d90ff0 views-view--locations views-view--locations--maps_common" data-dom-id="8e368c99890fc2c6d615cb057996bb97b3d3fab910830b5dcc1887b047d90ff0">
  
  
  

      <header>
      <span class="legend legend--global-center">Global Centre</span><span class="legend legend--field-office">Field Office</span><span class="legend legend--support-office">Support Office</span>
    </header>
  
  
  

  <div id="8e368c99890fc2c6d615cb057996bb97b3d3fab910830b5dcc1887b047d90ff0" class="geolocation-common-map"    data-centre-lat="29.161669" data-centre-lng="19.456068"   >
    <div class="geolocation-common-map-locations">
            <div
    class="geolocation"
    data-lat="34.352865"
    data-lng="62.2040287"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="34.352865" />
        <meta property="longitude" content="62.2040287" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Afghanistan</h4>
  <p class="map__year_est">Office Est. 2001</p>
  <a href="/afghanistan" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="41.3275459"
    data-lng="19.8186982"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="41.3275459" />
        <meta property="longitude" content="19.8186982" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Albania</h4>
  <p class="map__year_est">Office Est. 1999</p>
  <a href="/albania" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-8.823681"
    data-lng="13.239291"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-8.823681" />
        <meta property="longitude" content="13.239291" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Angola</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="/angola" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="40.1791857"
    data-lng="44.4991029"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="40.1791857" />
        <meta property="longitude" content="44.4991029" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Armenia</h4>
  <p class="map__year_est">Office Est. 1988</p>
  <a href="/armenia" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-37.852"
    data-lng="145.15"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-37.852" />
        <meta property="longitude" content="145.15" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Australia</h4>
  <p class="map__year_est">Office Est. 1966</p>
  <a href="https://www.worldvision.com.au/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="48.2081743"
    data-lng="16.3738189"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="48.2081743" />
        <meta property="longitude" content="16.3738189" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Austria</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://www.worldvision.at/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="23.810332"
    data-lng="90.4125181"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="23.810332" />
        <meta property="longitude" content="90.4125181" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Bangladesh</h4>
  <p class="map__year_est">Office Est. 1970</p>
  <a href="/bangladesh" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-16.489689"
    data-lng="-68.1192936"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-16.489689" />
        <meta property="longitude" content="-68.1192936" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Bolivia</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://www.worldvision.bo/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="43.8562586"
    data-lng="18.4130763"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="43.8562586" />
        <meta property="longitude" content="18.4130763" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Bosnia and Herzegovina</h4>
  <p class="map__year_est">Office Est. 1994</p>
  <a href="/bosnia-and-herzegovina" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-23.6026684"
    data-lng="-46.9194693"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-23.6026684" />
        <meta property="longitude" content="-46.9194693" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Brazil</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://visaomundial.org/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-2.8521841"
    data-lng="30.2209801"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-2.8521841" />
        <meta property="longitude" content="30.2209801" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Burundi</h4>
  <p class="map__year_est">Office Est. 1963</p>
  <a href="/burundi" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="11.5563738"
    data-lng="104.9282099"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="11.5563738" />
        <meta property="longitude" content="104.9282099" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Cambodia</h4>
  <p class="map__year_est">Office Est. 1970</p>
  <a href="/cambodia" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="43.5890452"
    data-lng="-79.6441198"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="43.5890452" />
        <meta property="longitude" content="-79.6441198" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Canada</h4>
  <p class="map__year_est">Office Est. 1957</p>
  <a href="https://www.worldvision.ca/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="12.1348457"
    data-lng="15.0557415"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="12.1348457" />
        <meta property="longitude" content="15.0557415" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Chad</h4>
  <p class="map__year_est">Office Est. 1984</p>
  <a href="/chad" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-33.4314474"
    data-lng="-70.6093325"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-33.4314474" />
        <meta property="longitude" content="-70.6093325" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Chile</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://www.worldvision.cl/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="22.3185673"
    data-lng="114.1796057"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="22.3185673" />
        <meta property="longitude" content="114.1796057" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">China</h4>
  <p class="map__year_est">Office Est. 1993</p>
  <a href="http://www.worldvision.org.cn/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="4.7109886"
    data-lng="-74.072092"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="4.7109886" />
        <meta property="longitude" content="-74.072092" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Colombia</h4>
  <p class="map__year_est">Office Est. 1978</p>
  <a href="https://www.worldvision.co/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-4.4419311"
    data-lng="15.2662931"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-4.4419311" />
        <meta property="longitude" content="15.2662931" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Congo (DRC)</h4>
  <p class="map__year_est">Office Est. 1984</p>
  <a href="/congo-drc" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="9.935177"
    data-lng="-84.0914663"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="9.935177" />
        <meta property="longitude" content="-84.0914663" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Costa Rica</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://www.worldvision.cr/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="18.4671703"
    data-lng="-69.9014878"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="18.4671703" />
        <meta property="longitude" content="-69.9014878" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Dominican Republic</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://www.worldvision.org.do/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-0.169162"
    data-lng="-78.4858497"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-0.169162" />
        <meta property="longitude" content="-78.4858497" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Ecuador</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://www.worldvision.org.ec/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="13.7078654"
    data-lng="-89.2213008"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="13.7078654" />
        <meta property="longitude" content="-89.2213008" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">El Salvador</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://www.worldvision.org.sv" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-26.3195625"
    data-lng="31.1346875"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-26.3195625" />
        <meta property="longitude" content="31.1346875" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Eswatini</h4>
  <p class="map__year_est">Office Est. 1992</p>
  <a href="/eswatini" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="8.9806034"
    data-lng="38.7577605"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="8.9806034" />
        <meta property="longitude" content="38.7577605" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Ethiopia</h4>
  <p class="map__year_est">Office Est. 1975</p>
  <a href="https://visionghs.github.io//ethiopia" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="60.166523"
    data-lng="24.9310077"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="60.166523" />
        <meta property="longitude" content="24.9310077" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Finland</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="http://www.worldvision.fi/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="48.8722656"
    data-lng="2.3461268"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="48.8722656" />
        <meta property="longitude" content="2.3461268" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">France</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="http://visiondumonde.fr" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="41.7069435"
    data-lng="44.7998639"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="41.7069435" />
        <meta property="longitude" content="44.7998639" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Georgia</h4>
  <p class="map__year_est">Office Est. 1996</p>
  <a href="https://visionghs.github.io//georgia" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="50.2536284"
    data-lng="8.646389"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="50.2536284" />
        <meta property="longitude" content="8.646389" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Germany</h4>
  <p class="map__year_est">Office Est. 1979</p>
  <a href="https://www.worldvision.de/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="5.5883948"
    data-lng="-0.2295751"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="5.5883948" />
        <meta property="longitude" content="-0.2295751" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Ghana</h4>
  <p class="map__year_est">Office Est. 1979</p>
  <a href="https://visionghs.github.io//ghana" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="51.510946"
    data-lng="-0.445826"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_global_center.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="51.510946" />
        <meta property="longitude" content="-0.445826" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Global Centre</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="/contact-us" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="14.6046032"
    data-lng="-90.5474496"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="14.6046032" />
        <meta property="longitude" content="-90.5474496" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Guatemala</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://www.worldvision.org.gt/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="18.5201751"
    data-lng="-72.3022522"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="18.5201751" />
        <meta property="longitude" content="-72.3022522" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Haiti</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://visionghs.github.io//haiti" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="14.1003926"
    data-lng="-87.179182"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="14.1003926" />
        <meta property="longitude" content="-87.179182" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Honduras</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://visionghs.github.io//index.jsp" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="22.320235"
    data-lng="114.1648827"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="22.320235" />
        <meta property="longitude" content="114.1648827" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Hong Kong</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="http://www.worldvision.org.hk/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="13.0768734"
    data-lng="80.2107313"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="13.0768734" />
        <meta property="longitude" content="80.2107313" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">India</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://www.worldvision.in/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-6.2637017"
    data-lng="106.6877139"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-6.2637017" />
        <meta property="longitude" content="106.6877139" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Indonesia</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="http://www.wahanavisi.org/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="36.1920098"
    data-lng="43.972435"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="36.1920098" />
        <meta property="longitude" content="43.972435" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Iraq</h4>
  <p class="map__year_est">Office Est. 2014</p>
  <a href="https://visionghs.github.io//iraq" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="53.319255"
    data-lng="-6.266809"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="53.319255" />
        <meta property="longitude" content="-6.266809" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Ireland</h4>
  <p class="map__year_est">Office Est. 1983</p>
  <a href="https://www.worldvision.ie/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="41.9264885"
    data-lng="12.5140514"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="41.9264885" />
        <meta property="longitude" content="12.5140514" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Italy</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://www.worldvision.it/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="35.6961878"
    data-lng="139.6833108"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="35.6961878" />
        <meta property="longitude" content="139.6833108" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Japan</h4>
  <p class="map__year_est">Office Est. 1987</p>
  <a href="https://www.worldvision.jp/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="31.7867012"
    data-lng="35.2495524"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="31.7867012" />
        <meta property="longitude" content="35.2495524" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Jerusalem West Bank Gaza</h4>
  <p class="map__year_est">Office Est. 1975</p>
  <a href="/jerusalem-west-bank-gaza" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="31.9664395"
    data-lng="35.933591"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="31.9664395" />
        <meta property="longitude" content="35.933591" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Jordan</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://visionghs.github.io//emergencies/syria-crisis-response" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-1.3466735"
    data-lng="36.7142064"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-1.3466735" />
        <meta property="longitude" content="36.7142064" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Kenya</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://visionghs.github.io//kenya" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="42.6573916"
    data-lng="21.1557596"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="42.6573916" />
        <meta property="longitude" content="21.1557596" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Kosovo</h4>
  <p class="map__year_est">Office Est. 1998</p>
  <a href="https://visionghs.github.io//kosovo/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="17.9757058"
    data-lng="102.6331035"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="17.9757058" />
        <meta property="longitude" content="102.6331035" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Laos</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://visionghs.github.io//laos" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="33.869778"
    data-lng="35.6080854"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="33.869778" />
        <meta property="longitude" content="35.6080854" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Lebanon</h4>
  <p class="map__year_est">Office Est. 1975</p>
  <a href="https://visionghs.github.io//lebanon" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-29.3047835"
    data-lng="27.4761934"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-29.3047835" />
        <meta property="longitude" content="27.4761934" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Lesotho</h4>
  <p class="map__year_est">Office Est. 1987</p>
  <a href="https://visionghs.github.io//lesotho" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-13.9738318"
    data-lng="33.7566994"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-13.9738318" />
        <meta property="longitude" content="33.7566994" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Malawi</h4>
  <p class="map__year_est">Office Est. 1982</p>
  <a href="https://visionghs.github.io//malawi" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="3.103959"
    data-lng="101.5970884"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="3.103959" />
        <meta property="longitude" content="101.5970884" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Malaysia</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://www.worldvision.com.my/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="12.6195385"
    data-lng="-7.9947117"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="12.6195385" />
        <meta property="longitude" content="-7.9947117" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Mali</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="/mali" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="18.0735299"
    data-lng="-15.9582372"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="18.0735299" />
        <meta property="longitude" content="-15.9582372" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Mauritania</h4>
  <p class="map__year_est">Office Est. 1983</p>
  <a href="https://visionghs.github.io//mauritania" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="19.434852"
    data-lng="-99.1729596"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="19.434852" />
        <meta property="longitude" content="-99.1729596" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Mexico</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://www.worldvisionmexico.org.mx/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="47.8863988"
    data-lng="106.9057439"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="47.8863988" />
        <meta property="longitude" content="106.9057439" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Mongolia</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://worldvision.mn/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-25.9621875"
    data-lng="32.5846875"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-25.9621875" />
        <meta property="longitude" content="32.5846875" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Mozambique</h4>
  <p class="map__year_est">Office Est. 1983</p>
  <a href="/mozambique" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="16.8658125"
    data-lng="96.1415625"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="16.8658125" />
        <meta property="longitude" content="96.1415625" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Myanmar</h4>
  <p class="map__year_est">Office Est. 1991</p>
  <a href="/myanmar" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="27.7138659"
    data-lng="85.3132179"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="27.7138659" />
        <meta property="longitude" content="85.3132179" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Nepal</h4>
  <p class="map__year_est">Office Est. 2001</p>
  <a href="/nepal" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="52.1524231"
    data-lng="5.3843146"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="52.1524231" />
        <meta property="longitude" content="5.3843146" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Netherlands</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://www.worldvision.nl/nl" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-36.9211343"
    data-lng="174.8205483"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-36.9211343" />
        <meta property="longitude" content="174.8205483" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">New Zealand</h4>
  <p class="map__year_est">Office Est. 1970</p>
  <a href="https://www.worldvision.org.nz/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="12.1398397"
    data-lng="-86.2806064"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="12.1398397" />
        <meta property="longitude" content="-86.2806064" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Nicaragua</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="http://www.worldvision.org.ni/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="14.0035625"
    data-lng="0.7583125"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="14.0035625" />
        <meta property="longitude" content="0.7583125" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Niger</h4>
  <p class="map__year_est">Office Est. 1994</p>
  <a href="https://visionghs.github.io//niger" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="39.0392193"
    data-lng="125.7625241"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="39.0392193" />
        <meta property="longitude" content="125.7625241" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">North Korea</h4>
  <p class="map__year_est">Office Est. 1994</p>
  <a href="https://visionghs.github.io//north-korea" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-9.4535093"
    data-lng="147.1943931"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-9.4535093" />
        <meta property="longitude" content="147.1943931" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Papua New Guinea</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://visionghs.github.io//papua-new-guinea" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-12.0825915"
    data-lng="-77.0489192"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-12.0825915" />
        <meta property="longitude" content="-77.0489192" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Peru</h4>
  <p class="map__year_est">Office Est. 1981</p>
  <a href="http://www.visionmundial.org.pe/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="14.6383237"
    data-lng="121.0275022"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="14.6383237" />
        <meta property="longitude" content="121.0275022" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Philippines</h4>
  <p class="map__year_est">Office Est. 1960</p>
  <a href="https://www.worldvision.org.ph/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="44.4635385"
    data-lng="26.0585529"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="44.4635385" />
        <meta property="longitude" content="26.0585529" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Romania</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://visionghs.github.io//romania" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-1.9409756"
    data-lng="30.0795103"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-1.9409756" />
        <meta property="longitude" content="30.0795103" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Rwanda</h4>
  <p class="map__year_est">Office Est. 1994</p>
  <a href="/rwanda" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="14.7309507"
    data-lng="-17.4729153"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="14.7309507" />
        <meta property="longitude" content="-17.4729153" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Senegal</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="/senegal" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="44.786568"
    data-lng="20.4489216"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="44.786568" />
        <meta property="longitude" content="20.4489216" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Serbia</h4>
  <p class="map__year_est">Office Est. 2015</p>
  <a href="https://visionghs.github.io//serbia" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="8.4656765"
    data-lng="-13.2317225"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="8.4656765" />
        <meta property="longitude" content="-13.2317225" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Sierra Leone</h4>
  <p class="map__year_est">Office Est. 1996</p>
  <a href="/sierra-leone" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="1.3291832"
    data-lng="103.8750262"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="1.3291832" />
        <meta property="longitude" content="103.8750262" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Singapore</h4>
  <p class="map__year_est">Office Est. 1983</p>
  <a href="https://www.worldvision.org.sg/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-9.4343125"
    data-lng="159.9640625"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-9.4343125" />
        <meta property="longitude" content="159.9640625" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Solomon Islands</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://visionghs.github.io//solomon-islands" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="2.1187375"
    data-lng="45.3369459"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="2.1187375" />
        <meta property="longitude" content="45.3369459" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Somalia</h4>
  <p class="map__year_est">Office Est. 1993</p>
  <a href="https://visionghs.github.io//somalia" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-26.0980855"
    data-lng="27.9993258"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-26.0980855" />
        <meta property="longitude" content="27.9993258" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">South Africa</h4>
  <p class="map__year_est">Office Est. 1967</p>
  <a href="https://www.worldvision.co.za/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="37.5243535"
    data-lng="126.9271369"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="37.5243535" />
        <meta property="longitude" content="126.9271369" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">South Korea</h4>
  <p class="map__year_est">Office Est. 1954</p>
  <a href="http://www.worldvision.or.kr/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="4.859363"
    data-lng="31.57125"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="4.859363" />
        <meta property="longitude" content="31.57125" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">South Sudan</h4>
  <p class="map__year_est">Office Est. 1989</p>
  <a href="/south-sudan" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="40.4465402"
    data-lng="-3.7021787"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="40.4465402" />
        <meta property="longitude" content="-3.7021787" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Spain</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="http://www.worldvision.es/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="6.9385188"
    data-lng="79.878245"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="6.9385188" />
        <meta property="longitude" content="79.878245" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Sri Lanka</h4>
  <p class="map__year_est">Office Est. 1977</p>
  <a href="https://visionghs.github.io//srilanka" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="15.5726513"
    data-lng="32.5484845"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="15.5726513" />
        <meta property="longitude" content="32.5484845" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Sudan</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="/sudan" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="47.4026861"
    data-lng="8.6163092"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="47.4026861" />
        <meta property="longitude" content="8.6163092" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Switzerland</h4>
  <p class="map__year_est">Office Est. 1982</p>
  <a href="https://www.worldvision.ch/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="25.0541591"
    data-lng="121.5638621"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="25.0541591" />
        <meta property="longitude" content="121.5638621" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Taiwan</h4>
  <p class="map__year_est">Office Est. 1964</p>
  <a href="https://www.worldvision.org.tw/index.php" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-6.7720403"
    data-lng="39.2565143"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-6.7720403" />
        <meta property="longitude" content="39.2565143" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Tanzania</h4>
  <p class="map__year_est">Office Est. 1981</p>
  <a href="https://visionghs.github.io//tanzania" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="13.769569"
    data-lng="100.591999"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="13.769569" />
        <meta property="longitude" content="100.591999" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Thailand</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="http://www.worldvision.or.th/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-8.5484375"
    data-lng="125.5896875"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-8.5484375" />
        <meta property="longitude" content="125.5896875" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Timor-Leste</h4>
  <p class="map__year_est">Office Est. 1999</p>
  <a href="https://visionghs.github.io//timor-leste/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="0.3204375"
    data-lng="32.5759375"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="0.3204375" />
        <meta property="longitude" content="32.5759375" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Uganda</h4>
  <p class="map__year_est">Office Est. 1986</p>
  <a href="https://visionghs.github.io//uganda" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="52.0502118"
    data-lng="-0.7079478"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="52.0502118" />
        <meta property="longitude" content="-0.7079478" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">United Kingdom</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://www.worldvision.org.uk/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="47.28949"
    data-lng="-122.2912115"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_support_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="47.28949" />
        <meta property="longitude" content="-122.2912115" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">United States</h4>
  <p class="map__year_est">Office Est. </p>
  <a href="https://www.worldvision.org/" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-17.7455625"
    data-lng="168.3183125"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-17.7455625" />
        <meta property="longitude" content="168.3183125" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Vanuatu</h4>
  <p class="map__year_est">Office Est.  1980</p>
  <a href="https://visionghs.github.io//vanuatu" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="21.0441142"
    data-lng="105.81394"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="21.0441142" />
        <meta property="longitude" content="105.81394" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Vietnam</h4>
  <p class="map__year_est">Office Est. 1990</p>
  <a href="https://visionghs.github.io//vietnam" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-15.4070625"
    data-lng="28.2861875"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-15.4070625" />
        <meta property="longitude" content="28.2861875" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Zambia</h4>
  <p class="map__year_est">Office Est. 1981</p>
  <a href="/zambia" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
            <div
    class="geolocation"
    data-lat="-17.7672324"
    data-lng="31.0478433"
    typeof="Place"
                data-set-marker="true"
         data-icon="https://visionghs.github.io//themes/custom/wvi_2018/images/markers/wvi_marker_field_office.png"             >
    <span property="geo" typeof="GeoCoordinates">
        <meta property="latitude" content="-17.7672324" />
        <meta property="longitude" content="31.0478433" />
    </span>
    <h2 class="location-title" property="name"></h2>
    <div class="location-content"><div class="views-field views-field-nothing"><span class="field-content"><div class="map__infowindow">
  <h4 class="map__title">Zimbabwe</h4>
  <p class="map__year_est">Office Est. 1973</p>
  <a href="/zimbabwe" class="btn--secondary--blue">Visit Site</a>
</div></span></div></div>
</div>
        </div>
    <div class="geolocation-common-map-container"></div>
</div>

  
  

  
  
  

  
</div>
</div>

    </div>
  </div>

        <div class="eck-entity component-cta background-color-white accent-color-orange image-align-right layout-card">
  <div class="cta__image"><div>
  
  
            <div class="field field--name-field-media-image field--type-image field--label-hidden">  <img src="https://visionghs.github.io//2020-03/Na_Hang_3_Medium_res_0.jpg" alt="COVID-19-Masks" typeof="foaf:Image" />

</div>
      
</div>
</div>
  <div class="cta__content">
    <div class="cta__content--inner">
    <div class="cta__icon"></div>
              <h3 class="cta__title">
        <p>COVID-19 and Children:</p>

        </h3>
                    <div class="cta__subtitle">
        We can do this!
        </div>
                    <div class="cta__description">
        
            <div class="field field--name-field-component-description field--type-text-long field--label-hidden"><p>How is the coronavirus affecting children so far? Who is at the greatest risk? And, what each of us can do to help protect our loved ones? Find out here. </p></div>
      
        </div>
                    <div class="cta__btns">
          <a href="https://visionghs.github.io//stories/coronavirus-health-crisis/covid-19-and-children-we-can-do" class="cta__btn">Learn More</a>
        </div>
          </div>
  </div>
</div>

        <div class="eck-entity component--container container--icon not-slider">
  <div class="container--inner">
          <h2 class="container__title">Every 60 seconds a family receives the tools to overcome poverty</h2>
              <div class="container__header"><p class="text--emphasis"><a href="/our-work">How we do it </a></p></div>
        <div class="container__components ">
            <div  class="eck-entity component-icon">
    <a class="icon__wrapper" href="/child-protection">
      <div class="icon__image">  <img src="https://visionghs.github.io//icon/icon/Asset%202.svg" alt="Child protection icon" typeof="foaf:Image" />

</div>
    <div class="icon__subtitle">Child Protection</div>
    </a>
  </div>

        <div  class="eck-entity component-icon">
    <a class="icon__wrapper" href="/disaster-management">
      <div class="icon__image">  <img src="https://visionghs.github.io//icon/icon/Disaster%20Management%20Icon.svg" alt="Disaster Management Icon" typeof="foaf:Image" />

</div>
    <div class="icon__subtitle">Disaster Management</div>
    </a>
  </div>

        <div  class="eck-entity component-icon">
    <a class="icon__wrapper" href="/education">
      <div class="icon__image">  <img src="https://visionghs.github.io//icon/icon/Education%20Icon.svg" alt="Education icon" typeof="foaf:Image" />

</div>
    <div class="icon__subtitle">Education</div>
    </a>
  </div>

        <div  class="eck-entity component-icon">
    <a class="icon__wrapper" href="/health">
      <div class="icon__image">  <img src="https://visionghs.github.io//icon/icon/Health%20Icon.svg" alt="Health Icon" typeof="foaf:Image" />

</div>
    <div class="icon__subtitle">Health</div>
    </a>
  </div>

        <div  class="eck-entity component-icon">
    <a class="icon__wrapper" href="/faith-and-development">
      <div class="icon__image">  <img src="https://visionghs.github.io//icon/icon/Faith%20Icon_0.svg" alt="Faith and Development icon" typeof="foaf:Image" />

</div>
    <div class="icon__subtitle">Faith &amp; Development</div>
    </a>
  </div>

        <div  class="eck-entity component-icon">
    <a class="icon__wrapper" href="/nutrition">
      <div class="icon__image">  <img src="https://visionghs.github.io//icon/icon/Nutrition%20Icon.svg" alt="Nutrition Icon" typeof="foaf:Image" />

</div>
    <div class="icon__subtitle">Nutrition</div>
    </a>
  </div>

        <div  class="eck-entity component-icon">
    <a class="icon__wrapper" href="/economic-development">
      <div class="icon__image">  <img src="https://visionghs.github.io//icon/icon/Economic%20Development.svg" alt="Economic Development Icon" typeof="foaf:Image" />

</div>
    <div class="icon__subtitle">Economic Development</div>
    </a>
  </div>

        <div  class="eck-entity component-icon">
    <a class="icon__wrapper" href="/cleanwater">
      <div class="icon__image">  <img src="https://visionghs.github.io//icon/icon/Water%20Icon.svg" alt="Water Icon" typeof="foaf:Image" />

</div>
    <div class="icon__subtitle">Water</div>
    </a>
  </div>

  
    </div>
          <div class="container__footer"><p><a class="btn--primary--orange" href="/all-sectors">SEE ALL</a></p></div>
        
  </div>
</div>

        <div class="eck-entity component--media background-color-white accent-color-orange single-item">
    
            <div class="field field--name-field-component-heading field--type-text-long field--label-hidden"><p><strong>Meet Nancy</strong></p>

<p>With the help of child sponsorship, Nancy became one of the first girls in her community to graduate high school and was inspired to become a humanitarian.</p></div>
      
      <div class="field field--name-field-component-media field--type-entity-reference field--label-hidden">
              <div><div>
  
  
            <div class="field field--name-field-media-oembed-video field--type-string field--label-hidden"><iframe src="/media/oembed?url=https%3A//www.youtube.com/watch%3Fv%3DRR6doOwK2wc&amp;max_width=0&amp;max_height=0&amp;hash=9gLU7b7g0n8rDjG_jELeWcsixSdjf18eg9izOoCQ6KI" frameborder="0" allowtransparency width="480" height="270" class="media-oembed-content" title="The Impact of Child Sponsorship - Meet Nancy (60 sec)"></iframe>
</div>
      
</div>
</div>
          </div>
  
</div>

        <div class="eck-entity component--container container--card js-slider">
  <div class="container--inner">
            <div class="container__slider">
            <div  class="eck-entity component-card">
    <a href="/about-us/our-vision-and-values">
      <div class="card__image"><div>
  
  
            <div class="field field--name-field-media-image field--type-image field--label-hidden">    <picture>
                <!--[if IE 9]><video style="display: none;"><![endif]-->
              <source srcset="https://visionghs.github.io//styles/extra_large_landscape/public/2019-03/BAIV1887-site.jpg?itok=2UL2FgfB 1x" media="(min-width: 960px)" type="image/jpeg"/>
              <source srcset="https://visionghs.github.io//styles/large_landscape/public/2019-03/BAIV1887-site.jpg?itok=4ISjY0r8 1x" media="(min-width: 768px)" type="image/jpeg"/>
              <source srcset="https://visionghs.github.io//styles/medium_landscape/public/2019-03/BAIV1887-site.jpg?itok=wS_AVd-- 1x" type="image/jpeg"/>
            <!--[if IE 9]></video><![endif]-->
            <img src="https://visionghs.github.io//styles/medium_landscape/public/2019-03/BAIV1887-site.jpg?itok=wS_AVd--" alt="A group of happy and smiling school children in Ghana" typeof="foaf:Image" />

  </picture>

</div>
      
</div>
</div>
    <div class="card__content">
            <div class="card__subtitle">
      Featured
      </div>
                  <div class="card__title">
      A Life of Fullness for Every Child
      </div>
                  <div class="card__description">
      
            <div class="field field--name-field-component-description field--type-text-long field--label-hidden"><p dir="ltr">We look forward to a world where every child experiences Jesus' promise of life in all its fullness. Where they are protected, cared for and given the...</p></div>
      
      </div>
                  <span class="card__btn">Learn More </span>
          </div>
    </a>
  </div>

        <div  class="eck-entity component-card">
    <a href="/our-history">
      <div class="card__image"><div>
  
  
            <div class="field field--name-field-media-image field--type-image field--label-hidden">    <picture>
                <!--[if IE 9]><video style="display: none;"><![endif]-->
              <source srcset="https://visionghs.github.io//styles/extra_large_landscape/public/2019-03/Sea%20Sweep_3.jpg?itok=M0YXSBha 1x" media="(min-width: 960px)" type="image/jpeg"/>
              <source srcset="https://visionghs.github.io//styles/large_landscape/public/2019-03/Sea%20Sweep_3.jpg?itok=1zEGzLmk 1x" media="(min-width: 768px)" type="image/jpeg"/>
              <source srcset="https://visionghs.github.io//styles/medium_landscape/public/2019-03/Sea%20Sweep_3.jpg?itok=vm8GtxYZ 1x" type="image/jpeg"/>
            <!--[if IE 9]></video><![endif]-->
            <img src="https://visionghs.github.io//styles/medium_landscape/public/2019-03/Sea%20Sweep_3.jpg?itok=vm8GtxYZ" alt="Operation Sea Sweep 1979" typeof="foaf:Image" />

  </picture>

</div>
      
</div>
</div>
    <div class="card__content">
                  <div class="card__title">
      Our history of helping children break free of poverty
      </div>
                  <div class="card__description">
      
            <div class="field field--name-field-component-description field--type-text-long field--label-hidden"><p>World Vision has nearly 70 years of experience working with communities, donors, partners, and governments to bring better futures for vulnerable...</p></div>
      
      </div>
                  <span class="card__btn">Learn More</span>
          </div>
    </a>
  </div>

        <div  class="eck-entity component-card">
    <a href="/1000-girls">
      <div class="card__image"><div>
  
  
            <div class="field field--name-field-media-image field--type-image field--label-hidden">    <picture>
                <!--[if IE 9]><video style="display: none;"><![endif]-->
              <source srcset="https://visionghs.github.io//styles/extra_large_landscape/public/2019-09/D165-0799-124.JPG_922094.png?itok=g4Qp8B2D 1x" media="(min-width: 960px)" type="image/png"/>
              <source srcset="https://visionghs.github.io//styles/large_landscape/public/2019-09/D165-0799-124.JPG_922094.png?itok=euT7Cv0z 1x" media="(min-width: 768px)" type="image/png"/>
              <source srcset="https://visionghs.github.io//styles/medium_landscape/public/2019-09/D165-0799-124.JPG_922094.png?itok=AeYBRC4G 1x" type="image/png"/>
            <!--[if IE 9]></video><![endif]-->
            <img src="https://visionghs.github.io//styles/medium_landscape/public/2019-09/D165-0799-124.JPG_922094.png?itok=AeYBRC4G" alt="A group of karate girls in India" typeof="foaf:Image" />

  </picture>

</div>
      
</div>
</div>
    <div class="card__content">
            <div class="card__subtitle">
      1000 Girls
      </div>
                  <div class="card__title">
      Help Empower Girls Across the World
      </div>
                  <div class="card__description">
      
            <div class="field field--name-field-component-description field--type-text-long field--label-hidden"><p>Each year, millions of girls in poverty are kept out of school. Instead, many are forced to stay home and work, while others are made to marry and...</p></div>
      
      </div>
                  <span class="card__btn">Help Set Her Free</span>
          </div>
    </a>
  </div>

  
    </div>
            
  </div>
</div>

        <div class="eck-entity component-cta background-color-offwhite accent-color-green image-align-left layout-card">
  <div class="cta__image"><div>
  
  
            <div class="field field--name-field-media-image field--type-image field--label-hidden">  <img src="https://visionghs.github.io//2019-03/Screen%20Shot%202019-03-25%20at%2010.39.12%20AM.png" alt="Screen Shot 2019-03-25 at 10.39.12 AM.png" typeof="foaf:Image" />

</div>
      
</div>
</div>
  <div class="cta__content">
    <div class="cta__content--inner">
    <div class="cta__icon">  <img src="https://visionghs.github.io//2019-03/Screen%20Shot%202019-03-25%20at%2010.39.06%20AM.png" alt="It takes a world" typeof="foaf:Image" />

</div>
              <h3 class="cta__title">
        <p>It Takes a World</p>

        </h3>
                    <div class="cta__subtitle">
        To end violence against children
        </div>
                    <div class="cta__description">
        
            <div class="field field--name-field-component-description field--type-text-long field--label-hidden"><p>Violence, in all its forms, is the biggest issue affecting children today. But it doesn't have to be this way.</p></div>
      
        </div>
                    <div class="cta__btns">
          <a href="/ittakesaworld" class="cta__btn">Learn More</a>
        </div>
          </div>
  </div>
</div>

          <div class="eck-entity component-cta background-color-orange accent-color-orange image-align-left layout-full-width same-color">
  <div class="cta__image"><div>
  
  
            <div class="field field--name-field-media-image field--type-image field--label-hidden">  <img src="https://visionghs.github.io//2019-03/Screen%20Shot%202019-03-25%20at%2010.42.29%20AM.png" alt="Screen Shot 2019-03-25 at 10.42.29 AM.png" typeof="foaf:Image" />

</div>
      
</div>
</div>
  <div class="cta__content">
    <div class="cta__content--inner">
    <div class="cta__icon"></div>
              <h3 class="cta__title">
        <p>Together we&#039;ve impacted the lives of over 200 million vulnerable children by tackling the root causes of poverty.</p>

        </h3>
                                <div class="cta__btns">
          <a href="/our-impact" class="cta__btn">Learn More </a>
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
        <a href="/about-us" data-drupal-link-system-path="node/72551">About Us</a>
                                <ul>
                    <li class="menu-item--our-vision--values">
        <a href="/our-vision-and-values">Our Vision &amp; Values</a>
              </li>
                <li class="menu-item--our-history">
        <a href="/our-history" data-drupal-link-system-path="node/72646">Our History</a>
              </li>
                <li class="menu-item--our-leadership">
        <a href="/our-leadership">Our Leadership</a>
              </li>
                <li class="menu-item--our-structure">
        <a href="/our-structure">Our Structure</a>
              </li>
                <li class="menu-item--our-partners">
        <a href="/our-partners" data-drupal-link-system-path="group/1026">Our Partners</a>
              </li>
                <li class="menu-item--accountability">
        <a href="/accountability" data-drupal-link-system-path="node/72741">Accountability</a>
              </li>
                <li class="menu-item--faq">
        <a href="/faq">FAQ</a>
              </li>
        </ul>
  
              </li>
                <li class="menu-item--our-approaches-to-change menu-item--expandable">
        <a href="/our-approaches" data-drupal-link-system-path="node/72731">Our Approaches to Change</a>
                                <ul>
                    <li class="menu-item--our-global-strategy">
        <a href="/our-promise" data-drupal-link-system-path="node/72696">Our Global Strategy</a>
              </li>
                <li class="menu-item--the-role-of-faith">
        <a href="/role-faith" data-drupal-link-system-path="node/72726">The Role of Faith</a>
              </li>
                <li class="menu-item--global-campaign">
        <a href="/ittakesaworld" data-drupal-link-system-path="group/1">Global Campaign</a>
              </li>
                <li class="menu-item--work-in-fragile-places">
        <a href="/fragile-context">Work in Fragile Places</a>
              </li>
        </ul>
  
              </li>
                <li class="menu-item--careers--internships menu-item--expandable">
        <a href="https://careers.wvi.org/">Careers &amp; Internships</a>
                                <ul>
                    <li class="menu-item--open-positions">
        <a href="https://careers.wvi.org/job-search">Open Positions</a>
              </li>
                <li class="menu-item--explore-teams">
        <a href="https://careers.wvi.org/teams">Explore Teams</a>
              </li>
                <li class="menu-item--explore-locations">
        <a href="https://careers.wvi.org/locations">Explore Locations</a>
              </li>
                <li class="menu-item--our-culture">
        <a href="https://careers.wvi.org/culture">Our Culture</a>
              </li>
        </ul>
  
              </li>
                <li class="menu-item--connect-with-us menu-item--expandable">
        <a href="/contact-us" data-drupal-link-system-path="node/72846">Connect With Us</a>
                                <ul>
                    <li class="menu-item--facebook">
        <a href="https://www.facebook.com/WorldVisionInternational" class="facebook-link" target="_blank">Facebook</a>
              </li>
                <li class="menu-item--youtube">
        <a href="https://www.youtube.com/user/WorldVisionStory" class="youtube-link" target="_blank">Youtube</a>
              </li>
                <li class="menu-item--twitter">
        <a href="https://twitter.com/WorldVision" class="twitter-link" target="_blank">Twitter</a>
              </li>
                <li class="menu-item--instagram">
        <a href="https://www.instagram.com/worldvision" class="instagram-link" target="_blank">Instagram</a>
              </li>
                <li class="menu-item--linkedin">
        <a href="https://www.linkedin.com/company/worldvision/" class="linkedin-link" target="_blank">LinkedIn</a>
              </li>
                <li class="menu-item--contact-us">
        <a href="/contact-us" data-drupal-link-system-path="node/72846">Contact Us</a>
              </li>
                <li class="menu-item--world-vision-in-your-country">
        <a href="/locations" data-drupal-link-system-path="node/72811">World Vision in Your Country</a>
              </li>
                <li class="menu-item--report-a-concern">
        <a href="http://worldvision.ethicspoint.com">Report a Concern</a>
              </li>
        </ul>
  
              </li>
        </ul>
  


  </nav>
<div class="mailchimp-signup-subscribe-form block block-mailchimp-signup block-mailchimp-signup-subscribe-blockget-our-newsletter block--mailchimpsubscriptionformgetournewsletter" data-drupal-selector="mailchimp-signup-subscribe-block-get-our-newsletter-form" id="block-mailchimpsubscriptionformgetournewsletter">
  
      <h4 class="block__title">Get Our Newsletter</h4>
    
      <form action="/" method="post" id="mailchimp-signup-subscribe-block-get-our-newsletter-form" accept-charset="UTF-8">
  <div>
  <div id="mailchimp-newsletter-805c2c8c67-mergefields" class="mailchimp-newsletter-mergefields"><div class="js-form-item form-item js-form-type-email form-item-mergevars-email js-form-item-mergevars-email form-no-label">
      <label for="edit-mergevars-email" class="visually-hidden js-form-required form-required">Email Address</label>
        <input data-drupal-selector="edit-mergevars-email" type="email" id="edit-mergevars-email" name="mergevars[EMAIL]" value="" size="25" maxlength="254" placeholder="Email Address" class="form-email required" required="required" aria-required="true" />

        </div>
<div class="js-form-item form-item js-form-type-checkbox form-item-mergevars-terms js-form-item-mergevars-terms">
        <input data-drupal-selector="edit-mergevars-terms" type="checkbox" id="edit-mergevars-terms" name="mergevars[terms]" value="1" class="form-checkbox required" required="required" aria-required="true" />

        <label for="edit-mergevars-terms" class="option js-form-required form-required">I agree to <a href="/terms">WVI's Terms & Conditions</a>.</label>
      </div>
<a class="form-submit-link" href="/"></a></div><input autocomplete="off" data-drupal-selector="form-yhimhatry4avrte0uixowmtnxz5zpl3ygikiwxxfzjo" type="hidden" name="form_build_id" value="form-yhImhaTry4AVrTE0UiXowMtnxz5zpL3ygIkiWXxFZJo" />
<input data-drupal-selector="edit-mailchimp-signup-subscribe-block-get-our-newsletter-form" type="hidden" name="form_id" value="mailchimp_signup_subscribe_block_get_our_newsletter_form" />
<div data-drupal-selector="edit-actions" class="form-actions js-form-wrapper form-wrapper" id="edit-actions"><input data-drupal-selector="edit-submit" type="submit" id="edit-submit" name="op" value="Submit" class="button js-form-submit form-submit" />
</div>

  </div>
</form>

  </div>
<div id="block-accountablenowlogo" class="block block-block-content block-block-contentc32d35ab-86e0-4257-b5df-c684ffe90575 block--accountablenowlogo">
  
    
      
            <div class="field field--name-body field--type-text-with-summary field--label-hidden"><p> </p>

<p><a href="https://accountablenow.org/"><img alt="Accountable Now" data-entity-type="file" data-entity-uuid="fdc87d61-f207-4043-8d97-37814a46bb97" src="https://visionghs.github.io//images/logo--accountable-now_11.png" /></a></p></div>
      
  </div>
<nav role="navigation" aria-labelledby="block-footerlegal-menu" id="block-footerlegal" class="block block-menu navigation menu--footer-legal">
            
  <h2 class="visually-hidden" id="block-footerlegal-menu">Footer Legal</h2>
  

        
              <ul data-region="footer">
          <li class='copyright'>&copy; 2020 World Vision International</li>
          <li>
        <a href="/privacy" data-drupal-link-system-path="node/41736">Privacy Policy</a>
              </li>
          <li>
        <a href="/terms-use" data-drupal-link-system-path="node/45251">Terms of Use</a>
              </li>
        </ul>
  


  </nav>

    </div>
  </div>

</footer>

  </div>

    
    <script type="application/json" data-drupal-selector="drupal-settings-json">{"path":{"baseUrl":"\/","scriptPath":null,"pathPrefix":"","currentPath":"node\/72661","currentPathIsAdmin":false,"isFront":true,"currentLanguage":"en"},"pluralDelimiter":"\u0003","suppressDeprecationErrors":true,"ajaxPageState":{"libraries":"anchor_link\/drupal.anchor_link,core\/html5shiv,core\/picturefill,eu_cookie_compliance\/eu_cookie_compliance_bare,media\/oembed.formatter,system\/base,views\/views.module,wvi_2018\/fonts,wvi_2018\/global-scripts,wvi_2018\/global-styling,wvi_maps\/locations_view","theme":"wvi_2018","theme_token":null},"ajaxTrustedUrl":{"form_action_p_pvdeGsVG5zNF_XLGPTvYSKCf43t8qZYSwcfZl2uzM":true},"eu_cookie_compliance":{"popup_enabled":true,"popup_agreed_enabled":false,"popup_hide_agreed":false,"popup_clicking_confirmation":false,"popup_scrolling_confirmation":false,"popup_html_info":"\u003Cdiv class=\u0022eu-cookie-compliance-banner eu-cookie-compliance-banner-info\u0022\u003E\n  \u003Cdiv class=\u0022popup-content info eu-cookie-compliance-content\u0022\u003E\n    \u003Cdiv id=\u0022popup-text\u0022 class=\u0022eu-cookie-compliance-message\u0022\u003E\n      \u003Cp\u003EThis site uses cookie to store information on your computer. By using this site you agree to our use of cookies. For More information see our \u003Ca href=\u0022\/privacy-policy\u0022\u003EPrivacy Policy\u003C\/a\u003E.\u003C\/p\u003E\n    \u003C\/div\u003E\n    \u003Cdiv id=\u0022popup-buttons\u0022 class=\u0022eu-cookie-compliance-buttons\u0022\u003E\n              \u003Cbutton type=\u0022button\u0022 class=\u0022decline-button eu-cookie-compliance-default-button btn--secondary--orange\u0022 \u003EDeny\u003C\/button\u003E\n            \u003Cbutton type=\u0022button\u0022 class=\u0022agree-button eu-cookie-compliance-secondary-button btn--primary--orange\u0022\u003EAccept\u003C\/button\u003E\n    \u003C\/div\u003E\n  \u003C\/div\u003E\n\u003C\/div\u003E","use_mobile_message":false,"mobile_popup_html_info":"\u003Cdiv class=\u0022eu-cookie-compliance-banner eu-cookie-compliance-banner-info\u0022\u003E\n  \u003Cdiv class=\u0022popup-content info eu-cookie-compliance-content\u0022\u003E\n    \u003Cdiv id=\u0022popup-text\u0022 class=\u0022eu-cookie-compliance-message\u0022\u003E\n      \n    \u003C\/div\u003E\n    \u003Cdiv id=\u0022popup-buttons\u0022 class=\u0022eu-cookie-compliance-buttons\u0022\u003E\n              \u003Cbutton type=\u0022button\u0022 class=\u0022decline-button eu-cookie-compliance-default-button btn--secondary--orange\u0022 \u003EDeny\u003C\/button\u003E\n            \u003Cbutton type=\u0022button\u0022 class=\u0022agree-button eu-cookie-compliance-secondary-button btn--primary--orange\u0022\u003EAccept\u003C\/button\u003E\n    \u003C\/div\u003E\n  \u003C\/div\u003E\n\u003C\/div\u003E","mobile_breakpoint":768,"popup_html_agreed":false,"popup_use_bare_css":true,"popup_height":"auto","popup_width":"100%","popup_delay":1000,"popup_link":"\/privacy-policy","popup_link_new_window":true,"popup_position":false,"fixed_top_position":true,"popup_language":"en","store_consent":false,"better_support_for_screen_readers":false,"cookie_name":"","reload_page":false,"domain":"","domain_all_sites":null,"popup_eu_only_js":false,"cookie_lifetime":100,"cookie_session":0,"disagree_do_not_show_popup":false,"method":"opt_in","whitelisted_cookies":"","withdraw_markup":"\u003Cbutton type=\u0022button\u0022 class=\u0022eu-cookie-withdraw-tab\u0022\u003EPrivacy settings\u003C\/button\u003E\n\u003Cdiv class=\u0022eu-cookie-withdraw-banner\u0022\u003E\n  \u003Cdiv class=\u0022popup-content info eu-cookie-compliance-content\u0022\u003E\n    \u003Cdiv id=\u0022popup-text\u0022 class=\u0022eu-cookie-compliance-message\u0022\u003E\n      \u003Ch2\u003EWe use cookies on this site to enhance your user experience\u003C\/h2\u003E\u003Cp\u003EYou have given your consent for us to set cookies.\u003C\/p\u003E\n    \u003C\/div\u003E\n    \u003Cdiv id=\u0022popup-buttons\u0022 class=\u0022eu-cookie-compliance-buttons\u0022\u003E\n      \u003Cbutton type=\u0022button\u0022 class=\u0022eu-cookie-withdraw-button\u0022\u003EWithdraw consent\u003C\/button\u003E\n    \u003C\/div\u003E\n  \u003C\/div\u003E\n\u003C\/div\u003E","withdraw_enabled":false,"withdraw_button_on_info_popup":null,"cookie_categories":[],"enable_save_preferences_button":null,"fix_first_cookie_category":null,"select_all_categories_by_default":null},"geolocation":{"commonMap":{"8e368c99890fc2c6d615cb057996bb97b3d3fab910830b5dcc1887b047d90ff0":{"settings":{"google_map_settings":{"type":"ROADMAP","zoom":"3","minZoom":0,"maxZoom":4,"rotateControl":0,"mapTypeControl":0,"streetViewControl":0,"zoomControl":1,"fullscreenControl":0,"scrollwheel":0,"disableDoubleClickZoom":0,"draggable":1,"height":"820px","width":"100%","info_auto_display":0,"marker_icon_path":"themes\/custom\/wvi_2018\/images\/markers\/wvi_marker_{{ type }}.png","disableAutoPan":0,"style":[{"featureType":"all","elementType":"labels","stylers":[{"visibility":"off"}]},{"featureType":"administrative","elementType":"geometry.fill","stylers":[{"color":"#fefefe"},{"lightness":20},{"visibility":"off"}]},{"featureType":"administrative","elementType":"geometry.stroke","stylers":[{"color":"#fefefe"},{"lightness":17},{"weight":1.2}]},{"featureType":"administrative","elementType":"labels","stylers":[{"visibility":"off"}]},{"featureType":"administrative.country","elementType":"geometry.stroke","stylers":[{"weight":"0.75"},{"color":"#dadada"},{"lightness":"0"}]},{"featureType":"administrative.province","elementType":"all","stylers":[{"visibility":"off"}]},{"featureType":"administrative.locality","elementType":"all","stylers":[{"visibility":"off"}]},{"featureType":"administrative.neighborhood","elementType":"all","stylers":[{"visibility":"off"}]},{"featureType":"administrative.land_parcel","elementType":"all","stylers":[{"visibility":"off"}]},{"featureType":"landscape","elementType":"geometry","stylers":[{"color":"#dadada"},{"visibility":"on"}]},{"featureType":"poi","elementType":"all","stylers":[{"visibility":"off"}]},{"featureType":"road","elementType":"all","stylers":[{"visibility":"off"}]},{"featureType":"water","elementType":"geometry","stylers":[{"color":"#f8f8f8"},{"lightness":17}]},{"featureType":"water","elementType":"labels","stylers":[{"visibility":"off"}]}],"preferScrollingToZooming":0,"gestureHandling":"cooperative"}}}},"google_map_url":"https:\/\/maps.googleapis.com\/maps\/api\/js?libraries=\u0026region=\u0026language=\u0026v=\u0026client=\u0026callback=Drupal.geolocation.googleCallback\u0026key=AIzaSyA8JO4Fet1f9TI0aW5n2YPs79geVEdUqMk"},"user":{"uid":0,"permissionsHash":"108ffe1feb20c047c66014a7d38f66d93fb5e11491fb28d60f0d65ac7f59da3e"}}</script>
<script src="https://visionghs.github.io//js/js_BAqaKhzdQpF_4bl5P0uflguXHhjaa6x5RJiqg5l-nmo.js"></script>

  <script type="text/javascript">window.NREUM||(NREUM={});NREUM.info={"beacon":"bam.nr-data.net","licenseKey":"006b5744c1","applicationID":"115598855","transactionName":"MVwHZkMDWxBSVhUPDQgWJFFFC1oNHHETExIHVTlxXhBQP3VaEws+IFYXX3MXXA9XUBNLXBRcC1ZUEGUPUlYEDg0KXQBAdw1HDnJWFQ8NCA==","queueTime":0,"applicationTime":311,"atts":"HRsEEAsZSB4=","errorBeacon":"bam.nr-data.net","agent":""}</script></body>
</html>
