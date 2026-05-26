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
--pink:#ff9fc5;
--border:#3d2b40;
}

.light-mode{
--bg:#fff6fa;
--bg2:#ffe7f0;
--panel:#fffafb;
--text:#2b1f26;
--pink:#d85d8d;
--border:#eabed0;
}

*{
margin:0;
padding:0;
box-sizing:border-box;
}

body{
background:linear-gradient(to bottom,#120d14,#0a060d);
font-family:'Quicksand',sans-serif;
color:var(--text);
padding:25px;
transition:.3s;
overflow-x:hidden;
}

.top-online{
text-align:center;
font-size:14px;
opacity:.7;
margin-bottom:14px;
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
background:var(--panel);
border:1px solid var(--border);
padding:22px 30px;
border-radius:24px;
font-family:'Special Elite',cursive;
font-size:42px;
color:var(--pink);
min-width:340px;
}

.search-area{
display:flex;
align-items:center;
gap:12px;
flex:1;
}

.search-area input{
flex:1;
padding:20px;
border-radius:22px;
border:1px solid var(--border);
background:var(--panel);
color:var(--text);
font-size:18px;
}

.search-area button{
padding:20px 28px;
border:none;
border-radius:22px;
background:var(--pink);
font-weight:bold;
cursor:pointer;
}

.profile-btn{
background:var(--panel);
border:1px solid var(--border);
padding:20px 28px;
border-radius:22px;
text-decoration:none;
color:var(--text);
font-weight:bold;
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
background:var(--panel);
border:1px solid var(--border);
border-radius:30px;
padding:24px;
}

.mascot{
text-align:center;
}

.mascot img{
width:100%;
max-width:180px;
border-radius:20px;
image-rendering:pixelated;
}

.mascot p{
margin-top:16px;
line-height:1.7;
}

.nav-title{
font-family:'Special Elite',cursive;
font-size:36px;
color:var(--pink);
margin-bottom:18px;
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

.nav-links a:hover{
background:var(--pink);
color:black;
}

.feed{
display:flex;
flex-direction:column;
gap:28px;
}

.post{
background:var(--panel);
border:1px solid var(--border);
border-radius:30px;
padding:28px;
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
margin-bottom:16px;
}

.post p{
line-height:1.8;
font-size:20px;
}

.right-image{
background:var(--panel);
border:1px solid var(--border);
border-radius:34px;
padding:20px;
text-align:center;
position:sticky;
top:20px;
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
flex-wrap:wrap;
gap:20px;
}

.disclaimer{
max-width:700px;
font-size:14px;
line-height:1.7;
opacity:.75;
}

.mode-toggle{
padding:20px 30px;
border-radius:20px;
border:none;
background:var(--pink);
font-weight:bold;
cursor:pointer;
font-size:18px;
}

@media(max-width:1200px){

.layout{
grid-template-columns:1fr;
}

.right-image{
position:relative;
top:0;
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
<input type="text" id="searchInput" placeholder="Search for cases...">
<button onclick="searchCase()">⌕</button>
</div>

<a href="#" class="profile-btn">
Sign in / profile
</a>

</div>

<div class="layout">

<div class="sidebar">

<div class="panel mascot">
<img src="mascot.png">
<p>
my image / mascot here
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

<div class="right-image">

<img src="sideimage.png">

</div>

</div>

<div class="footer">

<div class="disclaimer">
Disclaimer: Kotjas Archive does not condone violent actions.
This site is made for educational and awareness purposes only.
This site is still a work in progress and heavily inspired by Tumblr-style layouts.
Expect changes over time.
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

let input=document.getElementById("searchInput").value.toLowerCase();

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
