<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Loveroom Secret Jungle 🌿</title>

    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&family=Great+Vibes&display=swap" rel="stylesheet">

<style>
        /* Style de base */
        body {
            font-family: 'Roboto', sans-serif;
            background-color: #fff;
            color: #333;
            margin: 0;
            padding: 0;
            transition: background-color 0.3s, color 0.3s;
        }

        header {
            background-color: #228B22;
            color: white;
            padding: 20px;
            text-align: center;
            position: relative;
        }

        header h1 {
            font-family: 'Great Vibes', cursive;
            font-size: 3em;
            margin: 0;
        }

        nav {
            text-align: center;
            padding: 15px;
            background-color: #2E8B57;
        }

        nav a {
            color: white;
            padding: 14px 20px;
            text-decoration: none;
            font-weight: bold;
            display: inline-block;
            margin: 0 10px;
            border-radius: 5px;
        }

        nav a:hover {
            background-color: white;
            color: #2E8B57;
        }

        section {
            padding: 40px;
            max-width: 1200px;
            margin: auto;
            text-align: center;
        }

        h2, h3 {
            font-size: 2em;
            color: #2E8B57;
            margin-bottom: 20px;
        }

        .btn {
            background-color: #228B22;
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
            border-radius: 25px;
            font-size: 16px;
            margin-top: 10px;
            transition: background-color 0.3s ease;
        }

        .btn:hover {
            background-color: #2E8B57;
        }

        .pack {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
        }

        .pack-card {
            background-color: #f5f5f5;
            padding: 20px;
            margin: 10px;
            border-radius: 10px;
            width: 300px;
            text-align: center;
            box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }

        .pack-card:hover {
            transform: scale(1.05);
        }

        .pack-card img {
            width: 100%;
            border-radius: 10px;
            margin-bottom: 10px;
        }

        footer {
            text-align: center;
            padding: 20px;
            background-color: #228B22;
            color: white;
        }

        /* Modal */
        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0, 0, 0, 0.4); 
        }

        .modal-content {
            background-color: #fff;
            margin: 15% auto;
            padding: 20px;
            border-radius: 10px;
            max-width: 500px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }

        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
        }

        .close:hover,
        .close:focus {
            color: #000;
            cursor: pointer;
        }

        /* Styles des formulaires */
        form {
            display: flex;
            flex-direction: column;
        }

        label {
            margin-bottom: 5px;
            font-weight: bold;
        }

        input[type="text"],
        input[type="email"],
        input[type="tel"],
        input[type="date"],
        input[type="time"],
        textarea,
        select {
            padding: 10px;
            margin-bottom: 15px;
            border-radius: 5px;
            border: 1px solid #ccc;
            width: 100%;
        }

        button[type="submit"] {
            background-color: #228B22;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        button[type="submit"]:hover {
            background-color: #2E8B57;
        }

        /* Styles pour le mode rose */
        .pink-mode {
            background-color: #ffcccb;
            color: #333;
        }

        .pink-mode header {
            background-color: #ff69b4; /* Couleur rose vif */
        }

        .pink-mode nav {
            background-color: #ff1493; /* Couleur rose foncé */
        }

        .pink-mode .btn {
            background-color: #ff69b4; /* Couleur bouton rose */
        }

        .pink-mode .btn:hover {
            background-color: #ff1493; /* Couleur bouton rose foncé */
        }

        /* Styles pour le panier */
        #panier {
            display: none;
            position: fixed;
            top: 20px;
            right: 20px;
            background-color: white;
            border: 1px solid #ccc;
            border-radius: 10px;
            padding: 10px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
        }

        #panier h3 {
            margin: 0;
        }

        #panier .article {
            margin: 5px 0;
        }

        /* Styles pour le panier flottant */
        #panier {
            position: fixed;
            top: 20%;
            right: 0;
            width: 300px;
            padding: 15px;
            background-color: #f9f9f9;
            border: 1px solid #ccc;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            display: none;
        }
        
        /* Styles pour la notification rapide */
        #notification {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: #4caf50;
            color: white;
            padding: 10px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            display: none;
        }

        .pack-card {
            margin-bottom: 20px;
        }
    </style>
</head>
<body>

    <header>
        <h1>Loveroom Secret Jungle 🌿</h1>
        <button class="toggle-theme" onclick="toggleTheme()">Mode Punk Rose</button>
    </header>

    <nav>
        <a href="javascript:void(0)" onclick="openModal('aboutModal')">À propos de nous</a>
        <a href="javascript:void(0)" onclick="openModal('contactModal')">Contact</a>
        <a href="javascript:void(0)" onclick="openModal('reservationModal')">Réservation directe</a>
        <a href="javascript:void(0)" onclick="openModal('boutiqueModal')">Boutique</a>
        <a href="javascript:void(0)" onclick="togglePanier()">Panier</a>
    </nav>

    <section>
        <h2>Nos Services :</h2>
        <div class="pack">
            <div class="pack-card">
                <img src="https://mcusercontent.com/40a9f1a77d46874eba2309d88/images/ff8d406f-893c-3cbf-ba8a-8417501275e4.jpg" alt="Pack Romantique">
                <h3>Romantique</h3>
                <p>Décoration romantique avec des pétales de roses et bougies pour une soirée intime.</p>
                <p><strong>Prix : 50€</strong></p>
                <button class="btn" onclick="openReservation('Pack Romantique', 50)">Réserver</button>
            </div>

            <div class="pack-card">
                <img src="https://mcusercontent.com/40a9f1a77d46874eba2309d88/images/c8dbf126-5faa-ecbb-3944-83668e89f983.jpg" alt="Pack Anniversaire">
                <h3>Pack Anniversaire</h3>
                <p>Décoration festive pour célébrer un anniversaire inoubliable dans un cadre idyllique.</p>
                <p><strong>Prix : 50€</strong></p>
                <button class="btn" onclick="openReservation('Pack Anniversaire', 50)">Réserver</button>
            </div>

            <div class="pack-card">
                <img src="https://mcusercontent.com/40a9f1a77d46874eba2309d88/images/34f580d7-2eeb-cf49-9c46-0746e127fe45.jpg" alt="Pack Personnalisé">
                <h3>love couple</h3>
                <p>Décoration unique selon vos demandes pour tout type d'événements.</p>
                <p><strong>Prix : Sur demande</strong></p>
                <button class="btn" onclick="openReservation('Pack Personnalisé')">Réserver</button>
            </div>
            
                  <div class="pack-card">
                <img src="https://mcusercontent.com/40a9f1a77d46874eba2309d88/images/45e8d80f-0f2c-b50e-cc6a-8ce24cab1bd6.jpg" alt="Pack Personnalisé">
                <h3>Pack à la demande</h3>
                <p>Décoration unique selon vos demandes pour tout type d'événements.</p>
                <p><strong>Prix : Sur demande</strong></p>
                <button class="btn" onclick="openReservation('Pack Personnalisé')">Réserver</button>
            </div>
        </div>
    </section>

    <footer>
        <p>&copy; 2024 Loveroom Secret Jungle 🌿. Tous droits réservés.</p>
    </footer>

    <!-- Modals -->
    <!-- About Modal -->
    <div id="aboutModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('aboutModal')">&times;</span>
            <h2>À propos de nous</h2>
            <p>La Loveroom Secret Jungle est un lieu unique où romantisme et nature se rencontrent.</p>
        </div>
    </div>
    <!-- Contact Modal -->
    <div id="contactModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('contactModal')">&times;</span>
            <h2>Contactez-nous</h2>
            <form id="contactForm">
                <label for="contactName">Nom :</label>
                <input type="text" id="contactName" name="contactName" required>

                <label for="contactEmail">Email :</label>
                <input type="email" id="contactEmail" name="contactEmail" required>

                <label for="contactMessage">Message :</label>
                <textarea id="contactMessage" name="contactMessage" rows="4" required></textarea>

                <button type="submit">Envoyer</button>
            </form>
        </div>
    </div>

    <!-- Reservation Modal -->
    <div id="reservationModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('reservationModal')">&times;</span>
            <h2>Réservation</h2>
            <form id="reservationForm">
                <label for="serviceName">Nom du service :</label>
                <input type="text" id="serviceName" name="serviceName" readonly>

                <label for="reservationDate">Date :</label>
                <input type="date" id="reservationDate" name="reservationDate" required>

                <label for="reservationTime">Heure :</label>
                <input type="time" id="reservationTime" name="reservationTime" required>

                <label for="clientName">Votre nom :</label>
                <input type="text" id="clientName" name="clientName" required>

                <label for="clientEmail">Votre email :</label>
                <input type="email" id="clientEmail" name="clientEmail" required>

                <button type="submit">Réserver</button>
            </form>
        </div>
    </div>

    <!-- Boutique Modal -->
    <div id="boutiqueModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('boutiqueModal')">&times;</span>
            <h2>Boutique</h2>
            <p>Achetez nos produits exclusifs :</p>
            <div class="pack">
                <div class="pack-card">
                    <img src="https://mcusercontent.com/40a9f1a77d46874eba2309d88/images/c5ed5648-80a5-2cf0-9ae7-7abe36969786.jpeg" alt="Bougies Parfumées">
                    <h3>Bougies Parfumées</h3>
                    <p>Bougies parfumées pour créer une ambiance romantique et relaxante.</p>
                    <p><strong>Prix : 20€</strong></p>
                    <button class="btn" onclick="addToPanier('Bougies Parfumées', 20)">Ajouter au panier</button>
                </div>

                <div class="pack-card">
                    <img src="https://mcusercontent.com/40a9f1a77d46874eba2309d88/images/f7ef1922-2990-826c-eeb5-70a605e08a67.jpg" alt="Pétales de Roses">
                    <h3>Pétales de Roses</h3>
                    <p>Pétales de roses fraîches pour décorer et rendre vos moments inoubliables.</p>
                    <p><strong>Prix : 15€</strong></p>
                    <button class="btn" onclick="addToPanier('Pétales de Roses', 15)">Ajouter au panier</button>
                </div>

                <div class="pack-card">
                    <img src="https://mcusercontent.com/40a9f1a77d46874eba2309d88/images/ca3d8cf3-9554-52b6-e7c9-fc0fcb6e6ad2.jpeg" alt="Huile de Massage">
                    <h3>Huile de Massage</h3>
                    <p>Huile de massage aux senteurs exotiques pour une expérience relaxante.</p>
                    <p><strong>Prix : 25€</strong></p>
                    <button class="btn" onclick="addToPanier('Huile de Massage', 25)">Ajouter au panier</button>
                </div>
                   <div class="pack-card">
                <img src="https://mcusercontent.com/40a9f1a77d46874eba2309d88/images/2f70ab33-4d37-97d5-f666-a704295d253e.jpeg" alt="Pétales de Roses">
                <h3>Brume corporelle rafraîchissante</h3>
    <p>Une brume légère et parfumée pour hydrater et rafraîchir votre peau tout au long de la journée.</p>
    <p><strong>Prix : 18€</strong></p>
                <button class="btn" onclick="addToPanier('Pétales de Roses', 15)">Ajouter au panier</button>
            </div>
                <!-- Emplacement pour ajouter d'autres produits à l'avenir -->
                <div id="extraProducts"></div>
            </div>
        </div>
    </div>

    <!-- Panier flottant -->
    <div id="panier">
        <h3>Votre Panier</h3>
        <div id="panierItems"></div>
        <button class="btn" onclick="validerPanier()">Valider la commande</button>
    </div>

    <!-- Notification rapide -->
    <div id="notification"></div>

    <script>
        // Fonction pour ouvrir un modal
        function openModal(modalId) {
            document.getElementById(modalId).style.display = "block";
        }

        // Fonction pour fermer un modal
        function closeModal(modalId) {
            document.getElementById(modalId).style.display = "none";
        }

        // Fonction pour ouvrir/fermer le panier
        function togglePanier() {
            const panier = document.getElementById('panier');
            panier.style.display = (panier.style.display === 'none' || panier.style.display === '') ? 'block' : 'none';
        }

        // Fonction pour ajouter un article au panier
        const panierArticles = [];

        function addToPanier(nom, prix) {
            panierArticles.push({ nom, prix });
            updatePanier();
            showNotification(`${nom} ajouté au panier`);
            togglePanier();  // Afficher le panier automatiquement après ajout
        }

        // Fonction pour mettre à jour l'affichage du panier
        function updatePanier() {
            const panierItems = document.getElementById('panierItems');
            panierItems.innerHTML = '';
            panierArticles.forEach(article => {
                const div = document.createElement('div');
                div.className = 'article';
                div.textContent = `${article.nom} - ${article.prix}€`;
                panierItems.appendChild(div);
            });
        }

        // Fonction pour valider la commande
        function validerPanier() {
            if (panierArticles.length === 0) {
                alert("Votre panier est vide.");
                return;
            }
            alert("Commande validée !");
            panierArticles.length = 0; // Vider le panier
            updatePanier(); // Mettre à jour l'affichage
        }

        // Fonction pour ouvrir la réservation avec des informations pré-remplies
        function openReservation(serviceName, price) {
            document.getElementById('serviceName').value = serviceName;
            document.getElementById('reservationModal').style.display = "block";
        }

        // Fonction pour changer de thème
        function toggleTheme() {
            document.body.classList.toggle('pink-mode');
        }

        // Afficher la notification rapide
        function showNotification(message) {
            const notification = document.getElementById('notification');
            notification.textContent = message;
            notification.style.display = 'block';

            setTimeout(() => {
                notification.style.display = 'none';
            }, 2000);  // Notification disparaît après 2 secondes
        }

        // Fermer un modal si l'utilisateur clique en dehors du contenu
        window.onclick = function(event) {
            const modals = document.getElementsByClassName("modal");
            for (let i = 0; i < modals.length; i++) {
                if (event.target == modals[i]) {
                    modals[i].style.display = "none";
                }
            }
        }
    </script>

</body>
</html>
