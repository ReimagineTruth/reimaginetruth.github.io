# ReimagineTruth.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Reimagine Truth</title>
    <link rel="stylesheet" href="css/styles.css">
</head>
<body>
    <header>
        <img src="assets/logo.png" alt="Reimagine Truth Logo" class="logo">
        <h1>Welcome to Reimagine Truth</h1>
        <p>Explore the unique stories of our NFT characters.</p>
    </header>
    <main>
        <div id="nft-grid" class="grid"></div>
    </main>
    <footer>
        <p>© 2024 Reimagine Truth. All rights reserved.</p>
    </footer>
    <script src="js/main.js"></script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NFT Details</title>
    <link rel="stylesheet" href="css/styles.css">
</head>
<body>
    <header>
        <img src="assets/logo.png" alt="Reimagine Truth Logo" class="logo">
        <h1 id="nft-name">NFT Name</h1>
    </header>
    <main>
        <img id="nft-image" src="assets/nft/placeholder.png" alt="NFT Image" class="nft-image">
        <p id="nft-story">Loading story...</p>
        <p><strong>Rarity:</strong> <span id="nft-rarity">Unknown</span></p>
        <p><strong>Attributes:</strong> <span id="nft-attributes">N/A</span></p>
        <img id="qr-code" src="assets/qr/placeholder.png" alt="QR Code" class="qr-code">
    </main>
    <footer>
        <p>© 2024 Reimagine Truth. All rights reserved.</p>
    </footer>
    <script src="js/main.js"></script>
</body>
</html>

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    text-align: center;
    background-color: #f4f4f9;
    color: #333;
}

header {
    padding: 20px;
    background-color: #222;
    color: #fff;
}

.logo {
    width: 150px;
}

.grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    padding: 20px;
}

.grid div {
    border: 1px solid #ccc;
    padding: 10px;
    background-color: #fff;
}

footer {
    margin-top: 20px;
    padding: 10px;
    background-color: #222;
    color: #fff;
}

// Load NFT Data
fetch('data/nft.json')
    .then(response => response.json())
    .then(data => {
        displayNFTs(data);
        const urlParams = new URLSearchParams(window.location.search);
        const nftId = urlParams.get('id');
        if (nftId) {
            displayNFTDetails(data, nftId);
        }
    });

// Display NFTs in the grid
function displayNFTs(nfts) {
    const grid = document.getElementById('nft-grid');
    nfts.forEach(nft => {
        const div = document.createElement('div');
        div.innerHTML = `
            <img src="${nft.image}" alt="${nft.name}">
            <h3>${nft.name}</h3>
            <p>${nft.rarity}</p>
            <a href="nft.html?id=${nft.id}">View Details</a>
        `;
        grid.appendChild(div);
    });
}

// Display NFT details on the NFT details page
function displayNFTDetails(nfts, id) {
    const nft = nfts.find(nft => nft.id == id);
    if (nft) {
        document.getElementById('nft-name').innerText = nft.name;
        document.get
