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
  </style>
</head>
<body>

<audio id="bgMusic" loop>
  <source src="https://www.bensound.com/bensound-music/bensound-ukulele.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>

<h1>💌 Hey sweetie, let's play a fun quiz!<br>How well do you know me?</h1>

<form id="quizForm">

  <div class="slide active">
    <strong>🌤 But before we start... how are you today?</strong><br>
    <label><input type="radio" name="mood" value="good"> 😊 I'm good</label>
    <label><input type="radio" name="mood" value="not_good"> 🙁 Not so good</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>1. What month was I born?</strong><br>
    <label><input type="radio" name="q0" value="february"> ❄️ February</label>
    <label><input type="radio" name="q0" value="december"> 🎄 December</label>
    <label><input type="radio" name="q0" value="june"> ☀️ June</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>2. What's my favorite color?</strong><br>
    <label><input type="radio" name="q00" value="blue"> 💙 Blue</label>
    <label><input type="radio" name="q00" value="pink"> 💖 Pink</label>
    <label><input type="radio" name="q00" value="yellow"> 💛 Yellow</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>3. What food do I love the most?</strong><br>
    <label><input type="radio" name="q1" value="pizza"> 🍕 Pizza</label>
    <label><input type="radio" name="q1" value="noodles"> 🍜 Instant Noodles</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>4. What do I prefer on weekends?</strong><br>
    <label><input type="radio" name="q2" value="sleep"> 🛏 Sleep all day</label>
    <label><input type="radio" name="q2" value="walk"> 🏞 Go out for a walk</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>5. My favorite animal is:</strong><br>
    <label><input type="radio" name="q3" value="cat"> 🐱 Cat</label>
    <label><input type="radio" name="q3" value="dog"> 🐶 Dog</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>6. When I’m upset, I usually...</strong><br>
    <label><input type="radio" name="q4" value="music"> 🎧 Listen to music</label>
    <label><input type="radio" name="q4" value="sleep"> 💤 Sleep it off</label>
    <button type="button" onclick="showResult()">See Result</button>
  </div>

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
  <textarea id="messageText" rows="5" placeholder="Write your message here..."></textarea><br>
  <button onclick="sendMessage()">Send via WhatsApp</button>
</div>

<script>
  let currentSlide = 0;
  const slides = document.querySelectorAll(".slide");

  function nextSlide() {
    if (currentSlide === 0) {
      const bgMusic = document.getElementById("bgMusic");
      bgMusic.volume = 0.3;
      bgMusic.play().catch(e => console.log("Autoplay failed:", e));
    }
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
    let moodMessage = "";
    if (mood) {
      moodMessage = mood.value === "good"
        ? "Yay! I'm so glad you're feeling good today! 😊"
        : "Hope this quiz helped cheer you up a little! 💛";
    } else {
      moodMessage = "You didn’t answer how you’re feeling... but I hope you’re okay~";
    }

    let message = "";
    if (score === 6) message = "6/6! You totally know me! 💯✨";
    else if (score >= 4) message = score + "/6! You know me pretty well! 🤗";
    else message = score + "/6! We need more cozy chats! ☕";

    document.getElementById("moodResult").textContent = moodMessage;
    document.getElementById("scoreResult").textContent = message;

    document.getElementById("resultBox").style.display = "block";
    document.getElementById("messageBox").style.display = "block";
  }

  function sendMessage() {
    const text = document.getElementById("messageText").value;
    const phone = '085369261133'; // Nomor WhatsApp baru
    const encodedText = encodeURIComponent(text);
    const waUrl = `https://wa.me/${phone}?text=${encodedText}`;
    window.open(waUrl, '_blank');
  }
</script>

</body>
</html>
