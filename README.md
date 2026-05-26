<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kotjas Archive</title>

<link href="https://fonts.googleapis.com/css2?family=Patrick+Hand&family=Quicksand:wght@400;600&display=swap" rel="stylesheet">

<style>

:root{
--bg:#151017;
--panel:#211826;
--panel2:#1a131f;
--text:#fff4fa;
--border:#4a364f;
--pink:#ff9fc6;
}

.light-mode{
--bg:#f5eef3;
--panel:#ffffff;
--panel2:#fff8fb;
--text:#1d1620;
--border:#d8bfd0;
--pink:#c95f88;
}

*{
margin:0;
padding:0;
box-sizing:border-box;
}

body{
background:var(--bg);
color:var(--text);
font-family:'Quicksand',sans-serif;
transition:.3s;
overflow-x:hidden;
min-height:100vh;
}

/* ONLINE BAR */

.top-info{
width:100%;
padding:14px;
text-align:center;
font-size:16px;
border-bottom:2px solid var(--border);
font-family:'Patrick Hand',cursive;
}

/* MAIN WRAPPER */

.wrapper{
width:100%;
padding:20px;
}

/* HEADER */

.header{
display:grid;
grid-template-columns:1.2fr 1.8fr 1fr;
gap:24px;
align-items:center;
margin-bottom:24px;
width:100%;
}

.logo{
border:2px solid var(--border);
padding:18px;
font-size:58px;
font-family:'Patrick Hand',cursive;
background:var(--panel);
width:100%;
}

.searchbar{
display:flex;
align-items:center;
background:var(--panel);
border:2px solid var(--border);
border-radius:18px;
overflow:hidden;
height:95px;
width:100%;
}

.searchbar input{
flex:1;
height:100%;
border:none;
background:transparent;
padding:20px;
font-size:46px;
color:var(--text);
font-family:'Patrick Hand',cursive;
outline:none;
}

.searchbar button{
width:110px;
height:100%;
border:none;
background:transparent;
font-size:42px;
cursor:pointer;
color:var(--text);
}

.profile{
border:2px solid var(--border);
padding:16px;
text-align:center;
border-radius:25px;
font-size:26px;
font-family:'Patrick Hand',cursive;
background:var(--panel);
width:100%;
}

/* MAIN CONTENT */

.layout{
display:grid;
grid-template-columns:230px 1fr 300px;
gap:24px;
width:100%;
}

/* LEFT */

.left{
display:flex;
flex-direction:column;
gap:20px;
}

.image-box{
height:220px;
border:2px solid var(--border);
border-radius:35px;
overflow:hidden;
background:var(--panel);
}

.image-box img{
width:100%;
height:100%;
object-fit:cover;
}

.nav{
border:2px solid var(--border);
background:var(--panel);
padding:20px;
min-height:640px;
}

.nav a{
display:block;
text-decoration:none;
color:var(--text);
font-size:48px;
font-family:'Patrick Hand',cursive;
margin-bottom:18px;
}

/* CENTER */

.center{
display:flex;
flex-direction:column;
gap:28px;
}

.post{
border:2px solid var(--border);
background:var(--panel);
padding:24px;
min-height:240px;
width:100%;
}

.post-header{
display:flex;
align-items:center;
gap:16px;
margin-bottom:18px;
}

.circle{
width:50px;
height:50px;
border-radius:50%;
border:2px solid var(--border);
}

.post-title{
font-size:48px;
font-family:'Patrick Hand',cursive;
}

.small{
font-size:18px;
opacity:.7;
}

.post p{
font-size:28px;
line-height:1.5;
margin-top:12px;
max-width:90%;
font-family:'Patrick Hand',cursive;
}

/* RIGHT */

.right{
display:flex;
flex-direction:column;
gap:20px;
}

.right-image{
border:2px solid var(--border);
border-radius:40px;
height:720px;
overflow:hidden;
background:var(--panel);
}

.right-image img{
width:100%;
height:100%;
object-fit:cover;
}

/* DISCLAIMER */

.disclaimer{
margin-top:24px;
font-size:18px;
line-height:1.6;
font-family:'Patrick Hand',cursive;
max-width:500px;
}

/* TOGGLE */

.toggle{
position:fixed;
right:20px;
bottom:20px;
padding:18px 28px;
font-size:28px;
font-family:'Patrick Hand',cursive;
background:var(--panel);
border:2px solid var(--border);
color:var(--text);
cursor:pointer;
border-radius:12px;
z-index:999;
}

/* LARGE MONITORS */

@media(min-width:1800px){

.wrapper{
padding:30px 50px;
}

.logo{
font-size:72px;
}

.post p{
font-size:32px;
}

}

/* TABLET */

@media(max-width:1200px){

.header{
grid-template-columns:1fr;
}

.layout{
grid-template-columns:220px 1fr;
}

.right{
grid-column:1/3;
}

.right-image{
height:380px;
}

}

/* MOBILE */

@media(max-width:850px){

.wrapper{
padding:12px;
}

.layout{
grid-template-columns:1fr;
}

.header{
grid-template-columns:1fr;
gap:16px;
}

.logo{
font-size:42px;
}

.searchbar{
height:75px;
}

.searchbar input{
font-size:30px;
}

.searchbar button{
font-size:28px;
width:80px;
}

.profile{
font-size:22px;
}

.nav{
min-height:auto;
}

.nav a{
font-size:36px;
}

.post-title{
font-size:34px;
}

.post p{
font-size:22px;
max-width:100%;
}

.right-image{
height:340px;
}

.toggle{
position:relative;
right:auto;
bottom:auto;
width:100%;
margin-top:20px;
}

}

/* VERY SMALL */

@media(max-width:500px){

.logo{
font-size:34px;
}

.searchbar input{
font-size:24px;
}

.post p{
font-size:20px;
}

.nav a{
font-size:30px;
}

}

</style>
</head>

<body>

<!-- ONLINE INFO -->

<div class="top-info">
<span id="onlineUsers">127</span> people here now •
<span id="loggedUsers">48</span> logged into this site
</div>

<div class="wrapper">

<!-- HEADER -->

<div class="header">

<div class="logo">
Kotjas Archive
</div>

<div class="searchbar">
<input type="text" placeholder="Search for cases...">
<button>⌕</button>
</div>

<div class="profile">
Sign in / profile if logged in
</div>

</div>

<!-- MAIN -->

<div class="layout">

<!-- LEFT -->

<div class="left">

<div class="image-box">

<!-- PUT YOUR IMAGE -->
<img src="leftimage.png">

</div>

<div class="nav">

<a href="#">Home ▷</a>
<a href="#">Explore</a>
<a href="#">Account</a>
<a href="#">Inbox</a>
<a href="#">Settings</a>
<a href="#">Rules</a>
<a href="#">Socials</a>
<a href="#">Donations</a>

</div>

</div>

<!-- CENTER -->

<div class="center">

<div class="post">

<div class="post-header">

<div class="circle"></div>

<div>
<div class="post-title">
Community Notice
</div>

<div class="small">
by hearts4goo
</div>
</div>

</div>

<p>
Kotjas Archive does not support violence,
extremist ideologies or perpetrators.
Graphic content by users, harassment
and misinformation are prohibited.

<br><br>

For more, see Rules tab.
</p>

</div>

<div class="post" style="min-height:180px;">

<div class="post-header">

<div class="circle"></div>

<div>
<div class="post-title">
Newest updates
</div>

<div class="small">
by hearts4goo
</div>
</div>

</div>

<p>
Welcome! Nothing new here yet...
</p>

</div>

<div class="disclaimer">

Disclaimer: Kotjas Archive does not condone violent actions.
This site is made for educational purposes only.
This site is still in work in process.
This is heavily inspired by tumblr and wpd.
Expect changes.

</div>

</div>

<!-- RIGHT -->

<div class="right">

<div class="right-image">

<!-- PUT YOUR IMAGE -->
<img src="rightimage.png">

</div>

</div>

</div>

<button class="toggle" onclick="toggleMode()">
Switch light/dark mode
</button>

</div>

<script>

function toggleMode(){
document.body.classList.toggle("light-mode");
}

/* fake online counters */

function updateCounters(){

const online =
Math.floor(Math.random() * 120) + 80;

const logged =
Math.floor(Math.random() * 60) + 20;

document.getElementById("onlineUsers").innerText = online;
document.getElementById("loggedUsers").innerText = logged;

}

setInterval(updateCounters, 4000);

</script>

</body>
</html>
