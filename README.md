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
    <label><input type="radio" name="q1" value="Rice"> 🍚 Rice</label>
    <label><input type="radio" name="q1" value="noodles"> 🍜 Instant Noodles</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>4. What do I prefer on weekends?</strong><br>
    <label><input type="radio" name="q2" value="sleep"> 🛏 Sleep all day</label>
    <label><input type="radio" name="q2" value="walk"> 🏞 Go out for a walk</label>
    <button type="<label><input ty
      value="Movie"> 🎬 Watching Movie</label>
    <button type="<label><input ty
onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>5. My favorite animal is:</strong><br>
    <label><input type="radio" name="q3" value="cat"> 🐱 Cat</label>
    <label><input type="radio" name="q3" value="dog"> 🐶 Dog</label>
    <label><input type="radio" name="q3" value="Fisch"> 🐳 Fisch</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>6. What's my favorite Hobby?</strong><br>
    <label><input type="radio" name="q1" value="Reading"> 📖 Reading</label>
    <label><input type="radio" name="q1" value="Gaming"> 🎮 Gaming</label>
    <label><input type="radio" name="q1" value="Singing"> 🎤 Singing</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

 <div class="slide">
    <strong>7. Which genre movie do i love?</strong><br>
    <label><input type="radio" name="q1" value="Horror"> 👻 Horror</label>
    <label><input type="radio" name="q1" value="Comedy"> 😂 Comedy</label>
    <label><input type="radio" name="q1" value="Romance"> 🧑‍❤️‍💋‍🧑 Romance</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>8. What's my favorite season of the year ? </strong><strong><br>
    <label><input type="radio" name="q1" value="Summer"> ☀️ Summer</label>
    <label><input type="radio" name="q1" value="Winter"> ❄️ Winter</label>
    <label><input type="radio" name="q1" value="Spring"> 🌸 Spring</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>9. Which anime do i love the most?</strong><br>
    <label><input type="radio" name="q1" value="Naruto"> 🍥 Naruto</label>
    <label><input type="radio" name="q1" value="Violet Evergarden"> 💃 Violet Evergarden</label>
    <label><input type="radio" name="q1" value="One Piece"> 🏴‍☠️ One Piece</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>10. If i ware an animal,which one would i be ?</strong><br>
    <label><input type="radio" name="q1" value="Turtle"> 🐢 Turtle(slow but steady)</label>
    <label><input type="radio" name="q1" value="Monkey"> 🐒 Monkey(chaotic anergy)</label>
    <label><input type="radio" name="q1" value="Unicorn"> 🦄 Unicorn(magicsl und dramatic)</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>11. What supperpower would suit me best ?</strong><br>
    <label><input type="radio" name="q1" value="Sleep"> 😴 Sleep anywhere</label>
    <label><input type="radio" name="q1" value="Teleport"> 🛸 Teleport</label>
    <label><input type="radio" name="q1" value="Invisible"> 🫥 Invisible</label>
    <button type="button" onclick="nextSlide()">Next</button>
  </div>

  <div class="slide">
    <strong>12. When I’m upset, I usually...</strong><br>
    <label><input type="radio" name="q4" value="music"> 🎧 Listen to music
    <button type="<label><input ty
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
  <textarea rows="5" placeholder="Write your message here..."></textarea><br>
  <button onclick="alert('Your message has been sent. Thank you!')">Send</button>
</div>

<script>
  let currentSlide = 0;
  const slides = document.querySelectorAll(".slide");

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
      q4: "Gaming",
      q5: "Comedy",
      q6: "Summer",
      q7: "Naruto",
      q8: "Monkey",
      q9: "Teleport",
      q10: "sleep"
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
</script>

</body>
</html>
