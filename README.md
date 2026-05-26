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
--bg2:#1b1420;
--panel:#211826;
--text:#ffeef6;
--pink:#ff9dc0;
--accent:#ff5d95;
--border:#3a2b3d;
}

.light-mode{
--bg:#fff6fa;
--bg2:#ffe8f1;
--panel:#ffffff;
--text:#24171f;
--pink:#c95b84;
--accent:#ff5d95;
--border:#e9bfd0;
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

/* TOP BAR */

.topbar{
width:100%;
padding:18px 30px;
border-bottom:1px solid var(--border);
display:flex;
justify-content:space-between;
align-items:center;
gap:20px;
background:rgba(18,13,20,.85);
backdrop-filter:blur(12px);
position:sticky;
top:0;
z-index:999;
}

.logo{
font-family:'Special Elite',cursive;
font-size:38px;
color:var(--pink);
}

.search-area{
display:flex;
gap:12px;
width:50%;
}

.search-area input{
flex:1;
padding:16px;
border-radius:16px;
border:1px solid var(--border);
background:var(--bg2);
color:var(--text);
font-size:15px;
}

.search-area button{
padding:16px 24px;
border:none;
border-radius:16px;
background:var(--pink);
font-weight:bold;
cursor:pointer;
}

.profile-btn{
background:var(--bg2);
border:1px solid var(--border);
padding:16px 22px;
border-radius:16px;
cursor:pointer;
color:var(--text);
}

/* MAIN LAYOUT */

.layout{
display:grid;
grid-template-columns:260px 1fr 280px;
gap:24px;
padding:24px;
max-width:1700px;
margin:auto;
}

/* LEFT SIDEBAR */

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

.panel-title{
font-family:'Special Elite',cursive;
font-size:28px;
color:var(--pink);
margin-bottom:18px;
}

.mascot{
text-align:center;
}

.mascot img{
width:100%;
max-width:180px;
border-radius:20px;
}

.quote{
margin-top:14px;
line-height:1.8;
font-size:16px;
}

.nav-links{
display:flex;
flex-direction:column;
gap:14px;
}

.nav-links a{
text-decoration:none;
color:var(--text);
background:var(--bg2);
padding:15px;
border-radius:16px;
transition:.2s;
}

.nav-links a:hover{
background:var(--pink);
color:black;
}

/* CENTER CONTENT */

.feed{
display:flex;
flex-direction:column;
gap:24px;
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
margin-bottom:18px;
}

.avatar{
width:50px;
height:50px;
border-radius:50%;
background:var(--pink);
}

.post h2{
font-family:'Special Elite',cursive;
font-size:34px;
margin-bottom:18px;
color:var(--pink);
}

.post p{
line-height:1.9;
font-size:17px;
}

.actions{
display:flex;
gap:18px;
margin-top:20px;
opacity:.8;
}

/* HERO */

.hero{
padding:45px;
display:flex;
flex-direction:column;
gap:25px;
}

.hero-title{
font-family:'Special Elite',cursive;
font-size:76px;
line-height:1;
}

.hero-title span{
color:var(--pink);
}

.hero-buttons{
display:flex;
gap:14px;
flex-wrap:wrap;
}

.hero-buttons button{
padding:15px 24px;
border-radius:16px;
border:none;
cursor:pointer;
font-weight:bold;
}

.primary{
background:var(--pink);
}

.secondary{
background:var(--bg2);
color:var(--text);
border:1px solid var(--border);
}

/* RIGHT SIDEBAR */

.rightbar{
display:flex;
flex-direction:column;
gap:24px;
}

.case-card{
background:var(--bg2);
padding:18px;
border-radius:18px;
margin-bottom:14px;
cursor:pointer;
border:1px solid var(--border);
transition:.2s;
}

.case-card:hover{
transform:translateY(-3px);
border-color:var(--pink);
}

.case-card h3{
color:var(--pink);
font-size:20px;
}

/* FOOTER */

footer{
margin-top:20px;
padding:30px;
text-align:center;
opacity:.6;
font-size:14px;
}

/* TOGGLE */

.theme-toggle{
position:fixed;
right:20px;
bottom:20px;
padding:16px 20px;
border-radius:18px;
border:none;
background:var(--pink);
font-weight:bold;
cursor:pointer;
z-index:999;
}

/* RESPONSIVE */

/* TABLET */

@media(max-width:1100px){

.layout{
grid-template-columns:220px 1fr;
}

.rightbar{
grid-column:1/3;
flex-direction:row;
overflow:auto;
}

.case-card{
min-width:220px;
}

.hero-title{
font-size:58px;
}

}

/* MOBILE */

@media(max-width:800px){

.topbar{
flex-direction:column;
align-items:stretch;
}

.search-area{
width:100%;
}

.layout{
grid-template-columns:1fr;
padding:14px;
}

.sidebar,
.rightbar{
width:100%;
}

.hero-title{
font-size:46px;
}

.post{
padding:20px;
}

.panel{
padding:20px;
}

}

/* VERY SMALL */

@media(max-width:500px){

.logo{
font-size:28px;
}

.hero-title{
font-size:38px;
}

.search-area button{
padding:14px;
}

}

</style>
</head>

<body>

<!-- TOP BAR -->

<header class="topbar">

<div class="logo">
KOTJAS ARCHIVE
</div>

<div class="search-area">
<input type="text" id="searchInput" placeholder="Search for cases...">
<button onclick="searchCase()">Search</button>
</div>

<button class="profile-btn" onclick="openAccount()">
Sign in / Profile
</button>

</header>

<!-- MAIN -->

<div class="layout">

<!-- LEFT -->

<aside class="sidebar">

<div class="panel mascot">

<!-- PUT YOUR IMAGE FILE NAME HERE -->
<img src="mascot.png" alt="Mascot">

<div class="quote">
archive. awareness.<br>
remembrance.
</div>

</div>

<div class="panel">

<div class="panel-title">
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

<div class="panel">

<p style="line-height:1.9;">
Kotjas Archive does not condone violent actions,
extremist ideologies, or perpetrators.
This site is made for educational and awareness purposes only.
</p>

</div>

</aside>

<!-- CENTER -->

<main class="feed">

<div class="post hero">

<div class="hero-title">
archive<br>
the past.<br>
learn<br>
the patterns.<br>
<span>prevent<br>
the future.</span>
</div>

<p>
Kotjas Archive is a community-based awareness project documenting crimes,
disappearances, and tragedies while allowing users to discuss and archive information.
</p>

<div class="hero-buttons">

<button class="primary">
Explore Cases
</button>

<button class="secondary" onclick="openAccount()">
Create Account
</button>

</div>

</div>

<div class="post">

<div class="post-header">

<div class="avatar"></div>

<div>
<b>Community Notice</b><br>
by hearts4goo
</div>

</div>

<h2>Rules & Safety</h2>

<p>
Kotjas Archive does not support violence,
extremist ideologies, or glorification of perpetrators.
Graphic content uploaded by users, harassment,
and misinformation are prohibited.
</p>

<div class="actions">
<span>♡ 1.2k</span>
<span>✎ 210 comments</span>
</div>

</div>

<div class="post">

<div class="post-header">

<div class="avatar"></div>

<div>
<b>Newest Updates</b><br>
by hearts4goo
</div>

</div>

<h2>Welcome</h2>

<p>
Nothing new here yet...
</p>

<div class="actions">
<span>♡ 230</span>
<span>✎ 18 comments</span>
</div>

</div>

</main>

<!-- RIGHT -->

<aside class="rightbar">

<div class="panel">

<div class="panel-title">
Searchable Cases
</div>

<div class="case-card" onclick="openCase('Vova and Vika Stepsiblings')">
<h3>Vova and Vika Stepsiblings</h3>
</div>

<div class="case-card" onclick="openCase('Samantha Rupnow')">
<h3>Samantha Rupnow</h3>
</div>

<div class="case-card" onclick="openCase('Rina Palenkova')">
<h3>Rina Palenkova</h3>
</div>

<div class="case-card" onclick="openCase('Vladislav Roslyakov')">
<h3>Vladislav Roslyakov</h3>
</div>

<div class="case-card" onclick="openCase('Pekka')">
<h3>Pekka</h3>
</div>

<div class="case-card" onclick="openCase('Brenton')">
<h3>Brenton</h3>
</div>

<div class="case-card" onclick="openCase('Payton')">
<h3>Payton</h3>
</div>

<div class="case-card" onclick="openCase('Adam Lanza')">
<h3>Adam Lanza</h3>
</div>

<div class="case-card" onclick="openCase('Arthur Achleithner')">
<h3>Arthur Achleithner</h3>
</div>

</div>

<!-- RIGHT IMAGE PANEL -->

<div class="panel mascot">

<!-- PUT YOUR OTHER IMAGE HERE -->
<img src="sideimage.png" alt="Side Image">

</div>

</aside>

</div>

<footer>
Kotjas Archive • awareness project • responsive for pc, tablet, laptop, and mobile
</footer>

<button class="theme-toggle" onclick="toggleMode()">
Switch Light/Dark Mode
</button>

<script>

function toggleMode(){
document.body.classList.toggle("light-mode");
}

function openAccount(){
alert("Account system not added yet.");
}

function openCase(caseName){
alert("Opening case page for: " + caseName);
}

const cases = [
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

const input = document.getElementById("searchInput").value.toLowerCase();

if(cases.includes(input)){
alert("Opening archive page for: " + input);
}else{
alert("Case not found.");
}

}

</script>

</body>
</html>
</script>

</body>
</html>
