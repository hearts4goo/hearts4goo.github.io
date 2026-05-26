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
}

/* TOP INFO */

.top-info{
text-align:center;
padding:10px;
font-size:14px;
border-bottom:1px solid var(--border);
}

/* HEADER */

.header{
display:grid;
grid-template-columns:350px 1fr 220px;
gap:25px;
padding:24px;
align-items:center;
}

.logo{
border:2px solid var(--border);
padding:18px;
font-size:56px;
font-family:'Patrick Hand',cursive;
background:var(--panel);
}

.searchbar{
display:flex;
align-items:center;
background:var(--panel);
border:2px solid var(--border);
border-radius:18px;
overflow:hidden;
height:90px;
}

.searchbar input{
flex:1;
height:100%;
border:none;
background:transparent;
padding:20px;
font-size:42px;
color:var(--text);
font-family:'Patrick Hand',cursive;
outline:none;
}

.searchbar button{
width:110px;
height:100%;
border:none;
background:transparent;
font-size:40px;
cursor:pointer;
color:var(--text);
}

.profile{
border:2px solid var(--border);
padding:16px;
text-align:center;
border-radius:25px;
font-size:24px;
font-family:'Patrick Hand',cursive;
background:var(--panel);
}

/* MAIN LAYOUT */

.layout{
display:grid;
grid-template-columns:210px 1fr 260px;
gap:28px;
padding:0 24px 24px;
}

/* LEFT */

.left{
display:flex;
flex-direction:column;
gap:20px;
}

.image-box{
height:160px;
border:2px solid var(--border);
border-radius:30px;
display:flex;
justify-content:center;
align-items:center;
background:var(--panel);
overflow:hidden;
}

.image-box img{
width:100%;
height:100%;
object-fit:cover;
}

.nav{
border:2px solid var(--border);
background:var(--panel);
padding:18px;
min-height:620px;
}

.nav a{
display:block;
text-decoration:none;
color:var(--text);
font-size:44px;
font-family:'Patrick Hand',cursive;
margin-bottom:18px;
}

/* CENTER */

.center{
display:flex;
flex-direction:column;
gap:30px;
}

.post{
border:2px solid var(--border);
background:var(--panel);
padding:24px;
min-height:260px;
}

.post-header{
display:flex;
align-items:center;
gap:14px;
margin-bottom:18px;
}

.circle{
width:46px;
height:46px;
border-radius:50%;
border:2px solid var(--border);
}

.post-title{
font-size:42px;
font-family:'Patrick Hand',cursive;
}

.small{
font-size:18px;
opacity:.7;
}

.post p{
font-size:24px;
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
height:650px;
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
padding:0 24px 24px;
font-size:16px;
max-width:430px;
line-height:1.6;
font-family:'Patrick Hand',cursive;
}

/* TOGGLE */

.toggle{
position:fixed;
right:30px;
bottom:20px;
padding:18px 28px;
font-size:26px;
font-family:'Patrick Hand',cursive;
background:var(--panel);
border:2px solid var(--border);
color:var(--text);
cursor:pointer;
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
height:350px;
}

}

/* MOBILE */

@media(max-width:800px){

.layout{
grid-template-columns:1fr;
}

.nav{
min-height:auto;
}

.logo{
font-size:40px;
}

.searchbar{
height:70px;
}

.searchbar input{
font-size:28px;
}

.nav a{
font-size:34px;
}

.post-title{
font-size:30px;
}

.post p{
font-size:20px;
}

.profile{
font-size:20px;
}

}

</style>
</head>

<body>

<div class="top-info">
(insert number) people here now (insert number) people here
</div>

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

<div class="layout">

<!-- LEFT -->

<div class="left">

<div class="image-box">

<!-- INSERT YOUR IMAGE -->
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

<div class="post" style="min-height:170px;">

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

</div>

<!-- RIGHT -->

<div class="right">

<div class="right-image">

<!-- INSERT YOUR IMAGE -->
<img src="rightimage.png">

</div>

</div>

</div>

<div class="disclaimer">

Disclaimer: Kotjas Archive does not condone violent actions.
This site is made for educational purposes only.
This site is still in work in process.
This is heavily inspired by tumblr and wpd.
Expect changes.

</div>

<button class="toggle" onclick="toggleMode()">
Switch light/dark mode
</button>

<script>

function toggleMode(){
document.body.classList.toggle("light-mode");
}

</script>

</body>
</html>
