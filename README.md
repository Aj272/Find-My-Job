<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Find My Job</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; margin: 0; }
        .header { background: linear-gradient(to right, red, orange); color: white; padding: 20px; }
        .button { padding: 10px; border: none; border-radius: 10px; cursor: pointer; 
            background: linear-gradient(to right, red, orange); color: white; font-size: 18px; margin: 10px; }
        .button:hover { transform: scale(1.1); transition: 0.3s; }
        .container { display: none; padding: 20px; }
        #home { display: block; }
    </style>
</head>
<body>

    <!-- 🏠 Page de couverture -->
    <div class="container" id="cover">
        <div class="header">
            <h1>Bienvenue sur Find My Job</h1>
            <p>Votre avenir commence ici</p>
        </div>
        <button class="button" onclick="showPage('login')">🔒 Connexion</button>
        <button class="button" onclick="showPage('signup')">✍️ Inscription</button>
    </div>

    <!-- 🔑 Page de connexion -->
    <div class="container" id="login">
        <div class="header"><h1>Connexion</h1></div>
        <input type="email" placeholder="Email"><br>
        <input type="password" placeholder="Mot de passe"><br>
        <button class="button" onclick="showPage('home')">Se connecter</button>
    </div>

    <!-- 🆕 Page d'inscription -->
    <div class="container" id="signup">
        <div class="header"><h1>Inscription</h1></div>
        <input type="text" placeholder="Nom"><br>
        <input type="email" placeholder="Email"><br>
        <input type="password" placeholder="Mot de passe"><br>
        <button class="button" onclick="showPage('home')">S'inscrire</button>
    </div>

    <!-- 🏠 Page après connexion -->
    <div class="container" id="home">
        <div class="header"><h1>Bienvenue, [Nom de l'utilisateur] !</h1></div>
        <button class="button" onclick="showPage('search')">🔎 Rechercher un emploi</button>
        <button class="button" onclick="showPage('applications')">📄 Mes candidatures</button>
        <button class="button" onclick="showPage('profile')">👤 Mon profil</button>
        <button class="button" onclick="showPage('recommended')">⭐ Offres recommandées</button>
        <button class="button" onclick="showPage('cover')">🔓 Déconnexion</button>
    </div>

    <!-- 🔍 Recherche d'emploi -->
    <div class="container" id="search">
        <div class="header"><h1>🔎 Rechercher un emploi</h1></div>
        <p>Fonctionnalité en cours de développement...</p>
        <button class="button" onclick="showPage('home')">⬅️ Retour</button>
    </div>

    <!-- 📄 Mes candidatures -->
    <div class="container" id="applications">
        <div class="header"><h1>📄 Mes candidatures</h1></div>
        <p>Fonctionnalité en cours de développement...</p>
        <button class="button" onclick="showPage('home')">⬅️ Retour</button>
    </div>

    <!-- 👤 Mon profil -->
    <div class="container" id="profile">
        <div class="header"><h1>👤 Mon profil</h1></div>
        <p>Fonctionnalité en cours de développement...</p>
        <button class="button" onclick="showPage('home')">⬅️ Retour</button>
    </div>

    <!-- ⭐ Offres recommandées -->
    <div class="container" id="recommended">
        <div class="header"><h1>⭐ Offres recommandées</h1></div>
        <p>Fonctionnalité en cours de développement...</p>
        <button class="button" onclick="showPage('home')">⬅️ Retour</button>
    </div>

    <script>
        function showPage(pageId) {
            document.querySelectorAll('.container').forEach(page => page.style.display = 'none');
            document.getElementById(pageId).style.display = 'block';
        }
    </script>

</body>
</html>
