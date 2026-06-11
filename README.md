# zaproshennya-na-vesillya
<!DOCTYPE html>
<html lang="uk">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Весільне запрошення</title>

<link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">

<style>
body{
    margin:0;
    font-family:Montserrat,sans-serif;
    background:#fffaf5;
    color:#444;
}

.hero{
    height:100vh;
    background:linear-gradient(rgba(0,0,0,.35),rgba(0,0,0,.35)),
    url('https://images.unsplash.com/photo-1519741497674-611481863552?auto=format&fit=crop&w=1920&q=80');
    background-size:cover;
    background-position:center;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    color:white;
}

h1{
    font-family:'Dancing Script',cursive;
    font-size:72px;
    margin:0;
}

.date{
    font-size:24px;
    margin-top:15px;
}

.section{
    max-width:900px;
    margin:auto;
    padding:60px 20px;
    text-align:center;
}

.card{
    background:white;
    padding:25px;
    border-radius:20px;
    box-shadow:0 10px 25px rgba(0,0,0,.08);
}

#countdown{
    font-size:32px;
    font-weight:bold;
    margin-top:20px;
}

.button{
    display:inline-block;
    padding:14px 28px;
    background:#d4a373;
    color:white;
    text-decoration:none;
    border-radius:50px;
    margin-top:20px;
}
</style>
</head>

<body>

<section class="hero">
    <div>
        <p>МИ ОДРУЖУЄМОСЬ</p>
        <h1>Максим & Марія</h1>
        <div class="date">26 серпня 2026 • 12:00</div>
        <a href="#details" class="button">Деталі</a>
    </div>
</section>

<section id="details" class="section">
    <h2>Дорогі друзі та рідні!</h2>

    <p>
        Запрошуємо вас розділити з нами найщасливіший день нашого життя.
        Будемо раді бачити вас на нашій весільній церемонії.
    </p>

    <div class="card">
        <h3>💍 Церемонія</h3>
        <p><b>26 серпня 2026 року</b></p>
        <p><b>12:00</b></p>
        <p>Подільський ДРАЦС</p>
        <p>вул. Борисоглібська, 6, Київ</p>
    </div>
</section>

<section class="section">
    <h2>До зустрічі залишилось:</h2>
    <div id="countdown">Завантаження...</div>
</section>

<section class="section">
    <h2>📍 Локація</h2>

    <iframe
        src="https://maps.google.com/maps?q=Борисоглібська%206%20Київ&t=&z=15&ie=UTF8&iwloc=&output=embed"
        width="100%"
        height="400"
        style="border:0;border-radius:20px;"
        loading="lazy">
    </iframe>
</section>

<script>
const weddingDate = new Date("2026-08-26T12:00:00").getTime();

setInterval(() => {
    const now = new Date().getTime();
    const distance = weddingDate - now;

    const days = Math.floor(distance / (1000*60*60*24));
    const hours = Math.floor((distance % (1000*60*60*24)) / (1000*60*60));
    const minutes = Math.floor((distance % (1000*60*60)) / (1000*60));
    const seconds = Math.floor((distance % (1000*60)) / 1000);

    document.getElementById("countdown").innerHTML =
        `${days} днів ${hours} год ${minutes} хв ${seconds} сек`;

}, 1000);
</script>

</body>
</html>