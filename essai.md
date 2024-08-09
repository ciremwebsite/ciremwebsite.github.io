---
title: Lettre ouverte à M. Frédéric Valletoux, Ministre de la Santé
call_to_action: Contact
background_image_path:
large_header: false
show_in_navigation: false
---

<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://ciremwebsite.github.io/assets/css/style.css">
    <style>
        /* Styles supplémentaires spécifiques à cette page */
    .letter p {
        font-size: 1.7rem; /* Ajustez cette taille si nécessaire pour correspondre à "NOM" */
        margin-bottom: 15px;
        line-height: 1.6;
        }
        form {
            margin-top: 30px;
        }
        form label {
            font-weight: bold;
            margin-bottom: 5px;
        }
        form input[type="text"], form input[type="email"] {
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        form button {
            padding: 10px 20px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 1rem;
        }
        form button:hover {
            background-color: #0056b3;
        }
        .signatures {
            margin-top: 30px;
        }
        .signature-count {
            font-weight: bold;
            font-size: 1.2rem;
            color: #333;
        }
        .signatures ul {
            list-style-type: none;
            padding: 0;
        }
        .signatures ul li {
            padding: 5px 0;
            border-bottom: 1px solid #ddd;
        }
    </style>
</head>
<body>

    <div class="container">

        <div class="letter">
            <p><strong>À Paris, le 9 août 2024</strong></p>
            <p>Monsieur le Ministre,</p>
            <p>
                Le CIREM, représentant des étudiants en deuxième cycle des études de médecine, souhaite par la présente attirer publiquement votre attention sur les conséquences préoccupantes de la réforme actuelle du deuxième cycle des études de médecine (R2C). Bien que cette réforme ait été conçue pour moderniser le cursus médical, elle a entraîné une réduction drastique des postes disponibles dans les spécialités médicales autres que la médecine générale.
            </p>
            <p>
                Nous reconnaissons pleinement l'importance cruciale de la médecine générale dans notre système de santé, notamment pour répondre aux besoins des zones sous-dotées. Cependant, la réduction massive des postes dans les spécialités non générales compromet sérieusement l'offre de soins hospitalière. En effet, la diminution du nombre de spécialistes formés risque de limiter gravement la capacité de nos hôpitaux à assurer une prise en charge complète et de qualité des patients. Les spécialités telles que la cardiologie, la pédiatrie, la neurologie, et bien d'autres, sont indispensables pour traiter des pathologies complexes nécessitant une expertise spécifique. La réduction des postes dans ces domaines menace d'affaiblir considérablement l'ensemble du système hospitalier.
            </p>
            <p>
                Plus particulièrement, avec moins de spécialistes disponibles, la capacité des hôpitaux à organiser et à assurer les gardes et les astreintes sera fortement compromise. Les gardes hospitalières, qui sont déjà une tâche exigeante, risquent de devenir insoutenables pour les médecins restants. Une charge de travail accrue, sans renfort adéquat, pourrait entraîner une augmentation du stress, une baisse de la qualité des soins, et potentiellement un risque accru d'erreurs médicales. De plus, le manque de personnel spécialisé rendrait impossible l'organisation d'astreintes 24 h/24, 7 jours sur 7, compromettant ainsi la capacité des hôpitaux à répondre aux urgences spécialisées.
            </p>
            <p>
                Cette situation pourrait également accentuer les inégalités territoriales en matière de santé. Les hôpitaux situés dans les zones rurales ou sous-dotées, qui peinent déjà à recruter des spécialistes, seront particulièrement touchés. Sans un nombre suffisant de spécialistes, ces établissements risquent de voir leur offre de soins se réduire, obligeant les patients à se déplacer vers des centres hospitaliers plus éloignés, allongeant ainsi les délais de prise en charge et compromettant l'accès aux soins pour les populations les plus vulnérables.
            </p>
            <p>
                Nous souhaitons aussi souligner une situation alarmante concernant le nombre d'étudiants en deuxième cycle des études de médecine. Cette année, nous avons enregistré une perte de 15 % des étudiants, et les projections pour l'année prochaine ne laissent pas entrevoir de rééquilibrage. Les résultats des concours blancs indiquent que bon nombre d'étudiants de la nouvelle promotion ont déjà décidé de redoubler. Cette tendance pourrait aggraver encore davantage le déficit en spécialistes si des mesures correctives ne sont pas rapidement prises.
            </p>
            <p>
                Face à ces constats, nous sollicitons officiellement une rencontre avec vous, Monsieur le Ministre, ainsi qu'avec les directions générales des Agences Régionales de Santé (ARS), pour discuter d'une redistribution urgente des postes disponibles. Il est crucial de réévaluer la répartition des postes pour répondre aux besoins actuels et futurs du système de santé français.
            </p>
            <p>
                Le CIREM reste à votre disposition pour entamer un dialogue constructif sur ces questions cruciales pour l'avenir de notre système de santé.
            </p>
            <p>
                Dans l'attente de votre réponse et dans l'espoir d'une action rapide, nous vous prions d'agréer, Monsieur le Ministre, l'expression de notre haute considération.
            </p>
            <p><strong>Le Président du CIREM</strong></p>
        </div>

        <form id="signatureForm">
            <label for="name">Nom :</label>
            <input type="text" id="name" name="name" required>
            
            <label for="email">Email :</label>
            <input type="email" id="email" name="email" required>
            
            <button type="submit">Signer la Lettre</button>
        </form>

        <div class="signatures">
            <p>Nombre de signatures : <span id="signatureCount">0</span></p>
            <ul id="signatures"></ul>
        </div>
    </div>

  <script>
        const backendUrl = '[http://localhost:3000](https://nonstop-secret-sprite.glitch.me/)'; // URL de votre serveur Node.js

        document.getElementById('signatureForm').onsubmit = function(e) {
            e.preventDefault();
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            
            fetch(`${backendUrl}/signatures`, {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify({ name, email }),
            })
            .then(response => response.json())
            .then(data => {
                console.log('Success:', data);
                fetchSignatures(); // Recharger la liste des signatures
            })
            .catch((error) => {
                console.error('Error:', error);
            });

            document.getElementById('name').value = '';
            document.getElementById('email').value = '';
        }

        function fetchSignatures() {
            fetch(`${backendUrl}/signatures`)
                .then(response => response.json())
                .then(data => {
                    const signatureList = document.getElementById('signatures');
                    signatureList.innerHTML = '';
                    data.forEach((signature, index) => {
                        const li = document.createElement('li');
                        li.textContent = `${index + 1}. ${signature.name}`;
                        signatureList.appendChild(li);
                    });
                    document.getElementById('signatureCount').textContent = data.length;
                });
        }

        // Charger les signatures au démarrage
        fetchSignatures();
    </script>

</body>
</html>
