<html lang="en">
 <head>
  <meta charset="utf-8"/>
  <meta content="width=device-width, initial-scale=1.0" name="viewport"/>
  <title>
   Reimagine Truth
  </title>
  <script src="https://cdn.tailwindcss.com">
  </script>
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" rel="stylesheet"/>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&amp;display=swap" rel="stylesheet"/>
  <style>
   body {
            font-family: 'Roboto', sans-serif;
        }
  </style>
 </head>
 <body class="bg-gray-900 text-gray-200">
  <header class="bg-gray-800 text-white p-4 flex flex-col items-center">
   <img alt="Leonardo-Kino-XL-A-sharplydressed-intenselooking-male-characte-3" class="w-36 mb-2" height="50" src="https://i.ibb.co/FkQLvDk/Leonardo-Kino-XL-A-sharplydressed-intenselooking-male-characte-3.jpg" width="150"/>
   <h1 class="text-2xl font-bold">
    Welcome to Reimagine Truth
   </h1>
   <p class="text-lg">
    Explore the unique stories of our NFT characters.
   </p>
  </header>
  <main class="p-4">
   <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4" id="nft-grid">
    <div class="border border-gray-700 p-4 bg-gray-800">
     <img alt="Image-7" class="w-full mb-2" height="200" src="https://i.ibb.co/Wn4dwnd/Image-7.png" width="200"/>
     <h3 class="text-xl font-bold">
      Truth Seeker #1
     </h3>
     <p>
      Rarity: Common
     </p>
     <a class="text-blue-400" href="nft.html?id=1">
      View Details
     </a>
    </div>
    <div class="border border-gray-700 p-4 bg-gray-800">
     <img alt="Image-4" class="w-full mb-2" height="200" src="https://i.ibb.co/Hp4yn0y/Image-4.png" width="200"/>
     <h3 class="text-xl font-bold">
      Truth Seeker #2
     </h3>
     <p>
      Rarity: Rare
     </p>
     <a class="text-blue-400" href="nft.html?id=2">
      View Details
     </a>
    </div>
    <div class="border border-gray-700 p-4 bg-gray-800">
     <img alt="Image-3" class="w-full mb-2" height="200" src="https://i.ibb.co/phrB0xL/Image-3.png" width="200"/>
     <h3 class="text-xl font-bold">
      Truth Seeker #3
     </h3>
     <p>
      Rarity: Ultra Rare
     </p>
     <a class="text-blue-400" href="nft.html?id=3">
      View Details
     </a>
    </div>
   </div>
  </main>
  <footer class="bg-gray-800 text-white p-4 text-center">
   <p>
    © 2024 Reimagine Truth. All rights reserved.
   </p>
  </footer>
  <script>
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
                div.classList.add('border', 'border-gray-700', 'p-4', 'bg-gray-800');
                div.innerHTML = `
                    <img src="${nft.image}" alt="${nft.name}" class="w-full mb-2">
                    <h3 class="text-xl font-bold">${nft.name}</h3>
                    <p>Rarity: ${nft.rarity}</p>
                    <a href="nft.html?id=${nft.id}" class="text-blue-400">View Details</a>
                `;
                grid.appendChild(div);
            });
        }

        // Display NFT details on the NFT details page
        function displayNFTDetails(nfts, id) {
            const nft = nfts.find(nft => nft.id == id);
            if (nft) {
                document.getElementById('nft-name').innerText = nft.name;
                document.getElementById('nft-image').src = nft.image;
                document.getElementById('nft-image').alt = nft.name;
                document.getElementById('nft-story').innerText = nft.effect;
                document.getElementById('nft-rarity').innerText = nft.rarity;
                document.getElementById('nft-attributes').innerText = `Type: ${nft.type}, Level: ${nft.level}, Style Variant: ${nft.style_variant}, Attack: ${nft.attack}, Defense: ${nft.defense}, Set ID: ${nft.set_id}, Serial Number: ${nft.serial_number}, Symbol: ${nft.symbol}, Power: ${nft.attributes.power}, Color: ${nft.attributes.color}, Special Ability: ${nft.attributes.special_ability}`;
                document.getElementById('qr-code').src = nft.qrCode;
                document.getElementById('qr-code').alt = `QR Code for ${nft.name}`;
            }
        }
  </script>
 </body>
</html>
