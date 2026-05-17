# 📄 README -Pràctica Transicions, Animacions i Vídeo

## 📌 Descripció del projecte

Aquest projecte és una pàgina web d’un restaurant on he aplicat:

- Transicions CSS
- Animacions CSS
- Vídeo HTML5
- Controls personalitzats amb JavaScript
- Efectes amb scroll

Tot el projecte està fet sense utilitzar frameworks, només HTML, CSS i JavaScript bàsic.

# Pràctica. TRANSICIONS-ANIMACIONS-VIDEOS

## 🎯 Exercici 1 - Transicions

Les transicions s’han aplicat a les imatges de la galeria.

### ✔ Què he fet:

- Quan passo el ratolí per sobre les imatges:
  - fan zoom (`scale`)
  - giren (`rotate`)
  - canvien el filtre (`grayscale`, `contrast`, `brightness`, etc.)
- S’ha utilitzat `overflow: hidden` per evitar que les imatges surtin del contenidor.

📍 **codi:**

- Secció: Galeria d’imatges CSS: `.imag:hover` i `@keyframes`

.flex div:nth-child(2) .imag:hover {
animation: giroZoom 5s forwards;
transform-origin: center;
}
.flex div:nth-child(2) {
overflow: hidden;
}
@keyframes giroZoom {
0% {
transform: rotate(0deg) scale(1);
opacity: 0;
}

100% {
transform: rotate(360deg) scale(1.5);
opacity: 1;
}
}
.flex div:nth-child(3) .imag:hover {
animation: contra 3s forwards;
}

@keyframes contra {
0% {
filter: contrast(0%);
}
100% {
filter: contrast(100%);
}
}
.flex div:nth-child(4) .imag:hover {
animation: blu 4s forwards;
}

@keyframes blu {
0% {
filter: blur(0px);
}
100% {
filter: blur(5px);
}
}

.flex div:nth-child(5) .imag:hover {
animation: brit 3s forwards;
}

@keyframes brit {
0% {
filter: brightness(0%);
}
100% {
filter: brightness(100%);
}
}

.flex div:nth-child(6) .imag:hover {
animation: blck 5s forwards;
transform-origin: center;
}

@keyframes blck {
0% {
filter: grayscale(0%);
}

100% {
filter: grayscale(100%);
}
}

.flex div:nth-child(7) .imag:hover,
.flex div:nth-child(8) .imag:hover,
.flex div:nth-child(9) .imag:hover,
.flex div:nth-child(11) .imag:hover,
.flex div:nth-child(12) .imag:hover,
.flex div:nth-child(14) .imag:hover,
.flex div:nth-child(15) .imag:hover,
.flex div:nth-child(16) .imag:hover {
animation: saturat 3s forwards;
}

@keyframes saturat {
0% {
filter: saturate(0%);
}
100% {
filter: saturate(100%);
}
}

.flex div:nth-child(10) .imag:hover {
animation: sepi 5s forwards;
}
.flex div:nth-child(10) {
overflow: hidden;
}

@keyframes sepi {
0% {
filter: sepia(0%);
transform: scale(1);
}
100% {
filter: sepia(100%);
transform: scale(1.5);
}
}

- EXTRA

.footer-item .material-symbols-outlined {
animation: girarY 2s infinite;
display: inline-block;
}
@keyframes girarY {
0% {
transform: rotateY(0deg);
}
50% {
transform: rotateY(180deg);
}
100% {
transform: rotateY(360deg);
}
}
.form-button button {
animation: girarX 2s infinite;
display: inline-block;
}

@keyframes girarX {
0% {
transform: rotateX(0deg);
}
50% {
transform: rotateX(180deg);
}
100% {
transform: rotateX(360deg);
}
}

---

## 🎬 Exercici 2 - Animacions

### ✔ Animació del títol principal:

- El text de la capçalera apareix quan carrega la pàgina
- Es mou cap amunt progressivament
- Canvia de color fins arribar a l’estat final

### ✔ Animacions extra:

- He afegit altres animacions en imatges i botons
- Utilitzen transformacions i filtres CSS ()

📍 **codi:**

.header-text {
position: absolute;
animation-name: animations;
animation-duration: 7s;
animation-fill-mode: forwards;
}
@keyframes animations {
0% {
bottom: 0px;
left: 10rem;
opacity: 0;
}
25% {
color: white;
}
50% {
color: red;
}
75% {
color: purple;
}
100% {
bottom: 80px;
left: 10rem;
opacity: 1;
color: black;
}
}

- Extra
  .Boto:hover {
  text-decoration: underline;
  }

## 🎥 Exercici 3 - Vídeo HTML

- He afegit un vídeo dins la pàgina del restaurant
- Està centrat amb CSS
- És responsive i s’adapta a totes les pantalles
- No genera scroll horitzontal
- El vídeo està per defecte en mode silenciat

📍 **codi:**

- Video HTML

<video id="myVideo" muted>
    <source src="movie.mp4" type="video/mp4" />
    Tu navegador no soporta vídeo.
</video>

---

## 🎮 Exercici 4 - Controls de vídeo personalitzats

- He amagat els controls natius del vídeo
- He creat controls propis amb icones de Google Fonts

### ✔ Funcions:

- ▶ Play → reprodueix el vídeo
- ⏸ Pause → pausa el vídeo
- 🔊 Volume on → activa el so
- 🔇 Volume off → silencia el vídeo

📍 **On està:**

- HTML: `.video-controls`

- JS: funcions `playVideo()`, `pauseVideo()`, `volumeOn()`, `volumeOff()`

<div class="video-controls">
<span class="material-symbols-outlined" onclick="playVideo()">
    play_circle
</span>
<span class="material-symbols-outlined" onclick="pauseVideo()">
    pause_circle
</span>
<span class="material-symbols-outlined" onclick="volumeOn()">
    volume_up
</span>
<span class="material-symbols-outlined" onclick="volumeOff()">
    volume_off
</span>
</div>

- JS: funcions `playVideo()`, `pauseVideo()`, `volumeOn()`, `volumeOff()`

<script>
const video = document.getElementById("myVideo");
function playVideo() {
video.play();
}
function pauseVideo() {
video.pause();
}
function volumeOn() {
video.muted = false;
}
function volumeOff() {
video.muted = true;
}


## Exercici 5 - JavaScript amb scroll

- El menú es redueix quan es fa scroll
- El vídeo es reprodueix automàticament quan entra a la pantalla

📍 **On està:**
- JS: `scrollNavbar()` i `autoPlayVideo()`

window.onscroll = function () {
scrollNavbar();
autoPlayVideo();
};
function scrollNavbar() {
    if (
        document.body.scrollTop > 80 ||
        document.documentElement.scrollTop > 80
    ) {
        document.getElementById("navbar").style.padding = "20px 10px";
        document.getElementById("logo").style.fontSize = "20px";
    } else {
        document.getElementById("navbar").style.padding = "40px 10px";
        document.getElementById("logo").style.fontSize = "35px";
    }
}
function autoPlayVideo() {
const rect = video.getBoundingClientRect();
    if (rect.top >= 0 && rect.top <= window.innerHeight / 2) {
        video.play();
    }
}
- Navbar: `#navbar`

<script>
window.onscroll = function () {
scrollFunction();
};

window.onscroll = function () {
scrollFunction();
};

function scrollFunction() {
    if (
        document.body.scrollTop > 80 ||
        document.documentElement.scrollTop > 80
    ) {
        document.getElementById("navbar").style.padding = "30px 10px";
        document.getElementById("logo").style.fontSize = "25px";
    } else {
        document.getElementById("navbar").style.padding = "80px 10px";
        document.getElementById("logo").style.fontSize = "35px";
    }
}
</script>

---

## 🧩 Resum

Aquest projecte integra:

- Disseny responsive
- Animacions CSS sense JavaScript
- Interactivitat amb vídeo
- Efectes visuals en galeria
- JavaScript per scroll i control de vídeo
