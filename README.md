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
  <div class="flex">
   <aside class="w-64 bg-gray-800 h-screen p-4" id="sidebar">
    <div class="flex items-center mb-6">
     <img alt="A sharply dressed, intense-looking male character" class="w-16 h-16 rounded-full" height="64" src="https://i.ibb.co/p30Q5fs/Leonardo-Kino-XL-A-sharplydressed-intenselooking-male-characte-3.jpg" width="64"/>
     <h2 class="ml-4 text-xl font-bold">
      Reimagine Truth
     </h2>
    </div>
    <nav>
     <ul>
      <li class="mb-4">
       <a class="text-lg text-gray-200 hover:text-white" href="#">
        Home
       </a>
      </li>
      <li class="mb-4">
       <a class="text-lg text-gray-200 hover:text-white" href="#">
        My Assets
       </a>
      </li>
      <li class="mb-4">
       <a class="text-lg text-gray-200 hover:text-white" href="#">
        About
       </a>
      </li>
      <li class="mb-4">
       <a class="text-lg text-gray-200 hover:text-white" href="https://linktr.ee/reimagine_truth" target="_blank">
        Community
       </a>
      </li>
      <li class="mb-4">
       <a class="text-lg text-gray-200 hover:text-white" href="#">
        Settings
       </a>
      </li>
     </ul>
    </nav>
   </aside>
   <div class="flex-1">
    <header class="bg-gray-800 text-white p-4 flex justify-between items-center relative">
     <button class="md:hidden text-white absolute top-4 left-4" id="menu-button">
      <i class="fas fa-bars">
      </i>
     </button>
     <div class="flex flex-col items-center w-full">
      <img alt="A sharply dressed, intense-looking male character" class="w-36 mb-2" height="50" src="https://i.ibb.co/p30Q5fs/Leonardo-Kino-XL-A-sharplydressed-intenselooking-male-characte-3.jpg" width="150"/>
      <h1 class="text-2xl font-bold text-center">
       Welcome to Reimagine Truth
      </h1>
      <p class="text-lg text-center">
       Explore the unique stories of our NFT characters.
      </p>
     </div>
    </header>
    <main class="p-4">
     <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4" id="nft-grid">
      <div class="border border-gray-700 p-4 bg-gray-800">
       <img alt="NFT character with a futuristic look" class="w-full mb-2" height="200" src="https://storage.googleapis.com/a1aa/image/IbrCPWuuXPoNEJM03brifZTOH7fjre0jZHOLBqvupWffjMf9E.jpg" width="200"/>
       <h3 class="text-xl font-bold">
        Truth Seeker #1
       </h3>
       <p>
        Rarity: Common
       </p>
       <a class="text-blue-400" href="nft.html?id=1" target="_blank">
        View Details
       </a>
      </div>
      <div class="border border-gray-700 p-4 bg-gray-800">
       <img alt="NFT character with a mystical aura" class="w-full mb-2" height="200" src="https://storage.googleapis.com/a1aa/image/3kwmQeLeoBiLiUoL2a5l0vyqEe3bHGJAFphgSiUxO63CJzvnA.jpg" width="200"/>
       <h3 class="text-xl font-bold">
        Truth Seeker #2
       </h3>
       <p>
        Rarity: Rare
       </p>
       <a class="text-blue-400" href="nft.html?id=2" target="_blank">
        View Details
       </a>
      </div>
      <div class="border border-gray-700 p-4 bg-gray-800">
       <img alt="NFT character with a cyberpunk style" class="w-full mb-2" height="200" src="https://storage.googleapis.com/a1aa/image/J1fdfg0xfhZTTIJIoNZsLqPYDQ0PXKX9bKIFzYkeaaPJSmfeE.jpg" width="200"/>
       <h3 class="text-xl font-bold">
        Truth Seeker #3
       </h3>
       <p>
        Rarity: Ultra Rare
       </p>
       <a class="text-blue-400" href="nft.html?id=3" target="_blank">
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
   </div>
  </div>
  <script>
   document.getElementById('menu-button').addEventListener('click', function() {
            const sidebar = document.getElementById('sidebar');
            if (sidebar.classList.contains('hidden')) {
                sidebar.classList.remove('hidden');
            } else {
                sidebar.classList.add('hidden');
            }
        });
  </script>
 </body>
</html>
        });
  </script>
 </body>
</html>
