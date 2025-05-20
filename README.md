<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Inbyte - Agence Community Management & Création de Contenu</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');
  * {
    box-sizing: border-box;
  }
  body {
    margin: 0; padding: 0;
    font-family: 'Montserrat', sans-serif;
    background: linear-gradient(135deg, #f0f4ff, #d9e4ff);
    color: #1a1a1a;
  }
  a {
    color: #0056b3;
    text-decoration: none;
  }
  a:hover {
    text-decoration: underline;
  }
  .container {
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 20px 80px;
  }
  header {
    position: sticky;
    top: 0;
    background: #fff;
    box-shadow: 0 2px 6px rgba(0,0,0,0.1);
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 15px 20px;
    z-index: 1000;
  }
  header h1 {
    font-weight: 700;
    font-size: 1.6rem;
    color: #003366;
    margin: 0;
  }
  .btn-devis {
    background: #4f46e5;
    color: white;
    padding: 10px 18px;
    border-radius: 30px;
    font-weight: 600;
    cursor: pointer;
    box-shadow: 0 4px 8px rgba(79,70,229,0.3);
    transition: background 0.3s ease;
  }
  .btn-devis:hover {
    background: #3b35b3;
  }
  .hero {
    text-align: center;
    padding: 90px 20px 60px;
    background: radial-gradient(circle at center, #cdd7ff 0%, #6f86ff 100%);
    color: white;
    border-radius: 0 0 60px 60px;
    box-shadow: 0 8px 30px rgba(111,134,255,0.4);
  }
  .hero h2 {
    font-size: 2.8rem;
    margin-bottom: 15px;
    font-weight: 700;
  }
  .hero p {
    font-size: 1.2rem;
    margin-bottom: 30px;
    max-width: 600px;
    margin-left: auto;
    margin-right: auto;
    line-height: 1.5;
  }
  .hero a {
    background: white;
    color: #4f46e5;
    font-weight: 700;
    padding: 14px 28px;
    border-radius: 50px;
    font-size: 1.1rem;
    box-shadow: 0 4px 15px rgba(79,70,229,0.3);
    transition: background 0.3s ease, color 0.3s ease;
  }
  .hero a:hover {
    background: #3b35b3;
    color: white;
  }
  section {
    padding: 60px 20px;
    opacity: 0;
    transform: translateY(40px);
    animation: fadeInUp 1s forwards;
    animation-delay: 0.3s;
  }
  section:nth-of-type(2) { animation-delay: 0.5s; }
  section:nth-of-type(3) { animation-delay: 0.7s; }
  section:nth-of-type(4) { animation-delay: 0.9s; }
  section:nth-of-type(5) { animation-delay: 1.1s; }
  h3 {
    font-size: 2rem;
    color: #003366;
    margin-bottom: 20px;
    font-weight: 700;
    text-align: center;
  }
  .text-block {
    max-width: 900px;
    margin: 0 auto 40px;
    font-size: 1.1rem;
    line-height: 1.6;
    text-align: center;
  }
  .cards {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 24px;
  }
  .card {
    background: white;
    border-radius: 20px;
    box-shadow: 0 10px 25px rgba(79,70,229,0.15);
    padding: 30px 25px;
    width: 280px;
    transition: transform 0.3s ease;
    cursor: default;
  }
  .card:hover {
    transform: translateY(-10px);
    box-shadow: 0 20px 40px rgba(79,70,229,0.3);
  }
  .card h4 {
    color: #4f46e5;
    font-weight: 700;
    margin-bottom: 15px;
    font-size: 1.3rem;
  }
  .card ul {
    list-style: none;
    padding-left: 0;
    font-size: 1rem;
    color: #333;
  }
  .card ul li {
    margin-bottom: 10px;
    position: relative;
    padding-left: 22px;
  }
  .card ul li::before {
    content: "✔";
    color: #4f46e5;
    position: absolute;
    left: 0;
    top: 0;
    font-weight: bold;
  }
  form {
    background: white;
    max-width: 700px;
    margin: 0 auto;
    padding: 40px 30px;
    border-radius: 25px;
    box-shadow: 0 15px 30px rgba(79,70,229,0.15);
  }
  form label {
    display: block;
    margin-bottom: 6px;
    font-weight: 600;
    color: #003366;
    font-size: 0.95rem;
  }
  form input[type="text"],
  form input[type="email"],
  form input[type="tel"],
  form select,
  form textarea {
    width: 100%;
    padding: 12px 15px;
    margin-bottom: 20px;
    border: 2px solid #ddd;
    border-radius: 12px;
    font-size: 1rem;
    transition: border-color 0.3s ease;
  }
  form input[type="text"]:focus,
  form input[type="email"]:focus,
  form input[type="tel"]:focus,
  form select:focus,
  form textarea:focus {
    outline: none;
    border-color: #4f46e5;
  }
  form textarea {
    resize: vertical;
    min-height: 90px;
  }
  form button {
    background: #4f46e5;
    color: white;
    font-weight: 700;
    font-size: 1.1rem;
    padding: 14px 0;
    border: none;
    border-radius: 50px;
    cursor: pointer;
    width: 100%;
    box-shadow: 0 6px 18px rgba(79,70,229,0.3);
    transition: background 0.3s ease;
  }
  form button:hover {
    background: #3b35b3;
  }
  @keyframes fadeInUp {
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
  .checkbox-group {
    display: flex;
    flex-wrap: wrap;
    gap: 15px;
  }
  .checkbox-group label {
    display: flex;
    align-items: center;
    font-weight: 500;
    cursor: pointer;
    font-size: 0.95rem;
  }
  .checkbox-group input[type="checkbox"] {
    margin-right: 8px;
    width: 18px;
    height: 18px;
    cursor: pointer;
  }
  @media (max-width: 900px) {
    .cards {
      flex-direction: column;
      align-items: center;
    }
    .card {
      width: 90%;
    }
  }
</style>
</head>
<body>

<header>
  <h1>Inbyte</h1>
  <a href="#form-devis" class="btn-devis">Demande de devis</a>
</header>

<section class="hero">
  <h2>Boostez votre présence en ligne avec <br /><strong>Inbyte</strong></h2>
  <p>Stratégie social media, création de contenu, gestion de communauté : on s’occupe de tout pour faire briller votre marque.</p>
  <a href="#form-devis">Réservez un appel gratuit</a>
</section>

<section>
  <h3>Community Management</h3>
  <div class="text-block">
    <p>Le community management, c’est l’art de construire et d’animer votre communauté sur les réseaux sociaux. Chez Inbyte, nous gérons vos interactions, développons votre audience et assurons une présence cohérente et engagée pour votre marque.</p>
  </div>
</section>

<section>
  <h3>Création de Contenu</h3>
  <div class="text-block">
    <p>Nous créons du contenu visuel et textuel impactant et adapté à votre audience. Photos, vidéos, articles ou posts attractifs, notre équipe donne vie à votre message pour capter l’attention et fidéliser votre audience.</p>
  </div>
</section>

<section>
  <h3>Pourquoi c’est utile pour votre entreprise ?</h3>
  <div class="text-block">
    <p>Être présent et actif sur les réseaux sociaux permet d’améliorer votre notoriété, attirer de nouveaux clients et renforcer la relation avec votre audience. Une stratégie bien exécutée transforme vos abonnés en ambassadeurs enthousiastes.</p>
  </div>
</section>

<section>
  <h3>Nos Offres</h3>
  <div class="cards">
    <div class="card">
      <h4>Offre Essentielle</h4>
      <ul>
        <li>Community Management</li>
      </ul>
    </div>
    <div class="card">
      <h4>Offre Intermédiaire</h4>
      <ul>
        <li>Community Management</li>
        <li>Création de Contenu</li>
      </ul>
    </div>
    <div class="card">
      <h4>Offre Avancée</h4>
      <ul>
        <li>Community Management</li>
        <li>Création de Contenu</li>
        <li>Rapport d'analyse réseaux sociaux</li>
      </ul>
    </div>
  </div>
</section>

<section id="form-devis">
  <h3>Demande de devis</h3>
  <form action="https://formspree.io/f/xovdbkel" method="POST">
    <input type="hidden" name="_captcha" value="false" />
    
    <label for="entreprise">1. Nom de votre entreprise :</label>
    <input type="text" id="entreprise" name="entreprise" required />
    
    <label for="contact">2. Votre nom et prénom :</label>
    <input type="text" id="contact" name="contact" required />
    
    <label for="email">3. Adresse email :</label>
    <input type="email" id="email" name="email" required />
    
    <label for="telephone">4. Numéro de téléphone :</label>
    <input type="tel" id="telephone" name="telephone" />
    
    <label for="besoin">5. Quel service vous intéresse ?</label>
    <select id="besoin" name="besoin" required>
      <option value="" disabled selected>Choisissez une option</option>
      <option value="Offre Essentielle">Offre Essentielle (Community Management)</option>
      <option value="Offre Intermédiaire">Offre Intermédiaire (CM + Création de contenu)</option>
      <option value="Offre Avancée">Offre Avancée (CM + CC + Rapport d'analyse)</option>
    </select>
    
    <label for="details">6. Dites-nous en plus sur votre projet :</label>
    <textarea id="details" name="details" placeholder="Décrivez vos besoins, attentes ou questions..." ></textarea>
    
    <button type="submit">Envoyer ma demande</button>
  </form>
</section>

</body>
</html>
