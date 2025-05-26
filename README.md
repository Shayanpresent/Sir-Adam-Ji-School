<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Sir Adam Ji School</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(to bottom right, #004d00, #ffffcc);
      margin: 0;
      padding: 0;
    }
    header {
      background-color: #004d00;
      color: white;
      padding: 1rem;
      text-align: center;
    }
    h1 {
      margin: 0;
    }
    nav {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 1rem;
      margin: 1rem 0;
    }
    button.subject {
      padding: 0.5rem 1rem;
      background-color: #006600;
      color: white;
      border: none;
      cursor: pointer;
      border-radius: 5px;
    }
    .gallery {
      display: none;
      flex-wrap: wrap;
      justify-content: center;
      gap: 1rem;
      padding: 1rem;
    }
    .gallery img {
      max-width: 300px;
      border-radius: 8px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2);
    }
    .popup {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.7);
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 9999;
    }
    .popup-content {
      background-color: white;
      padding: 2rem;
      text-align: center;
      border-radius: 8px;
    }
    .popup-content button {
      margin-top: 1rem;
      background-color: #cc0000;
      color: white;
      padding: 0.5rem 1rem;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    footer {
      background-color: #003300;
      color: white;
      text-align: center;
      padding: 1rem;
      margin-top: 2rem;
    }
  </style>
</head>
<body>
  <header>
    <h1>Welcome to Sir Adam Ji School</h1>
    <p>Learn. Grow. Succeed.</p>
  </header>

  <div id="popup" class="popup">
    <div class="popup-content">
      <h2>Subscribe to our YouTube Channel!</h2>
      <p>Support our educational mission by subscribing to ShayanPresent96.</p>
      <button onclick="hidePopup()">Subscribe Now</button>
    </div>
  </div>

  <nav>
    <button class="subject" onclick="showGallery('computer')">Computer</button>
    <button class="subject" onclick="showGallery('math')">Math</button>
    <button class="subject" onclick="showGallery('urdu')">Urdu</button>
    <button class="subject" onclick="showGallery('islamiat')">Islamiat</button>
    <button class="subject" onclick="showGallery('physics')">Physics</button>
    <button class="subject" onclick="showGallery('chemistry')">Chemistry</button>
    <button class="subject" onclick="showGallery('english')">English</button>
    <button class="subject" onclick="showGallery('pst')">PST</button>
  </nav>

  <div id="gallery" class="gallery"></div>

  <footer>
    <p>Developed by ShayanPresent96 — All rights reserved © 2025</p>
  </footer>

  <script>
    const gallery = document.getElementById('gallery');

    function showGallery(subject) {
      gallery.innerHTML = '';
      for (let i = 1; i <= 5; i++) {
        const img = document.createElement('img');
        img.src = `assets/images/${subject}/${i}.jpg`;
        img.alt = `${subject} page ${i}`;
        gallery.appendChild(img);
      }
      gallery.style.display = 'flex';
    }

    function hidePopup() {
      const popup = document.getElementById('popup');
      popup.style.display = 'none';
      window.open("https://youtube.com/@shayanpresent96?sub_confirmation=1", "_blank");
    }
  </script>
</body>
</html>
