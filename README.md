
<!doctype html>
<html lang="nl">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Bestellen - EduSwitch</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&family=Sora:wght@600;700;800&display=swap" rel="stylesheet">
  <style>
    body {margin:0;font-family:'Inter',sans-serif;background:#f8fcff;color:#081125}
    header {position:sticky;top:0;background:linear-gradient(90deg,#0011aa,#00c2b3);color:#fff;padding:12px 24px;display:flex;justify-content:space-between;align-items:center}
    header a {color:#fff;margin-left:16px;text-decoration:none;font-weight:600}
    header .brand {font-family:'Sora',sans-serif;font-weight:800;font-size:22px}
    .content {max-width:900px;margin:40px auto;padding:0 20px}
    .btn {display:inline-block;background:linear-gradient(135deg,#0011aa,#00c2b3);color:#fff;padding:10px 16px;border-radius:8px;text-decoration:none;font-weight:700}
    .trust-badges {display:flex;gap:12px;margin-top:16px;flex-wrap:wrap}
    .trust-badge {background:#fff;padding:6px 12px;border-radius:8px;font-size:0.85rem;box-shadow:0 4px 12px rgba(0,0,0,0.08)}
    footer {text-align:center;padding:20px;background:#f1f5f9;margin-top:40px}
    /* Modal styling */
    .modal-overlay {display:none;position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.5);justify-content:center;align-items:center;z-index:1000}
    .modal {background:#fff;padding:20px;border-radius:12px;max-width:400px;width:90%;text-align:center;transform:scale(0.8);opacity:0;transition:all 0.3s ease-in-out}
    .modal.show {transform:scale(1);opacity:1}
    .close-btn {position:absolute;top:15px;right:15px;background:linear-gradient(135deg,#0011aa,#00c2b3);border:none;color:#fff;font-size:18px;border-radius:50%;width:28px;height:28px;cursor:pointer}
  </style>
</head>
<body>
<header>
  <a href="index.html" class="brand">EduSwitch</a>
  <nav>
    <a href="boek.html">Boek</a>
    <a href="ebook.html">E-book</a>
    <a href="diensten.html">Diensten</a>
    <a href="hulpvraag.html">Hulpvraag</a>
    <a href="over.html">Over</a>
    <a href="contact.html">Contact</a>
    <a href="bestellen.html">Bestellen</a>
  </nav>
</header>

<div class="content">
<h1>Bestel</h1><p>Bestelformulier komt hier.</p>
</div>

<div class="content">
  <h3>Wat anderen zeggen</h3>
  <div class="review-slider">
    <p>“Het boek heeft ons team enorm geholpen bij een vliegende start.” — Jan de Vries, directeur</p>
    <p>“Praktische tips die meteen toepasbaar zijn.” — Petra Jansen, docent</p>
    <p>“Geeft echt structuur aan het schooljaar.” — Ahmed El Amrani, directeur</p>
    <p>“Duidelijke handvatten voor het hele team.” — Lisa van Dijk, docent</p>
  </div>
</div>

<footer>
  <p>&copy; 2025 EduSwitch. Alle rechten voorbehouden.</p>
</footer>

<div class="modal-overlay" id="modal">
  <div class="modal" id="modal-box">
    <button class="close-btn" id="close-modal">&times;</button>
    <p id="modal-message"></p>
  </div>
</div>

<script>
  const modalOverlay = document.getElementById('modal');
  const modalBox = document.getElementById('modal-box');
  const modalMessage = document.getElementById('modal-message');
  const closeModal = document.getElementById('close-modal');
  closeModal.addEventListener('click', ()=> modalOverlay.style.display='none');
  modalOverlay.addEventListener('click', e => { if(e.target===modalOverlay) modalOverlay.style.display='none'; });

  document.querySelectorAll('form').forEach(form => {
    form.addEventListener('submit', function(e) {
      e.preventDefault();
      const formType = this.getAttribute('data-form-type');
      let message = "Bedankt voor uw bericht.";
      if(formType==="hulpvraag") message = "Bedankt voor het insturen van uw hulpvraag. We gaan ermee aan de slag.";
      if(formType==="bestelling") message = "Bedankt voor uw bestelling. U ontvangt spoedig een bevestiging in uw e-mail.";
      modalMessage.textContent = message;
      modalOverlay.style.display = 'flex';
      setTimeout(()=> modalBox.classList.add('show'), 10);
    });
  });
</script>

</body>
</html>

<!doctype html>
<html lang="nl">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Boek - EduSwitch</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&family=Sora:wght@600;700;800&display=swap" rel="stylesheet">
  <style>
    body {margin:0;font-family:'Inter',sans-serif;background:#f8fcff;color:#081125}
    header {position:sticky;top:0;background:linear-gradient(90deg,#0011aa,#00c2b3);color:#fff;padding:12px 24px;display:flex;justify-content:space-between;align-items:center}
    header a {color:#fff;margin-left:16px;text-decoration:none;font-weight:600}
    header .brand {font-family:'Sora',sans-serif;font-weight:800;font-size:22px}
    .content {max-width:900px;margin:40px auto;padding:0 20px}
    .btn {display:inline-block;background:linear-gradient(135deg,#0011aa,#00c2b3);color:#fff;padding:10px 16px;border-radius:8px;text-decoration:none;font-weight:700}
    .trust-badges {display:flex;gap:12px;margin-top:16px;flex-wrap:wrap}
    .trust-badge {background:#fff;padding:6px 12px;border-radius:8px;font-size:0.85rem;box-shadow:0 4px 12px rgba(0,0,0,0.08)}
    footer {text-align:center;padding:20px;background:#f1f5f9;margin-top:40px}
    /* Modal styling */
    .modal-overlay {display:none;position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.5);justify-content:center;align-items:center;z-index:1000}
    .modal {background:#fff;padding:20px;border-radius:12px;max-width:400px;width:90%;text-align:center;transform:scale(0.8);opacity:0;transition:all 0.3s ease-in-out}
    .modal.show {transform:scale(1);opacity:1}
    .close-btn {position:absolute;top:15px;right:15px;background:linear-gradient(135deg,#0011aa,#00c2b3);border:none;color:#fff;font-size:18px;border-radius:50%;width:28px;height:28px;cursor:pointer}
  </style>
</head>
<body>
<header>
  <a href="index.html" class="brand">EduSwitch</a>
  <nav>
    <a href="boek.html">Boek</a>
    <a href="ebook.html">E-book</a>
    <a href="diensten.html">Diensten</a>
    <a href="hulpvraag.html">Hulpvraag</a>
    <a href="over.html">Over</a>
    <a href="contact.html">Contact</a>
    <a href="bestellen.html">Bestellen</a>
  </nav>
</header>

<div class="content">
<h1>Goed begin, sterk jaar</h1><p>Ons fysieke boek vol praktische tips voor het onderwijs.</p><div class='trust-badges'><div class='trust-badge'>AVG-proof</div><div class='trust-badge'>4,8/5 tevredenheid</div><div class='trust-badge'>Veilige betaling</div></div>
</div>

<div class="content">
  <h3>Wat anderen zeggen</h3>
  <div class="review-slider">
    <p>“Het boek heeft ons team enorm geholpen bij een vliegende start.” — Jan de Vries, directeur</p>
    <p>“Praktische tips die meteen toepasbaar zijn.” — Petra Jansen, docent</p>
    <p>“Geeft echt structuur aan het schooljaar.” — Ahmed El Amrani, directeur</p>
    <p>“Duidelijke handvatten voor het hele team.” — Lisa van Dijk, docent</p>
  </div>
</div>

<footer>
  <p>&copy; 2025 EduSwitch. Alle rechten voorbehouden.</p>
</footer>

<div class="modal-overlay" id="modal">
  <div class="modal" id="modal-box">
    <button class="close-btn" id="close-modal">&times;</button>
    <p id="modal-message"></p>
  </div>
</div>

<script>
  const modalOverlay = document.getElementById('modal');
  const modalBox = document.getElementById('modal-box');
  const modalMessage = document.getElementById('modal-message');
  const closeModal = document.getElementById('close-modal');
  closeModal.addEventListener('click', ()=> modalOverlay.style.display='none');
  modalOverlay.addEventListener('click', e => { if(e.target===modalOverlay) modalOverlay.style.display='none'; });

  document.querySelectorAll('form').forEach(form => {
    form.addEventListener('submit', function(e) {
      e.preventDefault();
      const formType = this.getAttribute('data-form-type');
      let message = "Bedankt voor uw bericht.";
      if(formType==="hulpvraag") message = "Bedankt voor het insturen van uw hulpvraag. We gaan ermee aan de slag.";
      if(formType==="bestelling") message = "Bedankt voor uw bestelling. U ontvangt spoedig een bevestiging in uw e-mail.";
      modalMessage.textContent = message;
      modalOverlay.style.display = 'flex';
      setTimeout(()=> modalBox.classList.add('show'), 10);
    });
  });
</script>

</body>
</html>

<!doctype html>
<html lang="nl">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Contact - EduSwitch</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&family=Sora:wght@600;700;800&display=swap" rel="stylesheet">
  <style>
    body {margin:0;font-family:'Inter',sans-serif;background:#f8fcff;color:#081125}
    header {position:sticky;top:0;background:linear-gradient(90deg,#0011aa,#00c2b3);color:#fff;padding:12px 24px;display:flex;justify-content:space-between;align-items:center}
    header a {color:#fff;margin-left:16px;text-decoration:none;font-weight:600}
    header .brand {font-family:'Sora',sans-serif;font-weight:800;font-size:22px}
    .content {max-width:900px;margin:40px auto;padding:0 20px}
    .btn {display:inline-block;background:linear-gradient(135deg,#0011aa,#00c2b3);color:#fff;padding:10px 16px;border-radius:8px;text-decoration:none;font-weight:700}
    .trust-badges {display:flex;gap:12px;margin-top:16px;flex-wrap:wrap}
    .trust-badge {background:#fff;padding:6px 12px;border-radius:8px;font-size:0.85rem;box-shadow:0 4px 12px rgba(0,0,0,0.08)}
    footer {text-align:center;padding:20px;background:#f1f5f9;margin-top:40px}
    /* Modal styling */
    .modal-overlay {display:none;position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.5);justify-content:center;align-items:center;z-index:1000}
    .modal {background:#fff;padding:20px;border-radius:12px;max-width:400px;width:90%;text-align:center;transform:scale(0.8);opacity:0;transition:all 0.3s ease-in-out}
    .modal.show {transform:scale(1);opacity:1}
    .close-btn {position:absolute;top:15px;right:15px;background:linear-gradient(135deg,#0011aa,#00c2b3);border:none;color:#fff;font-size:18px;border-radius:50%;width:28px;height:28px;cursor:pointer}
  </style>
</head>
<body>
<header>
  <a href="index.html" class="brand">EduSwitch</a>
  <nav>
    <a href="boek.html">Boek</a>
    <a href="ebook.html">E-book</a>
    <a href="diensten.html">Diensten</a>
    <a href="hulpvraag.html">Hulpvraag</a>
    <a href="over.html">Over</a>
    <a href="contact.html">Contact</a>
    <a href="bestellen.html">Bestellen</a>
  </nav>
</header>

<div class="content">
<h1>Contact</h1><form action='https://formspree.io/f/xrbljyzg' method='POST' data-form-type='contact'><input type='text' name='name' placeholder='Naam' required><input type='email' name='email' placeholder='E-mail' required><textarea name='message' placeholder='Uw bericht' required></textarea><button type='submit' class='btn'>Verstuur</button></form>
</div>

<div class="content">
  <h3>Wat anderen zeggen</h3>
  <div class="review-slider">
    <p>“Het boek heeft ons team enorm geholpen bij een vliegende start.” — Jan de Vries, directeur</p>
    <p>“Praktische tips die meteen toepasbaar zijn.” — Petra Jansen, docent</p>
    <p>“Geeft echt structuur aan het schooljaar.” — Ahmed El Amrani, directeur</p>
    <p>“Duidelijke handvatten voor het hele team.” — Lisa van Dijk, docent</p>
  </div>
</div>

<footer>
  <p>&copy; 2025 EduSwitch. Alle rechten voorbehouden.</p>
</footer>

<div class="modal-overlay" id="modal">
  <div class="modal" id="modal-box">
    <button class="close-btn" id="close-modal">&times;</button>
    <p id="modal-message"></p>
  </div>
</div>

<script>
  const modalOverlay = document.getElementById('modal');
  const modalBox = document.getElementById('modal-box');
  const modalMessage = document.getElementById('modal-message');
  const closeModal = document.getElementById('close-modal');
  closeModal.addEventListener('click', ()=> modalOverlay.style.display='none');
  modalOverlay.addEventListener('click', e => { if(e.target===modalOverlay) modalOverlay.style.display='none'; });

  document.querySelectorAll('form').forEach(form => {
    form.addEventListener('submit', function(e) {
      e.preventDefault();
      const formType = this.getAttribute('data-form-type');
      let message = "Bedankt voor uw bericht.";
      if(formType==="hulpvraag") message = "Bedankt voor het insturen van uw hulpvraag. We gaan ermee aan de slag.";
      if(formType==="bestelling") message = "Bedankt voor uw bestelling. U ontvangt spoedig een bevestiging in uw e-mail.";
      modalMessage.textContent = message;
      modalOverlay.style.display = 'flex';
      setTimeout(()=> modalBox.classList.add('show'), 10);
    });
  });
</script>

</body>
</html>

<!doctype html>
<html lang="nl">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Diensten - EduSwitch</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&family=Sora:wght@600;700;800&display=swap" rel="stylesheet">
  <style>
    body {margin:0;font-family:'Inter',sans-serif;background:#f8fcff;color:#081125}
    header {position:sticky;top:0;background:linear-gradient(90deg,#0011aa,#00c2b3);color:#fff;padding:12px 24px;display:flex;justify-content:space-between;align-items:center}
    header a {color:#fff;margin-left:16px;text-decoration:none;font-weight:600}
    header .brand {font-family:'Sora',sans-serif;font-weight:800;font-size:22px}
    .content {max-width:900px;margin:40px auto;padding:0 20px}
    .btn {display:inline-block;background:linear-gradient(135deg,#0011aa,#00c2b3);color:#fff;padding:10px 16px;border-radius:8px;text-decoration:none;font-weight:700}
    .trust-badges {display:flex;gap:12px;margin-top:16px;flex-wrap:wrap}
    .trust-badge {background:#fff;padding:6px 12px;border-radius:8px;font-size:0.85rem;box-shadow:0 4px 12px rgba(0,0,0,0.08)}
    footer {text-align:center;padding:20px;background:#f1f5f9;margin-top:40px}
    /* Modal styling */
    .modal-overlay {display:none;position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.5);justify-content:center;align-items:center;z-index:1000}
    .modal {background:#fff;padding:20px;border-radius:12px;max-width:400px;width:90%;text-align:center;transform:scale(0.8);opacity:0;transition:all 0.3s ease-in-out}
    .modal.show {transform:scale(1);opacity:1}
    .close-btn {position:absolute;top:15px;right:15px;background:linear-gradient(135deg,#0011aa,#00c2b3);border:none;color:#fff;font-size:18px;border-radius:50%;width:28px;height:28px;cursor:pointer}
  </style>
</head>
<body>
<header>
  <a href="index.html" class="brand">EduSwitch</a>
  <nav>
    <a href="boek.html">Boek</a>
    <a href="ebook.html">E-book</a>
    <a href="diensten.html">Diensten</a>
    <a href="hulpvraag.html">Hulpvraag</a>
    <a href="over.html">Over</a>
    <a href="contact.html">Contact</a>
    <a href="bestellen.html">Bestellen</a>
  </nav>
</header>

<div class="content">
<h1>Onze Diensten</h1><p>Signaleren en aanpakken van inhoudelijke en organisatorische hiaten. Ontwikkelen en verkopen van praktische handboeken en hulpmiddelen. Ondersteuning en advies op maat voor scholen en organisaties.</p>
</div>

<div class="content">
  <h3>Wat anderen zeggen</h3>
  <div class="review-slider">
    <p>“Het boek heeft ons team enorm geholpen bij een vliegende start.” — Jan de Vries, directeur</p>
    <p>“Praktische tips die meteen toepasbaar zijn.” — Petra Jansen, docent</p>
    <p>“Geeft echt structuur aan het schooljaar.” — Ahmed El Amrani, directeur</p>
    <p>“Duidelijke handvatten voor het hele team.” — Lisa van Dijk, docent</p>
  </div>
</div>

<footer>
  <p>&copy; 2025 EduSwitch. Alle rechten voorbehouden.</p>
</footer>

<div class="modal-overlay" id="modal">
  <div class="modal" id="modal-box">
    <button class="close-btn" id="close-modal">&times;</button>
    <p id="modal-message"></p>
  </div>
</div>

<script>
  const modalOverlay = document.getElementById('modal');
  const modalBox = document.getElementById('modal-box');
  const modalMessage = document.getElementById('modal-message');
  const closeModal = document.getElementById('close-modal');
  closeModal.addEventListener('click', ()=> modalOverlay.style.display='none');
  modalOverlay.addEventListener('click', e => { if(e.target===modalOverlay) modalOverlay.style.display='none'; });

  document.querySelectorAll('form').forEach(form => {
    form.addEventListener('submit', function(e) {
      e.preventDefault();
      const formType = this.getAttribute('data-form-type');
      let message = "Bedankt voor uw bericht.";
      if(formType==="hulpvraag") message = "Bedankt voor het insturen van uw hulpvraag. We gaan ermee aan de slag.";
      if(formType==="bestelling") message = "Bedankt voor uw bestelling. U ontvangt spoedig een bevestiging in uw e-mail.";
      modalMessage.textContent = message;
      modalOverlay.style.display = 'flex';
      setTimeout(()=> modalBox.classList.add('show'), 10);
    });
  });
</script>

</body>
</html>

<!doctype html>
<html lang="nl">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>E-book - EduSwitch</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&family=Sora:wght@600;700;800&display=swap" rel="stylesheet">
  <style>
    body {margin:0;font-family:'Inter',sans-serif;background:#f8fcff;color:#081125}
    header {position:sticky;top:0;background:linear-gradient(90deg,#0011aa,#00c2b3);color:#fff;padding:12px 24px;display:flex;justify-content:space-between;align-items:center}
    header a {color:#fff;margin-left:16px;text-decoration:none;font-weight:600}
    header .brand {font-family:'Sora',sans-serif;font-weight:800;font-size:22px}
    .content {max-width:900px;margin:40px auto;padding:0 20px}
    .btn {display:inline-block;background:linear-gradient(135deg,#0011aa,#00c2b3);color:#fff;padding:10px 16px;border-radius:8px;text-decoration:none;font-weight:700}
    .trust-badges {display:flex;gap:12px;margin-top:16px;flex-wrap:wrap}
    .trust-badge {background:#fff;padding:6px 12px;border-radius:8px;font-size:0.85rem;box-shadow:0 4px 12px rgba(0,0,0,0.08)}
    footer {text-align:center;padding:20px;background:#f1f5f9;margin-top:40px}
    /* Modal styling */
    .modal-overlay {display:none;position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.5);justify-content:center;align-items:center;z-index:1000}
    .modal {background:#fff;padding:20px;border-radius:12px;max-width:400px;width:90%;text-align:center;transform:scale(0.8);opacity:0;transition:all 0.3s ease-in-out}
    .modal.show {transform:scale(1);opacity:1}
    .close-btn {position:absolute;top:15px;right:15px;background:linear-gradient(135deg,#0011aa,#00c2b3);border:none;color:#fff;font-size:18px;border-radius:50%;width:28px;height:28px;cursor:pointer}
  </style>
</head>
<body>
<header>
  <a href="index.html" class="brand">EduSwitch</a>
  <nav>
    <a href="boek.html">Boek</a>
    <a href="ebook.html">E-book</a>
    <a href="diensten.html">Diensten</a>
    <a href="hulpvraag.html">Hulpvraag</a>
    <a href="over.html">Over</a>
    <a href="contact.html">Contact</a>
    <a href="bestellen.html">Bestellen</a>
  </nav>
</header>

<div class="content">
<h1>E-book — Goed begin, sterk jaar</h1><p>Digitale versie, beveiligd tegen kopiëren en delen, direct beschikbaar na aankoop.</p><div class='trust-badges'><div class='trust-badge'>AVG-proof</div><div class='trust-badge'>4,8/5 tevredenheid</div><div class='trust-badge'>Veilige betaling</div></div>
</div>

<div class="content">
  <h3>Wat anderen zeggen</h3>
  <div class="review-slider">
    <p>“Het boek heeft ons team enorm geholpen bij een vliegende start.” — Jan de Vries, directeur</p>
    <p>“Praktische tips die meteen toepasbaar zijn.” — Petra Jansen, docent</p>
    <p>“Geeft echt structuur aan het schooljaar.” — Ahmed El Amrani, directeur</p>
    <p>“Duidelijke handvatten voor het hele team.” — Lisa van Dijk, docent</p>
  </div>
</div>

<footer>
  <p>&copy; 2025 EduSwitch. Alle rechten voorbehouden.</p>
</footer>

<div class="modal-overlay" id="modal">
  <div class="modal" id="modal-box">
    <button class="close-btn" id="close-modal">&times;</button>
    <p id="modal-message"></p>
  </div>
</div>

<script>
  const modalOverlay = document.getElementById('modal');
  const modalBox = document.getElementById('modal-box');
  const modalMessage = document.getElementById('modal-message');
  const closeModal = document.getElementById('close-modal');
  closeModal.addEventListener('click', ()=> modalOverlay.style.display='none');
  modalOverlay.addEventListener('click', e => { if(e.target===modalOverlay) modalOverlay.style.display='none'; });

  document.querySelectorAll('form').forEach(form => {
    form.addEventListener('submit', function(e) {
      e.preventDefault();
      const formType = this.getAttribute('data-form-type');
      let message = "Bedankt voor uw bericht.";
      if(formType==="hulpvraag") message = "Bedankt voor het insturen van uw hulpvraag. We gaan ermee aan de slag.";
      if(formType==="bestelling") message = "Bedankt voor uw bestelling. U ontvangt spoedig een bevestiging in uw e-mail.";
      modalMessage.textContent = message;
      modalOverlay.style.display = 'flex';
      setTimeout(()=> modalBox.classList.add('show'), 10);
    });
  });
</script>

</body>
</html>

<!doctype html>
<html lang="nl">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Hulpvraag - EduSwitch</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&family=Sora:wght@600;700;800&display=swap" rel="stylesheet">
  <style>
    body {margin:0;font-family:'Inter',sans-serif;background:#f8fcff;color:#081125}
    header {position:sticky;top:0;background:linear-gradient(90deg,#0011aa,#00c2b3);color:#fff;padding:12px 24px;display:flex;justify-content:space-between;align-items:center}
    header a {color:#fff;margin-left:16px;text-decoration:none;font-weight:600}
    header .brand {font-family:'Sora',sans-serif;font-weight:800;font-size:22px}
    .content {max-width:900px;margin:40px auto;padding:0 20px}
    .btn {display:inline-block;background:linear-gradient(135deg,#0011aa,#00c2b3);color:#fff;padding:10px 16px;border-radius:8px;text-decoration:none;font-weight:700}
    .trust-badges {display:flex;gap:12px;margin-top:16px;flex-wrap:wrap}
    .trust-badge {background:#fff;padding:6px 12px;border-radius:8px;font-size:0.85rem;box-shadow:0 4px 12px rgba(0,0,0,0.08)}
    footer {text-align:center;padding:20px;background:#f1f5f9;margin-top:40px}
    /* Modal styling */
    .modal-overlay {display:none;position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.5);justify-content:center;align-items:center;z-index:1000}
    .modal {background:#fff;padding:20px;border-radius:12px;max-width:400px;width:90%;text-align:center;transform:scale(0.8);opacity:0;transition:all 0.3s ease-in-out}
    .modal.show {transform:scale(1);opacity:1}
    .close-btn {position:absolute;top:15px;right:15px;background:linear-gradient(135deg,#0011aa,#00c2b3);border:none;color:#fff;font-size:18px;border-radius:50%;width:28px;height:28px;cursor:pointer}
  </style>
</head>
<body>
<header>
  <a href="index.html" class="brand">EduSwitch</a>
  <nav>
    <a href="boek.html">Boek</a>
    <a href="ebook.html">E-book</a>
    <a href="diensten.html">Diensten</a>
    <a href="hulpvraag.html">Hulpvraag</a>
    <a href="over.html">Over</a>
    <a href="contact.html">Contact</a>
    <a href="bestellen.html">Bestellen</a>
  </nav>
</header>

<div class="content">
<h1>Dien uw hulpvraag in</h1><form action='https://formspree.io/f/xrbljyzg' method='POST' data-form-type='hulpvraag'><input type='text' name='name' placeholder='Naam' required><input type='email' name='email' placeholder='E-mail' required><textarea name='message' placeholder='Uw hulpvraag' required></textarea><button type='submit' class='btn'>Verzend hulpvraag</button></form>
</div>

<div class="content">
  <h3>Wat anderen zeggen</h3>
  <div class="review-slider">
    <p>“Het boek heeft ons team enorm geholpen bij een vliegende start.” — Jan de Vries, directeur</p>
    <p>“Praktische tips die meteen toepasbaar zijn.” — Petra Jansen, docent</p>
    <p>“Geeft echt structuur aan het schooljaar.” — Ahmed El Amrani, directeur</p>
    <p>“Duidelijke handvatten voor het hele team.” — Lisa van Dijk, docent</p>
  </div>
</div>

<footer>
  <p>&copy; 2025 EduSwitch. Alle rechten voorbehouden.</p>
</footer>

<div class="modal-overlay" id="modal">
  <div class="modal" id="modal-box">
    <button class="close-btn" id="close-modal">&times;</button>
    <p id="modal-message"></p>
  </div>
</div>

<script>
  const modalOverlay = document.getElementById('modal');
  const modalBox = document.getElementById('modal-box');
  const modalMessage = document.getElementById('modal-message');
  const closeModal = document.getElementById('close-modal');
  closeModal.addEventListener('click', ()=> modalOverlay.style.display='none');
  modalOverlay.addEventListener('click', e => { if(e.target===modalOverlay) modalOverlay.style.display='none'; });

  document.querySelectorAll('form').forEach(form => {
    form.addEventListener('submit', function(e) {
      e.preventDefault();
      const formType = this.getAttribute('data-form-type');
      let message = "Bedankt voor uw bericht.";
      if(formType==="hulpvraag") message = "Bedankt voor het insturen van uw hulpvraag. We gaan ermee aan de slag.";
      if(formType==="bestelling") message = "Bedankt voor uw bestelling. U ontvangt spoedig een bevestiging in uw e-mail.";
      modalMessage.textContent = message;
      modalOverlay.style.display = 'flex';
      setTimeout(()=> modalBox.classList.add('show'), 10);
    });
  });
</script>

</body>
</html>

<!doctype html>
<html lang="nl">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Home - EduSwitch</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&family=Sora:wght@600;700;800&display=swap" rel="stylesheet">
  <style>
    body {margin:0;font-family:'Inter',sans-serif;background:#f8fcff;color:#081125}
    header {position:sticky;top:0;background:linear-gradient(90deg,#0011aa,#00c2b3);color:#fff;padding:12px 24px;display:flex;justify-content:space-between;align-items:center}
    header a {color:#fff;margin-left:16px;text-decoration:none;font-weight:600}
    header .brand {font-family:'Sora',sans-serif;font-weight:800;font-size:22px}
    .content {max-width:900px;margin:40px auto;padding:0 20px}
    .btn {display:inline-block;background:linear-gradient(135deg,#0011aa,#00c2b3);color:#fff;padding:10px 16px;border-radius:8px;text-decoration:none;font-weight:700}
    .trust-badges {display:flex;gap:12px;margin-top:16px;flex-wrap:wrap}
    .trust-badge {background:#fff;padding:6px 12px;border-radius:8px;font-size:0.85rem;box-shadow:0 4px 12px rgba(0,0,0,0.08)}
    footer {text-align:center;padding:20px;background:#f1f5f9;margin-top:40px}
    /* Modal styling */
    .modal-overlay {display:none;position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.5);justify-content:center;align-items:center;z-index:1000}
    .modal {background:#fff;padding:20px;border-radius:12px;max-width:400px;width:90%;text-align:center;transform:scale(0.8);opacity:0;transition:all 0.3s ease-in-out}
    .modal.show {transform:scale(1);opacity:1}
    .close-btn {position:absolute;top:15px;right:15px;background:linear-gradient(135deg,#0011aa,#00c2b3);border:none;color:#fff;font-size:18px;border-radius:50%;width:28px;height:28px;cursor:pointer}
  </style>
</head>
<body>
<header>
  <a href="index.html" class="brand">EduSwitch</a>
  <nav>
    <a href="boek.html">Boek</a>
    <a href="ebook.html">E-book</a>
    <a href="diensten.html">Diensten</a>
    <a href="hulpvraag.html">Hulpvraag</a>
    <a href="over.html">Over</a>
    <a href="contact.html">Contact</a>
    <a href="bestellen.html">Bestellen</a>
  </nav>
</header>

<div class="content">
<h1>Welkom bij EduSwitch</h1><p>EduSwitch helpt scholen en organisaties vooruit met praktische handvatten, boeken en advies op maat.</p>
</div>

<div class="content">
  <h3>Wat anderen zeggen</h3>
  <div class="review-slider">
    <p>“Het boek heeft ons team enorm geholpen bij een vliegende start.” — Jan de Vries, directeur</p>
    <p>“Praktische tips die meteen toepasbaar zijn.” — Petra Jansen, docent</p>
    <p>“Geeft echt structuur aan het schooljaar.” — Ahmed El Amrani, directeur</p>
    <p>“Duidelijke handvatten voor het hele team.” — Lisa van Dijk, docent</p>
  </div>
</div>

<footer>
  <p>&copy; 2025 EduSwitch. Alle rechten voorbehouden.</p>
</footer>

<div class="modal-overlay" id="modal">
  <div class="modal" id="modal-box">
    <button class="close-btn" id="close-modal">&times;</button>
    <p id="modal-message"></p>
  </div>
</div>

<script>
  const modalOverlay = document.getElementById('modal');
  const modalBox = document.getElementById('modal-box');
  const modalMessage = document.getElementById('modal-message');
  const closeModal = document.getElementById('close-modal');
  closeModal.addEventListener('click', ()=> modalOverlay.style.display='none');
  modalOverlay.addEventListener('click', e => { if(e.target===modalOverlay) modalOverlay.style.display='none'; });

  document.querySelectorAll('form').forEach(form => {
    form.addEventListener('submit', function(e) {
      e.preventDefault();
      const formType = this.getAttribute('data-form-type');
      let message = "Bedankt voor uw bericht.";
      if(formType==="hulpvraag") message = "Bedankt voor het insturen van uw hulpvraag. We gaan ermee aan de slag.";
      if(formType==="bestelling") message = "Bedankt voor uw bestelling. U ontvangt spoedig een bevestiging in uw e-mail.";
      modalMessage.textContent = message;
      modalOverlay.style.display = 'flex';
      setTimeout(()=> modalBox.classList.add('show'), 10);
    });
  });
</script>

</body>
</html>

<!doctype html>
<html lang="nl">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Over ons - EduSwitch</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&family=Sora:wght@600;700;800&display=swap" rel="stylesheet">
  <style>
    body {margin:0;font-family:'Inter',sans-serif;background:#f8fcff;color:#081125}
    header {position:sticky;top:0;background:linear-gradient(90deg,#0011aa,#00c2b3);color:#fff;padding:12px 24px;display:flex;justify-content:space-between;align-items:center}
    header a {color:#fff;margin-left:16px;text-decoration:none;font-weight:600}
    header .brand {font-family:'Sora',sans-serif;font-weight:800;font-size:22px}
    .content {max-width:900px;margin:40px auto;padding:0 20px}
    .btn {display:inline-block;background:linear-gradient(135deg,#0011aa,#00c2b3);color:#fff;padding:10px 16px;border-radius:8px;text-decoration:none;font-weight:700}
    .trust-badges {display:flex;gap:12px;margin-top:16px;flex-wrap:wrap}
    .trust-badge {background:#fff;padding:6px 12px;border-radius:8px;font-size:0.85rem;box-shadow:0 4px 12px rgba(0,0,0,0.08)}
    footer {text-align:center;padding:20px;background:#f1f5f9;margin-top:40px}
    /* Modal styling */
    .modal-overlay {display:none;position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.5);justify-content:center;align-items:center;z-index:1000}
    .modal {background:#fff;padding:20px;border-radius:12px;max-width:400px;width:90%;text-align:center;transform:scale(0.8);opacity:0;transition:all 0.3s ease-in-out}
    .modal.show {transform:scale(1);opacity:1}
    .close-btn {position:absolute;top:15px;right:15px;background:linear-gradient(135deg,#0011aa,#00c2b3);border:none;color:#fff;font-size:18px;border-radius:50%;width:28px;height:28px;cursor:pointer}
  </style>
</head>
<body>
<header>
  <a href="index.html" class="brand">EduSwitch</a>
  <nav>
    <a href="boek.html">Boek</a>
    <a href="ebook.html">E-book</a>
    <a href="diensten.html">Diensten</a>
    <a href="hulpvraag.html">Hulpvraag</a>
    <a href="over.html">Over</a>
    <a href="contact.html">Contact</a>
    <a href="bestellen.html">Bestellen</a>
  </nav>
</header>

<div class="content">
<h1>Over EduSwitch</h1><p>Wij helpen onderwijsinstellingen en organisaties vooruit door verbeterkansen te signaleren en te realiseren.</p>
</div>

<div class="content">
  <h3>Wat anderen zeggen</h3>
  <div class="review-slider">
    <p>“Het boek heeft ons team enorm geholpen bij een vliegende start.” — Jan de Vries, directeur</p>
    <p>“Praktische tips die meteen toepasbaar zijn.” — Petra Jansen, docent</p>
    <p>“Geeft echt structuur aan het schooljaar.” — Ahmed El Amrani, directeur</p>
    <p>“Duidelijke handvatten voor het hele team.” — Lisa van Dijk, docent</p>
  </div>
</div>

<footer>
  <p>&copy; 2025 EduSwitch. Alle rechten voorbehouden.</p>
</footer>

<div class="modal-overlay" id="modal">
  <div class="modal" id="modal-box">
    <button class="close-btn" id="close-modal">&times;</button>
    <p id="modal-message"></p>
  </div>
</div>

<script>
  const modalOverlay = document.getElementById('modal');
  const modalBox = document.getElementById('modal-box');
  const modalMessage = document.getElementById('modal-message');
  const closeModal = document.getElementById('close-modal');
  closeModal.addEventListener('click', ()=> modalOverlay.style.display='none');
  modalOverlay.addEventListener('click', e => { if(e.target===modalOverlay) modalOverlay.style.display='none'; });

  document.querySelectorAll('form').forEach(form => {
    form.addEventListener('submit', function(e) {
      e.preventDefault();
      const formType = this.getAttribute('data-form-type');
      let message = "Bedankt voor uw bericht.";
      if(formType==="hulpvraag") message = "Bedankt voor het insturen van uw hulpvraag. We gaan ermee aan de slag.";
      if(formType==="bestelling") message = "Bedankt voor uw bestelling. U ontvangt spoedig een bevestiging in uw e-mail.";
      modalMessage.textContent = message;
      modalOverlay.style.display = 'flex';
      setTimeout(()=> modalBox.classList.add('show'), 10);
    });
  });
</script>

</body>
</html>
