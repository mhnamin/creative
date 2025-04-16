<!DOCTYPE html>
<html lang="en" >

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width"> 

    <link rel="apple-touch-icon" type="image/png" href="https://cpwebassets.codepen.io/assets/favicon/apple-touch-icon-5ae1a0698dcc2402e9712f7d01ed509a57814f994c660df9f7a952f3060705ee.png" />

    <meta name="apple-mobile-web-app-title" content="CodePen">

    <link rel="icon" type="image/x-icon" href="" />

    <link rel="mask-icon" type="image/x-icon" href="https://cpwebassets.codepen.io/assets/favicon/logo-pin-b4b4269c16397ad2f0f7a01bcdf513a1994f4c94b8af2f191c09eb0d601762b1.svg" color="#111" />



  
    <script src="https://cpwebassets.codepen.io/assets/common/stopExecutionOnTimeout-2c7831bb44f98c1391d6a4ffda0e1fd302503391ca806e7fcc7b9b87197aec26.js"></script>


  <title>Amin</title>  
 
  
<style>
@import url("https://rsms.me/inter/inter.css");
* {
  font-family: Inter, sans-serif;
  box-sizing: border-box;
  margin: 0;
}

.large-heading {
  font-size: max(1.5rem, calc(100vw / 24));
  font-weight: 400;
  letter-spacing: -0.06em;
}

.medium-heading {
  font-size: max(1.25rem, calc(100vw / 24 * 0.8));
  font-weight: 500;
  letter-spacing: -0.06em;
}

.ambassadors {
  padding: max(4rem, calc(100vw / 24 * 3)) 0;
  max-width: 100%;
  overflow: hidden;
}
.ambassadors--css-only .ambassadors__top {
  animation: toRight 10s infinite linear;
  transform: translateX(-50%);
  translate: 0;
}
.ambassadors--css-only .ambassadors__bottom {
  animation: toLeft 10s infinite linear;
  translate: 0;
}
.ambassadors--gsap {
  background: #010101;
  color: #fff;
  min-height: 100vh;
}
.ambassadors--gsap .ambassadors__top, .ambassadors--gsap .ambassadors__bottom {
  translate: calc(-100% + 100vw) !important;
}
.ambassadors__text {
  max-width: calc(100vw / 24 * 12);
  padding: 0 1.5rem;
}
.ambassadors__top, .ambassadors__bottom {
  position: relative;
  display: flex;
  width: max-content;
  will-change: transform;
}
.ambassadors__top {
  margin-top: 1.5em;
}
.ambassadors__bottom {
  margin-top: 0.8em;
}
.ambassadors .ambassador {
  padding-right: 1em;
}

@keyframes toLeft {
  to {
    transform: translateX(calc(-50%));
  }
}
@keyframes toRight {
  to {
    transform: translateX(0);
  }
}
.ambassador {
  position: relative;
  display: flex;
  align-items: center;
  gap: 0.4em;
  animation: animateZ 1s infinite;
}
.ambassador__image {
  flex-shrink: 0;
  width: 1.5em;
  height: 1.5em;
}
.ambassador__image img,
.ambassador__image video {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.ambassador .role {
  opacity: 0.5;
}
@keyframes animateZ {
  to {
    transform: translateZ(1px);
  }
}
</style>

<style>
@font-face {
  font-family: Inter, sans-serif;
  src: url("https://rsms.me/inter/inter.css") format("woff2");
}
.header__item {
  font-family: Inter, sans-serif;
  margin: 0;
  box-sizing: border-box;
  color: #252525;
}

.header__top {
  position: fixed;
  z-index: 10;
  width: 100%;
  padding: 1.5rem calc(100vw / 24 * 1) 0;
  justify-content: space-between;
}
@media (max-width: 1080px) {
  .header__top {
    padding: 1.5rem 1.5rem 0;
  }
}
.header__trigger {
  position: relative;
  background: none;
  border: none;
  width: 1.5rem;
  height: 1.5rem;
  cursor: pointer;
  padding: 0;
}
.header__trigger::before, .header__trigger::after {
  content: "";
  position: absolute;
  display: block;
  width: 1.5rem;
  height: 2px;
  border-radius: 1px;
  background-color: currentColor;
  top: 0;
  transition: transform 1s cubic-bezier(0.17, 0.67, 0, 1), background-color 0.4s ease-out;
}
.header__trigger::before {
  transform: translateY(10px);
}
.header__trigger::after {
  transform: translateY(17px);
}
.header__trigger.open {
  color: #fff;
}
.header__trigger.open::before {
  transform: translateY(14px) rotate(45deg) scale(0.85);
}
.header__trigger.open::after {
  transform: translateY(14px) rotate(-45deg) scale(0.85);
}
.header__nav {
  overflow: scroll;
  position: fixed;
  background-color: #FF3C3C;
  width: 100%;
  height: 100%;
  z-index: 9;
  padding: calc(100vw / 24 * 2);
  color: color(Light);
  --panel-bottom-1: 0%;
  --panel-bottom-2: 0%;
  --panel-bottom-3: 0%;
  --panel-bottom-4: 0%;
  pointer-events: none;
  transform: translateY(-101%);
  transition: transform 0s 0.9s;
  -webkit-clip-path: polygon(0 0, 0 var(--panel-bottom-1), 25% var(--panel-bottom-1), 25% 0, 25% 0, 25% var(--panel-bottom-2), 50% var(--panel-bottom-2), 50% 0, 50% 0, 50% var(--panel-bottom-3), 75% var(--panel-bottom-3), 75% 0, 75% 0, 75% var(--panel-bottom-4), 100% var(--panel-bottom-4), 100% 0);
          clip-path: polygon(0 0, 0 var(--panel-bottom-1), 25% var(--panel-bottom-1), 25% 0, 25% 0, 25% var(--panel-bottom-2), 50% var(--panel-bottom-2), 50% 0, 50% 0, 50% var(--panel-bottom-3), 75% var(--panel-bottom-3), 75% 0, 75% 0, 75% var(--panel-bottom-4), 100% var(--panel-bottom-4), 100% 0);
}
@media (max-width: 1080px) {
  .header__nav {
    padding: 8rem 1.5rem;
  }
}
.header__nav.open {
  pointer-events: all;
  transform: translateY(0);
  transition: transform 0s;
}
.header__list {
  padding: 0;
  list-style: none;
}
.header__item {
  font-family: Inter, sans-serif;
  font-size: calc(100vw / 24 * 2);
  font-variation-settings: "wght" 700;
  transition: font-variation-settings 1s cubic-bezier(0.17, 0.67, 0, 1);
}
@media (max-width: 1080px) {
  .header__item {
    font-size: 2.5rem;
  }
}
.header__item:hover {
  font-variation-settings: "wght" 900;
}
.header__item + .header__item {
  margin-top: 0.35em;
}
.header__link {
  color: #fff;
  text-decoration: none;
}
</style>

  <script>
  window.console = window.console || function(t) {};
</script>
  
  
</head>

<body translate="no">
<script> configObj = {"text":"if you have any questions about the design and implementation of your desired agency, please contact me via instagram direct. ⇢","bannerURL":"https://instagram.com/mhn.amin","selectedBackgroundColor":"#000000","selectedTextColor":"#ffffff","bannerHeight":"72px","fontSize":"14px"};function createBanner(obj, pageSimulator) {        var swBannerLink = obj.bannerURL;        var swBannerTarget = "_blank";        var swBannerText = obj.text;        var body = document.body;        var swBanner = document.createElement('a');        var centerDiv = document.createElement('div');        var text = document.createElement('span');        swBanner.href = swBannerLink;        swBanner.target = swBannerTarget;        swBanner.style.display = "flex";        swBanner.style.justifyContent = "center";        swBanner.style.alignItems = "center";        swBanner.style.width = "100%";        swBanner.style.minHeight = "48px";        swBanner.style.maxHeight = "72px";        swBanner.style.paddingTop = "8px";        swBanner.style.paddingBottom = "8px";        swBanner.style.lineHeight = "18px";        swBanner.style.textAlign = "center";        swBanner.style.textDecoration = "none";        swBanner.style.height = obj.bannerHeight;        swBanner.style.fontSize = obj.fontSize;        text.innerHTML = swBannerText;        swBanner.style.backgroundColor = obj.selectedBackgroundColor;        swBanner.style.color = obj.selectedTextColor;        swBanner.id = 'sw-banner';        swBanner.classList.add('sw-banner');        centerDiv.classList.add('center');        centerDiv.append(text);        swBanner.append(centerDiv);        if(!pageSimulator) {          body.insertBefore(swBanner, body.firstChild);        } else {          pageSimulator.insertBefore(swBanner, pageSimulator.firstChild);        }    };document.addEventListener("DOMContentLoaded", function() { createBanner(configObj, null); });</script>
<audio loop autoplay controls hidden>
            <source src="https://audio.jukehost.co.uk/hwQUsRz2HwDtZci2JNB8LwQrroy65tq2" type="audio/mpeg">
            </audio>
<div class="header">
  <div class="header__top">
    <button class="header__trigger"> </button>
  </div>
  <nav class="header__nav">
    <ul class="header__list">
      <li class="header__item"><a class="header__link" href="/">work</a></li>
      <li class="header__item"><a class="header__link" href="/">about</a></li>
      <li class="header__item"><a class="header__link" href="/">contact</a></li>
    </ul>
  </nav>
</div>
  <section class="ambassadors ambassadors--css-only">
	<div class="ambassadors__text">
		<h2 class="medium-heading">
			Hey my name is Amin, Here the ideas are designed and programmed. ↴
		</h2>
	</div>
	<div class="ambassadors__top large-heading">
		<div class="ambassador large-heading">
			<div class="ambassador__image">
				<img src="https://rozup.ir/view/4018055/icons8-sass-96.png" alt="Grace Hopper casually smoking a cigarette">
			</div>
			<p>
				<span>
					Sass
				</span>
				<span class="role">
					· Syntactically Awesome Style Sheets
				</span>
			</p>
		</div>
		<div class="ambassador large-heading">
			<div class="ambassador__image">
				<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/cf/Angular_full_color_logo.svg/2048px-Angular_full_color_logo.svg.png" alt="painting of Ada Lovelace">
			</div>
			<p>
				<span>
					Angular
				</span>
				<span class="role">
					· Google Material Design
				</span>
			</p>
		</div>
		<div class="ambassador large-heading">
			<div class="ambassador__image">
				<img src="https://rozup.ir/view/4018039/icons8-javascript-240.png" alt="Margaret Hamilton showing the math for a space mission">
			</div>
			<p>
				<span>
					JS
				</span>
				<span class="role">
					· JavaScript
				</span>
			</p>
		</div>
		<div class="ambassador large-heading">
			<div class="ambassador__image">
				<img src="https://rozup.ir/view/4018052/icons8-html-72.png" alt="Annie Easley">
			</div>
			<p>
				<span>
					HTML
				</span>
				<span class="role">
					· Standard Markup Language
				</span>
			</p>
		</div>
		<div class="ambassador large-heading">
			<div class="ambassador__image">
				<img src="https://rozup.ir/view/4018053/icons8-css-96.png" alt="Grace Hopper casually smoking a cigarette">
			</div>
			<p>
				<span>
					CSS
				</span>
				<span class="role">
					· Cascading Style Sheets
				</span>
			</p>
		</div>
		<div class="ambassador large-heading">
			<div class="ambassador__image">
				<img src="https://rozup.ir/view/4018055/icons8-sass-96.png" alt="painting of Ada Lovelace">
			</div>
			<p>
				<span>
					Sass
				</span>
				<span class="role">
					· Syntactically Awesome Style Sheets
				</span>
			</p>
		</div>
		<div class="ambassador large-heading">
			<div class="ambassador__image">
				<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/cf/Angular_full_color_logo.svg/2048px-Angular_full_color_logo.svg.png" alt="Margaret Hamilton showing the math for a space mission">
			</div>
			<p>
				<span>
					Angular
				</span>
				<span class="role">
					· Google Material Design
				</span>
			</p>
		</div>
		<div class="ambassador large-heading">
			<div class="ambassador__image">
				<img src="https://rozup.ir/view/4018039/icons8-javascript-240.png" alt="Annie Easley">
			</div>
			<p>
				<span>
					JS
				</span>
				<span class="role">
					· JavaScript
				</span>
			</p>
		</div>
	</div>
	<div class="ambassadors__bottom large-heading">
		<div class="ambassador large-heading">
			<div class="ambassador__image">
				<img src="https://rozup.ir/view/4018052/icons8-html-72.png" alt="Grace Hopper casually smoking a cigarette">
			</div>
			<p>
				<span>
					HTML
				</span>
				<span class="role">
					· Standard Markup Language
				</span>
			</p>
		</div>
		<div class="ambassador large-heading">
			<div class="ambassador__image">
				<img src="https://rozup.ir/view/4018053/icons8-css-96.png" alt="painting of Ada Lovelace">
			</div>
			<p>
				<span>
					CSS
				</span>
				<span class="role">
					· Cascading Style Sheets
				</span>
			</p>
		</div>
		<div class="ambassador large-heading">
			<div class="ambassador__image">
				<img src="https://rozup.ir/view/4018055/icons8-sass-96.png" alt="Margaret Hamilton showing the math for a space mission">
			</div>
			<p>
				<span>
					Sass
				</span>
				<span class="role">
					· Syntactically Awesome Style Sheets
				</span>
			</p>
		</div>
		<div class="ambassador large-heading">
			<div class="ambassador__image">
				<img src="https://rozup.ir/view/4018039/icons8-javascript-240.png" alt="Annie Easley">
			</div>
			<p>
				<span>
					JS
				</span>
				<span class="role">
					· JavaScript
				</span>
			</p>
		</div>
		<div class="ambassador large-heading">
			<div class="ambassador__image">
				<img src="https://rozup.ir/view/4018056/icons8-php-server-96.png" alt="Grace Hopper casually smoking a cigarette">
			</div>
			<p>
				<span>
					PHP
				</span>
				<span class="role">
					· Personal Server
				</span>
			</p>
		</div>
		<div class="ambassador large-heading">
			<div class="ambassador__image">
				<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/cf/Angular_full_color_logo.svg/2048px-Angular_full_color_logo.svg.png" alt="painting of Ada Lovelace">
			</div>
			<p>
				<span>
					Angular
				</span>
				<span class="role">
					· Google Material Design
				</span>
			</p>
		</div>
		<div class="ambassador large-heading">
			<div class="ambassador__image">
				<img src="https://solarsystem.nasa.gov/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBaG8zIiwiZXhwIjpudWxsLCJwdXIiOiJibG9iX2lkIn19--90dcd5cb460c44999d7e8be1d8a9c1537d93730f/Margaret_Hamilton.jpg" alt="Margaret Hamilton showing the math for a space mission">
			</div>
			<p>
				<span>
					Margaret
				</span>
				<span class="role">
					· Computer Scientist
				</span>
			</p>
		</div>
		<div class="ambassador large-heading">
			<div class="ambassador__image">
				<img src="https://media.cleveland.com/plain-dealer/photo/2017/02/23/-15ab43bbeb622193.png" alt="Annie Easley">
			</div>
			<p>
				<span>
					Annie
				</span>
				<span class="role">
					· Computer Scientist
				</span>
			</p>
		</div>
	</div>
</section>

<section class="ambassadors ambassadors--gsap">
	<div class="ambassadors__text">
		<h2 class="medium-heading">
			Current Customers ⎋
		</h2>
	</div>
	<div class="ambassadors__top large-heading">
		<div class="ambassador large-heading">
			<p>
				<span>
					Digikala
				</span>
				<span class="role">
					· digikala.com
				</span>
			</p>
		</div>
		<div class="ambassador large-heading">
			<p>
				<span>
					Aparat
				</span>
				<span class="role">
					· aparat.com
				</span>
			</p>
		</div>
		<div class="ambassador large-heading">
			<p>
				<span>
					Filimo
				</span>
				<span class="role">
					· filimo.com
				</span>
			</p>
		</div>
		<div class="ambassador large-heading">
			<p>
				<span>
					Sabavision
				</span>
				<span class="role">
					· sabavision.com
				</span>
			</p>
		</div>
	</div>
	<div class="ambassadors__bottom large-heading">
		<div class="ambassador large-heading">
			<p>
				<span>
					Ham3d
				</span>
				<span class="role">
					· ham3d.co
				</span>
			</p>
		</div>
		<div class="ambassador large-heading">
			<p>
				<span>
					MCI
				</span>
				<span class="role">
					· mci.ir
				</span>
			</p>
		</div>
		<div class="ambassador large-heading">
			<p>
				<span>
					5040
				</span>
				<span class="role">
					· 5040.ir
				</span>
			</p>
		</div>
		<div class="ambassador large-heading">
			<p>
				<span>
					wiki.5040
				</span>
				<span class="role">
					· wiki.5040.ir
				</span>
			</p>
		</div>
	</div><br><br><br><br><br><br><br>
    <center style="color: #FFFFFF" style="font-family: Inter, sans-serif">copyright iamin all right reserved /. <br> this design is a preview and is not finished. <br> no team was involved in the design and programming of this site. <br> it was done from start to finish by myself, who created <br> the ongoing project while serving in the military /. <br><br><br>  </center>
</section>

  <script src='https://unpkg.com/gsap@3/dist/gsap.min.js'></script>
<script src='https://unpkg.com/gsap@3/dist/ScrollTrigger.min.js'></script>
      <script id="rendered-js" >
gsap.registerPlugin(ScrollTrigger);

// Based on this forum post: https://gsap.com/community/forums/topic/32738-increase-speed-of-marquee-when-user-scroll/

const initMarquees = () => {
  const ambassadors = [...document.querySelectorAll(".ambassadors--gsap")];
  if (ambassadors) {
    const marqueeObject = {
      top: {
        el: null,
        width: 0 },

      bottom: {
        el: null,
        width: 0 } };


    ambassadors.forEach(ambassadorBlock => {
      marqueeObject.top.el = ambassadorBlock.querySelector(".ambassadors__top");
      marqueeObject.bottom.el = ambassadorBlock.querySelector(
      ".ambassadors__bottom");

      marqueeObject.top.width = marqueeObject.top.el.offsetWidth;
      marqueeObject.bottom.width = marqueeObject.bottom.el.offsetWidth;
      marqueeObject.top.el.innerHTML += marqueeObject.top.el.innerHTML;
      marqueeObject.bottom.el.innerHTML += marqueeObject.bottom.el.innerHTML;

      let dirFromLeft = "-=50%";
      let dirFromRight = "+=50%";
      let master = gsap.
      timeline().
      add(marquee(marqueeObject.top.el, 20, dirFromLeft), 0).
      add(marquee(marqueeObject.bottom.el, 20, dirFromRight), 0);
      let tween = gsap.to(master, { duration: 1.5, timeScale: 1, paused: true });
      let timeScaleClamp = gsap.utils.clamp(1, 6);
      // disabling the scrolltrigger doesn't matter for the flashing incoming new items:
      ScrollTrigger.create({
        start: 0,
        end: "max",
        onUpdate: self => {
          master.timeScale(timeScaleClamp(Math.abs(self.getVelocity() / 200)));
          tween.invalidate().restart();
        } });

    });
  }
};

const marquee = (item, time, direction) => {
  let mod = gsap.utils.wrap(0, 50);
  return gsap.to(item, {
    duration: time,
    ease: "none",
    x: direction,
    modifiers: {
      x: x => direction = mod(parseFloat(x)) + "%" },

    repeat: -1 });

};

initMarquees();
//# sourceURL=pen.js
    </script>
    <script src='https://unpkg.co/gsap@3/dist/gsap.min.js'></script>
    <script id="rendered-js" type="module">
// import { gsap } from "http://iamin.r98.ir";
let open = false;

const trigger = document.querySelector(".header__trigger");
if (trigger) {
  const headerNav = document.querySelector(".header__nav");
  trigger.addEventListener("click", () => {
    trigger.classList.toggle("open");
    headerNav.classList.toggle("open");
    const amount = open ? 0 : 100;
    gsap.
    timeline({}).
    to(headerNav, 0.4, {
      "--panel-bottom-1": amount,
      ease: "Power1.easeOut" }).

    to(
    headerNav,
    0.4,
    {
      "--panel-bottom-2": amount,
      ease: "Power1.easeOut" },

    0.1).

    to(
    headerNav,
    0.4,
    {
      "--panel-bottom-3": amount,
      ease: "Power1.easeOut" },

    0.2).

    to(
    headerNav,
    0.4,
    {
      "--panel-bottom-4": amount,
      ease: "Power1.easeOut" },

    0.3);

    open = !open;
  });
}
//# sourceURL=pen.js
    </script>

  
</body>

</html>
