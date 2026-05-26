<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kotjas Archive</title>

<link href="https://fonts.googleapis.com/css2?family=Special+Elite&family=Quicksand:wght@400;600&display=swap" rel="stylesheet">

<style>

:root{

--bg:#120d14;
--bg2:#1d1522;
--panel:#221829;
--text:#fff1f6;
--textsoft:#d8c8d0;
--pink:#ff9fc5;
--border:#3d2b40;
--shadow:rgba(0,0,0,.35);

}

.light-mode{

--bg:#fff6fa;
--bg2:#ffe7f0;
--panel:#fffafb;
--text:#24151e;
--textsoft:#5f4654;
--pink:#d85d8d;
--border:#e7bfd0;
--shadow:rgba(0,0,0,.08);

}

*{
margin:0;
padding:0;
box-sizing:border-box;
}

html{
scroll-behavior:smooth;
}

body{

background:
linear-gradient(rgba(10,0,10,.75),rgba(10,0,10,.92)),
url('background.jpg');

background-size:cover;
background-position:center;
background-attachment:fixed;

font-family:'Quicksand',sans-serif;
color:var(--text);

padding:25px;
transition:.3s;

overflow-x:hidden;
min-height:100vh;

}

.light-mode body,
body.light-mode{

background:
linear-gradient(rgba(255,245,250,.88),rgba(255,245,250,.95)),
url('background-light.jpg');

background-size:cover;
background-position:center;
background-attachment:fixed;

}

.top-online{

text-align:center;
font-size:14px;
color:var(--textsoft);

margin-bottom:16px;

}

.topbar{

display:flex;
align-items:center;
justify-content:space-between;

gap:20px;
margin-bottom:30px;

flex-wrap:wrap;

}

.logo{

background:rgba(20,10,18,.82);
backdrop-filter:blur(12px);

border:1px solid var(--border);

padding:22px 30px;
border-radius:28px;

font-family:'Special Elite',cursive;
font-size:42px;

color:var(--pink);

box-shadow:0 0 20px var(--shadow);

}

.light-mode .logo{

background:rgba(255,255,255,.7);

}

.search-area{

display:flex;
align-items:center;
gap:12px;

flex:1;
min-width:260px;

}

.search-area input{

flex:1;

padding:20px;

border-radius:22px;
border:1px solid var(--border);

background:rgba(20,10,18,.82);
backdrop-filter:blur(12px);

color:var(--text);

font-size:18px;

outline:none;

}

.light-mode .search-area input{

background:rgba(255,255,255,.75);

}

.search-area button{

padding:20px 28px;

border:none;
border-radius:22px;

background:var(--pink);

font-weight:bold;
font-size:18px;

cursor:pointer;

transition:.2s;

}

.search-area button:hover{

transform:scale(1.03);

}

.profile-btn{

background:rgba(20,10,18,.82);
backdrop-filter:blur(12px);

border:1px solid var(--border);

padding:20px 28px;

border-radius:22px;

text-decoration:none;
color:var(--text);

font-weight:bold;

white-space:nowrap;

}

.light-mode .profile-btn{

background:rgba(255,255,255,.7);

}

.layout{

display:grid;

grid-template-columns:240px 1fr 280px;

gap:26px;

align-items:start;

}

.sidebar{

display:flex;
flex-direction:column;
gap:24px;

}

.panel{

background:rgba(20,10,18,.82);
backdrop-filter:blur(12px);

border:1px solid var(--border);

border-radius:34px;

padding:24px;

box-shadow:0 0 20px var(--shadow);

}

.light-mode .panel{

background:rgba(255,255,255,.72);

}

.mascot{

text-align:center;

}

.mascot img{

width:100%;
max-width:180px;

border-radius:22px;

image-rendering:pixelated;

}

.mascot p{

margin-top:18px;

line-height:1.8;
font-size:18px;

color:var(--textsoft);

}

.nav-title{

font-family:'Special Elite',cursive;

font-size:36px;

color:var(--pink);

margin-bottom:20px;

}

.nav-links{

display:flex;
flex-direction:column;
gap:14px;

}

.nav-links a{

background:rgba(0,0,0,.12);

padding:18px;

border-radius:18px;

text-decoration:none;

color:var(--text);

font-size:22px;

transition:.2s;

}

.light-mode .nav-links a{

background:rgba(255,255,255,.45);

}

.nav-links a:hover{

background:var(--pink);

color:black;

transform:translateX(5px);

}

.feed{

display:flex;
flex-direction:column;
gap:28px;

}

.post{

background:rgba(20,10,18,.82);
backdrop-filter:blur(12px);

border:1px solid var(--border);

border-radius:34px;

padding:30px;

box-shadow:0 0 20px var(--shadow);

}

.light-mode .post{

background:rgba(255,255,255,.72);

}

.post-header{

display:flex;
align-items:center;
gap:14px;

margin-bottom:20px;

}

.avatar{

width:54px;
height:54px;

border-radius:50%;

background:var(--pink);

}

.post-title{

font-size:34px;

font-family:'Special Elite',cursive;

color:var(--pink);

margin-bottom:18px;

}

.post p{

line-height:1.9;

font-size:20px;

color:var(--text);

}

.right-image{

background:rgba(20,10,18,.82);
backdrop-filter:blur(12px);

border:1px solid var(--border);

border-radius:34px;

padding:20px;

text-align:center;

position:sticky;
top:20px;

box-shadow:0 0 20px var(--shadow);

}

.light-mode .right-image{

background:rgba(255,255,255,.72);

}

.right-image img{

width:100%;

border-radius:24px;

}

.footer{

margin-top:40px;

display:flex;
justify-content:space-between;
align-items:center;

gap:20px;
flex-wrap:wrap;

}

.disclaimer{

max-width:700px;

font-size:14px;

line-height:1.8;

color:var(--textsoft);

}

.mode-toggle{

padding:20px 30px;

border:none;
border-radius:22px;

background:var(--pink);

font-size:18px;
font-weight:bold;

cursor:pointer;

transition:.2s;

}

.mode-toggle:hover{

transform:scale(1.03);

}

/* MOBILE */

@media(max-width:1200px){

.layout{

grid-template-columns:1fr;

}

.right-image{

position:relative;
top:0;

}

}

@media(max-width:900px){

.logo{

font-size:34px;
width:100%;

text-align:center;

}

.search-area{

width:100%;

}

.profile-btn{

width:100%;
text-align:center;

}

}

@media(max-width:700px){

body{

padding:14px;

}

.topbar{

flex-direction:column;
align-items:stretch;

}

.logo{

font-size:28px;

padding:18px;

}

.search-area{

flex-direction:column;

}

.search-area input{

width:100%;

padding:18px;

font-size:16px;

}

.search-area button{

width:100%;

padding:18px;

}

.profile-btn{

padding:18px;

}

.nav-title{

font-size:30px;

}

.nav-links a{

font-size:20px;

padding:16px;

}

.post{

padding:22px;

}

.post-title{

font-size:28px;

}

.post p{

font-size:17px;

line-height:1.8;

}

.footer{

flex-direction:column;
align-items:flex-start;

}

.mode-toggle{

width:100%;

}

}

</style>
</head>

<body>

<div class="top-online">
( insert number ) people here now
</div>

<div class="topbar">

<div class="logo">
Kotjas Archive
</div>

<div class="search-area">

<input
type="text"
id="searchInput"
placeholder="Search for cases..."
>

<button onclick="searchCase()">
⌕
</button>

</div>

<a href="#" class="profile-btn">
Sign in / profile
</a>

</div>

<div class="layout">

<!-- LEFT -->

<div class="sidebar">

<div class="panel mascot">

<img src="mascot.png">

<p>
archive. awareness.<br>
remembrance.
</p>

</div>

<div class="panel">

<div class="nav-title">
Navigation
</div>

<div class="nav-links">

<a href="#">Home</a>
<a href="#">Explore</a>
<a href="#">Account</a>
<a href="#">Inbox</a>
<a href="#">Settings</a>
<a href="#">Rules</a>
<a href="#">Socials</a>
<a href="#">Donations</a>

</div>

</div>

</div>

<!-- CENTER -->

<div class="feed">

<div class="post">

<div class="post-header">

<div class="avatar"></div>

<div>
<b>Community Notice</b><br>
<small>by hearts4goo</small>
</div>

</div>

<div class="post-title">
Important Notice
</div>

<p>

Kotjas Archive does not support violence,
extremist ideologies, or perpetrators.

Graphic content uploaded by users,
harassment, and misinformation are prohibited.

For more information, see the Rules tab.

This site exists for awareness,
discussion, timelines, documentation,
and remembrance.

</p>

</div>

<div class="post">

<div class="post-header">

<div class="avatar"></div>

<div>
<b>Newest Updates</b><br>
<small>by hearts4goo</small>
</div>

</div>

<div class="post-title">
Welcome
</div>

<p>
Nothing new here yet...
</p>

</div>

</div>

<!-- RIGHT -->

<div class="right-image">

<img src="sideimage.png">

</div>

</div>

<div class="footer">

<div class="disclaimer">

Disclaimer:
Kotjas Archive does not condone violent actions.

This site is made for educational and awareness purposes only.

This site is still a work in progress.

</div>

<button class="mode-toggle" onclick="toggleMode()">
Switch light/dark mode
</button>

</div>

<script>

function toggleMode(){

document.body.classList.toggle("light-mode");

}

const cases=[

"vova and vika stepsiblings",
"samantha rupnow",
"rina palenkova",
"vladislav roslyakov",
"pekka",
"brenton",
"payton",
"adam lanza",
"arthur achleithner"

];

function searchCase(){

let input=document
.getElementById("searchInput")
.value
.toLowerCase();

if(cases.includes(input)){

alert("Opening page for: "+input);

}
else{

alert("Case not found.");

}

}

</script>

</body>
</html>
