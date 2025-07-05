# ecogrow-site<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>EcoGrow - Vasos Inteligentes e Sustentáveis</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      margin: 0;
      padding: 0;
      background: #f5f9f6;
      color: #333;
    }
    header {
      background-color: #2e7d32;
      color: white;
      padding: 20px;
      text-align: center;
    }
    nav {
      background: #388e3c;
      display: flex;
      justify-content: center;
      gap: 30px;
      padding: 10px;
    }
    nav a {
      color: white;
      text-decoration: none;
      font-weight: bold;
    }
    section {
      padding: 40px 20px;
      max-width: 1000px;
      margin: auto;
    }
    .hero {
      text-align: center;
      background: url('https://source.unsplash.com/featured/?plant,pot') center/cover no-repeat;
      color: white;
      padding: 100px 20px;
    }
    .hero h1 {
      font-size: 3em;
      margin: 0;
    }
    .hero p {
      font-size: 1.2em;
    }
    .btn {
      background-color: #66bb6a;
      color: white;
      border: none;
      padding: 15px 25px;
      font-size: 1em;
      margin: 10px;
      cursor: pointer;
      border-radius: 8px;
    }
    .features, .products, .about, .contact {
      background-color: white;
      border-radius: 10px;
      padding: 20px;
      margin-top: 20px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    }
    footer {
      background: #2e7d32;
      color: white;
      text-align: center;
      padding: 20px;
    }
  </style>
</head>
<body>

<header>
  <h1>EcoGrow</h1>
  <p>Vasos Inteligentes e 100% Biodegradáveis</p>
</header>

<nav>
  <a href="#funciona">Como Funciona</a>
  <a href="#produtos">Loja</a>
  <a href="#app">App</a>
  <a href="#assinatura">Assinatura</a>
  <a href="#contato">Contato</a>
</nav>

<section class="hero">
  <h1>Cultive o futuro com inteligência</h1>
  <p>Vasos sustentáveis que ajudam você a cuidar das suas plantas</p>
  <button class="btn">Conheça nossos produtos</button>
</section>

<section id="funciona" class="features">
  <h2>Como Funciona</h2>
  <ul>
    <li><strong>Biodegradável:</strong> se decompõe e nutre o solo</li>
    <li><strong>Inteligente:</strong> sensores de umidade, luz e temperatura</li>
    <li><strong>Conectado:</strong> receba alertas no seu celular</li>
    <li><strong>Sustentável:</strong> sem plástico, sem culpa</li>
  </ul>
</section>

<section id="produtos" class="products">
  <h2>Nossos Produtos</h2>
  <ul>
    <li>Vaso EcoGrow Pequeno - R$ 39,90</li>
    <li>Vaso EcoGrow Médio - R$ 59,90</li>
    <li>Kit 3 Vasos + Mudas - R$ 129,90</li>
  </ul>
  <button class="btn">Comprar agora</button>
</section>

<section id="app" class="features">
  <h2>App EcoGrow</h2>
  <p>Monitore sua planta com facilidade: receba dicas, alertas e acompanhe o desenvolvimento em tempo real.</p>
  <button class="btn">Baixe o App</button>
</section>

<section id="assinatura" class="about">
  <h2>Assinatura Premium</h2>
  <p>Conteúdo exclusivo, comunidade de jardinagem e suporte personalizado para você cuidar ainda melhor do seu verde.</p>
  <button class="btn">Assinar agora</button>
</section>

<section id="contato" class="contact">
  <h2>Fale Conosco</h2>
  <form action="https://formspree.io/f/seu_id_aqui" method="POST">
    <input type="text" name="_gotcha" style="display:none">
    <label>Nome:<br><input type="text" name="nome" required></label><br><br>
    <label>Email:<br><input type="email" name="email" required></label><br><br>
    <label>Mensagem:<br><textarea name="mensagem" required></textarea></label><br><br>
    <button class="btn" type="submit">Enviar</button>
  </form>
</section>

<footer>
  <p>EcoGrow © 2025 – Todos os direitos reservados.</p>
</footer>

<script>
  const form = document.querySelector("form");
  form.addEventListener("submit", async (e) => {
    e.preventDefault();
    const data = new FormData(form);
    const response = await fetch(form.action, {
      method: form.method,
      body: data,
      headers: { 'Accept': 'application/json' }
    });
    if (response.ok) {
      alert("Mensagem enviada com sucesso! ??");
      form.reset();
    } else {
      alert("Ocorreu um erro. Tente novamente mais tarde.");
    }
  });
</script>

</body>
</html>