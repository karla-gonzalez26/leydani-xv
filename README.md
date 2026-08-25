<!DOCTYPE html>
<html lang="es-MX">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>XV Años | Leydani Troche</title>

  <!-- Fuentes -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=DM+Sans:wght@400;500;600;700&family=Great+Vibes&display=swap" rel="stylesheet">

  <style>

    /* =========================================================
       VARIABLES
    ========================================================= */

    :root {
      --verde-profundo: #061f1b;
      --verde: #0d4b3b;
      --verde-claro: #17634d;

      --dorado: #d9b45a;
      --dorado-claro: #f4dda0;

      --morado: #675083;
      --morado-claro: #a98dc5;

      --crema: #fff9e9;
      --texto: #25433b;

      --sombra: rgba(0,0,0,.45);
    }


    /* =========================================================
       RESET
    ========================================================= */

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: "DM Sans", sans-serif;
      background: var(--verde-profundo);
      color: var(--crema);
      overflow-x: hidden;
    }


    /* =========================================================
       FONDO PRINCIPAL
    ========================================================= */

    .app {
      min-height: 100vh;
      position: relative;
      overflow: hidden;

      background:
        radial-gradient(
          circle at 50% 10%,
          rgba(80,140,105,.30),
          transparent 35%
        ),

        radial-gradient(
          circle at 15% 80%,
          rgba(106,76,135,.22),
          transparent 30%
        ),

        linear-gradient(
          180deg,
          #061f1b 0%,
          #0b382d 45%,
          #061c18 100%
        );
    }


    /* =========================================================
       LUCES DEL PANTANO
    ========================================================= */

    .fireflies {
      position: fixed;
      inset: 0;
      pointer-events: none;
      z-index: 1;
    }

    .firefly {
      position: absolute;
      width: 5px;
      height: 5px;
      border-radius: 50%;

      background: #ffe8a0;

      box-shadow:
        0 0 8px #ffe8a0,
        0 0 18px rgba(255,220,120,.7);

      animation:
        floatFirefly 5s ease-in-out infinite,
        glowFirefly 2s ease-in-out infinite;
    }

    .firefly:nth-child(1) {
      left: 8%;
      top: 25%;
      animation-delay: 0s;
    }

    .firefly:nth-child(2) {
      left: 22%;
      top: 70%;
      animation-delay: 1s;
    }

    .firefly:nth-child(3) {
      left: 78%;
      top: 22%;
      animation-delay: 2s;
    }

    .firefly:nth-child(4) {
      left: 91%;
      top: 58%;
      animation-delay: .5s;
    }

    .firefly:nth-child(5) {
      left: 55%;
      top: 14%;
      animation-delay: 1.5s;
    }

    .firefly:nth-child(6) {
      left: 43%;
      top: 82%;
      animation-delay: 2.5s;
    }

    .firefly:nth-child(7) {
      left: 14%;
      top: 48%;
      animation-delay: 3s;
    }

    .firefly:nth-child(8) {
      left: 70%;
      top: 78%;
      animation-delay: 1.8s;
    }


    @keyframes floatFirefly {

      0%,100% {
        transform: translate(0,0);
      }

      50% {
        transform: translate(20px,-35px);
      }

    }

    @keyframes glowFirefly {

      0%,100% {
        opacity: .25;
        transform: scale(.7);
      }

      50% {
        opacity: 1;
        transform: scale(1.4);
      }

    }


    /* =========================================================
       DECORACIÓN
    ========================================================= */

    .leaf {
      position: absolute;
      font-size: 90px;
      opacity: .10;
      pointer-events: none;
      z-index: 0;
    }

    .leaf-1 {
      top: 5%;
      left: -20px;
      transform: rotate(-20deg);
    }

    .leaf-2 {
      top: 30%;
      right: -25px;
      transform: rotate(25deg);
    }

    .leaf-3 {
      bottom: 8%;
      left: -25px;
      transform: rotate(35deg);
    }

    .leaf-4 {
      bottom: 25%;
      right: -15px;
      transform: rotate(-30deg);
    }


    /* =========================================================
       CONTENEDOR
    ========================================================= */

    .container {
      width: min(94%, 720px);
      margin: auto;
      position: relative;
      z-index: 5;
    }


    /* =========================================================
       PORTADA
    ========================================================= */

    .cover {
      min-height: 100vh;

      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;

      text-align: center;
      padding: 40px 20px;
    }

    .small-title {
      font-size: .75rem;
      letter-spacing: .45em;
      text-transform: uppercase;
      color: var(--dorado-claro);
      margin-bottom: 15px;
    }

    .story {
      font-family: "Great Vibes", cursive;
      font-size: clamp(2.4rem, 8vw, 4rem);
      color: var(--dorado-claro);
    }

    .name {
      font-family: "Cormorant Garamond", serif;
      font-size: clamp(3.5rem, 13vw, 7rem);
      line-height: .9;
      font-weight: 600;

      color: #fff7d9;

      text-shadow:
        0 3px 20px rgba(0,0,0,.5),
        0 0 30px rgba(220,185,94,.18);
    }

    .subtitle {
      font-family: "Cormorant Garamond", serif;
      font-size: clamp(1.1rem, 4vw, 1.6rem);
      font-style: italic;
      color: var(--dorado-claro);
      margin-top: 18px;
    }


    /* =========================================================
       SOBRE
    ========================================================= */

    .envelope {
      width: min(90vw, 500px);
      height: 310px;
      position: relative;
      margin-top: 45px;
      cursor: pointer;
      perspective: 1200px;
    }

    .envelope-body {
      position: absolute;
      inset: 0;

      border-radius: 12px;

      background:
        linear-gradient(
          145deg,
          #155b48,
          #0a392e 60%,
          #06241e
        );

      border: 1px solid rgba(240,214,145,.5);

      box-shadow:
        0 30px 70px rgba(0,0,0,.5),
        inset 0 0 30px rgba(255,255,255,.04);
    }


    .envelope-left,
    .envelope-right {
      position: absolute;
      bottom: 0;

      width: 70%;
      height: 80%;

      background: #0b4638;
    }

    .envelope-left {
      left: -10%;
      transform: rotate(34deg);
      transform-origin: bottom left;
    }

    .envelope-right {
      right: -10%;
      transform: rotate(-34deg);
      transform-origin: bottom right;
    }


    .envelope-flap {
      position: absolute;
      top: 0;
      left: 0;

      width: 100%;
      height: 62%;

      background:
        linear-gradient(
          145deg,
          #1b7156,
          #0c4637
        );

      clip-path:
        polygon(
          0 0,
          100% 0,
          50% 100%
        );

      transform-origin: top;
      transition: transform .9s cubic-bezier(.2,.8,.2,1);

      z-index: 5;
    }


    .seal {
      position: absolute;

      left: 50%;
      top: 43%;

      transform: translate(-50%,-50%);

      width: 80px;
      height: 80px;

      border-radius: 50%;

      display: flex;
      align-items: center;
      justify-content: center;

      background:
        radial-gradient(
          circle,
          #f9e4a5,
          #d1a63d 55%,
          #805717
        );

      border: 3px solid #f7e4a6;

      font-size: 34px;

      box-shadow:
        0 8px 20px rgba(0,0,0,.4);

      z-index: 8;

      transition: .6s;
    }

    .envelope-text {
      position: absolute;
      bottom: 25px;
      width: 100%;

      text-align: center;

      font-family: "Cormorant Garamond", serif;
      font-size: 1.7rem;

      color: var(--dorado-claro);

      z-index: 7;
    }

    .envelope-subtext {
      display: block;

      font-family: "DM Sans", sans-serif;
      font-size: .65rem;

      letter-spacing: .3em;
      text-transform: uppercase;

      margin-top: 5px;
    }


    .envelope.open .envelope-flap {
      transform: rotateX(-175deg);
    }

    .envelope.open .seal {
      opacity: 0;
      transform:
        translate(-50%,-80%)
        scale(.6);
    }


    /* =========================================================
       CONTENIDO
    ========================================================= */

    .content {
      display: none;
      padding: 30px 0 80px;
      animation: fadeUp 1s ease forwards;
    }

    .content.visible {
      display: block;
    }

    @keyframes fadeUp {

      from {
        opacity: 0;
        transform: translateY(25px);
      }

      to {
        opacity: 1;
        transform: translateY(0);
      }

    }


    /* =========================================================
       TARJETAS
    ========================================================= */

    .card {
      background: rgba(255,249,233,.97);

      color: var(--texto);

      border-radius: 5px;

      padding: 45px 28px;

      margin-bottom: 25px;

      text-align: center;

      box-shadow:
        0 25px 70px rgba(0,0,0,.35);

      border:
        1px solid rgba(215,175,85,.75);

      position: relative;
      overflow: hidden;
    }

    .card::before {
      content: "✦";

      position: absolute;

      top: -25px;
      left: -10px;

      font-size: 100px;

      color: rgba(185,138,45,.12);
    }

    .card::after {
      content: "✦";

      position: absolute;

      bottom: -35px;
      right: -10px;

      font-size: 110px;

      color: rgba(185,138,45,.12);
    }


    /* =========================================================
       TÍTULOS
    ========================================================= */

    .section-title {
      font-family: "Cormorant Garamond", serif;

      font-size: clamp(2rem, 7vw, 3.2rem);

      color: var(--verde);

      margin-bottom: 15px;
    }

    .gold-title {
      color: #a47827;
    }

    .script {
      font-family: "Great Vibes", cursive;

      font-size: 2.2rem;

      color: #88652c;
    }

    .ornament {
      color: #b48931;
      letter-spacing: .4em;
      margin: 15px 0;
    }


    /* =========================================================
       FOTO
    ========================================================= */

    .portrait {
      width: min(70vw, 270px);
      aspect-ratio: 1;

      object-fit: cover;

      border-radius: 50%;

      border:
        5px solid var(--dorado);

      padding: 5px;

      background: var(--crema);

      box-shadow:
        0 20px 50px rgba(0,0,0,.25);

      margin-bottom: 20px;
    }


    /* =========================================================
       CUENTA REGRESIVA
    ========================================================= */

    .countdown {
      margin: 25px auto 0;

      max-width: 560px;

      padding: 25px 15px;

      border-radius: 4px;

      background:
        linear-gradient(
          145deg,
          rgba(255,249,233,.95),
          rgba(248,238,210,.95)
        );

      border:
        1px solid rgba(145,105,38,.35);
    }

    .countdown-title {
      font-size: .7rem;

      letter-spacing: .25em;

      text-transform: uppercase;

      color: #806025;

      margin-bottom: 20px;
    }

    .countdown-grid {
      display: grid;

      grid-template-columns:
        repeat(4, 1fr);

      gap: 8px;
    }

    .countdown-box {
      text-align: center;
    }

    .countdown-number {
      display: block;

      font-family: "Cormorant Garamond", serif;

      font-size: clamp(1.7rem, 7vw, 2.5rem);

      font-weight: 700;

      color: var(--verde);
    }

    .countdown-label {
      font-size: .6rem;

      letter-spacing: .1em;

      text-transform: uppercase;

      color: #98752f;
    }


    /* =========================================================
       EVENTOS
    ========================================================= */

    .event-card {
      margin-top: 25px;

      padding: 25px;

      border:
        1px solid rgba(151,113,49,.3);

      background:
        rgba(255,255,255,.55);

      position: relative;
      z-index: 2;
    }

    .event-icon {
      font-size: 2.5rem;
      margin-bottom: 10px;
    }

    .event-title {
      font-family: "Cormorant Garamond", serif;

      font-size: 1.9rem;

      color: var(--verde);

      margin-bottom: 8px;
    }

    .event-name {
      font-weight: 700;
      margin-bottom: 5px;
    }

    .event-address {
      font-size: .9rem;
      line-height: 1.5;

      color: #52655e;
    }


    /* =========================================================
       BOTONES
    ========================================================= */

    .button {
      display: inline-flex;

      align-items: center;
      justify-content: center;

      gap: 8px;

      margin-top: 17px;

      padding: 13px 23px;

      border-radius: 999px;

      text-decoration: none;

      background:
        linear-gradient(
          135deg,
          #145b47,
          #0a382e
        );

      color: white;

      font-weight: 700;

      font-size: .82rem;

      letter-spacing: .03em;

      border: none;

      cursor: pointer;

      box-shadow:
        0 10px 25px rgba(10,55,44,.2);

      transition:
        transform .2s ease,
        box-shadow .2s ease;
    }

    .button:hover {
      transform: translateY(-3px);

      box-shadow:
        0 15px 30px rgba(10,55,44,.3);
    }

    .button.gold {
      background:
        linear-gradient(
          135deg,
          #dcb95e,
          #9b7127
        );

      color: #fff;
    }

    .button.morado {
      background:
        linear-gradient(
          135deg,
          #80609a,
          #55406b
        );
    }


    /* =========================================================
       MÚSICA
    ========================================================= */

    .music-section {
      padding: 25px;

      background:
        linear-gradient(
          135deg,
          rgba(15,77,61,.08),
          rgba(104,78,132,.08)
        );

      border:
        1px solid rgba(140,105,47,.25);

      margin-top: 25px;
    }

    .music-icon {
      font-size: 2.5rem;
    }

    .music-text {
      margin-top: 8px;
      font-size: .9rem;
    }

    .youtube-player {
      position: fixed;

      width: 1px;
      height: 1px;

      opacity: 0;

      pointer-events: none;

      left: -9999px;
      top: -9999px;
    }


    /* =========================================================
       DRESS CODE
    ========================================================= */

    .dress {
      margin-top: 30px;

      padding: 25px;

      border-top:
        1px solid rgba(140,100,40,.3);

      border-bottom:
        1px solid rgba(140,100,40,.3);
    }

    .dress-title {
      font-family: "Cormorant Garamond", serif;

      font-size: 1.8rem;

      color: var(--verde);
    }


    /* =========================================================
       GALERÍA
    ========================================================= */

    .gallery {
      display: grid;

      grid-template-columns:
        repeat(2,1fr);

      gap: 10px;

      margin-top: 20px;
    }

    .gallery img {
      width: 100%;

      aspect-ratio: 1;

      object-fit: cover;

      border-radius: 4px;

      border:
        2px solid rgba(207,166,70,.55);

      background: #eee;
    }


    /* =========================================================
       CONFIRMACIÓN
    ========================================================= */

    .rsvp {
      background:
        linear-gradient(
          145deg,
          #0b4638,
          #06241e
        );

      color: white;

      border-color:
        rgba(226,194,106,.7);
    }

    .rsvp .section-title {
      color: var(--dorado-claro);
    }

    .rsvp-text {
      color: #f4eddb;
      line-height: 1.7;
    }


    /* =========================================================
       MENSAJE FINAL
    ========================================================= */

    .closing {
      text-align: center;

      padding: 35px 15px;

      font-family:
        "Cormorant Garamond",
        serif;

      font-size: 1.4rem;

      font-style: italic;

      color: var(--dorado-claro);
    }

    .closing-name {
      font-family: "Great Vibes", cursive;

      font-size: 2.8rem;

      color: var(--dorado);
      margin-top: 12px;
    }


    /* =========================================================
       BOTÓN MÚSICA FLOTANTE
    ========================================================= */

    .music-floating {
      position: fixed;

      right: 18px;
      bottom: 18px;

      width: 54px;
      height: 54px;

      border-radius: 50%;

      border: 2px solid var(--dorado-claro);

      background:
        rgba(7,40,33,.92);

      color: var(--dorado-claro);

      display: none;

      align-items: center;
      justify-content: center;

      font-size: 1.3rem;

      cursor: pointer;

      z-index: 999;

      box-shadow:
        0 8px 25px rgba(0,0,0,.35);
    }

    .music-floating.visible {
      display: flex;
    }


    /* =========================================================
       RESPONSIVE
    ========================================================= */

    @media(max-width:520px) {

      .card {
        padding:
          35px 18px;
      }

      .envelope {
        height: 250px;
      }

      .seal {
        width: 65px;
        height: 65px;
        font-size: 27px;
      }

      .countdown-grid {
        gap: 3px;
      }

      .gallery {
        gap: 7px;
      }

    }


    /* =========================================================
       ACCESIBILIDAD
    ========================================================= */

    @media(prefers-reduced-motion:reduce) {

      *,
      *::before,
      *::after {
        animation-duration: .01ms !important;
        transition-duration: .01ms !important;
      }

    }

  </style>
</head>


<body>

<div class="app" id="app">


  <!-- =======================================================
       LUCES
  ======================================================== -->

  <div class="fireflies">

    <span class="firefly"></span>
    <span class="firefly"></span>
    <span class="firefly"></span>
    <span class="firefly"></span>
    <span class="firefly"></span>
    <span class="firefly"></span>
    <span class="firefly"></span>
    <span class="firefly"></span>

  </div>


  <!-- DECORACIÓN -->

  <div class="leaf leaf-1">🌿</div>
  <div class="leaf leaf-2">🌿</div>
  <div class="leaf leaf-3">🍃</div>
  <div class="leaf leaf-4">🌿</div>


  <!-- =======================================================
       PORTADA
  ======================================================== -->

  <section class="cover" id="cover">

    <div class="container">

      <div class="small-title">
        Una historia está por comenzar...
      </div>

      <div class="story">
        Érase una vez...
      </div>

      <h1 class="name">
        Leydani
      </h1>

      <div class="subtitle">
        Mis XV años
      </div>


      <!-- SOBRE -->

      <div
        class="envelope"
        id="envelope"
        role="button"
        tabindex="0"
        aria-label="Abrir invitación"
      >

        <div class="envelope-body"></div>

        <div class="envelope-left"></div>
        <div class="envelope-right"></div>

        <div class="envelope-flap"></div>

        <div class="seal">
          👑
        </div>

        <div class="envelope-text">

          Abrir invitación

          <span class="envelope-subtext">
            05 · 12 · 2026
          </span>

        </div>

      </div>

    </div>

  </section>


  <!-- =======================================================
       CONTENIDO
  ======================================================== -->

  <main class="content" id="content">

    <div class="container">


      <!-- ===================================================
           PRESENTACIÓN
      ==================================================== -->

      <section class="card">

        <!--
        FOTO DE LEYDANI

        Reemplaza esta URL por la fotografía real.
        -->

        <img
          class="portrait"
          src="https://images.unsplash.com/photo-1517841905240-472988babdf9?auto=format&fit=crop&w=600&q=80"
          alt="Fotografía de Leydani"
        >

        <div class="script">
          Una noche mágica...
        </div>

        <h2 class="section-title">
          Leydani Troche
        </h2>

        <p>
          Hay momentos en la vida que se convierten
          en recuerdos para siempre.
        </p>

        <p style="margin-top:15px;">
          Hoy quiero compartir contigo uno de los días
          más especiales de mi vida.
        </p>

        <div class="ornament">
          ❦ ✦ ❦
        </div>

        <p style="font-family:'Cormorant Garamond',serif;font-size:1.3rem;font-style:italic;">
          Te invito a celebrar conmigo
          mis XV años.
        </p>

      </section>


      <!-- ===================================================
           CUENTA REGRESIVA
      ==================================================== -->

      <section class="card">

        <div class="script">
          El gran día se acerca...
        </div>

        <h2 class="section-title">
          Mi cuento comienza
        </h2>

        <div class="countdown">

          <div class="countdown-title">
            Faltan para el 5 de diciembre de 2026
          </div>

          <div class="countdown-grid">

            <div class="countdown-box">
              <span
                class="countdown-number"
                id="days"
              >
                0
              </span>

              <span class="countdown-label">
                Días
              </span>
            </div>


            <div class="countdown-box">
              <span
                class="countdown-number"
                id="hours"
              >
                0
              </span>

              <span class="countdown-label">
                Horas
              </span>
            </div>


            <div class="countdown-box">
              <span
                class="countdown-number"
                id="minutes"
              >
                0
              </span>

              <span class="countdown-label">
                Minutos
              </span>
            </div>


            <div class="countdown-box">
              <span
                class="countdown-number"
                id="seconds"
              >
                0
              </span>

              <span class="countdown-label">
                Segundos
              </span>
            </div>

          </div>

        </div>

      </section>


      <!-- ===================================================
           EVENTOS
      ==================================================== -->

      <section class="card">

        <div class="script">
          Acompáñame
        </div>

        <h2 class="section-title">
          El gran día
        </h2>


        <!-- IGLESIA -->

        <div class="event-card">

          <div class="event-icon">
            ⛪
          </div>

          <h3 class="event-title">
            Ceremonia
          </h3>

          <p class="event-name">
            Capilla de San Isidro
          </p>

          <p class="event-address">
            Av. Reforma, San Isidro,<br>
            52105 San Mateo Atenco, Méx.
          </p>

          <p style="margin-top:10px;font-size:.85rem;">
            🕐 <strong>Misa:</strong>
            <span style="color:#a24a35;">
              PENDIENTE
            </span>
          </p>


          <!--
          BOTÓN GOOGLE MAPS - IGLESIA
          -->

          <a
            class="button"
            href="https://maps.google.com/maps?vet=10CAAQoqAOahcKEwiwvvWXz7qWAxUAAAAAHQAAAAAQBQ..i&pvq=Cg0vZy8xMWI2YzV0czF0IhAKCnNhbiBpc2lkcm8QAhgD&lqi=CgpzYW4gaXNpZHJvSLnA87KZqoCACFoUEAAQARgAGAEiCnNhbiBpc2lkcm-SAQ9jYXRob2xpY19jaHVyY2g&fvr=1&cs=0&um=1&ie=UTF-8&fb=1&gl=mx&sa=X&ftid=0x85cd8ad47f87d41d:0x2aabdb4a8f5c362e"
            target="_blank"
            rel="noopener noreferrer"
          >
            📍 Ver ubicación
          </a>

        </div>


        <!-- SALÓN -->

        <div class="event-card">

          <div class="event-icon">
            🥂
          </div>

          <h3 class="event-title">
            Recepción
          </h3>

          <p class="event-name">
            Salón de eventos
          </p>

          <p class="event-address">
            Av. Reforma 102, Santa María,<br>
            San Isidro, 52105 San Mateo Atenco, Méx.
          </p>

          <p style="margin-top:10px;font-size:.85rem;">
            🕐 <strong>Recepción:</strong>
            <span style="color:#a24a35;">
              PENDIENTE
            </span>
          </p>


          <!--
          BOTÓN GOOGLE MAPS - SALÓN
          -->

          <a
            class="button gold"
            href="https://maps.google.com/maps?vet=10CAAQoqAOahcKEwiwvvWXz7qWAxUAAAAAHQAAAAAQHg..i&pvq=Cg0vZy8xMXhsOGoyempz&fvr=1&cs=0&um=1&ie=UTF-8&fb=1&gl=mx&sa=X&ftid=0x85cd8b0048dcb7fb:0xd29c02992f8c4cff"
            target="_blank"
            rel="noopener noreferrer"
          >
            📍 Ver ubicación
          </a>

        </div>

      </section>


      <!-- ===================================================
           MÚSICA
      ==================================================== -->

      <section class="card">

        <div class="music-section">

          <div class="music-icon">
            🎺
          </div>

          <h2 class="section-title">
            Música para mi historia
          </h2>

          <p class="music-text">
            Esta canción forma parte de la magia
            de esta noche.
          </p>


          <button
            class="button morado"
            id="musicButton"
            type="button"
          >
            🎵 Activar música
          </button>

        </div>

      </section>


      <!-- ===================================================
           DRESS CODE
      ==================================================== -->

      <section class="card">

        <div class="dress">

          <div style="font-size:2.5rem;">
            👗
          </div>

          <h2 class="dress-title">
            Código de vestimenta
          </h2>

          <p style="margin-top:8px;">
            <strong>Formal</strong>
          </p>

          <p style="margin-top:10px;color:#61736c;">
            Ven preparado/a para una noche
            llena de magia.
          </p>

        </div>

      </section>


      <!-- ===================================================
           GALERÍA
      ==================================================== -->

      <section class="card">

        <div class="script">
          Recuerdos de una princesa
        </div>

        <h2 class="section-title">
          Mi historia
        </h2>

        <p>
          Aquí podrás agregar las fotografías
          favoritas de Leydani.
        </p>


        <!--
        REEMPLAZA LAS IMÁGENES POR LAS FOTOS REALES.

        Puedes poner 4, 6 u 8 fotografías.
        -->

        <div class="gallery">

          <img
            src="https://images.unsplash.com/photo-1519741497674-611481863552?auto=format&fit=crop&w=600&q=80"
            alt="Foto Leydani 1"
          >

          <img
            src="https://images.unsplash.com/photo-1496747611176-843222e1e57c?auto=format&fit=crop&w=600&q=80"
            alt="Foto Leydani 2"
          >

          <img
            src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=600&q=80"
            alt="Foto Leydani 3"
          >

          <img
            src="https://images.unsplash.com/photo-1488426862026-3ee34a7d66df?auto=format&fit=crop&w=600&q=80"
            alt="Foto Leydani 4"
          >

        </div>

      </section>


      <!-- ===================================================
           CONFIRMACIÓN
      ==================================================== -->

      <section class="card rsvp">

        <div style="font-size:2.8rem;">
          💌
        </div>

        <h2 class="section-title">
          ¿Nos acompañas?
        </h2>

        <p class="rsvp-text">
          Tu presencia hará que esta noche
          sea todavía más especial.
        </p>


        <!--
        WHATSAPP PENDIENTE

        Cuando tengas el número, reemplaza:

        PENDIENTE

        por el número completo.

        Ejemplo:
        5217221234567
        -->

        <a
          class="button gold"
          href="#"
          id="whatsappButton"
        >
          💚 Confirmar asistencia
        </a>

        <p
          id="whatsappPending"
          style="
            margin-top:12px;
            font-size:.7rem;
            color:#f2c5bd;
          "
        >
          WhatsApp:
          PENDIENTE
        </p>

      </section>


      <!-- ===================================================
           DEJAR MENSAJE
      ==================================================== -->

      <section class="card">

        <div style="font-size:2.5rem;">
          🐸
        </div>

        <div class="script">
          Un deseo para la princesa
        </div>

        <h2 class="section-title">
          Deja un mensaje
        </h2>

        <p>
          Toda princesa merece un deseo.
          💚
        </p>

        <p style="margin-top:10px;color:#61736c;">
          Comparte unas palabras especiales
          para Leydani en este día tan importante.
        </p>


        <!--
        ESTE BOTÓN PUEDE CONECTARSE A WHATSAPP
        CUANDO TENGAMOS EL NÚMERO.
        -->

        <button
          class="button"
          type="button"
          onclick="alert('La opción de mensajes quedará disponible cuando agreguemos el número de WhatsApp.')"
        >
          ✨ Dejar un mensaje
        </button>

      </section>


      <!-- ===================================================
           CIERRE
      ==================================================== -->

      <section class="closing">

        <div>
          ✨ Y vivieron una noche mágica... ✨
        </div>

        <p style="margin-top:12px;">
          Pero esta historia apenas comienza.
        </p>

        <p style="margin-top:10px;">
          Gracias por formar parte de ella.
        </p>

        <div class="closing-name">
          Leydani Troche
        </div>

        <div style="
          font-family:'DM Sans',sans-serif;
          font-size:.75rem;
          letter-spacing:.25em;
          margin-top:12px;
        ">
          XV · 05 · 12 · 2026
        </div>

        <div class="ornament" style="color:#dcb95e;">
          🪷 ✦ 🐸 ✦ 🪷
        </div>

      </section>

    </div>

  </main>


  <!-- =======================================================
       BOTÓN MÚSICA FLOTANTE
  ======================================================== -->

  <button
    class="music-floating"
    id="floatingMusic"
    type="button"
    aria-label="Activar o pausar música"
  >
    🎵
  </button>


  <!-- =======================================================
       YOUTUBE
  ======================================================== -->

  <iframe
    id="youtubePlayer"
    class="youtube-player"
    width="1"
    height="1"
    src="https://www.youtube.com/embed/kYPGwIy-mbI?enablejsapi=1&loop=1&playlist=kYPGwIy-mbI"
    title="Música de la invitación"
    allow="autoplay"
  ></iframe>


</div>


<script>

  /* =========================================================
     ELEMENTOS
  ========================================================= */

  const envelope =
    document.getElementById("envelope");

  const content =
    document.getElementById("content");

  const musicButton =
    document.getElementById("musicButton");

  const floatingMusic =
    document.getElementById("floatingMusic");

  const youtubePlayer =
    document.getElementById("youtubePlayer");


  let musicPlaying = false;


  /* =========================================================
     ABRIR INVITACIÓN
  ========================================================= */

  function openInvitation() {

    if (
      envelope.classList.contains("open")
    ) {
      return;
    }

    envelope.classList.add("open");

    setTimeout(() => {

      content.classList.add("visible");

      floatingMusic.classList.add("visible");

      content.scrollIntoView({
        behavior: "smooth",
        block: "start"
      });

    }, 900);

  }


  envelope.addEventListener(
    "click",
    openInvitation
  );


  envelope.addEventListener(
    "keydown",
    function(event) {

      if (
        event.key === "Enter" ||
        event.key === " "
      ) {

        event.preventDefault();

        openInvitation();

      }

    }
  );


  /* =========================================================
     CUENTA REGRESIVA
     
     IMPORTANTE:
     COMO LA HORA DE LA RECEPCIÓN ESTÁ PENDIENTE,
     TEMPORALMENTE SE UTILIZA 19:00.

     CUANDO TENGAS LA HORA REAL,
     CAMBIA "19:00:00".
  ========================================================= */

  const targetDate =
    new Date(
      "2026-12-05T19:00:00-06:00"
    ).getTime();


  function updateCountdown() {

    const now =
      new Date().getTime();

    const distance =
      targetDate - now;


    if (distance <= 0) {

      document.getElementById(
        "days"
      ).textContent = "0";

      document.getElementById(
        "hours"
      ).textContent = "00";

      document.getElementById(
        "minutes"
      ).textContent = "00";

      document.getElementById(
        "seconds"
      ).textContent = "00";

      return;

    }


    const days =
      Math.floor(
        distance /
        (1000 * 60 * 60 * 24)
      );


    const hours =
      Math.floor(
        (distance %
        (1000 * 60 * 60 * 24)) /
        (1000 * 60 * 60)
      );


    const minutes =
      Math.floor(
        (distance %
        (1000 * 60 * 60)) /
        (1000 * 60)
      );


    const seconds =
      Math.floor(
        (distance %
        (1000 * 60)) /
        1000
      );


    document.getElementById(
      "days"
    ).textContent = days;


    document.getElementById(
      "hours"
    ).textContent =
      String(hours).padStart(2,"0");


    document.getElementById(
      "minutes"
    ).textContent =
      String(minutes).padStart(2,"0");


    document.getElementById(
      "seconds"
    ).textContent =
      String(seconds).padStart(2,"0");

  }


  updateCountdown();

  setInterval(
    updateCountdown,
    1000
  );


  /* =========================================================
     MÚSICA
     
     Video:
     https://youtu.be/kYPGwIy-mbI

     Se reproduce cuando la persona presiona el botón.
  ========================================================= */

  function playMusic() {

    youtubePlayer.contentWindow.postMessage(
      JSON.stringify({
        event: "command",
        func: "playVideo",
        args: []
      }),
      "*"
    );

    musicPlaying = true;

    musicButton.innerHTML =
      "⏸ Pausar música";

  }


  function pauseMusic() {

    youtubePlayer.contentWindow.postMessage(
      JSON.stringify({
        event: "command",
        func: "pauseVideo",
        args: []
      }),
      "*"
    );

    musicPlaying = false;

    musicButton.innerHTML =
      "🎵 Activar música";

  }


  function toggleMusic() {

    if (musicPlaying) {

      pauseMusic();

    } else {

      playMusic();

    }

  }


  musicButton.addEventListener(
    "click",
    toggleMusic
  );


  floatingMusic.addEventListener(
    "click",
    toggleMusic
  );


  /* =========================================================
     WHATSAPP
     
     PENDIENTE
     
     Cuando tengas el número:
     
     1. Busca:
        const whatsappNumber = "";

     2. Escribe el número:
        const whatsappNumber = "521XXXXXXXXXX";
  ========================================================= */

  const whatsappNumber = "";


  const whatsappButton =
    document.getElementById(
      "whatsappButton"
    );


  whatsappButton.addEventListener(
    "click",
    function(event) {

      event.preventDefault();


      if (!whatsappNumber) {

        alert(
          "El número de WhatsApp todavía está pendiente."
        );

        return;

      }


      const message =
        "Hola, confirmo mi asistencia a los XV años de Leydani Troche. 💚✨";


      const url =
        "https://wa.me/" +
        whatsappNumber +
        "?text=" +
        encodeURIComponent(message);


      window.open(
        url,
        "_blank"
      );

    }
  );


  /* =========================================================
     EFECTO DE ENTRADA
  ========================================================= */

  window.addEventListener(
    "load",
    function() {

      document.body.style.opacity = "1";

    }
  );

</script>

</body>
</html># leydani-xv
