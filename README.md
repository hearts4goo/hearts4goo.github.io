<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Kotjas Archive</title>

<link href="https://fonts.googleapis.com/css2?family=Special+Elite&family=Quicksand:wght@300;400;500;600&display=swap" rel="stylesheet">

<style>

:root{
--bg:#120d14;
--bg2:#1a131d;
--card:#1f1723;
--border:#3f2d40;
--pink:#f29ab6;
--pink2:#c76b89;
--text:#fff2f7;
--muted:#cba7b5;
}

*{
margin:0;
padding:0;
box-sizing:border-box;
}

body{
background:
linear-gradient(rgba(8,6,10,.92),rgba(8,6,10,.94)),
url("background.png");
background-size:cover;
background-attachment:fixed;
color:var(--text);
font-family:'Quicksand',sans-serif;
overflow-x:hidden;
}

/* grain */

body::before{
content:"";
position:fixed;
inset:0;
background:url("https://www.transparenttextures.com/patterns/asfalt-dark.png");
opacity:.25;
pointer-events:none;
}

/* header */

header{
display:flex;
justify-content:space-between;
align-items:center;
padding:18px 30px;
background:rgba(15,10,15,.82);
backdrop-filter:blur(10px);
border-bottom:1px solid rgba(255,255,255,.06);
position:sticky;
top:0;
z-index:1000;
flex-wrap:wrap;
gap:20px;
}

.logo-wrap{
display:flex;
align-items:center;
gap:18px;
}

.logo-icon{
width:55px;
height:55px;
border-radius:18px;
background:var(--card);
display:flex;
align-items:center;
justify-content:center;
font-size:24px;
border:1px solid var(--border);
}

.logo h1{
font-family:'Special Elite',cursive;
font-size:42px;
color:var(--pink);
}

.logo p{
font-size:13px;
margin-top:6px;
color:var(--muted);
}

nav{
display:flex;
gap:24px;
flex-wrap:wrap;
}

nav a{
text-decoration:none;
color:var(--text);
font-size:14px;
position:relative;
}

nav a:hover{
color:var(--pink);
}

.right-nav{
display:flex;
gap:12px;
align-items:center;
flex-wrap:wrap;
}

.search{
padding:12px 15px;
background:var(--card);
border:1px solid var(--border);
border-radius:14px;
color:white;
width:190px;
}

.top-btn{
padding:12px 20px;
border-radius:14px;
background:var(--card);
border:1px solid var(--border);
color:white;
cursor:pointer;
font-family:'Quicksand',sans-serif;
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

/* hero */

.hero{
display:grid;
grid-template-columns:420px 1fr;
gap:70px;
align-items:center;
padding:70px;
}

.mascot{
position:relative;
display:flex;
justify-content:center;
}

.mascot img{
width:100%;
max-width:350px;
image-rendering:pixelated;
filter:drop-shadow(0 0 25px rgba(242,154,182,.2));
}

.hero-text h2{
font-family:'Special Elite',cursive;
font-size:90px;
line-height:1;
margin-bottom:24px;
}

.hero-text span{
color:var(--pink);
}

.line{
width:140px;
height:3px;
background:var(--pink);
margin-bottom:28px;
border-radius:999px;
}

.hero-text p{
line-height:2;
max-width:700px;
color:var(--muted);
margin-bottom:30px;
font-size:16px;
}

.hero-buttons{
display:flex;
gap:16px;
flex-wrap:wrap;
}

.hero-btn{
padding:15px 24px;
border-radius:18px;
background:var(--card);
border:1px solid var(--border);
text-decoration:none;
color:white;
transition:.2s;
}

.hero-btn:hover{
background:var(--pink);
color:black;
}

/* main layout */

.main{
display:grid;
grid-template-columns:2fr 1fr;
gap:25px;
padding:0 70px 50px;
}

/* cards */

.section{
background:rgba(20,15,20,.88);
border:1px solid var(--border);
border-radius:28px;
padding:26px;
}

.section-header{
display:flex;
justify-content:space-between;
align-items:center;
margin-bottom:24px;
flex-wrap:wrap;
gap:12px;
}

.section-header h3{
font-family:'Special Elite',cursive;
font-size:32px;
color:var(--pink);
}

.section-header a{
text-decoration:none;
color:var(--pink);
}

.cards{
display:grid;
grid-template-columns:repeat(2,1fr);
gap:18px;
}

.card{
background:var(--card);
border:1px solid var(--border);
border-radius:22px;
overflow:hidden;
transition:.2s;
}

.card:hover{
transform:translateY(-4px);
}

.placeholder{
height:180px;
background:
linear-gradient(
45deg,
#241821,
#161016
);
border-bottom:1px solid var(--border);
}

.card-content{
padding:20px;
}

.card h4{
font-family:'Special Elite',cursive;
font-size:26px;
margin-bottom:12px;
color:var(--pink);
}

.card span{
display:block;
font-size:13px;
margin-bottom:14px;
color:var(--muted);
}

.card p{
line-height:1.9;
font-size:14px;
margin-bottom:14px;
}

.card a{
text-decoration:none;
color:var(--pink);
}

/* sidebar */

.sidebar{
display:flex;
flex-direction:column;
gap:22px;
}

.side-box{
background:rgba(20,15,20,.88);
border:1px solid var(--border);
border-radius:28px;
padding:26px;
}

.side-box h3{
font-family:'Special Elite',cursive;
font-size:30px;
margin-bottom:18px;
color:var(--pink);
}

.side-box p{
line-height:2;
font-size:14px;
color:var(--muted);
margin-bottom:22px;
}

.community-btn{
display:block;
text-align:center;
padding:16px;
border-radius:18px;
background:var(--pink);
color:black;
text-decoration:none;
font-weight:bold;
margin-bottom:24px;
}

.notice{
padding:20px;
border-radius:18px;
background:rgba(255,255,255,.02);
border:1px solid var(--border);
line-height:2;
font-size:14px;
}

/* rules */

.rules{
margin:0 70px 60px;
background:rgba(20,15,20,.88);
border:1px solid var(--border);
border-radius:28px;
padding:30px;
}

.rules h3{
font-family:'Special Elite',cursive;
font-size:34px;
margin-bottom:20px;
color:var(--pink);
}

.rules ul{
padding-left:24px;
line-height:2.2;
color:var(--muted);
}

/* footer */

footer{
display:flex;
justify-content:space-between;
align-items:center;
padding:30px 70px;
border-top:1px solid rgba(255,255,255,.06);
background:rgba(15,10,15,.82);
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
gap:24px;
flex-wrap:wrap;
}

.footer-links a{
text-decoration:none;
color:var(--muted);
font-size:14px;
}

/* modal */

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
background:var(--card);
border:1px solid var(--border);
padding:40px;
border-radius:30px;
max-width:500px;
width:90%;
}

.modal-box h3{
font-family:'Special Elite',cursive;
font-size:40px;
margin-bottom:20px;
color:var(--pink);
}

.modal-box p{
line-height:2;
color:var(--muted);
margin-bottom:24px;
}

.modal-buttons{
display:flex;
gap:14px;
}

.modal-buttons button{
flex:1;
padding:15px;
border:none;
border-radius:14px;
cursor:pointer;
font-family:'Quicksand',sans-serif;
}

.confirm{
background:var(--pink);
}

.cancel{
background:#140f14;
border:1px solid var(--border);
color:white;
}

/* responsive */

@media(max-width:1200px){

.hero{
grid-template-columns:1fr;
text-align:center;
}

.hero-buttons{
justify-content:center;
}

.line{
margin-left:auto;
margin-right:auto;
}

.main{
grid-template-columns:1fr;
}

}

@media(max-width:850px){

header{
justify-content:center;
}

.hero{
padding:40px 25px;
}

.main{
padding:0 25px 40px;
}

.rules{
margin:0 25px 40px;
}

footer{
padding:25px;
}

.cards{
grid-template-columns:1fr;
}

.hero-text h2{
font-size:58px;
}

.logo h1{
font-size:30px;
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
This site discusses real crimes and tragedies
for awareness and educational purposes.

Users must be 18 or older to create an account
or access sensitive content.
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

<p>
record. remember. raise awareness.
</p>

</div>

</div>

<nav>

<a href="#">HOME</a>
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

<div class="line"></div>

<p>

Kotjas Archive documents real crimes,
disappearances, attacks, and tragedies
to educate, inform, and preserve awareness.

This archive does not condone violence,
extremism, or glorification of perpetrators.

</p>

<div class="hero-buttons">

<a href="#" class="hero-btn">
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
VIEW ALL →
</a>

</div>

<div class="cards">

<!-- card -->

<div class="card">

<div class="placeholder"></div>

<div class="card-content">

<h4>Samantha Rupnow</h4>

<span>Latest archive update</span>

<p>
Timeline additions,
discussion archives,
and collected resources.
</p>

<a href="#">
Read More →
</a>

</div>

</div>

<!-- card -->

<div class="card">

<div class="placeholder"></div>

<div class="card-content">

<h4>Rina Palenkova</h4>

<span>Historical archive</span>

<p>
Community discussion,
timeline documentation,
and preserved information.
</p>

<a href="#">
Read More →
</a>

</div>

</div>

<!-- card -->

<div class="card">

<div class="placeholder"></div>

<div class="card-content">

<h4>Adam Lanza</h4>

<span>Case archive</span>

<p>
Educational resources,
public information,
and discussion archive.
</p>

<a href="#">
Read More →
</a>

</div>

</div>

<!-- card -->

<div class="card">

<div class="placeholder"></div>

<div class="card-content">

<h4>Vladislav Roslyakov</h4>

<span>Case timeline</span>

<p>
Collected timeline,
reports,
and archived discussion.
</p>

<a href="#">
Read More →
</a>

</div>

</div>

</div>

</div>

<!-- SIDEBAR -->

<div class="sidebar">

<div class="side-box">

<h3>A COMMUNITY FOR AWARENESS</h3>

<p>

Join discussions,
share information,
and help preserve accurate archives.

</p>

<a href="#" class="community-btn">
JOIN COMMUNITY →
</a>

<div class="notice">

<strong>IMPORTANT</strong>

<br><br>

• No glorification of violence<br>
• No harassment or threats<br>
• No graphic gore uploads<br>
• Educational discussion only<br>
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
This site exists for educational and archival purposes.
</li>

<li>
Kotjas Archive does not support violent actions.
</li>

<li>
Graphic or exploitative content is prohibited.
</li>

<li>
Harassment and extremist propaganda are forbidden.
</li>

<li>
Users must be 18+ to access sensitive content.
</li>

</ul>

</section>

<!-- FOOTER -->

<footer>

<div class="footer-left">

<img src="mascot.png">

<div>

<strong>© 2026 KOTJAS ARCHIVE</strong>

<br>

<span style="color:var(--muted)">
not just stories. real lives.
</span>

</div>

</div>

<div class="footer-links">

<a href="#">
PRIVACY POLICY
</a>

<a href="#">
TERMS OF SERVICE
</a>

<a href="#">
CONTENT POLICY
</a>

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

/* search */

const cases = {

"samantha rupnow":"samantha-rupnow.html",
"rina palenkova":"rina-palenkova.html",
"adam lanza":"adam-lanza.html",
"vladislav roslyakov":"vladislav-roslyakov.html"

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
