<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kamus English to Indonesian</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        h1 {
            text-align: center;
        }
        #searchInput {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            font-size: 16px;
        }
        #searchResult {
            list-style-type: none;
            padding: 0;
        }
        #searchResult li {
            padding: 10px;
            border-bottom: 1px solid #ccc;
        }
    </style>
</head>
<body>
    <h1>Kamus English to Indonesian</h1>
    <input type="text" id="searchInput" onkeyup="searchDictionary()" placeholder="Search...">
    <ul id="searchResult"></ul>

    <script>
        const dictionary = {
            "hello": "halo",
            "world": "dunia",
            "apple": "apel",
            "banana": "pisang",
            // Tambahkan entri kamus sesuai kebutuhan
        };

        function searchDictionary() {
            const searchInput = document.getElementById('searchInput').value.toLowerCase();
            const searchResult = document.getElementById('searchResult');
            searchResult.innerHTML = '';

            if (searchInput.length === 0) return;

            for (const [key, value] of Object.entries(dictionary)) {
                if (key.startsWith(searchInput)) {
                    const listItem = document.createElement('li');
                    listItem.textContent = `${key} - ${value}`;
                    searchResult.appendChild(listItem);
                }
            }
        }
    </script>
</body>
</html>
