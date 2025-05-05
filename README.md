<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Hey Sweetie - Fun Quiz</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(to bottom right, #cce3f0, #fef6ff);
      color: #333;
      padding: 20px;
      max-width: 600px;
      margin: auto;
    }
    .slide {
      display: none;
      background-color: #ffffffcc;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.05);
    }
    .slide.active {
      display: block;
    }
    h1, h2 {
      text-align: center;
      color: #4d6faf;
    }
    label {
      display: block;
      margin-top: 10px;
    }
    button {
      margin-top: 20px;
      background-color: #4d6faf;
      color: white;
      border: none;
      padding: 10px 15px;
      border-radius: 5px;
      cursor: pointer;
      font-weight: 600;
    }
    button:hover {
      background-color: #3d5e99;
    }
    .result, .message-box {
      display: none;
      background-color: #f0f9ff;
      padding: 20px;
      border-radius: 10px;
      margin-top: 20px;
    }
    textarea {
      width: 100%;
      font-family: 'Poppins', sans-serif;
      font-size: 14px;
      padding: 8px;
      border-radius: 5px;
      border: 1px solid #ccc;
    }
    #musicControl {
      position: fixed;
      top: 10px;
      right: 10px;
      background: #fff;
      border: 1px solid #ccc;
      border-radius: 30px;
      padding: 5px 15px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      font-size: 14px;
    }
  </style>
</head>
<body>

<h1>💌 Hey sweetie, let's play a fun quiz!<br>How well do you know me?</h1>

<!-- Audio Backsound -->
<audio id="bgMusic" autoplay loop>
  <source src="https://www.bensound.com/bensound-music/bensound-littleidea.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>
<button id="musicControl" onclick="toggleMusic()">Pause Music</button>

<form id="quizForm">
  <!-- Slides here (unchanged from previous version)... -->
  <!-- Hanya bagian JavaScript dan backsound yang ditambahkan -->
</form>

<div class="result" id="resultBox">
  <h2>✨ Your Quiz Result ✨</h2>
  <p id="moodResult"></p>
  <p id="scoreResult"></p>
  <p><strong>I just wanna say: keep going today, tomorrow, and every day!</strong><br>
  Don’t forget: you’re amazing, smart, beautiful, and… I love u! ❤️🌈</p>
</div>

<div class="message-box" id="messageBox">
  <h3>📩 Send Me a Message!</h3>
  <textarea rows="5" placeholder="Write your message here..."></textarea><br>
  <button onclick="alert('Your message has been sent. Thank you!')">Send</button>
</div>

<script>
  let currentSlide = 0;
  const slides = document.querySelectorAll(".slide");
  const bgMusic = document.getElementById("bgMusic");
  const musicControl = document.getElementById("musicControl");

  function nextSlide() {
    slides[currentSlide].classList.remove("active");
    currentSlide++;
    slides[currentSlide].classList.add("active");
  }

  function showResult() {
    slides[currentSlide].classList.remove("active");

    const answers = {
      q0: "february",
      q00: "blue",
      q1: "noodles",
      q2: "sleep",
      q3: "cat",
      q4: "music"
    };

    let score = 0;
    for (let key in answers) {
      const selected = document.querySelector(`input[name="${key}"]:checked`);
      if (selected && selected.value === answers[key]) {
        score++;
      }
    }

    let mood = document.querySelector('input[name="mood"]:checked');
    let moodMessage = mood
      ? (mood.value === "good"
          ? "Yay! I'm so glad you're feeling good today! 😊"
          : "Hope this quiz helped cheer you up a little! 💛")
      : "You didn’t answer how you’re feeling... but I hope you’re okay~";

    let message = score === 6
      ? "6/6! You totally know me! 💯✨"
      : score >= 4
        ? score + "/6! You know me pretty well! 🤗"
        : score + "/6! We need more cozy chats! ☕";

    document.getElementById("moodResult").textContent = moodMessage;
    document.getElementById("scoreResult").textContent = message;

    document.getElementById("resultBox").style.display = "block";
    document.getElementById("messageBox").style.display = "block";
  }

  function toggleMusic() {
    if (bgMusic.paused) {
      bgMusic.play();
      musicControl.innerText = "Pause Music";
    } else {
      bgMusic.pause();
      musicControl.innerText = "Play Music";
    }
  }
</script>

</body>
</html>
