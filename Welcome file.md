<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Welcome file</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
  <div class="stackedit__html"><h2 id="problème-1">Problème 1</h2>
<blockquote>
<p>Faut-il corriger ces lignes en : .section:nth-child(1)<br>
{background-image: url();}</p>
</blockquote>
<p>Ok pour nous.</p>
<h2 id="problème-2">Problème 2</h2>
<blockquote>
<p>Si tu mets full screen sur une vidéo puis que tu enlève le full screen<br>
puis que tu vas le faire sur une autre. Parfois ça te remet la<br>
première en full screen au lieu de mettre celle sur laquelle tu as<br>
cliqué.</p>
</blockquote>
<h2 id="html">HTML</h2>
<p><strong>Remplacer dans section-2.php (Ligne 15)</strong></p>
<pre><code>&lt;span class="fullscreenlink" id="fullscreen-2"&gt;&lt;img src="img/icon/full-screen.svg"&gt;Full Screen&lt;/span&gt;
&lt;video id="video-2" class="video-desktop" src="https://d1tfc4v6q01fki.cloudfront.net/static/landing/videos/video-1.mp4" poster="img/video/poster.png" controls autoplay="autoplay" loop intrinsicsize muted data-keepplaying&gt;&lt;/video&gt;
</code></pre>
<p><strong>Remplacer dans section-3.php (Ligne 25)</strong></p>
<pre><code>&lt;span class"fullscreenlink" id="fullscreen-3"&gt;&lt;img src="img/icon/full-screen.svg"&gt;Full Screen&lt;/span&gt;
&lt;video id='video-3' class="video-desktop-3" src="https://d1tfc4v6q01fki.cloudfront.net/static/landing/videos/video-2.mp4" poster="img/video/poster.png" controls autoplay="autoplay" loop intrinsicsize playsinline muted data-keepplaying&gt;&lt;/video&gt;
</code></pre>
<p><strong>Remplacer dans section-4.php (Ligne 35)</strong></p>
<pre><code>&lt;span id="fullscreen-4"&gt;&lt;img src="img/icon/full-screen.svg"&gt;Full Screen&lt;/span&gt;&lt;/a&gt;
&lt;video id="video-4" class="video-desktop-3" src="https://d1tfc4v6q01fki.cloudfront.net/static/landing/videos/video-3.mp4" poster="img/video/poster.png" controls autoplay="autoplay" loop intrinsicsize playsinline muted data-keepplaying&gt;&lt;/video&gt;
</code></pre>
<h2 id="css-mobile">CSS Mobile</h2>
<p><strong>Remplacer dans responsive.css (Ligne 105)</strong></p>
<pre><code>#fullscreen-1, #fullscreen-2, #fullscreen-3, #fullscreen-4  {display: none;}
</code></pre>
<h2 id="css-desktop">CSS Desktop</h2>
<p><strong>Remplacer dans responsive.css (Ligne 585)</strong></p>
<pre><code>#fullscreen-2 {
  position: absolute;
  bottom: 130px;
  margin-left: 44px;
  font-size: 13px;
  display: flex;
  align-items: center;
}

#fullscreen-2 img {
  width: 15px;
  padding-right: 10px;
}

#fullscreen-3 {
  position: absolute;
  bottom: 130px;
  margin-left: 0px;
  font-size: 13px;
  display: flex;
  align-items: center;
}

#fullscreen-3 img {
  width: 15px;
  padding-right: 10px;
}

#fullscreen-4 {
  position: absolute;
  bottom: 130px;
  margin-left: 0px;
  font-size: 13px;
  display: flex;
  align-items: center;
}

#fullscreen-4 img {
  width: 15px;
  padding-right: 10px;
}
</code></pre>
<h2 id="js">JS</h2>
<p><strong>Remplacer dans script.js (Ligne 84)</strong></p>
<pre><code>var element2 = document.getElementById('video-2');
var fullscreen2 = document.getElementById('fullscreen-2');

fullscreen2.addEventListener('click',function(){
    &lt;!--console.log ('it is working'); --&gt;
    if(element2.requestFullscreen){
        element2.requestFullscreen();
    }
    else if (element2.webkitRequestFullscreen){
        element2.webkitRequestFullscreen();
    }
    else if (element2.mozRequestFullScreen){
        element2.mozRequestFullScreen();
    }
    else if (element2.msRequestFullscreen){
        element2.msRequestFullscreen();
    }
});

var element3 = document.getElementById('video-3');
var fullscreen3 = document.getElementById('fullscreen-3');

fullscreen3.addEventListener('click',function(){
    &lt;!--console.log ('it is working'); --&gt;
    if(element3.requestFullscreen){
        element3.requestFullscreen();
    }
    else if (element3.webkitRequestFullscreen){
        element3.webkitRequestFullscreen();
    }
    else if (element3.mozRequestFullScreen){
        element3.mozRequestFullScreen();
    }
    else if (element3.msRequestFullscreen){
        element3.msRequestFullscreen();
    }
});

var element4 = document.getElementById('video-4');
var fullscreen4 = document.getElementById('fullscreen-4');

fullscreen4.addEventListener('click',function(){
    &lt;!--console.log ('it is working'); --&gt;
    if(element4.requestFullscreen){
        element4.requestFullscreen();
    }
    else if (element4.webkitRequestFullscreen){
        element4.webkitRequestFullscreen();
    }
    else if (element4.mozRequestFullScreen){
        element4.mozRequestFullScreen();
    }
    else if (element4.msRequestFullscreen){
        element4.msRequestFullscreen();
    }
});
</code></pre>
<h2 id="problème-3">Problème 3</h2>
<blockquote>
<p>Dans le code de section-2.php, il y a deux éléments video, l’un pour<br>
mobile et l’autre pour desktop. Au niveau de l’affichage pas de problème, mais par contre l’utilisateur charge la vidéo en double même s’ils l’affichent bien qu’une fois.</p>
</blockquote>
</div>
</body>

</html>
