<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>AK黙示録騎士 | OFFICIAL</title>

<meta
    name="description"
    content="AK黙示録騎士 - FLASH PARTY CLAN OFFICIAL SITE"
/>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<style>

@import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;600;700;900&family=Noto+Sans+JP:wght@400;500;700;900&display=swap');


/* ==================================================
   RESET
================================================== */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    background: #030303;
    color: #fff;

    font-family:
        "Noto Sans JP",
        sans-serif;

    overflow-x: hidden;
}


/* ==================================================
   COMMON
================================================== */

section {
    position: relative;

    padding:
        110px 20px;

    overflow: hidden;
}

.container {
    width:
        min(1100px, 100%);

    margin:
        0 auto;
}

.section-title {
    position: relative;

    text-align: center;

    margin-bottom: 55px;

    z-index: 2;
}

.section-title .en {
    display: block;

    color: #e60012;

    font-family:
        "Orbitron",
        sans-serif;

    font-size: 11px;

    letter-spacing: 6px;

    margin-bottom: 12px;
}

.section-title h2 {
    font-size: 36px;

    font-weight: 900;

    letter-spacing: 2px;
}

.section-title h2::after {
    content: "";

    display: block;

    width: 60px;
    height: 3px;

    margin:
        18px auto 0;

    background: #e60012;

    box-shadow:
        0 0 20px
        rgba(230,0,18,.9);
}


/* ==================================================
   GLOBAL BACKGROUND
================================================== */

body::before {
    content: "";

    position: fixed;

    inset: 0;

    z-index: -3;

    pointer-events: none;

    background:
        linear-gradient(
            115deg,
            transparent 0%,
            rgba(230,0,18,.025) 42%,
            rgba(230,0,18,.13) 50%,
            transparent 58%
        );
}

body::after {
    content: "";

    position: fixed;

    inset: 0;

    z-index: 999;

    pointer-events: none;

    background:
        repeating-linear-gradient(
            0deg,
            rgba(255,255,255,.015) 0px,
            rgba(255,255,255,.015) 1px,
            transparent 1px,
            transparent 4px
        );

    opacity: .3;
}


/* ==================================================
   HERO
================================================== */

.hero {
    min-height: 100vh;

    display: flex;

    align-items: center;
    justify-content: center;

    text-align: center;

    position: relative;

    overflow: hidden;

    background:
        radial-gradient(
            circle at center,
            rgba(230,0,18,.25),
            transparent 35%
        ),
        linear-gradient(
            135deg,
            #010101,
            #090909 55%,
            #030303
        );
}


/* 巨大ロゴ */

.hero-logo-bg {
    position: absolute;

    width: 850px;

    max-width: 90vw;

    opacity: .055;

    filter:
        grayscale(1)
        drop-shadow(
            0 0 40px
            rgba(230,0,18,.8)
        );

    transform:
        rotate(-8deg);

    pointer-events: none;

    animation:
        slowFloat
        8s
        ease-in-out
        infinite;
}


/* 赤い斜線 */

.hero::before {
    content: "";

    position: absolute;

    width: 160%;
    height: 180px;

    background:
        linear-gradient(
            90deg,
            transparent,
            rgba(230,0,18,.18),
            transparent
        );

    transform:
        rotate(-12deg);

    animation:
        slashMove
        7s
        linear
        infinite;
}


/* グリッド */

.hero::after {
    content: "";

    position: absolute;

    inset: 0;

    background:
        linear-gradient(
            rgba(255,255,255,.025) 1px,
            transparent 1px
        ),
        linear-gradient(
            90deg,
            rgba(255,255,255,.025) 1px,
            transparent 1px
        );

    background-size:
        50px 50px;

    mask-image:
        linear-gradient(
            to bottom,
            transparent,
            black 25%,
            black 75%,
            transparent
        );
}


.hero-content {
    position: relative;

    z-index: 3;

    width: 100%;

    padding: 30px;
}


/* メインロゴ */

.logo {
    width:
        min(280px, 65vw);

    max-height: 280px;

    object-fit: contain;

    margin-bottom: 25px;

    filter:
        drop-shadow(
            0 0 15px
            rgba(230,0,18,.7)
        )
        drop-shadow(
            0 0 45px
            rgba(230,0,18,.35)
        );

    animation:
        logoFloat
        4s
        ease-in-out
        infinite;
}


.hero h1 {
    position: relative;

    font-family:
        "Orbitron",
        sans-serif;

    font-size:
        clamp(
            34px,
            8vw,
            70px
        );

    font-weight: 900;

    letter-spacing: 3px;

    text-shadow:
        0 0 10px
        rgba(230,0,18,.9),

        0 0 30px
        rgba(230,0,18,.5),

        0 0 60px
        rgba(230,0,18,.25);

    animation:
        glitch
        5s
        infinite;
}


.hero-sub {
    margin-top: 14px;

    color: #999;

    font-family:
        "Orbitron",
        sans-serif;

    font-size: 12px;

    letter-spacing: 6px;
}


.est {
    margin-top: 10px;

    color: #555;

    font-family:
        "Orbitron",
        sans-serif;

    font-size: 10px;

    letter-spacing: 4px;
}


/* HERO BUTTON */

.hero-buttons {
    margin-top: 40px;

    display: flex;

    justify-content: center;

    gap: 15px;

    flex-wrap: wrap;
}


.btn {
    position: relative;

    display: inline-flex;

    align-items: center;
    justify-content: center;

    min-width: 160px;

    padding: 15px 30px;

    color: #fff;

    text-decoration: none;

    font-weight: 900;

    letter-spacing: 2px;

    border:
        1px solid #e60012;

    background:
        rgba(230,0,18,.06);

    overflow: hidden;

    transition: .3s;
}


.btn::before {
    content: "";

    position: absolute;

    width: 0;
    height: 100%;

    left: 0;
    top: 0;

    background: #e60012;

    transition: .3s;

    z-index: -1;
}


.btn:hover::before {
    width: 100%;
}


.btn:hover {
    box-shadow:
        0 0 25px
        rgba(230,0,18,.7);

    transform:
        translateY(-4px);
}


.btn-red {
    background: #e60012;
}


.scroll-down {
    position: absolute;

    bottom: 25px;

    left: 50%;

    transform:
        translateX(-50%);

    font-family:
        "Orbitron",
        sans-serif;

    font-size: 9px;

    letter-spacing: 4px;

    color: #555;

    z-index: 4;
}


.scroll-down::after {
    content: "";

    display: block;

    width: 1px;
    height: 35px;

    background: #e60012;

    margin:
        10px auto 0;

    animation:
        scrollLine
        1.5s
        infinite;
}


/* ==================================================
   ABOUT
================================================== */

.about {
    background:
        linear-gradient(
            135deg,
            #080808,
            #050505
        );
}


.about::before {
    content: "AK";

    position: absolute;

    right: -50px;
    bottom: -100px;

    font-family:
        "Orbitron",
        sans-serif;

    font-size: 300px;

    font-weight: 900;

    color:
        rgba(230,0,18,.025);

    pointer-events: none;
}


.about-box {
    max-width: 850px;

    margin: auto;

    padding: 45px;

    position: relative;

    background:
        linear-gradient(
            135deg,
            #121212,
            #070707
        );

    border:
        1px solid #222;

    border-left:
        3px solid #e60012;

    box-shadow:
        0 0 50px
        rgba(0,0,0,.8);
}


.about-box::after {
    content:
        "AK MOKUSHIROKU KISHI";

    position: absolute;

    right: 20px;
    bottom: 15px;

    color: #222;

    font-family:
        "Orbitron",
        sans-serif;

    font-size: 9px;

    letter-spacing: 2px;
}


.about-box p {
    color: #bbb;

    line-height: 2.2;

    text-align: center;

    font-size: 15px;
}


/* ==================================================
   STATS
================================================== */

.stats {
    padding:
        60px 20px;

    background: #030303;

    border-top:
        1px solid #151515;

    border-bottom:
        1px solid #151515;
}


.stats-grid {
    display: grid;

    grid-template-columns:
        repeat(3, 1fr);

    max-width: 800px;

    margin: auto;
}


.stat {
    text-align: center;

    padding: 20px;

    border-right:
        1px solid #222;
}


.stat:last-child {
    border-right: none;
}


.stat-number {
    display: block;

    font-family:
        "Orbitron",
        sans-serif;

    font-size: 38px;

    font-weight: 900;

    color: #e60012;

    text-shadow:
        0 0 20px
        rgba(230,0,18,.5);
}


.stat-label {
    display: block;

    margin-top: 8px;

    color: #666;

    font-family:
        "Orbitron",
        sans-serif;

    font-size: 10px;

    letter-spacing: 3px;
}


/* ==================================================
   MEMBERS
================================================== */

.members {
    background: #050505;
}


.member-list {
    display: grid;

    grid-template-columns:
        repeat(3, 1fr);

    gap: 18px;
}


.member {
    position: relative;

    min-height: 260px;

    background: #0c0c0c;

    border:
        1px solid #222;

    overflow: hidden;

    transition: .4s;
}


.member::before {
    content: "";

    position: absolute;

    left: 0;
    top: 0;

    width: 3px;
    height: 100%;

    background: #e60012;

    box-shadow:
        0 0 20px
        rgba(230,0,18,.8);

    z-index: 3;
}


.member:hover {
    transform:
        translateY(-8px);

    border-color:
        #e60012;

    box-shadow:
        0 15px 40px
        rgba(0,0,0,.8),

        0 0 25px
        rgba(230,0,18,.12);
}


.member-image {
    position: absolute;

    inset: 0;

    width: 100%;
    height: 100%;

    object-fit: cover;

    opacity: .65;

    transition: .5s;

    filter:
        grayscale(.35);
}


.member:hover .member-image {
    transform:
        scale(1.08);

    opacity: .85;

    filter:
        grayscale(0);
}


.member-overlay {
    position: absolute;

    inset: 0;

    background:
        linear-gradient(
            to top,
            #050505 0%,
            rgba(5,5,5,.8) 35%,
            transparent 75%
        );
}


.member-content {
    position: absolute;

    left: 20px;
    right: 20px;
    bottom: 18px;

    z-index: 3;
}


.member-number {
    color: #e60012;

    font-family:
        "Orbitron",
        sans-serif;

    font-size: 10px;

    letter-spacing: 2px;
}


.member-name {
    display: block;

    margin-top: 5px;

    font-size: 21px;

    font-weight: 900;
}


.member-role {
    display: block;

    margin-top: 4px;

    color: #666;

    font-family:
        "Orbitron",
        sans-serif;

    font-size: 9px;

    letter-spacing: 2px;
}


/* ==================================================
   MATCH RESULTS
================================================== */

.results {
    background:
        linear-gradient(
            135deg,
            #090909,
            #050505
        );
}


.match {
    position: relative;

    padding: 35px;

    margin-bottom: 20px;

    background: #0d0d0d;

    border:
        1px solid #242424;

    overflow: hidden;

    transition: .3s;
}


.match:hover {
    border-color:
        #e60012;

    box-shadow:
        0 0 30px
        rgba(230,0,18,.12);
}


.match::before {
    content:
        "CLAN BATTLE";

    position: absolute;

    top: 15px;
    right: 20px;

    font-family:
        "Orbitron",
        sans-serif;

    font-size: 9px;

    letter-spacing: 3px;

    color: #333;
}


.match-date {
    text-align: center;

    color: #555;

    font-family:
        "Orbitron",
        sans-serif;

    font-size: 10px;

    letter-spacing: 3px;

    margin-bottom: 25px;
}


.match-vs {
    display: grid;

    grid-template-columns:
        1fr auto 1fr;

    align-items: center;

    gap: 25px;
}


.team {
    text-align: center;
}


.team-name {
    font-size: 19px;

    font-weight: 900;
}


.team-tag {
    display: block;

    margin-top: 5px;

    color: #555;

    font-family:
        "Orbitron",
        sans-serif;

    font-size: 9px;

    letter-spacing: 2px;
}


.vs {
    font-family:
        "Orbitron",
        sans-serif;

    font-size: 15px;

    font-weight: 900;

    color: #e60012;

    text-shadow:
        0 0 15px
        rgba(230,0,18,.7);
}


.match-bottom {
    display: flex;

    align-items: center;

    justify-content: center;

    gap: 20px;

    margin-top: 25px;
}


.result-win {
    color: #e60012;

    font-family:
        "Orbitron",
        sans-serif;

    font-weight: 900;

    font-size: 12px;

    letter-spacing: 2px;
}


.match-score {
    font-family:
        "Orbitron",
        sans-serif;

    font-size: 28px;

    font-weight: 900;
}


/* ==================================================
   NEWS
================================================== */

.news {
    background: #050505;
}


.news-list {
    max-width: 850px;

    margin: auto;
}


.news-card {
    display: flex;

    align-items: center;

    gap: 25px;

    padding: 25px;

    margin-bottom: 15px;

    background: #0d0d0d;

    border:
        1px solid #222;

    transition: .3s;

    position: relative;
}


.news-card:hover {
    border-color:
        #e60012;

    transform:
        translateX(6px);
}


.news-date {
    min-width: 90px;

    color: #e60012;

    font-family:
        "Orbitron",
        sans-serif;

    font-size: 10px;

    letter-spacing: 1px;
}


.news-line {
    width: 1px;

    height: 35px;

    background: #333;
}


.news-title {
    font-size: 16px;

    font-weight: 900;
}


/* ==================================================
   JOIN / SOCIAL
================================================== */

.join {
    text-align: center;

    background:
        radial-gradient(
            circle at center,
            rgba(230,0,18,.22),
            transparent 55%
        ),
        #050505;
}


.join::before {
    content: "";

    position: absolute;

    width: 600px;
    height: 600px;

    border:
        1px solid
        rgba(230,0,18,.08);

    border-radius: 50%;

    left: 50%;
    top: 50%;

    transform:
        translate(-50%, -50%);

    animation:
        rotate
        30s
        linear
        infinite;
}


.join p {
    position: relative;

    color: #aaa;

    margin:
        20px 0 30px;

    z-index: 2;
}


/* SNS BUTTON AREA */

.social-buttons {
    position: relative;

    display: grid;

    grid-template-columns:
        repeat(
            2,
            minmax(250px, 1fr)
        );

    gap: 18px;

    max-width: 700px;

    margin:
        35px auto 0;

    z-index: 3;
}


.social-btn {
    position: relative;

    display: flex;

    align-items: center;

    min-height: 88px;

    padding:
        15px 20px;

    color: #fff;

    text-decoration: none;

    background:
        linear-gradient(
            135deg,
            rgba(20,20,20,.95),
            rgba(5,5,5,.95)
        );

    border:
        1px solid #292929;

    overflow: hidden;

    transition:
        transform .3s ease,
        border-color .3s ease,
        box-shadow .3s ease;
}


/* 赤いライン */

.social-btn::before {
    content: "";

    position: absolute;

    top: 0;
    left: 0;

    width: 100%;
    height: 2px;

    background: #e60012;

    transform:
        scaleX(0);

    transform-origin:
        left;

    transition:
        transform .4s ease;
}


/* 斜線 */

.social-btn::after {
    content: "";

    position: absolute;

    top: -60px;
    right: -80px;

    width: 220px;
    height: 220px;

    background:
        repeating-linear-gradient(
            135deg,
            transparent 0,
            transparent 8px,
            rgba(255,255,255,.025) 8px,
            rgba(255,255,255,.025) 10px
        );

    transform:
        rotate(15deg);

    pointer-events: none;
}


.social-btn:hover {
    transform:
        translateY(-5px);

    border-color:
        #e60012;

    box-shadow:
        0 10px 35px
        rgba(0,0,0,.8),

        0 0 25px
        rgba(230,0,18,.18);
}


.social-btn:hover::before {
    transform:
        scaleX(1);
}


/* SNS ICON */

.social-icon {
    position: relative;

    display: flex;

    align-items: center;
    justify-content: center;

    width: 54px;
    height: 54px;

    margin-right: 17px;

    flex-shrink: 0;

    color: #fff;

    background: #050505;

    border:
        1px solid #333;

    z-index: 2;

    transition: .3s;
}


.social-icon svg {
    width: 27px;
    height: 27px;

    display: block;
}


.social-btn:hover .social-icon {
    border-color:
        #e60012;

    box-shadow:
        0 0 20px
        rgba(230,0,18,.3);

    transform:
        scale(1.05);
}


/* TikTokカラーアクセント */

.tiktok-btn .social-icon::before {
    content: "";

    position: absolute;

    inset: 0;

    border:
        1px solid
        rgba(0,242,234,.18);

    transform:
        translate(2px, 2px);

    pointer-events: none;
}


.tiktok-btn .social-icon::after {
    content: "";

    position: absolute;

    inset: 0;

    border:
        1px solid
        rgba(255,0,80,.15);

    transform:
        translate(-2px, -2px);

    pointer-events: none;
}


/* SNS TEXT */

.social-text {
    position: relative;

    display: flex;

    flex-direction: column;

    align-items: flex-start;

    z-index: 2;
}


.social-text small {
    color: #666;

    font-family:
        "Orbitron",
        sans-serif;

    font-size: 8px;

    letter-spacing: 2px;

    margin-bottom: 5px;
}


.social-text strong {
    font-family:
        "Orbitron",
        sans-serif;

    font-size: 14px;

    letter-spacing: 1px;
}


/* ARROW */

.social-arrow {
    position: relative;

    margin-left: auto;

    color: #555;

    font-family:
        "Orbitron",
        sans-serif;

    font-size: 20px;

    z-index: 2;

    transition: .3s;
}


.social-btn:hover .social-arrow {
    color: #e60012;

    transform:
        translate(
            4px,
            -4px
        );
}


/* ==================================================
   FOOTER
================================================== */

footer {
    padding:
        40px 20px;

    text-align: center;

    border-top:
        1px solid #222;

    color: #444;

    font-family:
        "Orbitron",
        sans-serif;

    font-size: 9px;

    letter-spacing: 3px;
}


/* ==================================================
   SCROLL ANIMATION
================================================== */

.reveal {
    opacity: 0;

    transform:
        translateY(35px);

    transition:
        opacity .8s ease,
        transform .8s ease;
}


.reveal.active {
    opacity: 1;

    transform:
        translateY(0);
}


/* ==================================================
   ANIMATIONS
================================================== */

@keyframes rotate {

    from {
        transform:
            rotate(0deg);
    }

    to {
        transform:
            rotate(360deg);
    }

}


@keyframes logoFloat {

    0%, 100% {
        transform:
            translateY(0);
    }

    50% {
        transform:
            translateY(-8px);
    }

}


@keyframes slowFloat {

    0%, 100% {
        transform:
            rotate(-8deg)
            scale(1);
    }

    50% {
        transform:
            rotate(-5deg)
            scale(1.04);
    }

}


@keyframes slashMove {

    0% {
        transform:
            translateX(-100%)
            rotate(-12deg);
    }

    100% {
        transform:
            translateX(100%)
            rotate(-12deg);
    }

}


@keyframes scrollLine {

    0% {
        opacity: 0;

        transform:
            scaleY(0);

        transform-origin:
            top;
    }

    50% {
        opacity: 1;

        transform:
            scaleY(1);

        transform-origin:
            top;
    }

    100% {
        opacity: 0;

        transform:
            scaleY(1);

        transform-origin:
            bottom;
    }

}


@keyframes glitch {

    0%, 92%, 100% {
        transform:
            translate(0);
    }

    93% {
        transform:
            translate(
                2px,
                -1px
            );
    }

    94% {
        transform:
            translate(
                -2px,
                1px
            );
    }

    95% {
        transform:
            translate(0);
    }

}


/* ==================================================
   TABLET
================================================== */

@media (max-width: 800px) {

    section {
        padding:
            85px 15px;
    }


    .member-list {
        grid-template-columns:
            repeat(
                2,
                1fr
            );
    }


    .stats-grid {
        grid-template-columns:
            repeat(
                3,
                1fr
            );
    }


    .stat-number {
        font-size: 28px;
    }

}


/* ==================================================
   MOBILE
================================================== */

@media (max-width: 600px) {

    section {
        padding:
            70px 15px;
    }


    .hero h1 {
        letter-spacing:
            1px;
    }


    .hero-sub {
        letter-spacing:
            3px;
    }


    .hero-logo-bg {
        width:
            600px;
    }


    .section-title h2 {
        font-size:
            28px;
    }


    .member-list {
        grid-template-columns:
            1fr;
    }


    .member {
        min-height:
            230px;
    }


    .stats {
        padding:
            40px 15px;
    }


    .stat {
        padding:
            10px 5px;
    }


    .stat-number {
        font-size:
            25px;
    }


    .stat-label {
        font-size:
            8px;

        letter-spacing:
            1px;
    }


    .about-box {
        padding:
            30px 20px;
    }


    .match {
        padding:
            28px 15px;
    }


    .match-vs {
        gap:
            10px;
    }


    .team-name {
        font-size:
            15px;
    }


    .match-score {
        font-size:
            24px;
    }


    .news-card {
        gap:
            12px;

        align-items:
            flex-start;
    }


    .news-date {
        min-width:
            75px;

        font-size:
            9px;
    }


    .news-title {
        font-size:
            14px;
    }


    .social-buttons {
        grid-template-columns:
            1fr;

        max-width:
            400px;
    }


    .social-btn {
        min-height:
            82px;
    }

}

</style>
</head>


<body>


<!-- ==================================================
     HERO
================================================== -->

<header class="hero">

    <!-- 巨大背景ロゴ -->

    <img
        src="sfUqRIPD.jpg"
        alt=""
        class="hero-logo-bg"
    >


    <div class="hero-content">

        <!-- メインロゴ -->

        <img
            src="sfUqRIPD.jpg"
            alt="AK黙示録騎士"
            class="logo"
        >


        <h1>
            AK黙示録騎士
        </h1>


        <div class="hero-sub">
            FLASH PARTY CLAN
        </div>


        <div class="est">
            CLAN EST. 2026
        </div>


        <div class="hero-buttons">

            <a
                href="#members"
                class="btn btn-red"
            >
                MEMBERS
            </a>


            <a
                href="#results"
                class="btn"
            >
                MATCH RESULTS
            </a>

        </div>

    </div>


    <div class="scroll-down">
        SCROLL
    </div>

</header>


<!-- ==================================================
     ABOUT
================================================== -->

<section class="about">

    <div class="container reveal">

        <div class="section-title">

            <span class="en">
                WHO WE ARE
            </span>

            <h2>
                ABOUT US
            </h2>

        </div>


        <div class="about-box">

            <p>
                AK黙示録騎士は、<br>
                FLASH PARTYを中心に活動するゲームクラン。<br><br>

                仲間と共に戦い、<br>
                勝利を目指す。
            </p>

        </div>

    </div>

</section>


<!-- ==================================================
     STATS
================================================== -->

<section class="stats">

    <div class="container">

        <div class="stats-grid">

            <div class="stat reveal">

                <span class="stat-number">
                    2
                </span>

                <span class="stat-label">
                    MATCHES
                </span>

            </div>


            <div class="stat reveal">

                <span class="stat-number">
                    2
                </span>

                <span class="stat-label">
                    WINS
                </span>

            </div>


            <div class="stat reveal">

                <span class="stat-number">
                    100%
                </span>

                <span class="stat-label">
                    WIN RATE
                </span>

            </div>

        </div>

    </div>

</section>


<!-- ==================================================
     MEMBERS
================================================== -->

<section
    class="members"
    id="members"
>

    <div class="container reveal">

        <div class="section-title">

            <span class="en">
                OUR PLAYERS
            </span>

            <h2>
                MEMBERS
            </h2>

        </div>


        <div class="member-list">


            <!-- MEMBER 01 -->

            <div class="member">

                <img
                    src="images/member01.jpg"
                    alt="ミミズク"
                    class="member-image"
                >

                <div class="member-overlay"></div>

                <div class="member-content">

                    <span class="member-number">
                        PLAYER 01
                    </span>

                    <span class="member-name">
                        ミミズク
                    </span>

                    <span class="member-role">
                        FLASH PARTY PLAYER
                    </span>

                </div>

            </div>


            <!-- MEMBER 02 -->

            <div class="member">

                <img
                    src="images/member02.jpg"
                    alt="はゆ"
                    class="member-image"
                >

                <div class="member-overlay"></div>

                <div class="member-content">

                    <span class="member-number">
                        PLAYER 02
                    </span>

                    <span class="member-name">
                        はゆ
                    </span>

                    <span class="member-role">
                        FLASH PARTY PLAYER
                    </span>

                </div>

            </div>


            <!-- MEMBER 03 -->

            <div class="member">

                <img
                    src="images/member03.jpg"
                    alt="ステック"
                    class="member-image"
                >

                <div class="member-overlay"></div>

                <div class="member-content">

                    <span class="member-number">
                        PLAYER 03
                    </span>

                    <span class="member-name">
                        ステック
                    </span>

                    <span class="member-role">
                        FLASH PARTY PLAYER
                    </span>

                </div>

            </div>


            <!-- MEMBER 04 -->

            <div class="member">

                <img
                    src="images/member04.jpg"
                    alt="Oct."
                    class="member-image"
                >

                <div class="member-overlay"></div>

                <div class="member-content">

                    <span class="member-number">
                        PLAYER 04
                    </span>

                    <span class="member-name">
                        Oct.
                    </span>

                    <span class="member-role">
                        FLASH PARTY PLAYER
                    </span>

                </div>

            </div>


            <!-- MEMBER 05 -->

            <div class="member">

                <img
                    src="images/member05.jpg"
                    alt="あるちぬ"
                    class="member-image"
                >

                <div class="member-overlay"></div>

                <div class="member-content">

                    <span class="member-number">
                        PLAYER 05
                    </span>

                    <span class="member-name">
                        あるちぬ
                    </span>

                    <span class="member-role">
                        FLASH PARTY PLAYER
                    </span>

                </div>

            </div>


            <!-- MEMBER 06 -->

            <div class="member">

                <img
                    src="images/member06.jpg"
                    alt="Puppy"
                    class="member-image"
                >

                <div class="member-overlay"></div>

                <div class="member-content">

                    <span class="member-number">
                        PLAYER 06
                    </span>

                    <span class="member-name">
                        Puppy
                    </span>

                    <span class="member-role">
                        FLASH PARTY PLAYER
                    </span>

                </div>

            </div>


            <!-- MEMBER 07 -->

            <div class="member">

                <img
                    src="images/member07.jpg"
                    alt="もなか"
                    class="member-image"
                >

                <div class="member-overlay"></div>

                <div class="member-content">

                    <span class="member-number">
                        PLAYER 07
                    </span>

                    <span class="member-name">
                        もなか
                    </span>

                    <span class="member-role">
                        FLASH PARTY PLAYER
                    </span>

                </div>

            </div>


        </div>

    </div>

</section>


<!-- ==================================================
     MATCH RESULTS
================================================== -->

<section
    class="results"
    id="results"
>

    <div class="container reveal">

        <div class="section-title">

            <span class="en">
                CLAN BATTLE RECORD
            </span>

            <h2>
                MATCH RESULTS
            </h2>

        </div>


        <!-- MATCH 01 -->

        <div class="match">

            <div class="match-date">
                2026.08.22
            </div>


            <div class="match-vs">

                <div class="team">

                    <div class="team-name">
                        AK黙示録騎士
                    </div>

                    <span class="team-tag">
                        AK
                    </span>

                </div>


                <div class="vs">
                    VS
                </div>


                <div class="team">

                    <div class="team-name">
                        でかすぎ CLAN
                    </div>

                    <span class="team-tag">
                        OPPONENT
                    </span>

                </div>

            </div>


            <div class="match-bottom">

                <span class="result-win">
                    WIN
                </span>

                <span class="match-score">
                    10 - 0
                </span>

            </div>

        </div>


        <!-- MATCH 02 -->

        <div class="match">

            <div class="match-date">
                2026.07.26
            </div>


            <div class="match-vs">

                <div class="team">

                    <div class="team-name">
                        AK黙示録騎士
                    </div>

                    <span class="team-tag">
                        AK
                    </span>

                </div>


                <div class="vs">
                    VS
                </div>


                <div class="team">

                    <div class="team-name">
                        OTL CLAN
                    </div>

                    <span class="team-tag">
                        OPPONENT
                    </span>

                </div>

            </div>


            <div class="match-bottom">

                <span class="result-win">
                    WIN
                </span>

                <span class="match-score">
                    3 - 0
                </span>

            </div>

        </div>

    </div>

</section>


<!-- ==================================================
     NEWS
================================================== -->

<section
    class="news"
    id="news"
>

    <div class="container reveal">

        <div class="section-title">

            <span class="en">
                LATEST INFORMATION
            </span>

            <h2>
                NEWS
            </h2>

        </div>


        <div class="news-list">


            <div class="news-card">

                <div class="news-date">
                    2026.08.26
                </div>

                <div class="news-line"></div>

                <div class="news-title">
                    AK黙示録騎士 OFFICIAL SITE OPEN
                </div>

            </div>


            <div class="news-card">

                <div class="news-date">
                    2026.08.26
                </div>

                <div class="news-line"></div>

                <div class="news-title">
                    CLAN MEMBER RECRUITMENT
                </div>

            </div>


        </div>

    </div>

</section>


<!-- ==================================================
     OFFICIAL SOCIALS
================================================== -->

<section class="join">

    <div class="container">


        <div class="section-title">

            <span class="en">
                OFFICIAL SOCIALS
            </span>

            <h2>
                JOIN AK
            </h2>

        </div>


        <p>
            AK黙示録騎士の最新情報をチェック。
        </p>


        <div class="social-buttons">


            <!-- =========================
                 X
            ========================== -->

            <a
                href="https://x.com/AKclan_FP"
                target="_blank"
                rel="noopener noreferrer"
                class="social-btn x-btn"
            >

                <span class="social-icon">

                    <svg
                        viewBox="0 0 24 24"
                        aria-hidden="true"
                    >

                        <path
                            d="M18.244 2.25h3.308l-7.227 8.26
                            8.502 11.24h-6.657l-5.214-6.817
                            -5.963 6.817H1.684l7.73-8.835
                            L1.254 2.25H8.08l4.713 6.231
                            5.45-6.231Zm-1.161 17.52h1.833
                            L7.084 4.126H5.117L17.083 19.77Z"
                            fill="currentColor"
                        />

                    </svg>

                </span>


                <span class="social-text">

                    <small>
                        FOLLOW US
                    </small>

                    <strong>
                        X / TWITTER
                    </strong>

                </span>


                <span class="social-arrow">
                    ↗
                </span>

            </a>


            <!-- =========================
                 TIKTOK
            ========================== -->

            <a
                href="https://www.tiktok.com/@ak16735?_r=1&_t=ZS-99CvVNqpGBY"
                target="_blank"
                rel="noopener noreferrer"
                class="social-btn tiktok-btn"
            >

                <span class="social-icon">

                    <svg
                        viewBox="0 0 24 24"
                        aria-hidden="true"
                    >

                        <path
                            d="M19.59 6.69a4.83 4.83 0 0 1-3.77-4.24V2h-3.45
                            v13.67a2.92 2.92 0 1 1-2.92-2.92c.31 0 .61.05.89.14
                            v-3.52a6.35 6.35 0 1 0 5.48 6.3V8.36
                            a8.25 8.25 0 0 0 4.83 1.56V6.69h-1.06Z"
                            fill="currentColor"
                        />

                    </svg>

                </span>


                <span class="social-text">

                    <small>
                        FOLLOW US
                    </small>

                    <strong>
                        TIKTOK
                    </strong>

                </span>


                <span class="social-arrow">
                    ↗
                </span>

            </a>


        </div>

    </div>

</section>


<!-- ==================================================
     FOOTER
================================================== -->

<footer>

    © 2026 AK MOKUSHIROKU KISHI

</footer>


<!-- ==================================================
     JAVASCRIPT
================================================== -->

<script>


/* =========================================
   SCROLL REVEAL
========================================= */

const reveals =
    document.querySelectorAll(
        ".reveal"
    );


const observer =
    new IntersectionObserver(

        (entries) => {

            entries.forEach(
                (entry) => {

                    if (
                        entry.isIntersecting
                    ) {

                        entry.target
                            .classList
                            .add("active");

                    }

                }
            );

        },

        {
            threshold: 0.15
        }

    );


reveals.forEach(
    (element) => {

        observer.observe(
            element
        );

    }
);


</script>


</body>
</html>
