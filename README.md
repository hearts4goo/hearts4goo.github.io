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

/* TOP BAR */

header{

position:sticky;
top:0;
z-index:999;

background:rgba(20,10,18,.92);

backdrop-filter:blur(14px);

border-bottom:1px solid var(--border);

padding:18px 30px;

display:flex;

justify-content:space-between;

align-items:center;

gap:30px;

}

/* SEARCH */

.search-header{

display:flex;

align-items:center;

gap:12px;

width:100%;

max-width:700px;

}

.search-header input{

flex:1;

padding:15px 18px;

border-radius:18px;

border:1px solid var(--border);

background:var(--bg2);

color:var(--text);

font-size:15px;

outline:none;

}

.search-header button{

padding:15px 20px;

border:none;

border-radius:18px;

background:var(--pink);

font-weight:bold;

cursor:pointer;

}

/* NAVIGATION */

nav{

display:flex;

gap:26px;

align-items:center;

}

nav a{

text-decoration:none;

color:var(--text);

font-size:15px;

transition:.2s;

padding-bottom:4px;

border-bottom:2px solid transparent;

}

nav a:hover{

color:var(--pink);

border-color:var(--pink);

}

/* LAYOUT */

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
top:95px;
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

image-rendering:pixelated;

border-radius:18px;

}

.quote{

margin-top:14px;

line-height:1.8;

font-size:15px;

}

/* LINKS */

.links{

display:flex;

flex-direction:column;

gap:12px;

}

.links a{

background:var(--bg2);

padding:12px 14px;

border-radius:14px;

text-decoration:none;

color:var(--text);

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

font-size:62px;

line-height:1.05;

font-family:'Special Elite',cursive;

margin-bottom:20px;

}

.hero h1 span{

color:var(--pink);

}

.hero p{

line-height:1.9;

font-size:17px;

max-width:700px;

margin-bottom:28px;

}

/* BUTTONS */

.buttons{

display:flex;

gap:14px;

flex-wrap:wrap;

}

.btn{

padding:14px 26px;

border-radius:16px;

text-decoration:none;

font-weight:bold;

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

padding:16px;

border-radius:18px;

margin-bottom:14px;

border:1px solid var(--border);

cursor:pointer;

transition:.2s;

}

.case-card:hover{

transform:translateY(-3px);

border-color:var(--pink);

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

@media(max-width:700px){

header{
flex-direction:column;
align-items:stretch;
}

nav{
justify-content:center;
flex-wrap:wrap;
}

.hero h1{
font-size:44px;
}

.layout{
padding:18px;
}

.hero{
padding:30px;
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
You must be 18 or older to create an account and access sensitive content.
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

<div class="search-header">

<input
type="text"
id="searchInput"
placeholder="Search cases..."
>

<button onclick="searchCase()">
Search
</button>

</div>

<nav>

<a href="#">Home</a>

<a href="#">Account</a>

<a href="#">Inbox</a>

<a href="#">Explore</a>

<a href="#">Settings</a>

</nav>

</header>

<!-- MAIN LAYOUT -->

<div class="layout">

<!-- LEFT SIDEBAR -->

<aside class="sidebar">

<div class="panel mascot">

<img src="mascot.png" alt="Mascot">

<div class="quote">
archive. awareness. remembrance.
</div>

</div>

<div class="panel">

<div class="panel-title">
Navigation
</div>

<div class="links">

<a href="#">Recent Cases</a>
<a href="#">Historical Archive</a>
<a href="#">Community Posts</a>
<a href="#">Missing Persons</a>
<a href="#" onclick="openModal()">Account Login</a>

</div>

</div>

</aside>

<!-- FEED -->

<main class="feed">

<section class="hero">

<h1>
archive the past.<br>
learn the patterns.<br>
<span>prevent the future.</span>
</h1>

<p>
Kotjas Archive is a community-based awareness project documenting crimes,
disappearances, attacks, and tragedies through timelines, discussions,
and educational resources.
This site does not condone violence or extremist ideologies.
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

<!-- POSTS -->

<article class="post">

<div class="post-header">

<div class="avatar"></div>

<div>

<div class="user">
Latest Archive Post
</div>

<div class="tag">
newest case update
</div>

</div>

</div>

<h2>
Samantha Rupnow Archive Added
</h2>

<p>
New timeline documentation, public reports, discussions,
and educational resources regarding the case have been added to the archive.
</p>

<div class="actions">

<span>♡ 3.1k likes</span>
<span>✎ 402 comments</span>

</div>

</article>

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
extremist ideologies, or perpetrators.
Graphic content, harassment, and misinformation are prohibited.
</p>

<div class="actions">

<span>♡ 1.2k likes</span>
<span>✎ 88 comments</span>

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

'vova and vika stepsiblings':'https://en.wikipedia.org/wiki/',
'samantha rupnow':'https://en.wikipedia.org/wiki/',
'rina palenkova':'https://en.wikipedia.org/wiki/',
'vladislav roslyakov':'https://en.wikipedia.org/wiki/Vladislav_Roslyakov',
'pekka':'https://en.wikipedia.org/wiki/Pekka-Eric_Auvinen',
'brenton':'https://en.wikipedia.org/wiki/Christchurch_mosque_shootings',
'payton':'https://en.wikipedia.org/wiki/2022_Buffalo_shooting',
'adam lanza':'https://en.wikipedia.org/wiki/Adam_Lanza',
'arthur achleithner':'https://en.wikipedia.org/wiki/'

};

function searchCase(){

const input =
document.getElementById('searchInput')
.value
.toLowerCase()
.trim();

if(cases[input]){

window.location.href = cases[input];

}else{

alert('Case not found.');

}

}

function openCase(name){

alert('Opening archive page for: ' + name);

}

</script>

</body>
</html>
