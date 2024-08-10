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
                Le Comité Interfacultaire Représentant les Externes en Médecine (CIREM), association constituée en mars 2024 pour défendre les intérêts des étudiants directement impactés par la réforme du deuxième cycle des études de médecine (R2C), représente aujourd'hui plusieurs centaines d'étudiants en sixième année. Par la présente, nous tenons à exprimer notre profonde inquiétude face aux répercussions de cette réforme, qui, bien qu'elle vise à moderniser notre cursus, a engendré une réduction drastique des postes offerts dans les spécialités médicales hors médecine générale, avec une diminution moyenne de 15 % des effectifs. Cette décision intervient alors que la problématique des déserts médicaux n'a jamais été aussi pressante pour nos concitoyens, un sujet qui a déjà été soulevé à l'Assemblée nationale et qui constitue une priorité absolue en matière de politique publique de santé.
            </p>
            <p>
                Nous reconnaissons pleinement l'importance capitale de la médecine générale dans le cadre du système de santé français, en particulier pour répondre aux besoins urgents des zones sous-dotées. Toutefois, la réduction massive des postes dans les autres spécialités médicales menace gravement la capacité de nos hôpitaux à garantir une prise en charge complète et de qualité pour l'ensemble des patients. La diminution du nombre de spécialistes formés dans des domaines aussi cruciaux que la cardiologie, la neurologie, ou encore la psychiatrie, pourrait sérieusement compromettre l'efficacité de notre système de soins. Les délais d'attente pour accéder à des consultations spécialisées en endocrinologie, dermatologie, et néphrologie sont déjà préoccupants (parfois plus de six mois !), et cette réduction d'effectifs ne ferait qu'aggraver une situation déjà tendue.
            </p>
            <p>
                En outre, il convient de rappeler que la charge de travail imposée aux internes dépasse aujourd'hui largement le cadre légal. L'État a été condamné par le Conseil d'état pour la mauvaise comptabilisation des heures de travail des internes, et il a été mis en demeure de respecter le temps de travail légal, sans que cela ne soit suivi d'effets concrets. La réduction de 15 % des effectifs ne fera qu'accentuer les tensions dans les spécialités déjà sous-dotées, au détriment direct des patients. Il est également impératif de souligner la gravité de la situation en matière de santé mentale des internes : selon l'ISNI, un interne se suicide tous les 18 jours, et 4 % ont déjà fait une tentative de suicide. Ces chiffres alarmants ne peuvent être ignorés.
            </p>
            <p>
                De plus, il est essentiel de noter qu'aucune concertation collective n'a été menée avec les étudiants de notre promotion, qui ont découvert avec stupeur cette réduction de 15 % des places hors spécialités, imposée sans préavis. Cette décision unilatérale ne tient pas compte des réalités du terrain ni des besoins des futurs praticiens et de leurs patients.
            </p>
            <p>
                Face à ces constats, nous vous demandons respectueusement, Monsieur le Ministre, de bien vouloir nous accorder une rencontre, ainsi qu'avec les directions générales des Agences Régionales de Santé (ARS), afin de discuter d'une redistribution urgente des postes disponibles. Nous insistons pour que cette réunion ait lieu avant la fin du mois d'août, et avant l'étape de simulation définitive, afin de pouvoir réévaluer la répartition des postes et répondre aux besoins actuels et futurs de notre système de santé, garantissant ainsi à la population française un accès égalitaire et de qualité aux soins spécialisés.
            </p>
            <p>
                Le CIREM se tient à votre disposition pour engager un dialogue constructif sur ces questions cruciales pour l'avenir de notre système de santé.
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
    // Utilisation correcte de l'URL de base de votre backend
    const backendUrl = 'https://graceful-frost-bow.glitch.me'; // URL de votre serveur Node.js

    // Gestion de la soumission du formulaire
    document.getElementById('signatureForm').onsubmit = function(e) {
        e.preventDefault();
        const name = document.getElementById('name').value;
        const email = document.getElementById('email').value;
        
        // Envoi de la requête POST pour ajouter une nouvelle signature
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

        // Réinitialiser le formulaire après soumission
        document.getElementById('name').value = '';
        document.getElementById('email').value = '';
    }

    // Fonction pour récupérer et afficher les signatures
    function fetchSignatures() {
        fetch(`${backendUrl}/signatures`)
            .then(response => response.json())
            .then(data => {
                const signatureList = document.getElementById('signatures');
                signatureList.innerHTML = ''; // Vider la liste existante
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
