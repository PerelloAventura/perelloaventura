<!DOCTYPE html><html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Perelló Aventura Paintball</title>
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f7f7f7;
    }
  </style>
</head>
<body class="text-gray-900">
  <!-- Header -->
  <header class="bg-yellow-400 p-4 flex items-center justify-between">
    <img src="/logo.png" alt="Logo" class="h-16">
    <nav class="space-x-4">
      <button onclick="changeLang('es')">ES</button>
      <button onclick="changeLang('ca')">CAT</button>
      <button onclick="changeLang('fr')">FR</button>
      <button onclick="changeLang('en')">EN</button>
      <button onclick="changeLang('de')">DE</button>
    </nav>
  </header>  <!-- Hero Section -->  <section class="bg-green-900 text-white text-center p-10">
    <h1 class="text-4xl font-bold" id="hero-title">¡Ven a pasar un día diferente!</h1>
    <p class="text-xl mt-2" id="hero-sub">Paintball en Perelló Aventura</p>
  </section>  <!-- Prices -->  <section class="p-8">
    <h2 class="text-2xl font-bold mb-4" id="price-title">Precios</h2>
    <ul class="space-y-2">
      <li id="price1">Partida 100 bolas - 20€</li>
      <li id="price2">Partida 200 bolas - 24€</li>
      <li id="price3">Partida 300 bolas - 28€</li>
      <li id="recharges">Recargas - 6€ / Cada 5 recargas, 1 gratis</li>
    </ul>
  </section>  <!-- Calendar (placeholder for now) -->  <section class="p-8 bg-gray-100">
    <h2 class="text-2xl font-bold mb-4" id="calendar-title">Calendario de Reservas</h2>
    <p class="text-gray-700" id="calendar-msg">(Aquí irá un calendario interactivo...)</p>
  </section>  <!-- Reservation Form -->  <section class="p-8">
    <h2 class="text-2xl font-bold mb-4" id="form-title">Haz tu reserva</h2>
    <form action="https://formspree.io/f/xnnprgek" method="POST" class="space-y-4">
      <input type="text" name="nombre" placeholder="Nombre" class="border p-2 w-full" required>
      <input type="email" name="email" placeholder="Email" class="border p-2 w-full" required>
      <input type="tel" name="telefono" placeholder="Teléfono" class="border p-2 w-full">
      <input type="date" name="fecha" class="border p-2 w-full" required>
      <input type="number" name="personas" placeholder="Número de personas" class="border p-2 w-full" required>
      <input type="hidden" name="_subject" value="Nueva reserva desde la web">
      <input type="hidden" name="_next" value="https://perelloaventura.com/gracias.html">
      <button type="submit" class="bg-yellow-400 text-black p-2 rounded">Enviar</button>
    </form>
  </section>  <!-- Contact -->  <section class="p-8 bg-green-900 text-white">
    <h2 class="text-2xl font-bold mb-4" id="contact-title">Contacto</h2>
    <p>Polígono 9 Parcela 56, El Perelló, Tarragona</p>
    <p>Horario: 10:00 – 22:00</p>
    <p>Tel: +34 656 756 500</p>
  </section>  <footer class="bg-black text-white text-center p-4">
    <p>&copy; 2025 Perelló Aventura Paintball</p>
  </footer>  <!-- Simple i18n support -->  <script>
    const translations = {
      es: {
        'hero-title': '¡Ven a pasar un día diferente!',
        'hero-sub': 'Paintball en Perelló Aventura',
        'price-title': 'Precios',
        'price1': 'Partida 100 bolas - 20€',
        'price2': 'Partida 200 bolas - 24€',
        'price3': 'Partida 300 bolas - 28€',
        'recharges': 'Recargas - 6€ / Cada 5 recargas, 1 gratis',
        'calendar-title': 'Calendario de Reservas',
        'calendar-msg': '(Aquí irá un calendario interactivo...)',
        'form-title': 'Haz tu reserva',
        'contact-title': 'Contacto'
      },
      ca: {
        'hero-title': 'Vine a passar un dia diferent!',
        'hero-sub': 'Paintball a Perelló Aventura',
        'price-title': 'Preus',
        'price1': 'Partida 100 boles - 20€',
        'price2': 'Partida 200 boles - 24€',
        'price3': 'Partida 300 boles - 28€',
        'recharges': 'Recarregues - 6€ / Cada 5, 1 gratis',
        'calendar-title': 'Calendari de reserves',
        'calendar-msg': '(Aquí anirà un calendari interactiu...)',
        'form-title': 'Fes la teva reserva',
        'contact-title': 'Contacte'
      },
      fr: {
        'hero-title': 'Passez une journée différente !',
        'hero-sub': 'Paintball à Perelló Aventura',
        'price-title': 'Tarifs',
        'price1': 'Partie 100 billes - 20€',
        'price2': 'Partie 200 billes - 24€',
        'price3': 'Partie 300 billes - 28€',
        'recharges': 'Recharges - 6€ / Toutes les 5, 1 gratuite',
        'calendar-title': 'Calendrier des réservations',
        'calendar-msg': '(Calendrier interactif à venir...)',
        'form-title': 'Réservez maintenant',
        'contact-title': 'Contact'
      },
      en: {
        'hero-title': 'Come live a different day!',
        'hero-sub': 'Paintball at Perelló Aventura',
        'price-title': 'Prices',
        'price1': 'Game 100 balls - €20',
        'price2': 'Game 200 balls - €24',
        'price3': 'Game 300 balls - €28',
        'recharges': 'Reloads - €6 / Every 5, 1 free',
        'calendar-title': 'Booking Calendar',
        'calendar-msg': '(Interactive calendar coming soon...)',
        'form-title': 'Book your game',
        'contact-title': 'Contact'
      },
      de: {
        'hero-title': 'Erlebe einen anderen Tag!',
        'hero-sub': 'Paintball bei Perelló Aventura',
        'price-title': 'Preise',
        'price1': 'Spiel 100 Kugeln - 20€',
        'price2': 'Spiel 200 Kugeln - 24€',
        'price3': 'Spiel 300 Kugeln - 28€',
        'recharges': 'Nachladungen - 6€ / Jede 5., 1 gratis',
        'calendar-title': 'Reservierungskalender',
        'calendar-msg': '(Interaktiver Kalender in Kürze...)',
        'form-title': 'Jetzt reservieren',
        'contact-title': 'Kontakt'
      }
    };

    function changeLang(lang) {
      const dict = translations[lang];
      Object.keys(dict).forEach(id => {
        const el = document.getElementById(id);
        if (el) el.innerText = dict[id];
      });
    }
  </script></body>
</html>
