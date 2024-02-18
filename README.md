
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>English to Indonesian Dictionary</title>
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
        .resultItem {
            padding: 10px;
            border-bottom: 1px solid #ccc;
        }
        .resultItem:hover {
            background-color: #f4f4f4;
        }
    </style>
</head>
<body>
    <h1>English to Indonesian Dictionary</h1>
    <input type="text" id="searchInput" placeholder="Search...">
    <ul id="searchResult"></ul>

    <script>
        // Data kamus
        var dictionary = {
            "apple": "apel",
            "banana": "pisang",
            "orange": "jeruk",
            "grape": "anggur",
            "watermelon": "semangka",
            // Tambahkan kata-kata lain di sini
        };

        // Fungsi untuk mencari kata dalam kamus
        function searchDictionary() {
            var searchInput = document.getElementById("searchInput").value.toLowerCase();
            var searchResult = document.getElementById("searchResult");
            searchResult.innerHTML = "";

            for (var word in dictionary) {
                if (word.includes(searchInput)) {
                    var listItem = document.createElement("li");
                    listItem.setAttribute("class", "resultItem");
                    listItem.innerHTML = "<strong>" + word + "</strong> - " + dictionary[word];
                    searchResult.appendChild(listItem);
                }
            }
        }

        // Panggil fungsi pencarian saat input berubah
        document.getElementById("searchInput").addEventListener("input", searchDictionary);
    </script>
</body>
</html>
