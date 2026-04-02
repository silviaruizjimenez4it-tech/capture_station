# capture_station
Unterricht- Systemsicherheit

#1
cd /var/www/html/
#2 
touch wuff_vers_01.html
touch wuff.css   
#3
nano wuff_vers_01.html
 
<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Meine erste Webseite</title>
<link rel="stylesheet" href="wuff.css">
</head>
<body>
 
    <main class="dog-card">
<h1>Mein ASCII-Hund</h1>
 
        <pre role="img" aria-label="Ein freundlicher ASCII-Art Hund">
  / \__/ \
(  o o    )
/   V     \
/(  \^/  ) \
/  \__|__/  \
/    /    \   \
|___ /     \___|
</pre>
 
        <div class="description">
<p>Wuff! Ich bin ein freundlicher ASCII-Hund.</p>
<p><strong>Interaktion:</strong> Bewege die Maus über mich oder halte mich gedrückt!</>        </div>
</main>
 
</body>
</html>
 
nano wuff.css
 
/* CSS für den interaktiven ASCII-Hund
   Fokus: Box-Modell, Transformationen und Animationen
*/
 
/* 1. Grundlayout der Seite */
body {
    font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    margin: 0;
    background: linear-gradient(135deg, #e0eafc 0%, #cfdef3 100%);
}
 
/* 2. Karten-Container für den Hund */
.dog-card {
    background: #ffffff;
    padding: 2.5rem;
    border-radius: 20px;
    text-align: center;
    box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
    max-width: 400px;
    border: 1px solid rgba(255, 255, 255, 0.3);
}
 
/* 3. Das ASCII-Element (Kernstück) */
pre {
    font-family: "Courier New", Courier, monospace;
    font-size: 1.25rem;
    line-height: 1.3;
    display: inline-block; /* Ermöglicht Transformationen wie Skalierung/Rotation */
    color: #34495e;
    margin: 20px 0;
    cursor: pointer;
    user-select: none; /* Verhindert Markieren des Textes beim Klicken */
 
    /* Sanfter Übergang für alle Änderungen (Farbe, Größe, Position) */
    transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}
 
/* 4. Interaktion: Streicheln (:hover) */
pre:hover {
    color: #e67e22; /* Ein warmes Orange */
    transform: scale(1.1) translateY(-10px);
}
 
/* 5. Interaktion: Wedeln/Freude (:active) */
/* Wird ausgelöst, wenn man die Maustaste auf dem Element gedrückt hält */
pre:active {
    animation: wag-tail 0.15s infinite alternate;
}
 
/* 6. Definition der Animationen */
@keyframes wag-tail {
    from {
        transform: scale(1.1) rotate(-3deg);
    }
    to {
        transform: scale(1.1) rotate(3deg);
    }
}
 
/* 7. Typografie-Details */
h1 {
    color: #2c3e50;
    font-size: 1.4rem;
    margin-bottom: 0.5rem;
}
 
p {
    color: #7f8c8d;
    font-size: 0.95rem;
    line-height: 1.5;
}
 
em {
    color: #bdc3c7;
    font-style: italic;
    display: block;
    margin-top: 10px;
}