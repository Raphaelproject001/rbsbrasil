<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rádio HT Frequência Via Satélite</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #004c99;
            color: white;
            padding: 15px;
            text-align: center;
        }
        header h1 {
            margin: 0;
        }
        nav {
            background-color: #339966;
            padding: 10px;
            text-align: center;
        }
        nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
            font-weight: bold;
        }
        main {
            padding: 20px;
        }
        #map {
            width: 100%;
            height: 400px;
        }
        footer {
            background-color: #004c99;
            color: white;
            text-align: center;
            padding: 10px;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
        .frequencies {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
        }
        .frequency-link {
            margin: 10px;
            background-color: #339966;
            padding: 10px;
            border-radius: 5px;
            color: white;
            text-decoration: none;
            width: 45%;
            text-align: center;
        }
    </style>
    <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_GOOGLE_MAPS_API_KEY&callback=initMap" async defer></script>
</head>
<body>
    <header>
        <h1>Rádio HT Frequência Via Satélite</h1>
    </header>
    
    <nav>
        <a href="#mapa">Mapa</a>
        <a href="#frequencias">Frequências</a>
        <a href="#tradutor">Tradutor</a>
    </nav>
    
    <main>
        <section id="mapa">
            <h2>Localização via Google Maps</h2>
            <div id="map"></div>
        </section>

        <section id="frequencias">
            <h2>Frequências de Rádio no Brasil</h2>
            <div class="frequencies">
                <a href="https://www.example.com/frequencia1" class="frequency-link">Frequência 1</a>
                <a href="https://www.example.com/frequencia2" class="frequency-link">Frequência 2</a>
                <a href="https://www.example.com/frequencia3" class="frequency-link">Frequência 3</a>
                <a href="https://www.example.com/frequencia4" class="frequency-link">Frequência 4</a>
                <!-- Adicione outros links conforme necessário -->
            </div>
        </section>

        <section id="tradutor">
            <h2>Tradutor Google</h2>
            <div id="google_translate_element"></div>
            <script type="text/javascript">
                function googleTranslateElementInit() {
                    new google.translate.TranslateElement({pageLanguage: 'pt'}, 'google_translate_element');
                }
            </script>
            <script type="text/javascript" src="https://translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"></script>
        </section>

        <section>
            <h2>Link para a Estação de Rádio</h2>
            <p>Acesse a estação de rádio através deste <a href="https://www.airnavradar.com/stations/PGANRB501323?vhf=undefined" target="_blank">link</a>.</p>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 Rádio HT Frequência Via Satélite</p>
    </footer>

    <script>
        // Função de inicialização do Google Maps
        function initMap() {
            const location = { lat: -15.7801, lng: -47.9292 }; // Exemplo de localização (Brasília)
            const map = new google.maps.Map(document.getElementById("map"), {
                zoom: 4,
                center: location,
            });
            const marker = new google.maps.Marker({
                position: location,
                map: map,
            });
        }
    </script>
</body>
</html>
