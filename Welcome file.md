## Problème 1

> Faut-il corriger ces lignes en : .section:nth-child(1)
> {background-image: url();}

Ok pour nous.

## Problème 2

> Si tu mets full screen sur une vidéo puis que tu enlève le full screen
> puis que tu vas le faire sur une autre. Parfois ça te remet la
> première en full screen au lieu de mettre celle sur laquelle tu as
> cliqué.

## HTML 

**Remplacer dans section-2.php (Ligne 15)**

    <span class="fullscreenlink" id="fullscreen-2"><img src="img/icon/full-screen.svg">Full Screen</span>
    <video id="video-2" class="video-desktop" src="https://d1tfc4v6q01fki.cloudfront.net/static/landing/videos/video-1.mp4" poster="img/video/poster.png" controls autoplay="autoplay" loop intrinsicsize muted data-keepplaying></video>

**Remplacer dans section-3.php (Ligne 25)**

    <span class"fullscreenlink" id="fullscreen-3"><img src="img/icon/full-screen.svg">Full Screen</span>
    <video id='video-3' class="video-desktop-3" src="https://d1tfc4v6q01fki.cloudfront.net/static/landing/videos/video-2.mp4" poster="img/video/poster.png" controls autoplay="autoplay" loop intrinsicsize playsinline muted data-keepplaying></video>

**Remplacer dans section-4.php (Ligne 35)**

    <span id="fullscreen-4"><img src="img/icon/full-screen.svg">Full Screen</span></a>
    <video id="video-4" class="video-desktop-3" src="https://d1tfc4v6q01fki.cloudfront.net/static/landing/videos/video-3.mp4" poster="img/video/poster.png" controls autoplay="autoplay" loop intrinsicsize playsinline muted data-keepplaying></video>

## CSS Mobile

**Remplacer dans responsive.css (Ligne 105)**  

    #fullscreen-1, #fullscreen-2, #fullscreen-3, #fullscreen-4  {display: none;}

## CSS Desktop

**Remplacer dans responsive.css (Ligne 585)** 

    #fullscreen-2 {
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

## JS 

**Remplacer dans script.js (Ligne 84)** 

    var element2 = document.getElementById('video-2');
    var fullscreen2 = document.getElementById('fullscreen-2');
    
    fullscreen2.addEventListener('click',function(){
        <!--console.log ('it is working'); -->
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
        <!--console.log ('it is working'); -->
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
        <!--console.log ('it is working'); -->
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
    
## Problème 3

> Dans le code de section-2.php, il y a deux éléments video, l'un pour
> mobile et l'autre pour desktop. Au niveau de l'affichage pas de problème, mais par contre l'utilisateur charge la vidéo en double même s'ils l'affichent bien qu'une fois.

