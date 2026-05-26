<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kotjas Archive</title>

<link href="https://fonts.googleapis.com/css2?family=Patrick+Hand&display=swap" rel="stylesheet">

<style>

:root{
--bg:#120912;
--panel:#211327;
--border:#523553;
--text:#f6ecf4;
--soft:#b9a8b9;
}

.light-mode{
--bg:#f4eef4;
--panel:#ffffff;
--border:#c8b4ca;
--text:#231923;
--soft:#675967;
}

*{
margin:0;
padding:0;
box-sizing:border-box;
}

body{
background:var(--bg);
color:var(--text);
font-family:'Patrick Hand',cursive;
transition:.3s;
overflow-x:hidden;
}

/* TOP AREA */

.top-online{
width:100%;
text-align:center;
padding:10px;
font-size:24px;
border-bottom:1px solid var(--border);
}

.topbar{
width:100%;
display:flex;
align-items:center;
justify-content:space-between;
gap:30px;
padding:25px;
flex-wrap:wrap;
}

.title-box{
border:1px solid var(--border);
padding:25px;
min-width:280px;
font-size:70px;
background:var(--panel);
flex:1;
}

.search-box{
display:flex;
align-items:center;
gap:10px;
flex:2;
min-width:300px;
}

.search-box input{
width:100%;
padding:24px;
font-size:42px;
border-radius:25px;
border:1px solid var(--border);
background:var(--panel);
color:var(--text);
font-family:'Patrick Hand',cursive;
}

.search-btn{
padding:22px 30px;
border-radius:25px;
border:1px solid var(--border);
background:var(--panel);
color:var(--text);
font-size:34px;
cursor:pointer;
}

.login-box{
border:1px solid var(--border);
padding:22px;
border-radius:25px;
background:var(--panel);
font-size:32px;
text-align:center;
min-width:260px;
}

/* MAIN LAYOUT */

.layout{
display:grid;
grid-template-columns:280px 1fr 320px;
gap:30px;
padding:20px;
width:100%;
}

/* LEFT */

.left-column{
display:flex;
flex-direction:column;
gap:25px;
}

.image-box{
height:270px;
border-radius:35px;
overflow:hidden;
border:1px solid var(--border);
background:var(--panel);
}

.image-box img{
width:100%;
height:100%;
object-fit:cover;
}

.nav-box{
border:1px solid var(--border);
background:var(--panel);
padding:20px;
}

.nav-box a{
display:block;
text-decoration:none;
color:var(--text);
font-size:48px;
margin:18px 0;
}

.disclaimer{
font-size:18px;
line-height:1.4;
color:var(--soft);
padding:10px;
}

/* CENTER */

.center-column{
display:flex;
flex-direction:column;
gap:30px;
}

.post{
border:1px solid var(--border);
background:var(--panel);
padding:25px;
}

.post-header{
display:flex;
align-items:center;
gap:20px;
margin-bottom:20px;
}

.circle{
width:55px;
height:55px;
border-radius:50%;
border:1px solid var(--border);
}

.post-title{
font-size:62px;
line-height:1;
}

.username{
font-size:26px;
color:var(--soft);
}

.post-text{
font-size:34px;
line-height:1.5;
margin-top:20px;
}

/* RIGHT */

.right-image{
border:1px solid var(--border);
border-radius:40px;
overflow:hidden;
background:var(--panel);
min-height:700px;
}

.right-image img{
width:100%;
height:100%;
object-fit:cover;
}

/* THEME BUTTON */

.theme-toggle{
position:fixed;
bottom:20px;
right:20px;
padding:20px 28px;
font-size:30px;
border-radius:20px;
border:1px solid var(--border);
background:var(--panel);
color:var(--text);
cursor:pointer;
font-family:'Patrick Hand',cursive;
}

/* RESPONSIVE */

@media(max-width:1400px){

.layout{
grid-template-columns:240px 1fr 260px;
}

.title-box{
font-size:55px;
}

.search-box input{
font-size:32px;
}

}

@media(max-width:1100px){

.layout{
grid-template-columns:1fr;
}

.right-image{
min-height:400px;
}

.topbar{
flex-direction:column;
align-items:stretch;
}

.title-box,
.search-box,
.login-box{
width:100%;
}

}

@media(max-width:700px){

.title-box{
font-size:42px;
}

.search-box input{
font-size:24px;
padding:18px;
}

.search-btn{
font-size:22px;
padding:18px;
}

.login-box{
font-size:24px;
}

.nav-box a{
font-size:36px;
}

.post-title{
font-size:42px;
}

.post-text{
font-size:24px;
}

.theme-toggle{
font-size:22px;
}

}

</style>
</head>

<body>

<div class="top-online">
<span id="onlineUsers">0</span> people here now •
<span id="loggedUsers">0</span> logged into this site
</div>

<div class="topbar">

<div class="title-box">
Kotjas Archive
</div>

<div class="search-box">
<input type="text" id="searchInput" placeholder="Search for cases...">
<button class="search-btn" onclick="searchSite()">⌕</button>
</div>

<div class="login-box">
Sign in / profile if logged in
</div>

</div>

<div class="layout">

<!-- LEFT -->

<div class="left-column">

<div class="image-box">
<img src="yourimage1.jpg">
</div>

<div class="nav-box">
<a href="#">Home ▷</a>
<a href="#">Explore</a>
<a href="#">Account</a>
<a href="#">Inbox</a>
<a href="#">Settings</a>
<a href="#">Rules</a>
<a href="#">Socials</a>
<a href="#">Donations</a>
</div>

<div class="disclaimer">
Kotjas Archive does not condone violent actions. This site is made for educational purposes only. This site is still in work in progress. Inspired by Tumblr and web archives.
</div>

</div>

<!-- CENTER -->

<div class="center-column">

<div class="post">

<div class="post-header">
<div class="circle"></div>

<div>
<div class="post-title">Community Notice</div>
<div class="username">by hearts4goo</div>
</div>

</div>

<div class="post-text">
Kotjas Archive does not support violence, extremist ideologies or perpetrators.
Graphic content by users, harassment and misinformation are prohibited.
<br><br>
For more, see Rules tab.
</div>

</div>

<div class="post">

<div class="post-header">
<div class="circle"></div>

<div>
<div class="post-title">Newest updates</div>
<div class="username">by hearts4goo</div>
</div>

</div>

<div class="post-text">
Welcome! Nothing new here yet...
</div>

</div>

</div>

<!-- RIGHT -->

<div class="right-image">
<img src="yourimage2.jpg">
</div>

</div>

<button class="theme-toggle" onclick="toggleMode()">
Switch light/dark mode
</button>

<script>

/* DARK/LIGHT MODE */

function toggleMode(){
document.body.classList.toggle("light-mode");
}

/* SEARCH */

function searchSite(){

const input = document
.getElementById("searchInput")
.value
.toLowerCase();

const pages = {

"home":"#",
"explore":"#",
"account":"#",
"inbox":"#",
"settings":"#",
"rules":"#"

};

if(pages[input]){
window.location.href = pages[input];
}else{
alert("No page found.");
}

}

/* ONLINE USERS */

/*
REAL online user counts are NOT possible with
plain HTML alone.

For REAL live numbers you need:
- a database
- backend/server
- Firebase / Supabase / Node.js etc

So for now this simulates live changing numbers.
*/

function updateFakeStats(){

const online =
Math.floor(Math.random()*120)+20;

const logged =
Math.floor(Math.random()*50)+5;

document.getElementById("onlineUsers").innerText = online;
document.getElementById("loggedUsers").innerText = logged;

}

updateFakeStats();

setInterval(updateFakeStats,5000);

</script>

</body>
</html>

</script>

</body>
</html>
