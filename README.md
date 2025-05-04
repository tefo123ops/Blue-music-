<div class="music-card" data-platforms='{"spotify":"uri123","youtube":"vid456"}'>
       <h3>Song Title</h3>
       <p>Artist Name</p>
       <div class="platform-links">
           <a href="#" class="spotify-link" onclick="openInSpotify('uri123')">
               <img src="spotify-icon.png" alt="Play on Spotify">
           </a>
           <a href="#" class="youtube-link" onclick="openInYoutube('vid456')">
               <img src="youtube-icon.png" alt="Watch on YouTube">
           </a>
       </div>
   </div>

   <script>
   function openInSpotify(uri) {
       window.open(`https://open.spotify.com/track/${uri}`, '_blank');
   }
   
   function openInYoutube(videoId) {
       window.open(`https://youtube.com/watch?v=${videoId}`, '_blank');
   }
   </script># Blue-music-
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
<div class="attribution">
       <p>All music links direct to official platforms. We don't host any content.</p>
       <p>© Respective copyright holders. Fair use for discovery purposes.</p>
   </div>
   <div class="music-card" data-platforms='{"spotify":"uri123","youtube":"vid456"}'>
       <h3>Song Title</h3>
       <p>Artist Name</p>
       <div class="platform-links">
           <a href="#" class="spotify-link" onclick="openInSpotify('uri123')">
               <img src="spotify-icon.png" alt="Play on Spotify">
           </a>
           <a href="#" class="youtube-link" onclick="openInYoutube('vid456')">
               <img src="youtube-icon.png" alt="Watch on YouTube">
           </a>
       </div>
   </div>

   <script>
   function openInSpotify(uri) {
       window.open(`https://open.spotify.com/track/${uri}`, '_blank');
   }
   
   function openInYoutube(videoId) {
       window.open(`https://youtube.com/watch?v=${videoId}`, '_blank');
   }
   </script>
   // Fetch new releases from multiple APIs
   async function getNewReleases() {
       const [spotifyReleases, appleReleases] = await Promise.all([
           fetchSpotifyReleases(),
           fetchAppleMusicReleases()
       ]);
       return combineResults(spotifyReleases, appleReleases);
   }
   async function searchSpotify(query) {
    const response = await fetch(`https://api.spotify.com/v1/search?q=${query}&type=track`, {
        headers: {
            'Authorization': 'Bearer YOUR_ACCESS_TOKEN'
        }
    });
    const data = await response.json();
    return data.tracks.items;
}
<div class="music-results">
    <!-- Example result card -->
    <div class="track-card" data-id="spotify:track:123" data-platforms='{"spotify":"123","youtube":"abc"}'>
        <img src="album_cover.jpg" class="album-art">
        <div class="track-info">
            <h3>Song Name</h3>
            <p>Artist Name</p>
            <div class="platform-buttons">
                <button onclick="playOnSpotify('123')">▶️ Spotify</button>
                <button onclick="watchOnYouTube('abc')">▶️ YouTube</button>
            </div>
        </div>
    </div>
</div>
async function fetchTrendingVideos() {
    const response = await fetch(`https://www.googleapis.com/youtube/v3/search?part=snippet&q=official+music+video&type=video&key=YOUR_API_KEY`);
    const data = await response.json();
    return data.items;
}
{
    "name": "My Mixed Playlist",
    "tracks": [
        {
            "title": "Blinding Lights",
            "artist": "The Weeknd",
            "links": {
                "spotify": "spotify:track:0VjIjW4GlUZAMYd2vXMi3b",
                "youtube": "https://youtu.be/4NRXx6U8ABQ"
            }
        }
    ]
{
    "name": "My Mixed Playlist",
    "tracks": [
        {
            "title": "Blinding Lights",
            "artist": "The Weeknd",
            "links": {
                "spotify": "spotify:track:0VjIjW4GlUZAMYd2vXMi3b",
                "youtube": "https://youtu.be/4NRXx6U8ABQ"
            }
        }
    ]
}
<footer>
      <p>This site does not host or distribute music. All links direct to official platforms.</p>
      <p>© 2025 YourSite. All rights reserved.</p>
  </footer>
<header>
    <div class="brand">
        <img src="logo.png" alt="Blue Music Logo" class="logo">
        <h1>Blue Music</h1>
    </div>
    <!-- Navigation or search bar can go here -->
</header>
.brand {
    display: flex;
    align-items: center;
    gap: 10px;
    padding: 15px;
    background: linear-gradient(90deg, #1e3a8a, #3b82f6);
}

.logo {
    width: 40px;
    height: 40px;
}

.brand h1 {
    color: white;
    font-weight: 700;
    margin: 0;
    font-size: 1.5rem;
}
<head>
    <title>Blue Music</title>
    <link rel="icon" href="favicon.ico" type="image/x-icon">
</head>
<!DOCTYPE html>
<html>
<head>
    <title>Blue Music</title>
    <style>
        .brand-bar {
            background: #1e3a8a;
            color: white;
            padding: 15px;
            text-align: center;
            font-size: 1.5rem;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="brand-bar">🎵 Blue Music</div>
    <!-- Rest of your music player code -->
</body>
</html>
<div class="logo">
  <span class="blue">BLUE</span><span class="music">MUSIC</span>
</div>

<style>
.logo {
  font-family: 'Montserrat', sans-serif;
  font-weight: 800;
  font-size: 2.5rem;
  letter-spacing: -1px;
}
.blue { color: #2563eb; }
.music { color: #1e40af; }
</style>
<div class="logo">
  <svg class="logo-icon" viewBox="0 0 24 24" width="32" height="32">
    <path fill="#3b82f6" d="M12 3v10.55c-.59-.34-1.27-.55-2-.55-2.21 0-4 1.79-4 4s1.79 4 4 4 4-1.79 4-4V7h4V3h-6z"/>
  </svg>
  <span class="logo-text">Blue Music</span>
</div>

<style>
.logo {
  display: flex;
  align-items: center;
  gap: 10px;
}
.logo-text {
  font-family: 'Poppins', sans-serif;
  font-weight: 700;
  font-size: 1.8rem;
  color: #1e3a8a;
}
</style>
:root {
  /* Primary blues */
  --brand-dark: #1e3a8a;
  --brand-primary: #2563eb;
  --brand-light: #93c5fd;
  
  /* Accents */
  --accent-teal: #0d9488;
  --accent-purple: #7e22ce;
  
  /* Neutrals */
  --gray-dark: #1f2937;
  --gray-light: #f3f4f6;
}<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&family=Inter:wght@400;500&display=swap" rel="stylesheet">

<style>
body {
  font-family: 'Inter', sans-serif;
}
h1, h2, h3 {
  font-family: 'Poppins', sans-serif;
  font-weight: 700;
}
.brand-font {
  font-family: 'Poppins', sans-serif;
  font-weight: 600;
}
</style>
<header class="site-header">
  <div class="brand-container">
    <a href="/" class="brand-logo">
      <svg class="logo-icon" viewBox="0 0 24 24" width="32" height="32">
        <path fill="#3b82f6" d="M12 3v10.55c-.59-.34-1.27-.55-2-.55-2.21 0-4 1.79-4 4s1.79 4 4 4 4-1.79 4-4V7h4V3h-6z"/>
      </svg>
      <span class="logo-text">Blue Music</span>
    </a>
    <nav class="main-nav">
      <a href="/discover">Discover</a>
      <a href="/artists">Artists</a>
      <a href="/playlists">Playlists</a>
    </nav>
  </div>
</header>

<style>
.site-header {
  background: white;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
  position: sticky;
  top: 0;
  z-index: 100;
}

.brand-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 1rem 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.brand-logo {
  display: flex;
  align-items: center;
  gap: 12px;
  text-decoration: none;
}

.logo-text {
  font-family: 'Poppins', sans-serif;
  font-weight: 700;
  font-size: 1.5rem;
  color: var(--brand-dark);
  transition: color 0.2s;
}

.brand-logo:hover .logo-text {
  color: var(--brand-primary);
}

.main-nav {
  display: flex;
  gap: 2rem;
}

.main-nav a {
  text-decoration: none;
  color: var(--gray-dark);
  font-weight: 500;
  transition: color 0.2s;
}

.main-nav a:hover {
  color: var(--brand-primary);
}
</style>
<div class="download-options">
  <h3>Get This Song</h3>
  <div class="platform-buttons">
    <!-- Links to official purchase/download pages -->
    <a href="https://music.apple.com" class="download-btn apple">
      <i class="icon-apple"></i> Buy on Apple Music
    </a>
    <a href="https://www.amazon.com/music" class="download-btn amazon">
      <i class="icon-amazon"></i> Buy on Amazon Music
    </a>
    <a href="https://store.spotify.com" class="download-btn spotify">
      <i class="icon-spotify"></i> Spotify Premium
    </a>
  </div>
</div>

<style>
.download-options {
  background: #f8fafc;
  padding: 1.5rem;
  border-radius: 12px;
  margin: 2rem 0;
}

.download-btn {
  display: inline-flex;
  align-items: center;
  padding: 0.75rem 1.5rem;
  margin: 0.5rem;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 600;
  transition: transform 0.2s;
}

.download-btn:hover {
  transform: translateY(-2px);
}

.apple { background: #fa586a; color: white; }
.amazon { background: #FF9900; color: black; }
.spotify { background: #1DB954; color: white; }
</style>
<div class="legal-notice">
     <p>All downloads link to official sources. We do not host copyrighted content without permission.</p>
   </div>
   // Content verification system
   async function verifyUpload(file) {
     const response = await checkCopyrightDatabase(file);
     if (response.flagged) {
       alert("This content appears to be copyrighted. Please upload only original work.");
       return false;
     }
     return true;
   }
   a.download
   <div class="direct-download">
  <h4>Free Download (Artist Approved)</h4>
  <p>This track is provided directly by the artist for promotional use</p>
  <button onclick="downloadFile('song.mp3', 'artist-name_song-title')">
    <i class="icon-download"></i> Download MP3
  </button>
  <small>For personal use only</small>
</div>

<script>
function downloadFile(url, filename) {
  const a = document.createElement('a');
  a.href = url;
  a.download = filename;
  document.body.appendChild(a);
  a.click();
  document.body.removeChild(a);
}
</script>
