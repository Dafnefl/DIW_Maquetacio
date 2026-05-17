# 📄 README - Pràctica: Transicions, Animacions i Vídeo

## 📌 Descripció del projecte

Aquest projecte és una pàgina web d’un restaurant anomenat **Homies & Burgers**, desenvolupada amb HTML, CSS i JavaScript pur.

S’han aplicat els continguts de la pràctica:

- Transicions CSS
- Animacions CSS amb keyframes
- Vídeo HTML5 responsive
- Controls personalitzats amb JavaScript
- Efectes amb scroll (navbar i autoplay vídeo)
- Disseny responsive

---

# 🎯 EXERCICI 1 - TRANSICIONS

## ✔ Què he fet

He aplicat transicions a les imatges de la galeria. Quan l’usuari passa el ratolí:

- Zoom (`scale`)
- Rotació (`rotate`)
- Filtres (contrast, blur, brightness, grayscale, sepia, saturate)

També he utilitzat `overflow: hidden` per evitar que les imatges surtin del contenidor.

## 📍 Codi (CSS)

```css
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
```

# 🎬 EXERCICI 2 - ANIMACIONS

## ✔ Què he fet

- He creat una animació al títol principal (.header-text)
- El text apareix al carregar la pàgina
- Puja cap amunt
- Canvia de color durant l’entrada
- Es queda en estat final

## 📍 Codi (CSS)

```css
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
```

## ✔ Animacions extra

```css
.footer-item .material-symbols-outlined {
  animation: girarY 2s infinite;
}

@keyframes girarY {
  0% {
    transform: rotateY(0deg);
  }
  100% {
    transform: rotateY(360deg);
  }
}

.form-button button {
  animation: girarX 2s infinite;
}

@keyframes girarX {
  0% {
    transform: rotateX(0deg);
  }
  100% {
    transform: rotateX(360deg);
  }
}
```

# 🎥 EXERCICI 3 - VÍDEO HTML

## ✔ Què he fet

He afegit un vídeo dins de la pàgina del restaurant, situat després de la galeria.

## ✔ Característiques

- Centrat amb CSS
- Responsive
- Sense scroll horitzontal
- Per defecte: pausat i silenciat

## 📍 Codi (HTML + CSS)

```html
<div class="video-section">
  <div class="video-container">
    <video id="myVideo" muted>
      <source src="movie.mp4" type="video/mp4" />
    </video>
  </div>
</div>
```

```css
.video-section {
  width: 80%;
  max-width: 1200px;
  margin: 3rem auto;
  display: flex;
  justify-content: center;
}

.video-container {
  position: relative;
  width: 100%;
  max-width: 900px;
}

#myVideo {
  width: 100%;
  display: block;
  border-radius: 10px;
}
```

# 🎮 EXERCICI 4 - CONTROLS PERSONALITZATS

## ✔ Què he fet

He creat controls personalitzats per al vídeo amb icones de Google Fonts.

✔ Funcions

- ▶ Play
- ⏸ Pause
- 🔊 So ON
- 🔇 So OFF

## 📍 Codi (HTML + CSS + JS)

```html
<div class="video-controls">
  <span class="material-symbols-outlined" onclick="playVideo()"
    >play_circle</span
  >
  <span class="material-symbols-outlined" onclick="pauseVideo()"
    >pause_circle</span
  >
  <span class="material-symbols-outlined" onclick="volumeOn()">volume_up</span>
  <span class="material-symbols-outlined" onclick="volumeOff()"
    >volume_off</span
  >
</div>
```

```css
.video-controls {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  background: rgba(0, 0, 0, 0.5);

  display: flex;
  justify-content: center;
  gap: 2rem;
  padding: 1rem;
}

.video-controls .material-symbols-outlined {
  color: white;
  font-size: 3rem;
  cursor: pointer;
  transition:
    transform 0.3s ease,
    text-shadow 0.3s ease;
}

.video-controls .material-symbols-outlined:hover {
  transform: scale(1.2);
  text-shadow: 0 0 15px white;
}
```

```javaScript
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
```

# 🧠 EXERCICI 5 - JAVASCRIPT AMB SCROLL

## ✔ Què he fet

He implementat funcionalitats amb JavaScript + scroll:

- 📉 Navbar que es redueix amb el scroll
- 🎥 Vídeo que es reprodueix automàticament quan entra a pantalla

## 📍 Codi (JavaScript)

```javaScript
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
    document.getElementById("navbar").style.padding = "80px 10px";
    document.getElementById("logo").style.fontSize = "35px";
  }
}

const video = document.getElementById("myVideo");

function autoPlayVideo() {
  const rect = video.getBoundingClientRect();

  if (rect.top >= 0 && rect.top <= window.innerHeight / 2) {
    video.play();
  }
}
```

# 🧩 RESUM FINAL

Aquest projecte inclou:

- Disseny responsive complet
- Animacions CSS sense JavaScript
- Transicions en galeria
- Vídeo HTML5 amb controls personalitzats
- JavaScript per scroll i interacció
- Experiència d’usuari moderna i dinàmica
