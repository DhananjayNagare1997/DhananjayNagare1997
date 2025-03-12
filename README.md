<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dhananjay Nagare - Data Analyst Portfolio</title>
  <style>
    /* Global Styles */
    body {
      font-family: 'Arial', sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f9f9f9;
      display: flex;
      flex-direction: column;
      align-items: center;
      animation: fadeIn 2s ease-in-out;
    }

    h1, h3 {
      margin: 0;
      font-family: 'Arial', sans-serif;
    }

    /* Header Section */
    .header {
      background-color: #1f77b4;
      color: white;
      width: 100%;
      padding: 60px 0;
      text-align: center;
      border-bottom: 3px solid #2a6496;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
      margin-bottom: 30px;
      animation: slideIn 1.5s ease-in-out;
    }

    .header h1 {
      font-size: 3em;
    }

    .header h3 {
      font-size: 1.4em;
      font-weight: 300;
    }

    /* Profile Info Container */
    .profile-info {
      width: 80%;
      max-width: 1100px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 40px;
      padding: 20px;
      background-color: white;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      animation: fadeIn 2s ease-in-out;
    }

    /* Profile Text */
    .profile-info div {
      max-width: 50%;
    }

    .profile-info p {
      font-size: 1.1em;
      line-height: 1.6em;
      color: #333;
    }

    /* Profile Image */
    .profile-info img {
      border-radius: 12px;
      width: 300px;
      height: auto;
      border: 4px solid #eaeaea;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease-in-out;
    }

    .profile-info img:hover {
      transform: scale(1.05);
    }

    /* Image Toggle Section */
    .image-container {
      margin: 20px 0;
      width: 100%;
      display: flex;
      justify-content: center;
      transition: opacity 1s ease-in-out;
    }

    img {
      width: 100%;
      max-width: 800px; /* Increased the image size */
      border-radius: 10px;
    }

    /* Loading Spinner */
    .loading {
      font-size: 24px;
      font-weight: bold;
      color: #1f77b4;
      display: none;
      margin-top: 20px;
    }

    /* GitHub Stats Section */
    .github-stats {
      display: flex;
      justify-content: center;
      align-items: center;
      margin-top: 40px;
      gap: 20px;
    }

    .github-stats img {
      max-width: 400px;
      border-radius: 10px;
    }

    /* Button Styling */
    .load-button {
      background-color: #1f77b4;
      color: white;
      padding: 15px 30px;
      font-size: 18px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.3s ease;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }

    .load-button:hover {
      background-color: #145a8d;
      transform: translateY(-2px);
    }

    /* Animation */
    @keyframes fadeIn {
      0% {
        opacity: 0;
      }
      100% {
        opacity: 1;
      }
    }

    @keyframes slideIn {
      0% {
        transform: translateX(-100%);
      }
      100% {
        transform: translateX(0);
      }
    }

  </style>
</head>
<body>

  <!-- Header Section with Name & Job Profile -->
  <div class="header">
    <h1>Dhananjay Nagare</h1>
    <h3>Data Analyst | Python | MySQL & SSMS Expert | ETL Enthusiast</h3>
  </div>

  <!-- Profile Info Section -->
  <div class="profile-info">
    <div>
      <p>🌱 I’m currently learning <strong>ETL</strong></p>
      <p>💬 Ask me about <strong>Data Analysis, MySQL, ETL, Python, SSMS</strong></p>
      <p>📫 How to reach me: <a href="mailto:nagaredhananjay5004@gmail.com">nagaredhananjay5004@gmail.com</a></p>
      <p>📄 Know about my experiences: 
        <a href="https://github.com/DhananjayNagare1997/Certifications/blob/main/Dhananjay%20Nagarer%20ML%20%26%20Data%20Analyst.pdf" target="_blank">Resume</a>
      </p>
    </div>

    <!-- Image Toggle Section -->
    <div class="image-container">
      <img id="toggleImage" src="https://www.scnsoft.com/blog-pictures/business-intelligence/real-time-big-data-analytics-02_1.png" alt="Toggle Image">
    </div>
  </div>

  <!-- Button to Load Stats -->
  <button class="load-button" id="loadButton">Load GitHub Stats</button>

  <!-- Loading Spinner -->
  <div class="loading" id="loadingMessage">Fetching data...</div>

  <!-- GitHub Stats Section -->
  <div class="github-stats" id="githubStats" style="display: none;">
    <div>
      <img align="left" src="https://github-readme-stats.vercel.app/api/top-langs?username=dhananjaynagare1997&show_icons=true&locale=en&layout=compact" alt="Top Languages">
      <img align="center" src="https://github-readme-stats.vercel.app/api?username=dhananjaynagare1997&show_icons=true&locale=en" alt="GitHub Stats">
      <img align="center" src="https://github-readme-streak-stats.herokuapp.com/?user=dhananjaynagare1997&" alt="GitHub Streak">
    </div>
  </div>

  <script>
    // Handle the button click to load GitHub stats
    document.getElementById("loadButton").addEventListener("click", function() {
      // Show the loading message
      document.getElementById("loadingMessage").style.display = "block";
      document.getElementById("githubStats").style.display = "none";

      // Simulate a delay of 2 seconds to fetch GitHub stats
      setTimeout(function() {
        document.getElementById("loadingMessage").style.display = "none";
        document.getElementById("githubStats").style.display = "block";
      }, 2000);
    });

    // Function to toggle the images every 5 seconds
    const images = [
      "https://www.scnsoft.com/blog-pictures/business-intelligence/real-time-big-data-analytics-02_1.png",
      "https://thumbs.dreamstime.com/b/use-realtime-data-feeds-commentators-can-provide-indepth-analysis-breakdowns-replays-giving-viewers-closer-look-319052761.jpg"
    ];
    let currentImageIndex = 0;

    function toggleImage() {
      currentImageIndex = (currentImageIndex + 1) % images.length;
      document.getElementById("toggleImage").src = images[currentImageIndex];
    }

    setInterval(toggleImage, 5000); // Change image every 5 seconds
  </script>

</body>
</html>
