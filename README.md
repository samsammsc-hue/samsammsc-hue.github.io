
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ThinkTalk</title>
	<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
</head>
<body>

<style>

#episodes {
  scroll-margin-top: 70px;
}

/* Add spacing around the resource list container */
#meditations .resource-list {
    display: flex;          /* keep the cards in a row */
    flex-wrap: wrap;        /* wrap to next line if needed */
    gap: 20px;              /* space between cards */
    padding: 0 20px;        /* space from left and right edges */
    justify-content: center; /* optional: center cards */
}

/* Make sure individual cards don't stretch too much */
#meditations .resource-card {
    height: 350px;
	width: 350px;
}

#episodes {
    background-color: #FAFCFF; 
    padding: 50px 0; 
}

/* Navbar background */
header, nav {
  background-color: #0D3B66 !important;
}

/* Navigation links */
.nav-links a {
  color: #FAFCFF; /* white text */
  text-decoration: none;
  font-weight: 600;
  transition: all 0.3s ease;
  padding: 8px 14px;
  border-radius: 6px;
}

/* Gradient hover and active link effect */
.nav-links a:hover,
.nav-links a.active {
  background: linear-gradient(135deg, #FAFCFF, #FAFCFF);
  color: #0D3B66; /* dark text for contrast */
}

.nav-links a {
  transition: background 0.3s ease, color 0.3s ease;
}

/*

@charset "utf-8";
/* CSS Document */

* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
}

:root {
	--primary: #2D5A87;
	--secondary: #4A7C8A;
	--accent: #6B9B7A;
	--light: #F7F7F7;
	--dark: #2A2A3E;
	--gradient-1: linear-gradient(135deg, #2D5A87 0%, #4A7C8A 100%);
	--gradient-2: linear-gradient(135deg, #F1E5AC 0%, #4a90e2 100%);
}

body {
	font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
	line-height: 1.6;
	color: var(--dark);
	background: #FAFCFF;
	overflow-x: hidden;
}

/* Geometric Background Pattern */
.geometric-bg {
	position: fixed;
	top: 0;
	left: 0;
	width: 100%;
	height: 100%;
	z-index: -1;
	opacity: 0.03;
	background-image:
		repeating-linear-gradient(45deg, transparent, transparent 35px, rgba(107, 91, 149, 0.1) 35px, rgba(107, 91, 149, 0.1) 70px),
		repeating-linear-gradient(-45deg, transparent, transparent 35px, rgba(136, 176, 211, 0.1) 35px, rgba(136, 176, 211, 0.1) 70px);
}

/* Header */
header {
	background: rgba(255, 255, 255, 0.95);
	backdrop-filter: blur(10px);
	box-shadow: 0 2px 20px rgba(0, 0, 0, 0.05);
	position: fixed;
	width: 100%;
	top: 0;
	z-index: 1000;
	transition: all 0.3s ease;
}

nav {
	display: flex;
	justify-content: space-between;
	align-items: center;
	padding: 0.8rem 5%;
	max-width: 1400px;
	margin: 0 auto;
	flex-wrap: wrap;
}

@media (max-width: 1000px) and (min-width: 769px) {
	nav {
		flex-direction: column;
		gap: 1rem;
		padding: 1rem 5%;
	}

.nav-links {
    width: 100%;
	justify-content: center;
	color: #FAFCFF
	}
}

/* Logo SVG */
.logo {
	display: flex;
	align-items: center;
	gap: 10px;
	text-decoration: none;
	transition: transform 0.3s ease;
}

.logo:hover {
	transform: scale(1.05);
}

.logo svg {
    width: 40px;
    height: 40px;
}

.logo-text {
	font-size: 1.8rem;
	font-weight: bold;
	background: #B076D6;
	-webkit-background-clip: text;
	-webkit-text-fill-color: transparent;
	background-clip: text;
}

.nav-links {
	display: flex;
	list-style: none;
	gap: 2.5rem;
}

.nav-links a {
	text-decoration: none;
	color: var(--dark);
	font-weight: 500;
	font-size: 1rem;
	transition: all 0.3s ease;
	position: relative;
	padding: 0.6rem 1.2rem;
	border-radius: 6px;
	border: 1px solid transparent;
}

/* Mobile Menu Toggle */
.menu-toggle {
	display: none;
	flex-direction: column;
	cursor: pointer;
	gap: 4px;
}

.menu-toggle span {
	width: 25px;
	height: 3px;
	background: var(--dark);
	transition: all 0.3s ease;
	border-radius: 3px;
}

.menu-toggle.active span:nth-child(1) {
	transform: rotate(45deg) translate(5px, 5px);
}

.menu-toggle.active span:nth-child(2) {
	opacity: 0;
}

.menu-toggle.active span:nth-child(3) {
	transform: rotate(-45deg) translate(7px, -6px);
}

/* Hero Section with Enhanced Animated Background */
#hero {
	min-height: 60vh;
	display: flex;
	align-items: center;
	justify-content: center;
	background: var(--gradient-2);
	position: relative;
	margin-top: 60px;
	overflow: hidden;
}

/* Central Light Core */

/* Connecting Lines and Dots Background */
.network-bg {
	position: absolute;
	width: 100%;
	height: 100%;
	top: 0;
	left: 0;
	opacity: 0.3;
}

.network-line {
	position: absolute;
	background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.5), transparent);
	height: 1px;
	transform-origin: left center;
}

.network-line:nth-child(1) {
	width: 200px;
	top: 20%;
	left: 10%;
	transform: rotate(25deg);
	animation: pulseLine 4s ease-in-out infinite;
}

.network-line:nth-child(2) {
	width: 150px;
	top: 40%;
	right: 20%;
	transform: rotate(-45deg);
	animation: pulseLine 4s ease-in-out infinite 1s;
}

.network-line:nth-child(3) {
	width: 180px;
	bottom: 30%;
	left: 30%;
	transform: rotate(60deg);
	animation: pulseLine 4s ease-in-out infinite 2s;
}

.network-line:nth-child(4) {
	width: 220px;
	top: 60%;
	right: 15%;
	transform: rotate(-20deg);
	animation: pulseLine 4s ease-in-out infinite 3s;
}

.network-line:nth-child(5) {
	width: 160px;
	bottom: 20%;
	right: 35%;
	transform: rotate(40deg);
	animation: pulseLine 4s ease-in-out infinite 1.5s;
}

@keyframes pulseLine {

	0%,
	100% {
		opacity: 0.1;
		transform: scaleX(0.8) rotate(var(--rotation));
	}

	50% {
		opacity: 0.5;
		transform: scaleX(1) rotate(var(--rotation));
	}
}

.network-dot {
	position: absolute;
	width: 6px;
	height: 6px;
	background: white;
	border-radius: 50%;
	box-shadow: 0 0 10px rgba(255, 255, 255, 0.5);
}

.network-dot:nth-child(6) {
	top: 20%;
	left: 10%;
	animation: dotPulse 3s ease-in-out infinite;
}

.network-dot:nth-child(7) {
	top: 40%;
	right: 20%;
	animation: dotPulse 3s ease-in-out infinite 0.5s;
}

.network-dot:nth-child(8) {
	bottom: 30%;
	left: 30%;
	animation: dotPulse 3s ease-in-out infinite 1s;
}

.network-dot:nth-child(9) {
	top: 60%;
	right: 15%;
	animation: dotPulse 3s ease-in-out infinite 1.5s;
}

.network-dot:nth-child(10) {
	bottom: 20%;
	right: 35%;
	animation: dotPulse 3s ease-in-out infinite 2s;
}

.network-dot:nth-child(11) {
	top: 35%;
	left: 25%;
	animation: dotPulse 3s ease-in-out infinite 2.5s;
}

.network-dot:nth-child(12) {
	bottom: 40%;
	right: 25%;
	animation: dotPulse 3s ease-in-out infinite 0.8s;
}

.network-dot:nth-child(13) {
	top: 15%;
	left: 60%;
	animation: dotPulse 3s ease-in-out infinite 1.2s;
}

.network-dot:nth-child(14) {
	bottom: 50%;
	left: 15%;
	animation: dotPulse 3s ease-in-out infinite 2.8s;
}

.network-dot:nth-child(15) {
	top: 70%;
	left: 45%;
	animation: dotPulse 3s ease-in-out infinite 0.3s;
}

.network-dot:nth-child(16) {
	top: 25%;
	right: 40%;
	animation: dotPulse 3s ease-in-out infinite 1.8s;
}

.network-dot:nth-child(17) {
	bottom: 15%;
	left: 55%;
	animation: dotPulse 3s ease-in-out infinite 2.3s;
}

@keyframes dotPulse {

	0%,
	100% {
		transform: scale(1);
		opacity: 0.4;
	}

	50% {
		transform: scale(1.5);
		opacity: 1;
	}
}

/* Inner Peace Animated Background */
.peace-bg {
	position: absolute;
	width: 100%;
	height: 100%;
	top: 0;
	left: 0;
}

.breathing-circle {
	position: absolute;
	border-radius: 50%;
	background: radial-gradient(circle, rgba(255, 255, 255, 0.1) 0%, transparent 70%);
	animation: breathe 8s ease-in-out infinite;
}

.breathing-circle:nth-child(1) {
	width: 300px;
	height: 300px;
	top: 10%;
	left: 10%;
	animation-delay: 0s;
}

.breathing-circle:nth-child(2) {
	width: 200px;
	height: 200px;
	top: 60%;
	right: 15%;
	animation-delay: 2s;
}

.breathing-circle:nth-child(3) {
	width: 250px;
	height: 250px;
	bottom: 20%;
	left: 30%;
	animation-delay: 4s;
}

.breathing-circle:nth-child(4) {
	width: 180px;
	height: 180px;
	top: 30%;
	right: 25%;
	animation-delay: 6s;
}

@keyframes breathe {

	0%,
	100% {
		transform: scale(1) translate(0, 0);
		opacity: 0.3;
	}

	25% {
		transform: scale(1.2) translate(-10px, -10px);
		opacity: 0.5;
	}

	50% {
		transform: scale(1.4) translate(10px, -20px);
		opacity: 0.3;
	}

	75% {
		transform: scale(1.1) translate(-5px, 10px);
		opacity: 0.4;
	}
}

.floating-elements {
	position: absolute;
	width: 100%;
	height: 100%;
}

.zen-stone {
	position: absolute;
	width: 60px;
	height: 60px;
	background: radial-gradient(circle, rgba(255, 255, 255, 0.2) 0%, transparent 60%);
	border-radius: 50%;
	animation: float 15s ease-in-out infinite;
}

.zen-stone:nth-child(1) {
	top: 20%;
	left: 5%;
	animation-delay: 0s;
}

.zen-stone:nth-child(2) {
	top: 70%;
	right: 10%;
	animation-delay: 5s;
}

.zen-stone:nth-child(3) {
	bottom: 30%;
	left: 50%;
	animation-delay: 10s;
}

@keyframes float {

	0%,
	100% {
		transform: translateY(0) translateX(0) rotate(0deg);
	}

	33% {
		transform: translateY(-30px) translateX(20px) rotate(120deg);
	}

	66% {
		transform: translateY(20px) translateX(-20px) rotate(240deg);
	}
}

.mandala-bg {
	position: absolute;
	width: 500px;
	height: 500px;
	top: 50%;
	left: 50%;
	transform: translate(-50%, -50%);
	opacity: 0.1;
}

.mandala-circle {
	position: absolute;
	border: 2px solid white;
	border-radius: 50%;
	animation: rotate 60s linear infinite;
}

.mandala-circle:nth-child(1) {
	width: 100%;
	height: 100%;
	animation-duration: 60s;
}

.mandala-circle:nth-child(2) {
	width: 80%;
	height: 80%;
	top: 10%;
	left: 10%;
	animation-duration: 50s;
	animation-direction: reverse;
}

.mandala-circle:nth-child(3) {
	width: 60%;
	height: 60%;
	top: 20%;
	left: 20%;
	animation-duration: 40s;
}

@keyframes rotate {
	from {
		transform: rotate(0deg);
	}

	to {
		transform: rotate(360deg);
	}
}

.hero-content {
	text-align: center;
	z-index: 1;
	padding: 2rem;
	max-width: 800px;
	position: relative;
}

.hero-content h1 {
	font-size: 3.5rem;
	color: white;
	margin-bottom: 1rem;
	animation: fadeInUp 1s ease;
	text-align: center;
}

.hero-content p {
	font-size: 1.3rem;
	color: rgba(255, 255, 255, 0.9);
	margin-bottom: 2rem;
	animation: fadeInUp 1s ease 0.2s;
	animation-fill-mode: both;
}

.hero-content p {
	font-size: 1.3rem;
	color: rgba(255, 255, 255, 0.9);
	margin-bottom: 2rem;
	animation: fadeInUp 1s ease 0.2s;
	animation-fill-mode: both;
}

.cta-button {
	display: inline-block;
	padding: 1rem 2.5rem;
	background: white;
	color: var(--primary);
	text-decoration: none;
	border-radius: 50px;
	font-weight: 600;
	transition: all 0.3s ease;
	animation: fadeInUp 1s ease 0.4s;
	animation-fill-mode: both;
	box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
}

.cta-button:hover {
	transform: translateY(-3px);
	box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
}

@keyframes fadeInUp {
	from {
		opacity: 0;
		transform: translateY(30px);
	}

	to {
		opacity: 1;
		transform: translateY(0);
	}
}

/* About Section - Complete Redesign */
#about {
	padding: 5rem 5%;
	max-width: 1200px;
	margin: 0 auto;
}

.section-title {
	text-align: center;
	font-size: 2.5rem;
	margin-bottom: 1rem;
	position: relative;
	color: var(--dark);
}

.section-subtitle {
	text-align: center;
	max-width: 800px;
	margin: 0 auto 3rem;
	color: #666;
	font-size: 1.1rem;
}

/* Floating Cards Design */
.about-floating-cards {
	display: grid;
	grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
	gap: 2rem;
	margin-bottom: 4rem;
}

.floating-card {
	background: white;
	border-radius: 25px;
	padding: 2.5rem;
	position: relative;
	overflow: hidden;
	box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
	transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}

.floating-card::before {
	content: '';
	position: absolute;
	top: -50%;
	right: -50%;
	width: 200%;
	height: 200%;
	background: radial-gradient(circle, var(--accent) 0%, transparent 70%);
	opacity: 0;
	transition: opacity 0.4s ease;
}

.floating-card:hover {
	transform: translateY(-10px) rotate(1deg);
	box-shadow: 0 20px 40px rgba(0, 0, 0, 0.12);
}

.floating-card:hover::before {
	opacity: 0.05;
}

.card-icon {
	width: 80px;
	height: 80px;
	margin-bottom: 1.5rem;
	position: relative;
}

.icon-wrapper {
	width: 100%;
	height: 100%;
	background: var(--gradient-2);
	border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
	display: flex;
	align-items: center;
	justify-content: center;
	font-size: 2.5rem;
	animation: morphShape 8s ease-in-out infinite;
	box-shadow: 0 10px 25px rgba(136, 176, 211, 0.3);
}

@keyframes morphShape {

	0%,
	100% {
		border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
		transform: rotate(0deg);
	}

	25% {
		border-radius: 70% 30% 30% 70% / 70% 70% 30% 30%;
		transform: rotate(90deg);
	}

	50% {
		border-radius: 30% 70% 70% 30% / 70% 30% 30% 70%;
		transform: rotate(180deg);
	}

	75% {
		border-radius: 70% 30% 30% 70% / 30% 70% 70% 30%;
		transform: rotate(180deg);
	}
}

.floating-card h3 {
	font-size: 1.4rem;
	margin-bottom: 1rem;
	color: var(--dark);
}

.floating-card p {
	color: #666;
	line-height: 1.6;
}

/* Stats Banner */
.stats-banner {
	background: linear-gradient(135deg, #F1E5AC 0%, #4a90e2 100%);
	border-radius: 30px;
	padding: 3rem;
	display: flex;
	justify-content: space-around;
	align-items: center;
	flex-wrap: wrap;
	gap: 2rem;
	margin-bottom: 4rem;
	position: relative;
	overflow: hidden;
}

.stats-banner::before {
	content: '';
	position: absolute;
	top: -50%;
	left: -50%;
	width: 200%;
	height: 200%;
	background: repeating-linear-gradient(45deg,
			transparent,
			transparent 10px,
			rgba(255, 255, 255, 0.05) 10px,
			rgba(255, 255, 255, 0.05) 20px);
	animation: slidePattern 20s linear infinite;
}

@keyframes slidePattern {
	0% {
		transform: translate(0, 0);
	}

	100% {
		transform: translate(50px, 50px);
	}
}

.stat-block {
	text-align: center;
	position: relative;
	z-index: 1;
}

.stat-value {
	font-size: 3rem;
	font-weight: bold;
	color: white;
	text-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
}

.stat-desc {
	color: rgba(255, 255, 255, 0.9);
	font-size: 1rem;
	margin-top: 0.5rem;
}
#practices {
	padding: 5rem 5%;
	background-color: #FAFCFF;
}

.practices-container {
	max-width: 1200px;
	margin: 0 auto;
	background-color: #FAFCFF;
}

.practice-layout {
	display: grid;
	grid-template-columns: 280px 1fr;
	gap: 3rem;
	margin-top: 3rem;
}

/* ===== Features Container ===== */
.features-container {
    position: relative;
    height: 520px;
    perspective: 1200px;
    margin: 50px 0;
    overflow: visible; /* allow buttons to be seen */
}

/* ===== 3D Carousel Wrapper ===== */
.carousel-3d {
    position: absolute;
    width: 100%;
    height: 100%;
    transform-style: preserve-3d;
    transition: transform 0.8s cubic-bezier(0.4, 0, 0.2, 1);
    will-change: transform;
}

/* ===== Feature Cards ===== */
.feature-card-3d {
    position: absolute;
    width: 250px;
    height: 360px;
    left: 50%;
    top: 50%;
    margin-left: -125px;
    margin-top: -180px;
    background: rgba(255, 255, 255, 0.12); /* slightly more visible than before */
    border: 2px solid rgba(255, 255, 255, 0.2);
    border-radius: 22px;
    padding: 20px;
    text-align: center;
    transition: all 0.3s ease;
    cursor: pointer;
    overflow: hidden;
    box-shadow: 0 4px 15px rgba(0,0,0,0.1);
}

.feature-card-3d:hover {
    box-shadow: 0 10px 25px rgba(0,0,0,0.2);
}

/* ===== Badge ===== */
.feature-badge {
    position: absolute;
    top: 15px;
    right: 15px;
    background: var(--primary, #00d9ff);
    color: #fff;
    font-weight: 700;
    font-size: 0.85rem;
    padding: 5px 10px;
    border-radius: 12px;
    z-index: 10;
}

/* ===== Card Content ===== */
.feature-image {
    font-size: 60px;
    margin-bottom: 20px;
}

.feature-title {
    font-family: var(--font-heading);
    color: #fff;
    font-size: 1.2rem;
    font-weight: 600;
    margin-bottom: 10px;
}

.feature-description {
    font-family: var(--font-heading);
    color: rgba(255, 255, 255, 0.9);
    font-size: 0.9rem;
    line-height: 1.5;
}

/* ===== 3D Positioning ===== */
.feature-card-3d:nth-child(1) { transform: rotateY(0deg) translateZ(320px); }
.feature-card-3d:nth-child(2) { transform: rotateY(60deg) translateZ(320px); }
.feature-card-3d:nth-child(3) { transform: rotateY(120deg) translateZ(320px); }
.feature-card-3d:nth-child(4) { transform: rotateY(180deg) translateZ(320px); }
.feature-card-3d:nth-child(5) { transform: rotateY(240deg) translateZ(320px); }
.feature-card-3d:nth-child(6) { transform: rotateY(300deg) translateZ(320px); }

/* ===== Carousel Controls ===== */
/* Carousel controls container no longer has a background */
.carousel-controls {
    position: absolute;
    top: 50%;
    left: 0;
    width: 100%;
    display: flex;
    justify-content: space-between; /* place prev on left, next on right */
    transform: translateY(-50%);
    padding: 0 20px;
    z-index: 1000;
    pointer-events: none; /* allow buttons to float */
}

/* Individual buttons as circles */
.carousel-btn {
    width: 50px;
    height: 50px;
    background-color: #FAFCFF;
    border: none;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    font-size: 24px;
    color: #0D3B66;
    transition: all 0.3s ease;
    pointer-events: auto; /* enable clicking */
    box-shadow: 0 5px 15px rgba(0,0,0,0.2);
}

.carousel-btn:hover {
    background-color: #e0f2ff;
    transform: scale(1.1);
}

.carousel-btn:active {
    transform: scale(0.95);
}

/* Remove background from old control bar if any */
.carousel-controls {
    background: transparent;
    padding: 0;
}

/* ===== Carousel Indicators ===== */
.carousel-indicators {
    position: absolute;
    bottom: -60px;
    left: 50%;
    transform: translateX(-50%);
    display: flex;
    gap: 10px;
}

.indicator {
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background: #0D3B66;
    cursor: pointer;
    transition: all 0.3s ease;
}

.indicator.active {
    background: var(--primary, #00d9ff);
    transform: scale(1.3);
}

.feature-card-3d {
    position: absolute;
    width: 300px; /* adjust size as needed */
    height: 400px;
    left: 50%;
    top: 50%;
    margin-left: -150px;
    margin-top: -200px;
    background-size: cover;      /* ensure the image covers the card */
    background-position: center; /* center the image */
    background-repeat: no-repeat;
    border-radius: 20px;
    box-shadow: 0 10px 20px rgba(0,0,0,0.2);
    text-align: center;
    color: #fff;
    font-family: var(--font-heading);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    cursor: pointer;
    overflow: hidden;
}

/* Optional overlay to make text readable */
.feature-card-overlay {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    padding: 15px;
    background: rgba(0, 0, 0, 0.4); /* semi-transparent overlay */
}

/* Feature badge stays on top */
.feature-badge {
    position: absolute;
    top: 18px;
    right: 15px;
    background: var(--primary, #00d9ff);
    color: #fff;
    font-weight: 700;
    font-size: 0.85rem;
    padding: 5px 10px;
    border-radius: 12px;
}

/* Feature title inside overlay */
.feature-title {
    font-size: 1.2rem;
    font-weight: 600;
    margin-bottom: 5px;
}

/* Feature description inside overlay */
.feature-description {
    font-size: 0.9rem;
    line-height: 1.3;
}

/* Futuristic Left Timeline */
.timeline-track {
	position: relative;
	padding: 2rem 0;
}

.timeline-progress {
	position: absolute;
	left: 50%;
	top: 2rem;
	bottom: 2rem;
	width: 2px;
	background: rgba(107, 91, 149, 0.1);
	transform: translateX(-50%);
}

.timeline-progress::before {
	content: '';
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	height: 0;
	background: var(--gradient-1);
	animation: fillTimeline 3s ease forwards;
}

@keyframes fillTimeline {
	to {
		height: 100%;
	}
}

.timeline-points {
	position: relative;
	height: 100%;
	display: flex;
	flex-direction: column;
	justify-content: space-between;
}

.timeline-point {
	display: flex;
	align-items: center;
	justify-content: center;
	cursor: pointer;
	transition: all 0.3s ease;
	position: relative;
}

.futuristic-label {
	position: relative;
	padding: 1rem 2rem;
	background: white;
	border-radius: 50px;
	font-weight: 600;
	color: var(--dark);
	transition: all 0.3s ease;
	box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
	z-index: 5;
	min-width: 200px;
	text-align: center;
}

.futuristic-label::before {
	content: '';
	position: absolute;
	inset: -2px;
	border-radius: 50px;
	background: var(--gradient-1);
	opacity: 0;
	transition: opacity 0.3s ease;
	z-index: -1;
}

.futuristic-label::after {
	content: '';
	position: absolute;
	inset: 0;
	border-radius: 50px;
	background: linear-gradient(45deg, transparent 30%, rgba(255, 255, 255, 0.3) 50%, transparent 70%);
	transform: translateX(-100%);
	transition: transform 0.6s ease;
	z-index: -1;
}

.timeline-point:hover .futuristic-label,
.timeline-point.active .futuristic-label {
	animation: zoomPulse 0.6s ease-in-out;
}

@keyframes zoomPulse {
	0% {
		transform: scale(1);
	}

	50% {
		transform: scale(1.05);
	}

	100% {
		transform: scale(1);
	}
}


.timeline-point:hover .timeline-indicator,
.timeline-point.active .timeline-indicator {
	transform: translateX(-50%) scale(1.3);
	background: var(--primary);
	box-shadow: 0 0 15px rgba(45, 90, 135, 0.6);
}

.label-text {
	position: relative;
	z-index: 2;
	font-size: 1.1rem;
	letter-spacing: 0.5px;
}

/* Glowing dot indicator */
.timeline-indicator {
	position: absolute;
	left: 50%;
	transform: translateX(-50%);
	width: 12px;
	height: 12px;
	background: white;
	border: 2px solid var(--primary);
	border-radius: 50%;
	z-index: 2;
}

.timeline-point.active .timeline-indicator {
	background: var(--primary);
	box-shadow: 0 0 20px rgba(107, 91, 149, 0.5);
}

/* Right Content Area */
.practice-content-area {
	display: grid;
	gap: 2rem;
}

.practice-card-new {
	background: white;
	padding: 2.5rem;
	border-radius: 20px;
	box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
	transition: all 0.3s ease;
	position: relative;
	overflow: hidden;
}

.practice-card-new::before {
	content: '';
	position: absolute;
	top: 0;
	left: 0;
	width: 5px;
	height: 100%;
	background: var(--gradient-1);
}

.practice-card-new:hover {
	transform: translateX(10px);
	box-shadow: 0 10px 30px rgba(0, 0, 0, 0.12);
}

.practice-header {
	display: flex;
	align-items: center;
	gap: 1.5rem;
	margin-bottom: 1.5rem;
}

.practice-icon-new {
	width: 60px;
	height: 60px;
	background: var(--gradient-2);
	border-radius: 15px;
	display: flex;
	align-items: center;
	justify-content: center;
	font-size: 2rem;
}

.practice-info h3 {
	font-size: 1.5rem;
	color: var(--dark);
	margin-bottom: 0.3rem;
}

.practice-duration {
	font-size: 0.9rem;
	color: var(--primary);
	font-weight: 500;
}

.practice-description {
	color: #666;
	line-height: 1.8;
	margin-bottom: 1.5rem;
}

.practice-benefits {
	display: flex;
	gap: 1rem;
	flex-wrap: wrap;
}

.benefit-tag {
	padding: 0.5rem 1rem;
	background: linear-gradient(135deg, rgba(45, 90, 135, 0.1) 0%, rgba(74, 124, 138, 0.1) 100%);
	border-radius: 20px;
	font-size: 0.85rem;
	color: var(--primary);
	font-weight: 500;
	cursor: pointer;
	transition: all 0.3s ease;
	text-decoration: none;
	display: inline-block;
}

.benefit-tag:hover {
	background: linear-gradient(135deg, #F1E5AC 0%, #4a90e2 100%);
	color: white;
	transform: translateY(-2px);
	box-shadow: 0 5px 15px rgba(74, 144, 226, 0.3);
}

#resources {
	padding: 5rem 5%;
	max-width: 1200px;
	margin: 0 auto;
}

.resource-tabs {
	display: flex;
	justify-content: center;
	gap: 1rem;
	margin-bottom: 3rem;
}

.tab-btn {
	padding: 0.8rem 2rem;
	background: white;
	border: 2px solid var(--primary);
	border-radius: 25px;
	color: var(--primary);
	font-weight: 600;
	cursor: pointer;
	transition: all 0.3s ease;
}

.tab-btn.active,
.tab-btn:hover {
	background: var(--gradient-1);
	color: white;
	border-color: transparent;
}

.tab-content {
	display: none;
}

.tab-content.active {
	display: block;
	animation: fadeIn 0.5s ease;
}

@keyframes fadeIn {
	from {
		opacity: 0;
	}

	to {
		opacity: 1;
	}
}

.resource-list {
	display: grid;
	grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
	gap: 2rem;
}

.resource-card {
	background: white;
	border-radius: 15px;
	overflow: hidden;
	box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
	transition: all 0.3s ease;
}

.resource-card:hover {
	transform: translateY(-5px);
	box-shadow: 0 10px 30px rgba(0, 0, 0, 0.12);
}

.resource-image {
	height: 200px;
	background: var(--gradient-2);
	position: relative;
	overflow: hidden;
	display: flex;
	align-items: center;
	justify-content: center;
}

.resource-thumbnail {
	width: 100%;
	height: 100%;
	background-size: cover;
	background-position: center;
	background-repeat: no-repeat;
	display: flex;
	align-items: center;
	justify-content: center;
	font-size: 0;
	color: transparent;
	position: relative;
	z-index: 1;
}

/* Real thumbnail images */
.morning-meditation {
	background-image: url('images/snoopypost.png');
}

.stress-relief {
	background-image: url('images/cs.png');
}

.sleep-meditation {
	background-image: url('images/icons.png');
}

.resource-image::before {
	content: '';
	position: absolute;
	width: 200%;
	height: 200%;
	background: repeating-linear-gradient(45deg,
			transparent,
			transparent 10px,
			rgba(255, 255, 255, 0.1) 10px,
			rgba(255, 255, 255, 0.1) 20px);
	animation: slide 20s linear infinite;
}

@keyframes slide {
	0% {
		transform: translate(-50%, -50%);
	}

	100% {
		transform: translate(0, 0);
	}
}

.resource-body {
	padding: 1.5rem;
}

/* Contact Section - Two Columns */
#contact {
	background: linear-gradient(135deg, #0D3B66 0%, #FAF0CA 100%);
	padding: 5rem 5%;
	color: white;
}

.contact-container {
	max-width: 1200px;
	margin: 0 auto;
}

.contact-container h2 {
	color: white;
	margin-bottom: 3rem;
}

.contact-wrapper {
	display: grid;
	grid-template-columns: 1fr 1fr;
	gap: 3rem;
	background: rgba(255, 255, 255, 0.95);
	padding: 3rem;
	border-radius: 20px;
	box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
}

.contact-info {
	padding: 2rem;
}

.contact-info h3 {
	color: var(--primary);
	margin-bottom: 2rem;
	font-size: 1.8rem;
}

.info-item {
	display: flex;
	align-items: center;
	gap: 1rem;
	margin-bottom: 1.5rem;
	color: var(--dark);
	padding: 1rem;
	border-radius: 15px;
	transition: all 0.3s ease;
	cursor: pointer;
	position: relative;
	overflow: hidden;
}

.info-item::before {
	content: '';
	position: absolute;
	top: 0;
	left: -100%;
	width: 100%;
	height: 100%;
	background: linear-gradient(90deg, transparent, rgba(45, 90, 135, 0.1), transparent);
	transition: left 0.5s ease;
}

.info-item:hover {
	background: linear-gradient(135deg, rgba(45, 90, 135, 0.05) 0%, rgba(74, 124, 138, 0.05) 100%);
	transform: translateX(5px);
	box-shadow: 0 5px 20px rgba(45, 90, 135, 0.1);
}

.info-item:hover::before {
	left: 100%;
}

.info-item:hover .info-icon {
	transform: scale(1.1) rotate(5deg);
	box-shadow: 0 8px 25px rgba(45, 90, 135, 0.3);
}

.info-icon {
	width: 50px;
	height: 50px;
	background: var(--gradient-2);
	border-radius: 50%;
	display: flex;
	align-items: center;
	justify-content: center;
	font-size: 1.3rem;
	transition: all 0.3s ease;
	flex-shrink: 0;
}

.info-text h4 {
	margin-bottom: 0.25rem;
	color: var(--primary);
}

.info-text p {
	color: #666;
	font-size: 0.95rem;
}

.social-links {
	display: flex;
	gap: 1rem;
}

.social-link {
	width: 40px;
	height: 40px;
	background: var(--gradient-1);
	border-radius: 50%;
	display: flex;
	align-items: center;
	justify-content: center;
	color: white;
	text-decoration: none;
	transition: transform 0.3s ease;
}

.social-link:hover {
	transform: translateY(-3px);
}

.contact-form {
	padding: 2rem;
}

.form-group {
	margin-bottom: 1.5rem;
}

.form-group label {
	display: block;
	margin-bottom: 0.5rem;
	color: var(--dark);
	font-weight: 500;
}

.form-group input,
.form-group textarea {
	width: 100%;
	padding: 1rem;
	border: 2px solid #ddd;
	border-radius: 10px;
	background: white;
	transition: all 0.3s ease;
	font-family: inherit;
	color: var(--dark);
}

.form-group input:focus,
.form-group textarea:focus {
	outline: none;
	border-color: var(--primary);
	background: white;
}

.submit-btn {
	background: var(--gradient-1);
	color: white;
	padding: 1rem 3rem;
	border: none;
	border-radius: 50px;
	font-size: 1.1rem;
	font-weight: 600;
	cursor: pointer;
	transition: all 0.3s ease;
	width: 100%;
}

.submit-btn:hover {
	transform: translateY(-2px);
	box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
}

/* Footer */
footer {
	background: var(--dark);
	color: white;
	padding: 2rem 5%;
	text-align: center;
}

.footer-content {
	max-width: 1200px;
	margin: 0 auto;
}

.footer-links {
	display: flex;
	justify-content: center;
	gap: 2rem;
	margin-bottom: 1rem;
}

.footer-links a {
	color: white;
	text-decoration: none;
	transition: color 0.3s ease;
}

.footer-links a:hover {
	color: var(--accent);
}

.copyright {
	margin-top: 1rem;
	padding-top: 1rem;
	border-top: 1px solid rgba(255, 255, 255, 0.1);
	font-size: 0.9rem;
	color: rgba(255, 255, 255, 0.7);
}

/* Mobile Responsive */
@media (max-width: 768px) {
	.menu-toggle {
		display: flex;
	}

.nav-links {
		position: fixed;
		top: 80px;
		right: -100%;
		width: 100%;
		height: calc(100vh - 80px);
		background: rgba(255, 255, 255, 0.98);
		flex-direction: column;
		align-items: center;
		justify-content: start;
		padding-top: 3rem;
		transition: right 0.3s ease;
		gap: 1rem;
		z-index: 999;
	}

.nav-links.active {
		right: 0;
	}

	.nav-links li {
		width: 80%;
	}

	.nav-links a {
		width: 100%;
		text-align: center;
		padding: 1rem;
		margin: 0;
		display: block;
		box-sizing: border-box;
	}

	.hero-content h1 {
		font-size: 2.5rem;
	}

	.hero-content p {
		font-size: 1.1rem;
	}

	.mandala-bg {
		width: 300px;
		height: 300px;
	}

	.about-content,
	.contact-wrapper {
		grid-template-columns: 1fr;
	}

	.stats-counter {
		grid-template-columns: repeat(2, 1fr);
	}

	.benefits-grid {
		grid-template-columns: 1fr;
	}

	.journey-path {
		flex-direction: column;
		gap: 2rem;
	}

	.journey-path::before {
		display: none;
	}

	.practice-layout {
		grid-template-columns: 1fr;
	}

	.timeline-track {
		display: none;
	}

	.practice-content-area {
		gap: 1.5rem;
	}

	.section-title {
		font-size: 2rem;
	}

	.footer-links {
		flex-direction: column;
		gap: 1rem;
	}
}

@media (max-width: 480px) {
	.hero-content h1 {
		font-size: 2rem;
	}

	.stats-counter {
		grid-template-columns: 1fr;
	}

	.stat-item::after {
		display: none;
	}

	.benefits-grid {
		grid-template-columns: 1fr;
	}

	.resource-tabs {
		flex-direction: column;
	}

	.tab-btn {
		width: 100%;
	}
}

</style>

    <div class="geometric-bg"></div>

    <!-- Header -->
    <header>
        <nav>
            <a href="#hero" class="logo">
                <svg viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg">
                    <defs>
                        <linearGradient id="logoGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                            <stop offset="0%" style="stop-color:#667eea;stop-opacity:1" />
                            <stop offset="100%" style="stop-color:#764ba2;stop-opacity:1" />
                        </linearGradient>
                    </defs>
                    <circle cx="20" cy="20" r="18" fill="none" stroke="url(#logoGradient)" stroke-width="2"/>
                    <circle cx="20" cy="20" r="14" fill="none" stroke="url(#logoGradient)" stroke-width="1.5" opacity="0.7"/>
                    <circle cx="20" cy="20" r="10" fill="none" stroke="url(#logoGradient)" stroke-width="1" opacity="0.5"/>
                    <circle cx="20" cy="20" r="6" fill="none" stroke="url(#logoGradient)" stroke-width="0.5" opacity="0.3"/>
                    <circle cx="20" cy="20" r="3" fill="url(#logoGradient)"/>
                </svg>
                <span class="logo-text">ThinkTalk</span>
            </a>
            <div class="menu-toggle" onclick="toggleMenu()">
                <span></span>
                <span></span>
                <span></span>
            </div>
            <ul class="nav-links">
    <li><a href="#home" class="nav-link active"><i class="fa fa-home"></i> Home</a></li>
    <li><a href="#about" class="nav-link"><i class="fa fa-user"></i> About</a></li>
	<li><a href="#episodes" class="nav-link"><i class="fa fa-video-camera"></i> Episodes</a></li>
    <li><a href="#contact" class="nav-link"><i class="fa fa-envelope"></i> Contact</a></li>
</ul>

        </nav>
    </header>

    <!-- Hero Section with Enhanced Background -->
    <section id="home">
    <div class="full-width-container" style="background-color: #FAF0CA;">
      <center>
        <img
          src="images/snoopy.png"
          width="1200"
          height="550"
          style="padding-top: 84px;"
          alt="ThinkTalk Logo"
        />
      </center>
      <p><br /></p>
    </div>
  </section>

    <!-- About Section -->
    <section id="about"style="background-color: #FAFCFF;">
        <h2 class="section-title">About ThinkTalk</h2>
        <p class="section-subtitle">
            ThinkTalk is an interactive and educational livestream designed to show how social media—specifically Tiktok—can be used as a powerful tool for learning. Instead of using Tiktok only for entertainment, ThinkTalk teaches students how to properly use social media applications to make learning and education more fun.
        </p>
        
        <!-- Floating Cards Design -->
        <div class="about-floating-cards">
            <div class="floating-card">
                <div class="card-icon">
                    <div class="icon-wrapper">▶️</div>
                </div>
                <h3>What We Do</h3>
                <p>During every livestream, we:<br>
				<ul><br>
<li>Teach digital literacy and responsible social media use</li><br>
<li>Demonstrate practical ways to use Tiktok for studying</li><br>
<li>Allow viewers to participate through live questions, polls and quizzes</li></p>
            </div>
			
            <div class="floating-card">
                <div class="card-icon">
                    <div class="icon-wrapper">🌟</div>
                </div>
                <h3>Our Mission</h3>
                <p><ul>We aim to empower students to learn smarter by using the platforms they already have. <br>
<br>
“Education doesn’t have to be boring—you just need the right feed.”</ul></p>
            </div>
			
            <div class="floating-card">
                <div class="card-icon">
                    <div class="icon-wrapper">🎯</div>
                </div>
                <h3>Who It’s For</h3>
                <p>ThinkTalk is created for: <br>
				<ul><br>
<li>Junior and Senior High School students (ages 12 - 18)</li><br>
<li>College students and young adults (ages 18 - 25) interested in productive social media use</li><br>
<li>Teachers and/or parents who strive for knowledge on learning how to use social media properly</li></p>
            </div>
            
            
        </div>

<div class="features-container">
    <!-- 3D Carousel -->
	
    <h2 class="section-title">Meet the Group</h2>

    <div id="carousel" class="carousel-3d">

        <!-- Feature Card 1 -->
        <div class="feature-card-3d" style="background-image: url('images/Coming.png');">

</div>

        <!-- Feature Card 1 -->
        <div class="feature-card-3d" style="background-image: url('images/paul.png');">
    <div class="feature-badge">Leader</div>
        <h3 class="feature-title">Paul</h3>
</div>


        <!-- Feature Card 2 -->
        <div class="feature-card-3d" style="background-image: url('images/sam.png');">
    <div class="feature-badge">Moderator</div>
        <h3 class="feature-title">Sam</h3>
</div>

        <!-- Feature Card 3 -->
        <div class="feature-card-3d" style="background-image: url('images/thia.png');">
    <div class="feature-badge">Member</div>
        <h3 class="feature-title">Santhia</h3>
</div>

        <!-- Feature Card 4 -->
        <div class="feature-card-3d" style="background-image: url('images/april.png');">
    <div class="feature-badge">Member</div>
        <h3 class="feature-title">April</h3>
</div>

        <!-- Feature Card 5 -->
        <div class="feature-card-3d" style="background-image: url('images/ainsley.png');">
    <div class="feature-badge">Member</div>
        <h3 class="feature-title">Ainsley</h3>
</div>

    

</div>

<!-- Carousel Controls -->
    <div class="carousel-controls">
        <button id="prevBtn" class="carousel-btn">‹</button>
        <button id="nextBtn" class="carousel-btn">›</button>
    </div>

<!-- Carousel Indicators -->
    <div id="indicators" class="carousel-indicators"></div>




    </section>

    <!-- Episodes Section - Tab Structure -->
    <section id="episodes" style="background-color: #FAFCFF;">
        <h2 class="section-title">Episodes</h2>
        <p class="section-subtitle">The key to all our upcoming content — your sneak peek into what’s next on ThinkTalk!</p>
        
        <div class="resource-tabs">
            <button class="tab-btn active" onclick="showTab('meditations')">Content</button>
            <button class="tab-btn" onclick="showTab('courses')">Schedule</button>
            <button class="tab-btn" onclick="showTab('tools')">Feed</button>
        </div>

        <div id="meditations" class="tab-content active">
            <div class="resource-list">
                <div class="resource-card">
                    <div class="resource-image">
                        <div class="resource-thumbnail morning-meditation"></div>
                    </div>
                    <div class="resource-body">
                        <h3>Episode 1</h3>
                        <p>COMING SOON</p>
                    </div>
                </div>
                <div class="resource-card">
                    <div class="resource-image">
                        <div class="resource-thumbnail stress-relief"></div>
                    </div>
                    <div class="resource-body">
                        <h3>Episode 2</h3>
                        <p>COMING SOON</p>
                    </div>
                </div>
                <div class="resource-card">
                    <div class="resource-image">
                        <div class="resource-thumbnail sleep-meditation"></div>
                    </div>
                    <div class="resource-body">
                        <h3>Episode 3</h3>
                        <p>COMING SOON</p>
                    </div>
                </div>
            </div>
        </div>

        <div id="courses" class="tab-content">
            <div class="resource-list">
               
                    <div class="practices-container">
            
            <div class="practice-layout" style="background-color: #FAFCFF;">
                <!-- Futuristic Left Timeline -->
                <div class="timeline-track">
                    <div class="timeline-progress"></div>
                    <div class="timeline-points">
                        <div class="timeline-point active">
                            <div class="futuristic-label">
                                <span class="label-text">Date TBD</span>
                            </div>
                            <div class="timeline-indicator"></div>
                        </div>
                        <div class="timeline-point">
                            <div class="futuristic-label">
                                <span class="label-text">Date TBD</span>
                            </div>
                            <div class="timeline-indicator"></div>
                        </div>
                        <div class="timeline-point">
                            <div class="futuristic-label">
                                <span class="label-text">Date TBD</span>
                            </div>
                            <div class="timeline-indicator"></div>
                        </div>
                        <div class="timeline-point">
                            <div class="futuristic-label">
                                <span class="label-text">Date TBD</span>
                            </div>
                            <div class="timeline-indicator"></div>
                        </div>
                    </div>
                </div>

                <!-- Right Content Area -->
                <div class="practice-content-area">
                    <div class="practice-card-new">
                        <div class="practice-header">
                            <div class="practice-icon-new">📹</div>
                            <div class="practice-info">
                                <h3>???</h3>
                                <span class="practice-duration">???</span>
                            </div>
                        </div>
                        <p class="practice-description">
                            ???
                        </p>
                        <div class="practice-benefits">
                            <a href="#" class="benefit-tag">???</a>
                            <a href="#" class="benefit-tag">???</a>
                            <a href="#" class="benefit-tag">???</a>
                            <a href="#" class="benefit-tag">???</a>
                        </div>
                    </div>

                    <div class="practice-card-new">
                        <div class="practice-header">
                            <div class="practice-icon-new">📹</div>
                            <div class="practice-info">
                                <h3>???</h3>
                                <span class="practice-duration">???</span>
                            </div>
                        </div>
                        <p class="practice-description">
                            ???
                        </p>
                        <div class="practice-benefits">
                            <a href="#" class="benefit-tag">???</a>
                            <a href="#" class="benefit-tag">???</a>
                            <a href="#" class="benefit-tag">???</a>
                            <a href="#" class="benefit-tag">???</a>
                        </div>
                    </div>

                    <div class="practice-card-new">
                        <div class="practice-header">
                            <div class="practice-icon-new">📹</div>
                            <div class="practice-info">
                                <h3>???</h3>
                                <span class="practice-duration">???</span>
                            </div>
                        </div>
                        <p class="practice-description">
                            ???
                        </p>
                        <div class="practice-benefits">
                            <a href="#" class="benefit-tag">???</a>
                            <a href="#" class="benefit-tag">???</a>
                            <a href="#" class="benefit-tag">???</a>
                            <a href="#" class="benefit-tag">???</a>
                        </div>
                    </div>

                    <div class="practice-card-new">
                        <div class="practice-header">
                            <div class="practice-icon-new">📹</div>
                            <div class="practice-info">
                                <h3>???</h3>
                                <span class="practice-duration">???</span>
                            </div>
                        </div>
                        <p class="practice-description">
                            ???
                        </p>
                        <div class="practice-benefits">
                            <a href="#" class="benefit-tag">???</a>
                            <a href="#" class="benefit-tag">???</a>
                            <a href="#" class="benefit-tag">???</a>
                            <a href="#" class="benefit-tag">???</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
                </div>
            </div>
       

        <div id="tools" class="tab-content">
            <div class="resource-list">
     
                    
                </div>
                <div class="resource-card">
                     
                    <div class="resource-body">
                        <center><h3>COMING SOON</h3></center>
                        
                    </div>
                </div>
            </div>
        </div>
		<br>
		<br>
		<br>
		<br>
    </section>
                        

    <!-- Contact Section - Two Columns -->
    <section id="contact">
        <div class="contact-container">
            <h2 class="section-title">Connect With Us</h2>
            
            <div class="contact-wrapper">
                <div class="contact-info">
                    <h3>Get in Touch</h3>
                    
                    <div class="info-item">
                        <div class="info-icon">📍</div>
                        <div class="info-text">
                            <h4>Visit Us</h4>
                            <p>APEC Schools - Pateros<br>
							Elisco Road, Sto. Rosario - Silangan<br>
							Pateros, Metro Manila</p>
                        </div>
                    </div>

                    <div class="info-item">
                        <div class="info-icon">📧</div>
                        <div class="info-text">
                            <h4>Email</h4>
                            <p>thinktalkgrp9@gmail.com</p>
                        </div>
                    </div>

                    
                    <div class="info-item">
                        <div class="info-icon">👥</div>
                        <div class="info-text">
                            <h4>Members</h4>
                            <p>Paul Yssen Lumbang<br>
							Mia Samantha Calingo<br>
							April Sarah Bernal<br>
							Ainsley Jovan Castillo<br>
							Santhia Jewel Santiago
						</p>
                        </div>
                    </div>
                    <div class="info-item">
  <div class="info-icon">📱</div>
  <div class="info-text">
    <h4>Socials</h4>
    <div class="social-links">
      <a href="https://www.facebook.com/YourPage" class="social-link" target="_blank"><i class="fab fa-facebook-f"></i></a>
	  <a href="https://www.linkedin.com/company/YourPage" class="social-link" target="_blank"><i class="fab fa-tiktok"></i></a>
      <a href="https://twitter.com/YourPage" class="social-link" target="_blank"><i class="fab fa-youtube"></i></a>
	  <a href="https://www.instagram.com/thinktalkgrp9?utm_source=ig_web_button_share_sheet&igsh=ZDNlZDc0MzIxNw==" class="social-link" target="_blank"><i class="fab fa-instagram"></i></a>
    </div>
  </div>
</div>

                </div>

                <div class="contact-form">
                    <h3 style="color: var(--primary); font-size: 1.8rem; margin-bottom: 2rem;">Send a Message</h3>
                    <form>
                        <div class="form-group">
                            <label for="name">Your Name</label>
                            <input type="text" id="name" name="name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email Address</label>
                            <input type="email" id="email" name="email" required>
                        </div>
                        <div class="form-group">
                            <label for="subject">Subject</label>
                            <input type="text" id="subject" name="subject" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" name="message" rows="4" required></textarea>
                        </div>
                        <button type="submit" class="submit-btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-links">
                <a href="#privacy">Privacy Policy</a>
                <a href="#terms">Terms of Service</a>
                <a href="#support">Support</a>
            </div>
            <div class="copyright">
                <p>&copy; 2025 ThinkTalk. All rights reserved. Education reimagined. 
            </div>
        </div>
    </footer>
<script>
// JavaScript Document

// Mobile menu toggle
        function toggleMenu() {
            const menuToggle = document.querySelector('.menu-toggle');
            const navLinks = document.querySelector('.nav-links');
            if (menuToggle && navLinks) {
                menuToggle.classList.toggle('active');
                navLinks.classList.toggle('active');
            }
        }

        // Close mobile menu when clicking a link
        document.addEventListener('DOMContentLoaded', function() {
            const navLinks = document.querySelectorAll('.nav-links a');
            navLinks.forEach(link => {
                link.addEventListener('click', () => {
                    const menuToggle = document.querySelector('.menu-toggle');
                    const navLinksContainer = document.querySelector('.nav-links');
                    if (menuToggle && navLinksContainer) {
                        menuToggle.classList.remove('active');
                        navLinksContainer.classList.remove('active');
                    }
                });
            });

            // Active menu highlighting
            const sections = document.querySelectorAll('section');
            const menuLinks = document.querySelectorAll('.nav-link');

            if (sections.length && menuLinks.length) {
                window.addEventListener('scroll', () => {
                    let current = '';
                    sections.forEach(section => {
                        const sectionTop = section.offsetTop;
                        const sectionHeight = section.clientHeight;
                        if (window.scrollY >= (sectionTop - 200)) {
                            current = section.getAttribute('id');
                        }
                    });

                    menuLinks.forEach(link => {
                        link.classList.remove('active');
                        const href = link.getAttribute('href');
                        if (href && href.slice(1) === current) {
                            link.classList.add('active');
                        }
                    });
                });
            }

            // Smooth scrolling for anchor links
            const anchorLinks = document.querySelectorAll('a[href^="#"]');
            anchorLinks.forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    const href = this.getAttribute('href');
                    if (href && href !== '#') {
                        e.preventDefault();
                        const target = document.querySelector(href);
                        if (target) {
                            target.scrollIntoView({
                                behavior: 'smooth',
                                block: 'start'
                            });
                        }
                    }
                });
            });

            // Header scroll effect
            const header = document.querySelector('header');
            if (header) {
                window.addEventListener('scroll', () => {
                    if (window.scrollY > 100) {
                        header.style.background = 'rgba(255, 255, 255, 0.98)';
                        header.style.boxShadow = '0 2px 30px rgba(0, 0, 0, 0.1)';
                    } else {
                        header.style.background = 'rgba(255, 255, 255, 0.95)';
                        header.style.boxShadow = '0 2px 20px rgba(0, 0, 0, 0.05)';
                    }
                });
            }

            // Tab functionality
            window.showTab = function(tabName) {
    const tabs = document.querySelectorAll('.tab-content');
    const buttons = document.querySelectorAll('.tab-btn');

    // Hide all tab contents
    tabs.forEach(tab => tab.classList.remove('active'));

    // Remove 'active' from all buttons
    buttons.forEach(btn => btn.classList.remove('active'));

    // Show the selected tab
    const targetTab = document.getElementById(tabName);
    if (targetTab) targetTab.classList.add('active');

    // Activate the clicked button based on its onclick attribute
    const clickedButton = document.querySelector(`.tab-btn[onclick="showTab('${tabName}')"]`);
    if (clickedButton) clickedButton.classList.add('active');
};

            // Form submission handler
            const contactForm = document.querySelector('.contact-form form');
            if (contactForm) {
                contactForm.addEventListener('submit', (e) => {
                    e.preventDefault();
                    alert('Thank you for reaching out! We will get back to you soon.');
                    e.target.reset();
                });
            }
        });

// 3D Carousel Controls
const carousel = document.getElementById('carousel');
const prevBtn = document.getElementById('prevBtn');
const nextBtn = document.getElementById('nextBtn');
const indicatorsContainer = document.getElementById('indicators');
const featureCards = document.querySelectorAll('.feature-card-3d');

let currentRotation = 0;
let currentIndex = 0;

// Create indicators
featureCards.forEach((_, index) => {
   const indicator = document.createElement('div');
   indicator.className = 'indicator';
   if (index === 0) indicator.classList.add('active');
   indicator.addEventListener('click', () => goToSlide(index));
   indicatorsContainer.appendChild(indicator);
});

const indicators = document.querySelectorAll('.indicator');

// Update view - always use 3D rotation
function updateView() {
   carousel.style.transform = `rotateY(${currentRotation}deg)`;
   updateIndicators();
}

// Update indicators
function updateIndicators() {
   indicators.forEach((indicator, index) => {
      indicator.classList.toggle('active', index === currentIndex);
   });
}

// Go to specific slide
function goToSlide(index) {
   currentIndex = index;
   currentRotation = -index * 60;
   updateView();
}

// Previous button
prevBtn.addEventListener('click', () => {
   currentIndex = (currentIndex - 1 + featureCards.length) % featureCards.length;
   currentRotation += 60;
   updateView();
});

// Next button
nextBtn.addEventListener('click', () => {
   currentIndex = (currentIndex + 1) % featureCards.length;
   currentRotation -= 60;
   updateView();
});

// Touch support for mobile
let touchStartX = 0;
let touchEndX = 0;

carousel.addEventListener('touchstart', (e) => {
   touchStartX = e.changedTouches[0].screenX;
});

carousel.addEventListener('touchend', (e) => {
   touchEndX = e.changedTouches[0].screenX;
   handleSwipe();
});

function handleSwipe() {
   if (touchEndX < touchStartX - 50) {
      // Swipe left - next
      nextBtn.click();
   }
   if (touchEndX > touchStartX + 50) {
      // Swipe right - previous
      prevBtn.click();
   }
}

</script>

</body>
</html>
