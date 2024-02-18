<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kamus English to Indonesian</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Kamus English to Indonesian</h1>
    <input type="text" id="searchInput" placeholder="Search...">
    <ul id="searchResult"></ul>

    <script src="script.js"></script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kamus English to Indonesian</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Kamus English to Indonesian</h1>
    <input type="text" id="searchInput" placeholder="Search...">
    <ul id="searchResult"></ul>

    <script src="script.js"></script>
</body>
</html>

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
