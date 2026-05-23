<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>

<title>Kotjas Archive</title>

<link href="https://fonts.googleapis.com/css2?family=Special+Elite&family=IBM+Plex+Mono:wght@300;400;500&display=swap" rel="stylesheet">

<style>

:root{
--bg:#080608;
--bg2:#120d12;
--card:#100c10;
--border:#4a2635;
--pink:#d67a95;
--text:#f4dfe7;
--muted:#b88c99;
--accent:#ff8ead;
}

*{
margin:0;
padding:0;
box-sizing:border-box;
}

body{
background:
linear-gradient(rgba(0,0,0,.82),rgba(0,0,0,.9)),
url("https://images.unsplash.com/photo-1519501025264-65ba15a82390?q=80&w=1600&auto=format&fit=crop");
background-size:cover;
background-attachment:fixed;
color:var(--text);
font-family:'IBM Plex Mono',monospace;
overflow-x:hidden;
}

/* grain overlay */

body::before{
content:"";
position:fixed;
inset:0;
background:url("https://www.transparenttextures.com/patterns/asfalt-dark.png");
opacity:.3;
pointer-events:none;
z-index:-1;
}

/* HEADER */

header{
display:flex;
justify-content:space-between;
align-items:center;
padding:22px 45px;
border-bottom:1px solid rgba(255,255,255,.08);
background:rgba(0,0,0,.45);
backdrop-filter:blur(8px);
position:sticky;
top:0;
z-index:999;
}

.logo-wrap{
display:flex;
align-items:center;
gap:18px;
}

.logo-icon{
width:55px;
height:55px;
border:1px solid var(--border);
display:flex;
align-items:center;
justify-content:center;
border-radius:8px;
background:rgba(255,255,255,.02);
font-size:22px;
}

.logo h1{
font-family:'Special Elite',cursive;
font-size:40px;
color:var(--pink);
letter-spacing:2px;
}

.logo p{
font-size:13px;
margin-top:4px;
color:var(--muted);
}

nav{
display:flex;
gap:34px;
align-items:center;
}

nav a{
text-decoration:none;
color:var(--text);
font-size:14px;
position:relative;
padding-bottom:6px;
}

nav a:hover{
color:var(--pink);
}

nav a.active::after{
content:"";
position:absolute;
left:0;
bottom:0;
width:100%;
height:2px;
background:var(--pink);
}

.right-nav{
display:flex;
align-items:center;
gap:14px;
}

.search{
background:rgba(255,255,255,.03);
border:1px solid var(--border);
padding:11px 14px;
border-radius:6px;
color:white;
width:180px;
}

.top-btn{
padding:12px 22px;
border:1px solid var(--border);
background:transparent;
color:var(--text);
cursor:pointer;
font-family:'IBM Plex Mono',monospace;
transition:.2s;
}

.top-btn:hover{
background:var(--pink);
color:black;
}

.signup{
background:var(--pink);
color:black;
}

/* HERO */

.hero{
display:grid;
grid-template-columns:1fr 1fr;
gap:60px;
padding:70px 70px 40px;
align-items:center;
border-bottom:1px solid rgba(255,255,255,.06);
}

.mascot{
display:flex;
justify-content:center;
position:relative;
}

.mascot img{
width:100%;
max-width:420px;
image-rendering:pixelated;
filter:drop-shadow(0 0 30px rgba(214,122,149,.25));
}

.hero-text h2{
font-size:82px;
line-height:1;
font-family:'Special Elite',cursive;
margin-bottom:30px;
}

.hero-text h2 span{
color:var(--pink);
}

.hero-text p{
line-height:2;
max-width:650px;
color:var(--muted);
margin-bottom:30px;
font-size:15px;
}

.hero-buttons{
display:flex;
gap:18px;
flex-wrap:wrap;
}

.hero-btn{
padding:16px 28px;
border:1px solid var(--border);
text-decoration:none;
color:var(--text);
transition:.2s;
}

.hero-btn:hover{
background:var(--pink);
color:black;
}

.primary{
background:rgba(214,122,149,.15);
}

/* MAIN */

.main{
display:grid;
grid-template-columns:2fr 1fr;
gap:35px;
padding:40px 70px;
}

/* RECENT CASES */

.section{
border:1px solid var(--border);
padding:26px;
background:rgba(10,10,10,.5);
}

.section-header{
display:flex;
justify-content:space-between;
align-items:center;
margin-bottom:24px;
}

.section-header h3{
font-family:'Special Elite',cursive;
font-size:30px;
color:var(--pink);
}

.section-header a{
text-decoration:none;
color:var(--pink);
font-size:14px;
}

.cards{
display:grid;
grid-template-columns:repeat(3,1fr);
gap:18px;
}

.card{
border:1px solid var(--border);
background:rgba(255,255,255,.02);
overflow:hidden;
transition:.2s;
}

.card:hover{
transform:translateY(-4px);
}

.card img{
width:100%;
height:180px;
object-fit:cover;
filter:brightness(.75);
}

.card-content{
padding:18px;
}

.card h4{
font-size:24px;
margin-bottom:12px;
color:var(--pink);
font-family:'Special Elite',cursive;
}

.card span{
font-size:13px;
color:var(--muted);
display:block;
margin-bottom:14px;
}

.card p{
font-size:14px;
line-height:1.8;
margin-bottom:16px;
}

.card a{
color:var(--pink);
text-decoration:none;
}

/* SIDEBAR */

.sidebar{
display:flex;
flex-direction:column;
gap:24px;
}

.side-box{
border:1px solid var(--border);
padding:28px;
background:rgba(10,10,10,.5);
}

.side-box h3{
font-family:'Special Elite',cursive;
font-size:28px;
margin-bottom:18px;
color:var(--pink);
}

.side-box p{
line-height:2;
font-size:14px;
color:var(--muted);
margin-bottom:24px;
}

.community-btn{
display:block;
padding:16px;
text-align:center;
background:var(--pink);
color:black;
text-decoration:none;
margin-bottom:20px;
font-weight:bold;
}

.notice{
border:1px solid rgba(214,122,149,.3);
padding:20px;
line-height:2;
font-size:14px;
}

/* RULES */

.rules{
margin:0 70px 40px;
border:1px solid var(--border);
padding:35px;
background:rgba(10,10,10,.55);
}

.rules h3{
font-family:'Special Elite',cursive;
font-size:34px;
margin-bottom:20px;
color:var(--pink);
}

.rules ul{
padding-left:22px;
line-height:2.2;
color:var(--muted);
}

/* FOOTER */

footer{
display:flex;
justify-content:space-between;
align-items:center;
padding:35px 70px;
border-top:1px solid rgba(255,255,255,.08);
background:rgba(0,0,0,.4);
flex-wrap:wrap;
gap:20px;
}

.footer-left{
display:flex;
align-items:center;
gap:16px;
}

.footer-left img{
width:55px;
image-rendering:pixelated;
}

.footer-links{
display:flex;
gap:30px;
flex-wrap:wrap;
}

.footer-links a{
text-decoration:none;
color:var(--muted);
font-size:14px;
}

.socials{
display:flex;
gap:14px;
}

.social{
width:48px;
height:48px;
display:flex;
align-items:center;
justify-content:center;
border:1px solid var(--border);
font-size:20px;
}

/* AGE MODAL */

.modal{
display:none;
position:fixed;
inset:0;
background:rgba(0,0,0,.8);
justify-content:center;
align-items:center;
z-index:3000;
}

.modal-box{
width:90%;
max-width:500px;
background:var(--card);
border:1px solid var(--border);
padding:40px;
}

.modal-box h3{
font-size:38px;
font-family:'Special Elite',cursive;
margin-bottom:18px;
color:var(--pink);
}

.modal-box p{
line-height:2;
margin-bottom:24px;
color:var(--muted);
}

.modal-buttons{
display:flex;
gap:14px;
}

.modal-buttons button{
flex:1;
padding:15px;
border:none;
cursor:pointer;
font-family:'IBM Plex Mono',monospace;
}

.confirm{
background:var(--pink);
}

.cancel{
background:#1a1117;
color:white;
border:1px solid var(--border);
}

/* RESPONSIVE */

@media(max-width:1200px){

.hero{
grid-template-columns:1fr;
text-align:center;
}

.hero-buttons{
justify-content:center;
}

.main{
grid-template-columns:1fr;
}

.cards{
grid-template-columns:1fr;
}

}

@media(max-width:850px){

header{
flex-direction:column;
gap:20px;
padding:25px;
}

nav{
flex-wrap:wrap;
justify-content:center;
}

.hero,
.main,
.rules,
footer{
padding-left:25px;
padding-right:25px;
margin-left:0;
margin-right:0;
}

.hero-text h2{
font-size:52px;
}

}

</style>
</head>

<body>

<!-- AGE MODAL -->

<div class="modal" id="ageModal">

<div class="modal-box">

<h3>18+ Confirmation</h3>

<p>
This archive discusses real crimes, violence,
and disturbing events for awareness and
educational documentation purposes.

You must be 18 or older to create an account
or access sensitive footage/discussions.
</p>

<div class="modal-buttons">

<button class="confirm" onclick="closeModal()">
I AM 18+
</button>

<button class="cancel" onclick="closeModal()">
CANCEL
</button>

</div>

</div>

</div>

<!-- HEADER -->

<header>

<div class="logo-wrap">

<div class="logo-icon">
🗂
</div>

<div class="logo">
<h1>KOTJAS ARCHIVE</h1>
<p>record. remember. raise awareness.</p>
</div>

</div>

<nav>

<a href="#" class="active">HOME</a>
<a href="#">CASES</a>
<a href="#">MISSING</a>
<a href="#">TIMELINE</a>
<a href="#">COMMUNITY</a>
<a href="#">RESOURCES</a>
<a href="#">ABOUT</a>

</nav>

<div class="right-nav">

<input
type="text"
class="search"
id="searchInput"
placeholder="search cases..."
>

<button class="top-btn">
LOGIN
</button>

<button
class="top-btn signup"
onclick="openModal()"
>
SIGN UP
</button>

</div>

</header>

<!-- HERO -->

<section class="hero">

<div class="mascot">
<img src="mascot.png">
</div>

<div class="hero-text">

<h2>
truth.<br>
awareness.<br>
<span>change.</span>
</h2>

<p>
Kotjas Archive documents real crimes,
disappearances, attacks, and tragedies
to educate, inform, and raise awareness.

This archive does not condone violent acts,
extremism, or glorification of perpetrators.
</p>

<div class="hero-buttons">

<a href="#" class="hero-btn primary">
EXPLORE CASES →
</a>

<a href="#" class="hero-btn">
COMMUNITY →
</a>

</div>

</div>

</section>

<!-- MAIN -->

<section class="main">

<!-- LEFT -->

<div class="section">

<div class="section-header">

<h3>RECENT CASES</h3>

<a href="#">
VIEW ALL CASES →
</a>

</div>

<div class="cards">

<!-- CARD 1 -->

<div class="card">

<img src="https://images.unsplash.com/photo-1519501025264-65ba15a82390?q=80&w=1200&auto=format&fit=crop">

<div class="card-content">

<h4>Samantha Rupnow</h4>

<span>May 15, 2026</span>

<p>
Latest timeline additions,
documents, and discussion archive.
</p>

<a href="#">
Read More →
</a>

</div>

</div>

<!-- CARD 2 -->

<div class="card">

<img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?q=80&w=1200&auto=format&fit=crop">

<div class="card-content">

<h4>Rina Palenkova</h4>

<span>May 10, 2026</span>

<p>
Community timeline and
historical archive documentation.
</p>

<a href="#">
Read More →
</a>

</div>

</div>

<!-- CARD 3 -->

<div class="card">

<img src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?q=80&w=1200&auto=format&fit=crop">

<div class="card-content">

<h4>Adam Lanza</h4>

<span>April 28, 2026</span>

<p>
Case archive, timeline,
and educational resources.
</p>

<a href="#">
Read More →
</a>

</div>

</div>

</div>

</div>

<!-- RIGHT -->

<div class="sidebar">

<div class="side-box">

<h3>A COMMUNITY FOR AWARENESS</h3>

<p>
Join discussions, share information,
and help preserve accurate archives
while respecting victims and families.
</p>

<a href="#" class="community-btn">
JOIN THE COMMUNITY →
</a>

<div class="notice">

<strong>IMPORTANT</strong><br><br>

• No glorification of violence<br>
• No graphic gore uploads<br>
• No harassment or threats<br>
• Educational purposes only<br>
• Accounts required for comments

</div>

</div>

</div>

</section>

<!-- RULES -->

<section class="rules">

<h3>CONTENT POLICY</h3>

<ul>

<li>
This site exists for educational awareness and archival purposes.
</li>

<li>
Kotjas Archive does not support or glorify violent actions.
</li>

<li>
Graphic or exploitative material is prohibited.
</li>

<li>
Harassment, threats, and extremist propaganda are forbidden.
</li>

<li>
Users must be 18+ to access sensitive content or create accounts.
</li>

</ul>

</section>

<!-- FOOTER -->

<footer>

<div class="footer-left">

<img src="mascot.png">

<div>

<strong>© 2026 KOTJAS ARCHIVE</strong><br>

<span style="color:var(--muted)">
not just stories. real lives.
</span>

</div>

</div>

<div class="footer-links">

<a href="#">PRIVACY POLICY</a>
<a href="#">TERMS OF SERVICE</a>
<a href="#">CONTENT POLICY</a>

</div>

<div class="socials">

<div class="social">✉</div>
<div class="social">☾</div>
<div class="social">★</div>

</div>

</footer>

<script>

function openModal(){
document.getElementById("ageModal")
.style.display = "flex";
}

function closeModal(){
document.getElementById("ageModal")
.style.display = "none";
}

/* SEARCH */

const cases = {
"samantha rupnow":"samantha-rupnow.html",
"rina palenkova":"rina-palenkova.html",
"adam lanza":"adam-lanza.html",
"vladislav roslyakov":"vladislav-roslyakov.html",
"pekka":"pekka.html",
"brenton":"brenton.html",
"payton":"payton.html",
"arthur achleithner":"arthur-achleithner.html"
};

document
.getElementById("searchInput")
.addEventListener("keypress", function(e){

if(e.key === "Enter"){

const value =
this.value.toLowerCase().trim();

if(cases[value]){
window.location.href = cases[value];
}else{
alert("Case not found.");
}

}

});

</script>

</body>
</html>
