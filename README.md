# index.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kotjas Archive</title>

<link href="https://fonts.googleapis.com/css2?family=Special+Elite&family=Quicksand:wght@400;600&display=swap" rel="stylesheet">

<style>

:root{
--bg:#0c0b10;
--bg2:#15131b;
--card:#1b1822;
--text:#ffeef5;
--pink:#ff8db4;
--accent:#ff5c97;
--border:#312737;
--shadow:rgba(255,141,180,0.15);
}

.light-mode{
--bg:#fff3f7;
--bg2:#ffe6ef;
--card:#fff9fc;
--text:#2b1d25;
--pink:#d85b87;
--accent:#b10053;
--border:#efbfd1;
--shadow:rgba(216,91,135,0.15);
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
transition:0.3s;
overflow-x:hidden;
}

::-webkit-scrollbar{
width:10px;
}

::-webkit-scrollbar-thumb{
background:var(--pink);
border-radius:20px;
}

header{
position:sticky;
top:0;
z-index:999;
background:rgba(10,10,10,0.75);
backdrop-filter:blur(12px);
border-bottom:1px solid var(--border);
padding:18px 40px;
display:flex;
justify-content:space-between;
align-items:center;
}

.logo{
font-family:'Special Elite',cursive;
font-size:32px;
color:var(--pink);
letter-spacing:2px;
}

.logo small{
display:block;
font-size:12px;
color:var(--text);
opacity:0.7;
margin-top:4px;
font-family:'Quicksand',sans-serif;
}

nav{
display:flex;
gap:24px;
align-items:center;
}

nav a{
color:var(--text);
text-decoration:none;
font-size:14px;
transition:0.2s;
}

nav a:hover{
color:var(--pink);
}

.toggle{
background:var(--card);
border:1px solid var(--border);
color:var(--text);
padding:10px 18px;
border-radius:14px;
cursor:pointer;
font-weight:bold;
}

.layout{
display:grid;
grid-template-columns:280px 1fr 320px;
gap:24px;
padding:30px;
}

.sidebar,
.rightbar{
position:sticky;
top:100px;
height:fit-content;
}

.panel{
background:var(--card);
border:1px solid var(--border);
border-radius:24px;
padding:24px;
margin-bottom:24px;
box-shadow:0 0 30px var(--shadow);
}

.panel-title{
font-family:'Special Elite',cursive;
font-size:24px;
margin-bottom:18px;
color:var(--pink);
}

.mascot{
text-align:center;
}

.mascot img{
width:100%;
max-width:220px;
image-rendering:pixelated;
filter:drop-shadow(0 0 20px var(--shadow));
animation:float 4s ease-in-out infinite;
}

@keyframes float{
0%{transform:translateY(0px);} 
50%{transform:translateY(-8px);} 
100%{transform:translateY(0px);} 
}

.quote{
margin-top:16px;
font-size:15px;
line-height:1.8;
opacity:0.9;
}

.links{
display:flex;
flex-direction:column;
gap:14px;
}

.links a{
text-decoration:none;
color:var(--text);
padding:12px 14px;
border-radius:14px;
background:var(--bg2);
transition:0.2s;
}

.links a:hover{
background:var(--pink);
color:black;
}

.feed{
display:flex;
flex-direction:column;
gap:24px;
}

.hero{
background:linear-gradient(145deg,var(--card),var(--bg2));
border:1px solid var(--border);
border-radius:30px;
padding:50px;
position:relative;
overflow:hidden;
}

.hero::before{
content:"";
position:absolute;
width:300px;
height:300px;
background:var(--pink);
opacity:0.08;
border-radius:50%;
top:-120px;
right:-120px;
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
max-width:700px;
line-height:1.9;
font-size:17px;
opacity:0.9;
margin-bottom:30px;
}

.buttons{
display:flex;
gap:16px;
flex-wrap:wrap;
}

.btn{
padding:14px 28px;
border-radius:16px;
text-decoration:none;
font-weight:bold;
transition:0.2s;
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

.btn:hover{
transform:translateY(-3px);
}

.post{
background:var(--card);
border:1px solid var(--border);
border-radius:24px;
padding:24px;
box-shadow:0 0 25px var(--shadow);
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

.user{
font-weight:bold;
}

.tag{
font-size:13px;
opacity:0.7;
}

.post img{
width:100%;
border-radius:18px;
margin:18px 0;
}

.post h2{
margin-bottom:14px;
font-family:'Special Elite',cursive;
color:var(--pink);
}

.post p{
line-height:1.9;
opacity:0.95;
}

.actions{
display:flex;
gap:18px;
margin-top:18px;
font-size:14px;
opacity:0.8;
}

.case-card{
background:var(--bg2);
padding:18px;
border-radius:18px;
border:1px solid var(--border);
margin-bottom:16px;
}

.case-card h3{
margin-bottom:10px;
color:var(--pink);
}

.case-card p{
font-size:14px;
line-height:1.7;
}

.warning{
background:rgba(255,92,151,0.1);
border:1px solid rgba(255,92,151,0.3);
padding:18px;
border-radius:18px;
line-height:1.8;
font-size:14px;
}

footer{
padding:30px;
text-align:center;
opacity:0.6;
font-size:14px;
}

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
padding:20px;
flex-direction:column;
gap:20px;
}

nav{
flex-wrap:wrap;
justify-content:center;
}

.hero{
padding:30px;
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

<header>
<div class="logo">
KOTJAS ARCHIVE
<small>record. remember. awareness.</small>
</div>

<nav>
<a href="#">Home</a>
<a href="#">Cases</a>
<a href="#">Missing</a>
<a href="#">Timeline</a>
<a href="#">Community</a>
<a href="#">Resources</a>
</nav>

<button class="toggle" onclick="toggleMode()">
Toggle Theme
</button>
</header>

<div class="layout">

<aside class="sidebar">

<div class="panel mascot">
<img src="mascot.png" alt="Mascot">
<div class="quote">
truth. awareness. change.
</div>
</div>

<div class="panel">
<div class="panel-title">Navigation</div>
<div class="links">
<a href="#">Recent Cases</a>
<a href="#">Historical Archive</a>
<a href="#">Community Posts</a>
<a href="#">Missing Persons</a>
<a href="#">Safety Resources</a>
</div>
</div>

</aside>

<main class="feed">

<section class="hero">
<h1>
truth.<br>
awareness.<br>
<span>change.</span>
</h1>

<p>
Kotjas Archive is a community-driven awareness project documenting crimes, disappearances, and tragedies through timelines, discussions, archives, and educational resources.
</p>

<div class="buttons">
<a href="#" class="btn primary">Explore Cases</a>
<a href="#" class="btn secondary">Join Community</a>
</div>
</section>

<article class="post">
<div class="post-header">
<div class="avatar"></div>
<div>
<div class="user">Kotjas Archive</div>
<div class="tag">featured archive post</div>
</div>
</div>

<h2>Recent Community Discussion</h2>

<p>
Users can discuss timelines, theories, safety awareness, and verified updates in a moderated environment focused on education and remembrance.
</p>

<img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?q=80&w=1200&auto=format&fit=crop" alt="Dark forest">

<p>
This layout mixes fandom-style archives with Tumblr-inspired community posting and scrolling discussions.
</p>

<div class="actions">
<span>♡ 2.4k likes</span>
<span>✎ 184 comments</span>
<span>↻ share</span>
</div>
</article>

<article class="post">
<div class="post-header">
<div class="avatar"></div>
<div>
<div class="user">Moderator Team</div>
<div class="tag">community update</div>
</div>
</div>

<h2>Community Guidelines</h2>

<p>
We do not glorify violence or share graphic material. The purpose of this archive is awareness, documentation, education, and respectful discussion.
</p>

<div class="actions">
<span>♡ 891 likes</span>
<span>✎ 72 comments</span>
</div>
</article>

</main>

<aside class="rightbar">

<div class="panel">
<div class="panel-title">Trending Cases</div>

<div class="case-card">
<h3>City Mall Shooting</h3>
<p>Timeline archive and ongoing discussion thread.</p>
</div>

<div class="case-card">
<h3>Riverside Disappearance</h3>
<p>Community research and evidence timeline.</p>
</div>

<div class="case-card">
<h3>Oakwood Murders</h3>
<p>Historical case archive with witness reports.</p>
</div>

</div>

<div class="panel warning">
<strong>Important:</strong><br><br>
This site discusses real crimes and tragedies for awareness and educational purposes. Graphic content, harassment, glorification, and misinformation are prohibited.
</div>

</aside>

</div>

<footer>
Kotjas Archive • community awareness project
</footer>

<script>
function toggleMode(){
document.body.classList.toggle('light-mode');
}
</script>

</body>
</html>
