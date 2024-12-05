<html lang="en">
<head>
    <meta charset="utf-8"/>
    <meta content="width=device-width, initial-scale=1.0" name="viewport"/>
    <title>Reimagine Truth</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" rel="stylesheet"/>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet"/>
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            padding: 0;
            height: 100vh;
            overflow-x: hidden;
        }

        .nft-card img {
            width: 100%;
            height: auto;
            object-fit: cover;
        }

        .nft-card {
            transition: transform 0.3s ease-in-out;
        }

        .nft-card:hover {
            transform: scale(1.05);
        }

        .sidebar {
            transition: transform 0.3s ease-in-out;
        }

        .sidebar-item {
            transition: background-color 0.3s ease-in-out, color 0.3s ease-in-out;
        }

        .sidebar-item:hover {
            background-color: #4A5568;
            color: #FFFFFF;
        }

        .sticky-sidebar {
            position: sticky;
            top: 0;
        }

        @media screen and (min-width: 1024px) {
            .nft-card {
                padding: 1.5rem;
            }

            .nft-card img {
                height: 400px;
                object-fit: contain;
            }

            .main-content {
                padding: 2rem;
            }
        }

        @media screen and (max-width: 1023px) {
            .nft-card img {
                height: 250px;
            }
        }

        .full-page {
            height: 100vh;
            display: flex;
            flex-direction: column;
        }

        .nft-grid {
            flex: 1;
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 1rem;
            padding: 1rem;
            overflow-y: auto;
        }

        .nft-card {
            background-color: #2d3748;
            border-radius: 8px;
            padding: 1rem;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            color: #e2e8f0;
        }

        .nft-card h3 {
            margin-bottom: 0.5rem;
        }

        .nft-card p {
            font-size: 1rem;
            margin-bottom: 0.5rem;
        }
    </style>
</head>
<body class="bg-gray-900 text-gray-200">
    <div class="full-page flex flex-row">
        <!-- Sidebar -->
        <aside class="w-64 bg-gray-800 h-full p-4 sticky-sidebar sidebar hidden lg:block">
            <div class="flex items-center mb-6">
                <img alt="A sharply dressed, intense-looking male character" class="w-16 h-16 rounded-full" height="64" src="https://i.ibb.co/p30Q5fs/Leonardo-Kino-XL-A-sharplydressed-intenselooking-male-characte-3.jpg" width="64"/>
                <h2 class="ml-4 text-xl font-bold">Reimagine Truth</h2>
            </div>
            <nav>
                <ul>
                    <li class="mb-4">
                        <a class="text-lg text-gray-200 hover:text-white sidebar-item" href="#" onclick="scrollToStart()">Home</a>
                    </li>
                    <li class="mb-4">
                        <a class="text-lg text-gray-200 hover:text-white sidebar-item" href="#">My Assets</a>
                    </li>
                    <li class="mb-4">
                        <a class="text-lg text-gray-200 hover:text-white sidebar-item" href="#">About</a>
                    </li>
                    <li class="mb-4">
                        <a class="text-lg text-gray-200 hover:text-white sidebar-item" href="https://linktr.ee/reimagine_truth" target="_blank">Community</a>
                    </li>
                    <li class="mb-4">
                        <a class="text-lg text-gray-200 hover:text-white sidebar-item" href="#">Settings</a>
                    </li>
                </ul>
            </nav>
        </aside>

        <!-- Main Content -->
        <div class="flex-1 overflow-y-auto main-content bg-gray-900 text-gray-200">
            <!-- Header -->
            <header class="bg-gray-800 text-white p-4 flex flex-col items-center relative">
                <div class="flex justify-between items-center w-full">
                    <button class="lg:hidden text-white absolute top-4 left-4" id="menu-button">
                        <i class="fas fa-bars"></i>
                    </button>
                </div>
                <div class="flex flex-col items-center">
                    <img alt="Logo" class="w-36 mb-2 fade-in" src="https://i.ibb.co/p30Q5fs/Leonardo-Kino-XL-A-sharplydressed-intenselooking-male-characte-3.jpg" width="150"/>
                    <h1 class="text-4xl font-bold text-center fade-in">Welcome to Reimagine Truth</h1>
                    <p class="text-lg text-center fade-in">Explore the unique stories of our NFT characters.</p>
                </div>
            </header>

            <!-- Main Section -->
            <main class="flex-1">
                <!-- Search Bar -->
                <div class="flex justify-center mb-6">
                    <input type="text" id="search-bar" placeholder="Search your NFT serial number #" class="w-full max-w-md p-2 rounded bg-gray-700 text-white placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-blue-500">
                    <button class="ml-2 p-2 bg-blue-500 text-white rounded hover:bg-blue-600 focus:outline-none focus:ring-2 focus:ring-blue-500" onclick="searchNFT()">Search</button>
                </div>
                <div class="flex justify-center mb-6" id="view-all-container" style="display: none;">
                    <button class="p-2 bg-blue-500 text-white rounded hover:bg-blue-600 focus:outline-none focus:ring-2 focus:ring-blue-500" onclick="showAllNFTs()">View All</button>
                </div>

                <!-- NFT Grid -->
                <div class="nft-grid">
                    <!-- Card 1 -->
                    <div class="nft-card" data-serial="#1">
                        <img alt="NFT character with a futuristic look" src="https://i.ibb.co/1mJM8ns/Image-7.png">
                        <h3 class="text-xl font-bold">Truth Seeker #1</h3>
                        <p>Rarity: Common</p>
                        <a href="#" class="text-blue-400">View Details</a>
                    </div>

                    <!-- Card 2 -->
                    <div class="nft-card" data-serial="#2">
                        <img alt="NFT character with a mystical aura" src="https://i.ibb.co/zbjm89d/Image-4.png">
                        <h3 class="text-xl font-bold">Truth Seeker #2</h3>
                        <p>Rarity: Rare</p>
                        <a href="#" class="text-blue-400">View Details</a>
                    </div>

                    <!-- Card 3 -->
                    <div class="nft-card" data-serial="#3">
                        <img alt="NFT character with a cyberpunk style" src="https://i.ibb.co/z8F7HW5/Image-3.png">
                        <h3 class="text-xl font-bold">Truth Seeker #3</h3>
                        <p>Rarity: Ultra Rare</p>
                        <a href="#" class="text-blue-400">View Details</a>
                    </div>

                    <!-- Card 4 -->
                    <div class="nft-card" data-serial="#4">
                        <img alt="NFT character with a mystical aura" src="https://i.ibb.co/XXWGTy4/Image-5.png">
                        <h3 class="text-xl font-bold">Truth Seeker #4</h3>
                        <p>Rarity: Rare</p>
                        <a href="#" class="text-blue-400">View Details</a>
                    </div>
                </div>
            </main>

            <!-- Footer -->
            <footer class="bg-gray-800 text-white p-4 text-center">
                <p>© 2024 Reimagine Truth. All rights reserved.</p>
            </footer>
        </div>
    </div>

    <audio id="click-sound" src="https://www.soundjay.com/button/sounds/button-16.mp3" preload="auto"></audio>

    <script>
        // Optional JavaScript for interactive functionality (like search and sidebar toggle)
    </script>
</body>
</html>

