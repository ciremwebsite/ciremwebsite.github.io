---
title: dev
call_to_action: Contact
background_image_path:
large_header: false
show_in_navigation: false
---

### La presse en parle

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Accordéon Exemple</title>
    <style>
        .accordion {
            background-color: #eee;
            color: #444;
            cursor: pointer;
            padding: 18px;
            width: 100%;
            border: none;
            text-align: left;
            outline: none;
            font-size: 15px;
            transition: 0.4s;
        }

        .active, .accordion:hover {
            background-color: #ccc;
        }

        .accordion:after {
            content: '\002B'; /* Unicode character for "plus" sign (+) */
            color: #777;
            font-weight: bold;
            float: right;
            margin-left: 5px;
        }

        .active:after {
            content: "\2212"; /* Unicode character for "minus" sign (-) */
        }

        .panel {
            padding: 0 18px;
            background-color: white;
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.2s ease-out;
        }
    </style>
</head>
<body>

#### la presse en parle

<button class="accordion">Édition 2024-2025</button>
<div class="panel">
  <p>Guide des doubles-cursus et de la recherche scientifique 2023-2024 (rédigé par Ella Callas)</p>
  <a href="#">Guide DC 2024-2025</a>
</div>

<button class="accordion">Édition 2023-2024</button>
<div class="panel">
  <p>Contenu de l'édition 2023-2024.</p>
</div>

<button class="accordion">Édition 2022-2023</button>
<div class="panel">
  <p>Contenu de l'édition 2022-2023.</p>
</div>

<script>
    var acc = document.getElementsByClassName("accordion");
    var i;

    for (i = 0; i < acc.length; i++) {
        acc[i].addEventListener("click", function() {
            this.classList.toggle("active");
            var panel = this.nextElementSibling;
            if (panel.style.maxHeight) {
                panel.style.maxHeight = null;
            } else {
                panel.style.maxHeight = panel.scrollHeight + "px";
            } 
        });
    }
</script>

</body>
</html>
