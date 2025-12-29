<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Nova Beats Album</title>

  <style>
    /* Reset + Base */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: "Segoe UI", Arial, sans-serif;
    }

    body {
      min-height: 100vh;
      background: radial-gradient(circle at top, #1db954 0%, #0f2027 45%, #000 100%);
      background-repeat: no-repeat;
      background-attachment: fixed;
      background-size: cover;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 20px;
      color: #fff;
    }

    /* Album Layout */
    .album-wrapper {
      width: 100%;
      max-width: 1200px;
      padding: 30px;
      display: flex;
      gap: 40px;
      align-items: flex-start;
      flex-wrap: wrap;
    }

    /* Album Info Card */
    .album {
      width: 100%;
      max-width: 400px;
      height: auto;
      background: rgba(0, 0, 0, 0.55);
      border-radius: 26px;
      padding: 30px;
      text-align: center;
      border: 2px solid rgba(255, 255, 255, 0.25);
      box-shadow: 0 25px 70px rgba(0, 0, 0, 0.7);
      animation: albumReveal 1.4s ease forwards;
    }

    .cover {
      width: 220px;
      height: 200px;
      margin: 0 auto 20px;
      border-radius: 20px;
      background: linear-gradient(135deg, #ff512f, #dd2476);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 30px;
      font-weight: bold;
      letter-spacing: 3px;
    }

    .album h2 {
      font-size: clamp(22px, 4vw, 30px);
      margin-bottom: 6px;
    }

    .album p {
      opacity: 0.85;
      margin-bottom: 14px;
    }

    .badge {
      display: inline-block;
      padding: 10px 28px;
      border-radius: 40px;
      background: #1db954;
      color: #000;
      font-weight: bold;
      letter-spacing: 1px;
      animation: pulse 1.5s infinite;
    }

    /* Tracklist Section */
    .tracks {
      flex: 1;
      min-width: 280px;
    }

    .tracks h1 {
      font-size: clamp(32px, 6vw, 60px);
      letter-spacing: 4px;
      margin-bottom: 6px;
    }

    .tracks span {
      font-size: 16px;
      opacity: 0.85;
    }

    .tracklist {
      margin-top: 40px;
      display: flex;
      flex-direction: column;
      gap: 18px;
      width: 100%;
    }

    input {
      display: none;
    }

    .track {
      padding: 18px 24px;
      border-radius: 18px;
      background: rgba(255, 255, 255, 0.12);
      border: 2px solid rgba(255, 255, 255, 0.3);
      cursor: pointer;
      display: flex;
      justify-content: space-between;
      align-items: center;
      transition: 0.4s;
      animation: trackReveal 0.8s forwards;
    }

    .track:hover {
      background: #1db954;
      color: #000;
    }

    input:checked + label {
      background: #ffd700;
      color: #000;
      font-weight: bold;
    }

    audio {
      width: 100%;
      margin-top: 10px;
      display: none;
    }

    input:checked + label + audio {
      display: block;
    }

    /* Artist Info */
    .artist {
      margin-top: 40px;
      padding: 25px;
      border-radius: 24px;
      background: rgba(0, 0, 0, 0.35);
    }

    .artist h3 {
      font-size: clamp(20px, 4vw, 26px);
      margin-bottom: 10px;
    }

    .artist p {
      opacity: 0.85;
    }

    /* Animations */
    @keyframes albumReveal {
      from { transform: scale(0.9); }
      to { transform: scale(1); }
    }

    @keyframes trackReveal {
      from { opacity: 0; transform: translateX(40px); }
      to { opacity: 1; transform: translateX(0); }
    }

    @keyframes pulse {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.1); }
    }

    /* Responsive */
    @media (max-width: 768px) {
      .album-wrapper {
        justify-content: center;
        text-align: center;
      }

      .track {
        flex-direction: column;
        gap: 8px;
      }
    }

    @media (max-width: 480px) {
      .cover {
        width: 180px;
        height: 170px;
      }

      .album {
        padding: 20px;
      }
    }
  </style>
</head>

<body>

  <div class="album-wrapper">

    <!-- Left Side Album Info -->
    <div class="album">
      <div class="cover">NOVA</div>
      <h2>Nova Beats</h2>
      <p>Electronic / Indie Pop</p>
      <div class="badge">Now Streaming</div>
    </div>

    <!-- Right Side Tracks -->
    <div class="tracks">
      <h1>ALBUM LAUNCH</h1>
      <span>Click a track to play</span>

      <div class="tracklist">

        <input type="radio" name="song" id="t1">
        <label for="t1" class="track">
          <strong>01. First Song</strong>
          <small>3:45</small>
        </label>
        <audio controls>
          <source src="song1.mp3">
        </audio>

        <input type="radio" name="song" id="t2">
        <label for="t2" class="track">
          <strong>02. Second Song</strong>
          <small>3:45</small>
        </label>
        <audio controls>
          <source src="song2.mp3">
        </audio>

        <input type="radio" name="song" id="t3">
        <label for="t3" class="track">
          <strong>03. Third Song</strong>
          <small>3:45</small>
        </label>
        <audio controls>
          <source src="song3.mp3">
        </audio>

        <input type="radio" name="song" id="t4">
        <label for="t4" class="track">
          <strong>04. Fourth Song</strong>
          <small>3:45</small>
        </label>
        <audio controls>
          <source src="song4.mp3">
        </audio>

      </div>

      <div class="artist">
        <h3>About the Artist</h3>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat consectetur voluptate sapiente laudantium molestiae inventore cum in nulla maiores dolor.
        </p>
      </div>

    </div>
  </div>

</body>
</html>
