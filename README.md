<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family: Arial, sans-serif;
}
body{
    line-height:1.6;
    color:#222;
}
a{
    text-decoration:none;
    color:inherit;
}
.topbar{
    background:#222;
    color:#fff;
    padding:8px 30px;
    font-size:14px;
    display:flex;
    justify-content:flex-end;
    gap:20px;
}
.header{
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:20px 40px;
    background:#fff;
    border-bottom:1px solid #ddd;
}
.logo{
    font-size:28px;
    font-weight:bold;
    color:#036A38;
}
.header-buttons{
    display:flex;
    gap:15px;
}
.btn{
    padding:10px 20px;
    border-radius:25px;
    border:2px solid #036A38;
    color:#036A38;
    font-weight:bold;
    transition:0.3s;
}
.btn:hover{
    background:#036A38;
    color:#fff;
}
.navbar{
    background:#036A38;
    color:#fff;
}
.navbar ul{
    display:flex;
    list-style:none;
    justify-content:center;
    flex-wrap:wrap;
}
.navbar li{
    padding:18px 20px;
    cursor:pointer;
}
.navbar li:hover{
    background:#02572d;
}
.hero{
    height:500px;
    background:url('https://images.unsplash.com/photo-1448375240586-882707db888b') center/cover no-repeat;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    color:#fff;
}
.hero h1{
    font-size:52px;
    background:rgba(0,0,0,0.45);
    padding:20px 30px;
    border-radius:8px;
}
.cta{
    padding:60px 20px;
    text-align:center;
    background:#fff;
}
.cta h2{
    font-size:38px;
    margin-bottom:20px;
    color:#036A38;
}
.cta p{
    max-width:900px;
    margin:auto;
    margin-bottom:25px;
    font-size:18px;
}
.cta .btn{
    background:#036A38;
    color:#fff;
}
.news-section{
    display:flex;
    flex-wrap:wrap;
    padding:50px 30px;
    background:#f8f8f8;
}
.sidebar{
    flex:1;
    min-width:250px;
    max-width:300px;
    background:#fff;
    padding:25px;
    border-radius:8px;
    box-shadow:0 2px 8px rgba(0,0,0,0.1);
}
.sidebar h3{
    margin-bottom:20px;
    color:#036A38;
}
.sidebar ul{
    list-style:none;
}
.sidebar li{
    padding:12px 0;
    border-bottom:1px solid #ddd;
    cursor:pointer;
}
.sidebar li:hover{
    color:#036A38;
}
.cards{
    flex:3;
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:20px;
    padding-left:30px;
}
.card{
    background:#fff;
    border-radius:8px;
    overflow:hidden;
    box-shadow:0 2px 8px rgba(0,0,0,0.1);
}
.card img{
    width:100%;
    height:180px;
    object-fit:cover;
}
.card-content{
    padding:20px;
}
.card-content h4{
    margin-bottom:10px;
    color:#036A38;
}
.footer{
    background:#222;
    color:#fff;
    text-align:center;
    padding:20px;
}
@media(max-width:768px){
    .header{
        flex-direction:column;
        gap:15px;
    }
    .hero h1{
        font-size:32px;
    }
    .news-section{
        flex-direction:column;
    }
    .cards{
        padding-left:0;
        margin-top:20px;
    }
}
</style>
</head>
<body>

<div class="topbar">
    <a href="#">CUFN Exchange</a>
    <a href="#">Français</a>
</div>

<header class="header">
    <div class="logo">🌳 Tree Canada</div>
    <div class="header-buttons">
        <a href="#" class="btn">Search</a>
        <a href="#" class="btn">Donate</a>
    </div>
</header>

<nav class="navbar">
    <ul>
        <li>About Us</li>
        <li>Our Programs</li>
        <li>Research & Engagement</li>
        <li>Grants & Awards</li>
        <li>Resources</li>
        <li>Take Action</li>
    </ul>
</nav>

<section class="hero">
    <h1>Growing Better Places to Live</h1>
</section>

<section class="cta">
    <h2>Growing Better Places to Live</h2>
    <p>
        Tree Canada is the only national non-profit organization dedicated to planting and nurturing trees
        in rural and urban environments across the country.
    </p>
    <a href="#" class="btn">Plant Trees</a>
</section>

<section class="news-section">
    <aside class="sidebar">
        <h3>What's New</h3>
        <ul>
            <li onclick="filterCards('featured')">Featured</li>
            <li onclick="filterCards('programs')">Our Programs</li>
            <li onclick="filterCards('stories')">News & Stories</li>
        </ul>
    </aside>

    <div class="cards" id="cardsContainer">
        <div class="card featured">
            <img src="https://images.unsplash.com/photo-1501004318641-b39e6451bec6" alt="">
            <div class="card-content">
                <h4>Community Tree Grants</h4>
                <p>Helping communities plant and care for trees.</p>
            </div>
        </div>

        <div class="card programs">
            <img src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e" alt="">
            <div class="card-content">
                <h4>National Greening Program</h4>
                <p>Supporting reforestation projects nationwide.</p>
            </div>
        </div>

        <div class="card stories">
            <img src="https://images.unsplash.com/photo-1465146344425-f00d5f5c8f07" alt="">
            <div class="card-content">
                <h4>Success Stories</h4>
                <p>Read about our impact in communities.</p>
            </div>
        </div>
    </div>
</section>

<footer class="footer">
    © 2026 Tree Canada Demo. All rights reserved.
</footer>

<script>
function filterCards(category){
    const cards = document.querySelectorAll('.card');
    cards.forEach(card=>{
        if(card.classList.contains(category)){
            card.style.display='block';
        } else {
            card.style.display='none';
        }
    });
}
</script>

</body>
</html>
