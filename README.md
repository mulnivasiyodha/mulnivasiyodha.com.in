<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
 <!-- Primary Meta Tags -->
<title>Mulnivasi Yodha | Official Page</title>
<meta name="title" content="Mulnivasi Yodha | Official Page">
<meta name="description" content="Official website of Mulnivasi Yodha. Stay updated with the latest news, awareness campaigns, and community initiatives for social justice and equality.">

<!-- Canonical -->
<link rel="canonical" href="https://mulnivasiyodha.github.io/mulnivasiyodha.com.in/">

<!-- Open Graph / Facebook -->
<meta property="og:type" content="website">
<meta property="og:url" content="https://mulnivasiyodha.github.io/mulnivasiyodha.com.in/">
<meta property="og:title" content="Mulnivasi Yodha | Official Page">
<meta property="og:description" content="Official website of Mulnivasi Yodha. Stay updated with the latest news, awareness campaigns, and community initiatives.">
<meta property="og:image" content="https://mulnivasiyodha.github.io/mulnivasiyodha.com.in/images/banner.jpg"> <!-- Change to your actual banner URL -->

<!-- Twitter -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:url" content="https://mulnivasiyodha.github.io/mulnivasiyodha.com.in/">
<meta name="twitter:title" content="Mulnivasi Yodha | Official Page">
<meta name="twitter:description" content="Latest updates and initiatives from Mulnivasi Yodha. Connect with the community.">
<meta name="twitter:image" content="https://mulnivasiyodha.github.io/mulnivasiyodha.com.in/images/banner.jpg">

<!-- Optional: Favicon -->
<link rel="icon" href="/favicon.ico" type="image/x-icon">
  <meta name="description" content="Mulnivasi Yodha is a community-driven platform promoting social justice, awareness, and unity among India's indigenous and marginalized communities. Follow us for updates, news, and initiatives.">
  
  <title>Mulnivasi Yodha AJAX Page</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #111 0%, #222 80%);
      color: #f0f0f0;
      overflow-x: hidden;
    }

    #warrior-container {
      position: relative;
      max-width: 400px;
      margin: 60px auto;
      perspective: 1000px;
      box-shadow:
        0 4px 8px rgba(0, 0, 0, 0.3),
        0 12px 20px rgba(0, 0, 0, 0.4);
      border-radius: 16px;
      transition: box-shadow 0.3s ease;
    }

    #warrior-container:hover {
      box-shadow:
        0 6px 16px rgba(255, 140, 0, 0.6),
        0 14px 40px rgba(255, 140, 0, 0.5);
    }

    #warrior {
      width: 100%;
      display: block;
      filter:
        drop-shadow(0 25px 25px rgba(0, 0, 0, 0.35))
        drop-shadow(inset 0 0 6px rgba(255, 140, 0, 0.2));
      border-radius: 16px;
      transition: transform 0.3s ease, filter 0.3s ease, box-shadow 0.3s ease;
      transform-style: preserve-3d;
      cursor: pointer;
      animation: float 3s ease-in-out infinite;
    }

    #warrior-container:hover #warrior {
      transform: rotateY(10deg) rotateX(6deg) scale(1.04);
      filter:
        drop-shadow(0 35px 40px rgba(255, 140, 0, 0.7));
      box-shadow: 0 0 12px 3px rgba(255, 140, 0, 0.6);
    }

    @keyframes float {
      0% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
      100% { transform: translateY(0); }
    }

    #sword-button {
      position: absolute;
      bottom: 280px;
      right: 200px;
      width: 50px;
      height: 50px;
      cursor: pointer;
      background: rgba(255, 255, 255, 0);
      z-index: 10;
      transition: box-shadow 0.3s ease;
    }

    #sword-button:hover {
      box-shadow: 0 0 12px 4px rgba(59, 89, 152, 0.8);
    }

    /* Glassmorphism effect on about section */
    .about-container {
      background: rgba(255, 255, 255, 0.05);
      backdrop-filter: blur(10px);
      -webkit-backdrop-filter: blur(10px);
      border-radius: 16px;
      box-shadow: 0 8px 32px rgba(255, 140, 0, 0.2);
      padding: 25px;
      margin: 30px auto 60px auto;
      color: #ffd580;
      font-weight: 500;
      line-height: 1.6;
      max-width: 600px;
      text-align: center;
      transition: box-shadow 0.3s ease, color 0.3s ease;
    }

    .about-container:hover {
      box-shadow: 0 12px 48px rgba(255, 140, 0, 0.5);
      color: #fff3cc;
    }
  </style>
</head>
<body>

  <!-- Warrior Image and Hidden Sword Button -->
  <div id="warrior-container">
    <img
      id="warrior"
      src="https://i.ibb.co/4R1sM3J2/World-king-ashoka-chakravarti-samrat-ashoka-mourya-emperor-of-asea-photo-edit-by-mulnivasi-yodha.png"
      alt="Warrior"
    />
    <div id="sword-button" title="Click sword to open Facebook page"></div>
  </div>

  <!-- Display About Info with AJAX -->
  <div class="about-container" id="about-info">Loading...</div>

  <!-- Facebook Button Script -->
  <script>
    // Function to fetch About info dynamically using AJAX
    function fetchInfo() {
      fetch("info.php")
        .then(response => response.json())
        .then(data => {
          document.getElementById("about-info").innerHTML = data.content;
        })
        .catch(error => {
          console.error("Error fetching data:", error);
        });
    }

    // Load data when the page is ready
    document.addEventListener("DOMContentLoaded", fetchInfo);

    // Facebook Button Interaction
    const swordBtn = document.getElementById('sword-button');
    swordBtn.addEventListener('click', () => {
      window.open("https://www.facebook.com/mulnivasiyodha.com.in", "_blank");
    });
  </script>

</body>
</html>
