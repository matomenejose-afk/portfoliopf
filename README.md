# portfoliopf

<!DOCTYPE html>
<html lang="pt">
<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Portfolio.pf | Loja Online</title>

<style>

/* =========================
   CONFIGURAÇÃO GERAL
========================= */

:root {
    --verde: #00ff88;
    --verde-escuro: #00b36b;
    --preto: #050505;
    --cinza: #111111;
    --texto: #cccccc;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

html {
    scroll-behavior: smooth;
    scroll-padding-top: 100px;
}

body {
    background: var(--preto);
    color: white;
}

/* =========================
   CABEÇALHO
========================= */

header {
    background: rgba(0,0,0,0.97);
    border-bottom: 1px solid var(--verde);
    padding: 18px 30px;

    position: fixed;
    width: 100%;
    top: 0;
    left: 0;
    z-index: 1000;
}

nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo {
    color: var(--verde);
    font-size: 28px;
    font-weight: bold;
    letter-spacing: 2px;
    text-shadow: 0 0 12px var(--verde);
}

.menu {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
}

.menu a {
    color: white;
    text-decoration: none;
    font-size: 14px;
    transition: .3s;
}

.menu a:hover {
    color: var(--verde);
    text-shadow: 0 0 10px var(--verde);
}

/* =========================
   CAPA PRINCIPAL
========================= */

.banner {
    margin-top: 70px;
    min-height: 480px;

    background:
    linear-gradient(
        rgba(0,0,0,.65),
        rgba(0,0,0,.75)
    ),
    url("img/capa.jpg") center/cover;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    text-align: center;
    padding: 40px 20px;
}

.banner h1 {
    color: var(--verde);
    font-size: 48px;
    margin-bottom: 20px;
    text-shadow: 0 0 20px rgba(0,255,136,.5);
}

.banner p {
    color: white;
    font-size: 20px;
    margin-bottom: 25px;
}

.botao-banner {
    display: inline-block;
    background: var(--verde);
    color: black;
    padding: 14px 30px;
    border-radius: 5px;
    font-weight: bold;
    text-decoration: none;
    transition: .3s;
}

.botao-banner:hover {
    background: white;
    box-shadow: 0 0 20px var(--verde);
}

/* =========================
   SECÇÕES GERAIS
========================= */

section {
    padding: 75px 25px;
    max-width: 1250px;
    margin: auto;
}

h2 {
    color: var(--verde);
    text-align: center;
    font-size: 32px;
    margin-bottom: 40px;
    text-shadow: 0 0 10px rgba(0,255,136,.2);
}

h2::after {
    content: "";
    display: block;
    width: 70px;
    height: 3px;
    background: var(--verde);
    margin: 15px auto 0;
}

/* =========================
   VÍDEO DE APRESENTAÇÃO
========================= */

.video-section {
    text-align: center;
}

.video-section > p {
    color: var(--texto);
    margin-bottom: 30px;
    line-height: 1.7;
}

.video-container {
    max-width: 850px;
    margin: auto;
    padding: 10px;

    background: var(--cinza);
    border: 1px solid var(--verde);
    border-radius: 15px;

    box-shadow: 0 0 20px rgba(0,255,136,.2);
}

.video-container video {
    width: 100%;
    display: block;
    border-radius: 10px;
    background: black;
}

/* =========================
   SOBRE NÓS
========================= */

.sobre {
    background: var(--cinza);
    border: 1px solid #164b34;
    padding: 35px;
    border-radius: 12px;
    text-align: center;
    line-height: 1.9;
    color: var(--texto);
    font-size: 17px;
}

/* =========================
   PRODUTOS
========================= */

.cards {
    display: grid;

    grid-template-columns:
    repeat(auto-fit, minmax(230px, 1fr));

    gap: 28px;
}

.card {
    background: #101010;
    border: 1px solid #164b34;
    border-radius: 12px;
    overflow: hidden;
    text-align: center;
    transition: .35s;
}

.card:hover {
    transform: translateY(-8px);
    border-color: var(--verde);
    box-shadow: 0 0 22px rgba(0,255,136,.22);
}

.card img {
    width: 100%;
    height: 230px;
    object-fit: cover;
    display: block;
}

.card h3 {
    color: var(--verde);
    font-size: 20px;
    margin: 18px 0 10px;
}

.card p {
    color: #aaaaaa;
    padding: 0 15px;
    line-height: 1.6;
    margin-bottom: 12px;
}

.preco {
    color: var(--verde);
    font-size: 23px;
    font-weight: bold;
    margin: 18px;
}

/* BOTÃO COMPRAR */

.botao {
    display: inline-block;
    background: var(--verde);
    color: black;
    padding: 11px 25px;
    border-radius: 5px;
    font-weight: bold;
    text-decoration: none;
    margin-bottom: 22px;
    transition: .3s;
}

.botao:hover {
    background: white;
    box-shadow: 0 0 15px var(--verde);
}

/* =========================
   CONTACTOS
========================= */

.contactos {
    background: var(--cinza);
    border: 1px solid #164b34;
    border-radius: 12px;
    padding: 35px;
    text-align: center;
    line-height: 2.2;
}

.contactos p {
    color: var(--texto);
}

.contactos strong {
    color: var(--verde);
}

/* =========================
   MAPA
========================= */

.mapa-container {
    display: grid;
    grid-template-columns: 1fr 1.5fr;
    gap: 30px;
    align-items: center;
}

.mapa-info {
    background: var(--cinza);
    border: 1px solid #164b34;
    padding: 30px;
    border-radius: 12px;
}

.mapa-info h3 {
    color: var(--verde);
    margin-bottom: 20px;
    font-size: 23px;
}

.mapa-info p {
    color: var(--texto);
    margin-bottom: 15px;
    line-height: 1.7;
}

.mapa-container iframe {
    width: 100%;
    height: 350px;
    border: 1px solid var(--verde);
    border-radius: 12px;
}

/* =========================
   RODAPÉ
========================= */

footer {
    background: #000;
    border-top: 1px solid var(--verde);
    padding: 30px 20px;
    text-align: center;
}

footer p {
    color: var(--verde);
    font-size: 14px;
}

/* =========================
   RESPONSIVIDADE
========================= */

@media(max-width: 750px) {

    header {
        padding: 15px;
    }

    nav {
        flex-direction: column;
        gap: 15px;
    }

    .menu {
        justify-content: center;
        gap: 13px;
    }

    .menu a {
        font-size: 13px;
    }

    .banner {
        margin-top: 120px;
        min-height: 350px;
    }

    .banner h1 {
        font-size: 32px;
    }

    .banner p {
        font-size: 16px;
    }

    h2 {
        font-size: 26px;
    }

    .mapa-container {
        grid-template-columns: 1fr;
    }

    .mapa-container iframe {
        height: 300px;
    }

}

</style>
</head>

<body>

<!-- =========================
     CABEÇALHO
========================= -->

<header>

<nav>

    <div class="logo">
        Portfolio.pf
    </div>

    <div class="menu">

        <a href="#inicio">Inicial</a>

        <a href="#video">Vídeo</a>

        <a href="#sobre">Sobre Nós</a>

        <a href="#grupo1">Produtos</a>

        <a href="#grupo2">Novidades</a>

        <a href="#grupo3">Promoções</a>

        <a href="#contactos">Contactos</a>

        <a href="#mapa">Onde Estamos</a>

    </div>

</nav>

</header>


<!-- =========================
     CAPA PRINCIPAL
========================= -->

<div class="banner" id="inicio">

    <h1>PORTFOLIO.PF</h1>

    <p>
        Inovação, qualidade e exclusividade.
    </p>

    <a href="#grupo1" class="botao-banner">
        EXPLORAR PRODUTOS
    </a>

</div>


<!-- =========================
     VÍDEO DE APRESENTAÇÃO
========================= -->

<section class="video-section" id="video">

    <h2>Conheça a Portfolio.pf</h2>

    <p>
        Descubra os nossos produtos e novidades
        através do nosso vídeo de apresentação.
    </p>

    <div class="video-container">

        <video
            controls
            muted
            playsinline
            preload="metadata">

            <source
                src="videos/apresentacao.mp4"
                type="video/mp4">

            O seu navegador não suporta vídeos.

        </video>

    </div>

</section>


<!-- =========================
     SOBRE NÓS
========================= -->

<section id="sobre">

    <h2>Sobre Nós</h2>

    <div class="sobre">

        <p>
            Bem-vindo à Portfolio.pf.

            Uma loja dedicada à inovação,
            qualidade e excelência.

            Descubra os nossos produtos,
            conheça as novidades e encontre
            as melhores soluções para si.
        </p>

    </div>

</section>


<!-- =========================
     GRUPO 1 - PRODUTOS
========================= -->

<section id="grupo1">

    <h2>Produtos em Destaque</h2>

    <div class="cards">

        <div class="card">

            <img src="img/produto1.jpg" alt="Produto 1">

            <h3>Produto 1</h3>

            <p>Descrição do primeiro produto.</p>

            <div class="preco">25,00 €</div>

            <a href="#" class="botao">Comprar</a>

        </div>


        <div class="card">

            <img src="img/produto2.jpg" alt="Produto 2">

            <h3>Produto 2</h3>

            <p>Descrição do segundo produto.</p>

            <div class="preco">35,00 €</div>

            <a href="#" class="botao">Comprar</a>

        </div>


        <div class="card">

            <img src="img/produto3.jpg" alt="Produto 3">

            <h3>Produto 3</h3>

            <p>Descrição do terceiro produto.</p>

            <div class="preco">45,00 €</div>

            <a href="#" class="botao">Comprar</a>

        </div>


        <div class="card">

            <img src="img/produto4.jpg" alt="Produto 4">

            <h3>Produto 4</h3>

            <p>Descrição do quarto produto.</p>

            <div class="preco">50,00 €</div>

            <a href="#" class="botao">Comprar</a>

        </div>

    </div>

</section>


<!-- =========================
     GRUPO 2 - NOVIDADES
========================= -->

<section id="grupo2">

    <h2>Novidades</h2>

    <div class="cards">

        <div class="card">

            <img src="img/novidade1.jpg" alt="Novidade 1">

            <h3>Novidade 1</h3>

            <p>Conheça este novo produto.</p>

            <div class="preco">29,00 €</div>

            <a href="#" class="botao">Comprar</a>

        </div>


        <div class="card">

            <img src="img/novidade2.jpg" alt="Novidade 2">

            <h3>Novidade 2</h3>

            <p>Conheça este novo produto.</p>

            <div class="preco">39,00 €</div>

            <a href="#" class="botao">Comprar</a>

        </div>


        <div class="card">

            <img src="img/novidade3.jpg" alt="Novidade 3">

            <h3>Novidade 3</h3>

            <p>Conheça este novo produto.</p>

            <div class="preco">49,00 €</div>

            <a href="#" class="botao">Comprar</a>

        </div>

    </div>

</section>


<!-- =========================
     GRUPO 3 - PROMOÇÕES
========================= -->

<section id="grupo3">

    <h2>Produtos em Promoção</h2>

    <div class="cards">

        <div class="card">

            <img src="img/promocao1.jpg" alt="Promoção 1">

            <h3>Promoção 1</h3>

            <p>Produto com preço especial.</p>

            <div class="preco">19,00 €</div>

            <a href="#" class="botao">Comprar</a>

        </div>


        <div class="card">

            <img src="img/promocao2.jpg" alt="Promoção 2">

            <h3>Promoção 2</h3>

            <p>Produto com preço especial.</p>

            <div class="preco">24,00 €</div>

            <a href="#" class="botao">Comprar</a>

        </div>

    </div>

</section>


<!-- =========================
     CONTACTOS
========================= -->

<section id="contactos">

    <h2>Contactos</h2>

    <div class="contactos">

        <p>
            <strong>Email:</strong>
            contacto@portfolio.pf
        </p>

        <p>
            <strong>Telefone:</strong>
            +351 000 000 000
        </p>

        <p>
            <strong>Horário:</strong>
            Segunda a Sexta
        </p>

    </div>

</section>


<!-- =========================
     MAPA
========================= -->

<section id="mapa">

    <h2>Onde Estamos</h2>

    <div class="mapa-container">

        <div class="mapa-info">

            <h3>Visite a Portfolio.pf</h3>

            <p>
                📍 Morada: Coloque aqui a morada da loja.
            </p>

            <p>
                📧 Email: contacto@portfolio.pf
            </p>

            <p>
                📞 Telefone: +351 000 000 000
            </p>

            <p>
                🕒 Horário: Segunda a Sexta.
            </p>

        </div>

        <iframe
            src="https://www.google.com/maps?q=Bilbao,Spain&output=embed"
            loading="lazy"
            allowfullscreen
            referrerpolicy="no-referrer-when-downgrade">
        </iframe>

    </div>

</section>


<!-- =========================
     RODAPÉ
========================= -->

<footer>

    <p>
        © 2026 Portfolio.pf |
        Todos os direitos reservados.
    </p>

</footer>

</body>
</html>
