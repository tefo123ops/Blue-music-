# Blue-music-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Blue Music</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: #e0f2fe;
      color: #000;
    }

    header {
      position: sticky;
      top: 0;
      background-color: #1e3a8a;
      color: white;
      padding: 15px 10px;
      text-align: center;
      z-index: 999;
    }

    nav {
      display: flex;
      justify-content: center;
      gap: 20px;
      background-color: #111;
      padding: 10px;
    }

    nav a {
      color: white;
      text-decoration: none;
      font-weight: bold;
      transition: color 0.3s;
    }

    nav a:hover {
      color: #60a5fa;
    }

    .section {
      padding: 20px;
    }

    h2 {
      border-left: 5px solid #1e3a8a;
      padding-left: 10px;
      margin-bottom: 15px;
    }

    .search-box {
      margin: 20px 0;
      text-align: center;
    }

    .search-box input {
      padding: 10px;
      width: 80%;
      max-width: 400px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    .music-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 15px;
    }

    .music-card {
      background: white;
      border-left: 5px solid black;
      border-radius: 8px;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
      padding: 15px;
      transition: transform 0.3s ease, background 0.3s ease;
    }

    .music-card:hover {
      transform: scale(1.02);
      background: #bae6fd;
    }

    .music-title {
      font-size: 1.2rem;
      font-weight: bold;
    }

    .release-time {
      color: #555;
      font-size: 0.9rem;
    }

    .download-btn {
      margin-top: 10px;
      background: #000;
      color: #fff;
      border: none;
      padding: 8px 12px;
      border-radius: 5px;
      cursor: pointer;
      transition: background 0.3s;
    }

    .download-btn:hover {
      background: #1e3a8a;
    }

    footer {
      text-align: center;
      padding: 20px;
      background: #1e3a8a;
      color: white;
      margin-top: 40px;
    }
  </style>
</head>
<body>

<header>
  Blue Music
</header>

<nav>
  <a href="#home">Home</a>
  <a href="#latest">New Releases</a>
  <a href="#artists">Artists</a>
</nav>

<div class="section" id="home">
  <h2>Search Music</h2>
  <div class="search-box">
    <input type="text" id="searchInput" onkeyup="filterMusic()" placeholder="Search by artist, title, or type...">
  </div>
</div>

<div class="section" id="latest">
  <h2>New Releases</h2>
  <div class="music-grid" id="musicList">

    <div class="music-card" data-type="album" data-title="Dreams" data-artist="Artist A">
      <div class="music-title">Artist A - Album "Dreams"</div>
      <div class="release-time">Released: May 3, 2025</div>
      <button class="download-btn" onclick="downloadSong('dreams.zip')">Download Album</button>
    </div>

    <div class="music-card" data-type="ep" data-title="Night Vibes" data-artist="Artist B">
      <div class="music-title">Artist B - EP "Night Vibes"</div>
      <div class="release-time">Released: May 1, 2025</div>
      <button class="download-btn" onclick="downloadSong('night-vibes.zip')">Download EP</button>
    </div>

    <div class="music-card" data-type="single" data-title="Sky High" data-artist="Artist C">
      <div class="music-title">Artist C - Single "Sky High"</div>
      <div class="release-time">Released: April 28, 2025</div>
      <button class="download-btn" onclick="downloadSong('sky-high.mp3')">Download Song</button>
    </div>

  </div>
</div>

<div class="section" id="artists">
  <h2>Featured Artists</h2>
  <ul>
    <li>Artist A – Known for smooth vocals</li>
    <li>Artist B – EP king of Botswana vibes</li>
    <li>Artist C – Trending with “Sky High”</li>
  </ul>
</div>

<footer>
  &copy; 2025 Blue Music. All rights reserved.
</footer>

<script>
  function downloadSong(fileName) {
    alert("Starting download: " + fileName);
    // window.location.href = "music/" + fileName; // Uncomment to use real links
  }

  function filterMusic() {
    const input = document.getElementById("searchInput").value.toLowerCase();
    const cards = document.querySelectorAll(".music-card");

    cards.forEach(card => {
      const title = card.getAttribute("data-title").toLowerCase();
      const artist = card.getAttribute("data-artist").toLowerCase();
      const type = card.getAttribute("data-type").toLowerCase();

      if (title.includes(input) || artist.includes(input) || type.includes(input)) {
        card.style.display = "block";
      } else {
        card.style.display = "none";
      }
    });
  }
</script>

</body>
</html>
