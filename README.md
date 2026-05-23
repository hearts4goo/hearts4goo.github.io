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
--bg2:#1a1320;
--card:#211826;
--text:#ffeef6;
--pink:#ff9dc0;
--accent:#ff5d95;
--border:#3d2d3f;
}

.light-mode{
--bg:#fff6fa;
--bg2:#ffe7f0;
--card:#fffafb;
--text:#2a1d26;
--pink:#cf5e88;
--accent:#a70052;
--border:#edbfd0;
}

*{
margin:0;
padding:0;
box-sizing:border-box;
}

body{
background:linear-gradient(var(--bg),#0f0a12);
color:var(--text);
font-family:'Quicksand',sans-serif;
overflow-x:hidden;
transition:.3s;
}

/* HEADER */

header{
position:sticky;
top:0;
z-index:999;

background:rgba(20,10,18,.88);

backdrop-filter:blur(14px);

border-bottom:1px solid var(--border);

padding:22px 28px;
}

.topbar{
display:flex;
align-items:center;
justify-content:space-between;
gap:30px;
flex-wrap:wrap;
}

/* LOGO */

.logo{
font-family:'Special Elite',cursive;
font-size:42px;
color:var(--pink);
line-height:1.1;
}

.logo small{
display:block;
font-size:12px;
margin-top:8px;
opacity:.7;
font-family:'Quicksand',sans-serif;
}

/* SEARCH */

.search-box{
display:flex;
gap:12px;
align-items:center;
}

.search-box input{
width:350px;

padding:15px 16px;

border-radius:16px;

border:1px solid var(--border);

background:var(--bg2);

color:var(--text);

font-size:14px;

outline:none;
}

.search-box button{

padding:15px 22px;

border:none;

border-radius:16px;

background:var(--pink);

font-weight:bold;

cursor:pointer;
}

/* MAIN LAYOUT */

.layout{

display:grid;

grid-template-columns:260px 1fr 320px;

gap:24px;

padding:30px;
}

/* PANELS */

.panel,
.post,
.hero{

background:rgba(33,24,38,.92);

border:1px solid var(--border);

border-radius:28px;
}

.panel{
padding:22px;
margin-bottom:24px;
}

.sidebar,
.rightbar{
position:sticky;
top:110px;
height:fit-content;
}

.panel-title{
font-family:'Special Elite',cursive;
font-size:24px;
margin-bottom:16px;
color:var(--pink);
}

/* MASCOT */

.mascot{
text-align:center;
}

.mascot img{
width:100%;
max-width:220px;
border-radius:20px;
image-rendering:pixelated;
}

.quote{
margin-top:14px;
line-height:1.8;
font-size:15px;
}

/* LEFT NAV */

.links{
display:flex;
flex-direction:column;
gap:12px;
}

.links a{
background:var(--bg2);
padding:15px;
border-radius:14px;
text-decoration:none;
color:var(--text);
transition:.2s;
font-size:15px;
}

.links a:hover{
background:#2a1f31;
transform:translateX(3px);
}

/* FEED */

.feed{
display:flex;
flex-direction:column;
gap:24px;
}

/* HERO */

.hero{
padding:50px;
}

.hero h1{
font-size:70px;
line-height:1;
font-family:'Special Elite',cursive;
margin-bottom:20px;
}

.hero h1 span{
color:var(--pink);
}

.hero p{
line-height:1.9;
font-size:17px;
margin-top:25px;
max-width:700px;
}

/* BUTTONS */

.buttons{
display:flex;
gap:14px;
margin-top:28px;
flex-wrap:wrap;
}

.btn{
padding:14px 24px;
border-radius:16px;
text-decoration:none;
font-weight:bold;
transition:.2s;
}

.btn:hover{
transform:translateY(-2px);
}

.primary{
background:var(--pink);
color:black;
}

.secondary{
background:var(--bg2);
border:1px solid var(--border);
color:var(--text);
}

/* POSTS */

.post{
padding:24px;
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
margin-bottom:16px;
color:var(--pink);
}

.post p{
line-height:1.9;
}

.actions{
display:flex;
gap:18px;
margin-top:18px;
font-size:14px;
opacity:.8;
}

/* CASES */

.case-card{
background:var(--bg2);
padding:18px;
border-radius:18px;
margin-bottom:14px;
border:1px solid var(--border);
cursor:pointer;
transition:.2s;
}

.case-card:hover{
transform:translateY(-3px);
background:#2a1f31;
}

.case-card h3{
color:var(--pink);
}

/* RULES */

.rules{
line-height:1.9;
font-size:14px;
}

/* MODAL */

.age-modal{
display:none;
position:fixed;
inset:0;
background:rgba(0,0,0,.7);
justify-content:center;
align-items:center;
z-index:2000;
}

.modal-box{
background:var(--card);
padding:35px;
border-radius:24px;
max-width:450px;
width:90%;
text-align:center;
border:1px solid var(--border);
}

.modal-box h2{
margin-bottom:16px;
font-family:'Special Elite',cursive;
color:var(--pink);
}

.modal-box p{
line-height:1.8;
margin-bottom:20px;
}

.modal-box button{
margin:6px;
padding:12px 20px;
border:none;
border-radius:12px;
cursor:pointer;
font-weight:bold;
}

.confirm{
background:var(--pink);
}

.cancel{
background:var(--bg2);
color:var(--text);
border:1px solid var(--border);
}

/* FOOTER */

footer{
padding:30px;
text-align:center;
opacity:.6;
}

/* MOBILE */

@media(max-width:1200px){

.layout{
grid-template-columns:1fr;
}

.sidebar,
.rightbar{
position:relative;
top:0;
}

}

@media(max-width:800px){

.topbar{
flex-direction:column;
align-items:flex-start;
}

.search-box{
width:100%;
}

.search-box input{
width:100%;
}

.hero h1{
font-size:48px;
}

.layout{
padding:18px;
}

}

</style>
</head>

<body>

<!-- AGE MODAL -->

<div class="age-modal" id="ageModal">

<div class="modal-box">

<h2>18+ Confirmation</h2>

<p>
This site discusses real crimes and disturbing events for awareness and educational purposes.
You must be 18 or older to create an account in order to communicate or view sensitive content.
</p>

<button class="confirm" onclick="closeModal()">
I am 18+
</button>

<button class="cancel" onclick="closeModal()">
Cancel
</button>

</div>

</div>

<!-- HEADER -->

<header>

<div class="topbar">

<div class="logo">
KOTJAS ARCHIVE

<small>
a wip archive for violent crimes
</small>

</div>

<div class="search-box">

<input
type="text"
id="searchInput"
placeholder="Search cases..."
>

<button onclick="searchCase()">
Search
</button>

</div>

</div>

</header>

<!-- MAIN -->

<div class="layout">

<!-- LEFT SIDEBAR -->

<aside class="sidebar">

<div class="panel mascot">

<img src="mascot.png" alt="Mascot">

<div class="quote">
archive. awareness.<br>
remembrance.
</div>

</div>

<!-- THIS IS THE CHANGED NAVIGATION -->

<div class="panel">

<div class="panel-title">
feed
</div>

<div class="links">

<a href="#">Home</a>

<a href="#" onclick="openModal()">
Account
</a>

<a href="#">
Inbox
</a>

<a href="#">
Explore
</a>

<a href="#" onclick="toggleMode()">
Settings
</a>

</div>

</div>

</aside>

<!-- CENTER FEED -->

<main class="feed">

<section class="hero">

<p>

Kotjas Archive is a community-based awareness project documenting crimes and tragedies aswell as letting users discuss those .

This site does not condone violent actions .

</p>

<div class="buttons">

<a href="#" class="btn primary">
Explore Cases
</a>

<a href="#" class="btn secondary" onclick="openModal()">
Create Account
</a>

</div>

</section>

<!-- POST -->

<article class="post">

<div class="post-header">

<div class="avatar"></div>

<div>

<div class="user">
Welcome
</div>

<div class="tag">
website work in progress
</div>

</div>

</div>

<h2>
Note from hearts4goo
</h2>

<p>
Me and nutelok just are still working on this, dont expect anything to work incase you even found this
we started this 23/05/2026
</p>

<div class="actions">

<span>♡ 2 likes</span>

<span>✎ 0 comments</span>

</div>

</article>

<!-- POST -->

<article class="post">

<div class="post-header">

<div class="avatar"></div>

<div>

<div class="user">
Community Notice
</div>

<div class="tag">
moderation update
</div>

</div>

</div>

<h2>
Content Policy
</h2>

<p>
Kotjas Archive does not glorify violence,
extremist ideologies,
or perpetrators.

Graphic content by users,
harassment,
and misinformation are prohibited.
</p>

<div class="actions">

<span>♡ 1 likes</span>

<span>✎ 0 comments</span>

</div>

</article>

</main>

<!-- RIGHT SIDEBAR -->

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

<div class="panel rules">

<div class="panel-title">
Rules
</div>

No glorification of violence.<br>
No harassment or threats.<br>
No graphic gore uploads.<br>
No misinformation or conspiracy spam.<br>
Educational discussion only.<br>
Accounts required to comment or access sensitive footage.

</div>

</aside>

</div>

<footer>
Kotjas Archive • awareness project • this site does not condone violent actions
</footer>

<script>

function toggleMode(){

document.body.classList.toggle('light-mode');

}

function openModal(){

document.getElementById('ageModal').style.display='flex';

}

function closeModal(){

document.getElementById('ageModal').style.display='none';

}

const cases = {

"vova and vika stepsiblings":"cases/vova.html",

"samantha rupnow":"cases/samantha.html",

"rina palenkova":"cases/rina.html",

"vladislav roslyakov":"cases/vladislav.html",

"pekka":"cases/pekka.html",

"brenton":"cases/brenton.html",

"payton":"cases/payton.html",

"adam lanza":"cases/adam.html",

"arthur achleithner":"cases/arthur.html"

};

function searchCase(){

const input = document
.getElementById("searchInput")
.value
.toLowerCase()
.trim();

if(cases[input]){

window.location.href = cases[input];

}else{

alert("Case not found.");

}

}

function openCase(name){

const key = name.toLowerCase();

if(cases[key]){

window.location.href = cases[key];

}

}

document
.getElementById("searchInput")
.addEventListener("keypress", function(e){

if(e.key === "Enter"){

searchCase();

}

});

</script>

</body>
</html>
