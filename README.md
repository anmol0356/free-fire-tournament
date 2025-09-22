<!ANMOL>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Free Fire Tournament Registration</title>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: 'Orbitron', sans-serif;
      background: linear-gradient(135deg, #1a1a1a, #ff4444);
      color: #fff;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }
    .hero {
      background-image: url('https://via.placeholder.com/1200x400?text=Free+Fire+Tournament'); /* Replace with Free Fire image URL */
      background-size: cover;
      background-position: center;
      padding: 40px;
      text-align: center;
      box-shadow: inset 0 0 50px rgba(0, 0, 0, 0.8);
    }
    .hero h1 {
      font-size: 3em;
      text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.7);
    }
    .hero p {
      font-size: 1.2em;
      margin-top: 10px;
    }
    main {
      max-width: 800px;
      margin: 20px auto;
      padding: 30px;
      background: rgba(0, 0, 0, 0.85);
      border-radius: 15px;
      box-shadow: 0 0 20px rgba(255, 68, 68, 0.7);
    }
    form {
      display: flex;
      flex-direction: column;
      gap: 15px;
    }
    label {
      font-size: 1.1em;
      color: #ff4444;
    }
    input, select, textarea {
      padding: 12px;
      border: 2px solid #ff4444;
      border-radius: 8px;
      background: #222;
      color: #fff;
      font-size: 1em;
      transition: border-color 0.3s, transform 0.2s;
    }
    input:focus, select:focus, textarea:focus {
      outline: none;
      border-color: #ff9900;
      transform: scale(1.02);
    }
    .team-section {
      display: none;
      flex-direction: column;
      gap: 15px;
      padding: 15px;
      background: #333;
      border-radius: 8px;
    }
    .team-section.active {
      display: flex;
    }
    .team-member {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      gap: 10px;
      padding: 10px;
      border-bottom: 1px solid #ff4444;
    }
    .team-member label {
      font-size: 1em;
    }
    button {
      padding: 15px;
      background: linear-gradient(45deg, #ff4444, #ff9900);
      color: #fff;
      border: none;
      border-radius: 8px;
      font-size: 1.2em;
      cursor: pointer;
      transition: transform 0.2s, box-shadow 0.2s;
    }
    button:hover {
      transform: scale(1.05);
      box-shadow: 0 0 15px rgba(255, 153, 0, 0.7);
    }
    footer {
      margin-top: auto;
      text-align: center;
      padding: 15px;
      background: #000;
      color: #ff4444;
      font-size: 0.9em;
      opacity: 0.8;
    }
    @media (max-width: 600px) {
      .hero h1 {
        font-size: 2em;
      }
      main {
        margin: 10px;
        padding: 20px;
      }
      .team-member {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>
  <div class="hero">
    <h1>🔥 Free Fire Battle Royale 2025 🔥</h1>
    <p>Join the ultimate showdown! Register now and claim victory!</p>
  </div>
  
  <main>
    <form id="registrationForm" onsubmit="handleSubmit(event)">
      <label for="fullName">Full Name:</label>
      <input type="text" id="fullName" name="fullName" placeholder="Enter your full name" required>

      <label for="email">Email Address:</label>
      <input type="email" id="email" name="email" placeholder="Enter your email" required>

      <label for="playerId">Your Free Fire UID:</label>
      <input type="text" id="playerId" name="playerId" placeholder="Enter your Free Fire UID" required>

      <label for="teamName">Team Name (if applicable):</label>
      <input type="text" id="teamName" name="teamName" placeholder="Enter team name">

      <label>
        <input type="checkbox" id="isTeam" name="isTeam" onchange="toggleTeamSection()"> Registering as a Team
      </label>

      <div id="teamSection" class="team-section">
        <div class="team-member">
          <div>
            <label for="member1Name">Member 1 Name:</label>
            <input type="text" id="member1Name" name="member1Name" placeholder="Full name">
          </div>
          <div>
            <label for="member1InGame">Member 1 In-Game Name:</label>
            <input type="text" id="member1InGame" name="member1InGame" placeholder="In-game name">
          </div>
          <div>
            <label for="member1Uid">Member 1 UID:</label>
            <input type="text" id="member1Uid" name="member1Uid" placeholder="Free Fire UID">
          </div>
        </div>
        <div class="team-member">
          <div>
            <label for="member2Name">Member 2 Name:</label>
            <input type="text" id="member2Name" name="member2Name" placeholder="Full name">
          </div>
          <div>
            <label for="member2InGame">Member 2 In-Game Name:</label>
            <input type="text" id="member2InGame" name="member2InGame" placeholder="In-game name">
          </div>
          <div>
            <label for="member2Uid">Member 2 UID:</label>
            <input type="text" id="member2Uid" name="member2Uid" placeholder="Free Fire UID">
          </div>
        </div>
        <div class="team-member">
          <div>
            <label for="member3Name">Member 3 Name:</label>
            <input type="text" id="member3Name" name="member3Name" placeholder="Full name">
          </div>
          <div>
            <label for="member3InGame">Member 3 In-Game Name:</label>
            <input type="text" id="member3InGame" name="member3InGame" placeholder="In-game name">
          </div>
          <div>
            <label for="member3Uid">Member 3 UID:</label>
            <input type="text" id="member3Uid" name="member3Uid" placeholder="Free Fire UID">
          </div>
        </div>
        <div class="team-member">
          <div>
            <label for="member4Name">Member 4 Name:</label>
            <input type="text" id="member4Name" name="member4Name" placeholder="Full name">
          </div>
          <div>
            <label for="member4InGame">Member 4 In-Game Name:</label>
            <input type="text" id="member4InGame" name="member4InGame" placeholder="In-game name">
          </div>
          <div>
            <label for="member4Uid">Member 4 UID:</label>
            <input type="text" id="member4Uid" name="member4Uid" placeholder="Free Fire UID">
          </div>
        </div>
      </div>

      <label for="phone">Phone Number:</label>
      <input type="tel" id="phone" name="phone" placeholder="Enter your phone number" required>

      <label for="discord">Discord Username (for updates):</label>
      <input type="text" id="discord" name="discord" placeholder="Enter Discord username">

      <label>
        <input type="checkbox" id="terms" name="terms" required> I agree to the tournament rules and terms
      </label>

      <button type="submit">Register Now!</button>
    </form>
  </main>
  
  <footer>
    &copy; 2025 Free Fire Tournament | Watermark: rajput_anmolsingh3
  </footer>

  <!-- EmailJS Integration -->
  <script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@4/dist/email.min.js"></script>
  <script>
    // Initialize EmailJS
    emailjs.init({ publicKey: "blxqzhVgoaA55BAua" });

    function toggleTeamSection() {
        const teamSection = document.getElementById('teamSection');
        const isTeam = document.getElementById('isTeam').checked;
        teamSection.classList.toggle('active', isTeam);
    }

    function handleSubmit(event) {
        event.preventDefault();

        // Send form data via EmailJS
        emailjs.sendForm("service_6pqc98c", "template_5a15jyd", event.target)
          .then(() => {
            alert("✅ Registration submitted successfully! We’ll contact you soon.");
            event.target.reset();
            document.getElementById('teamSection').classList.remove('active');
            document.getElementById('isTeam').checked = false;
          })
          .catch((error) => {
            console.error("❌ Error:", error);
            alert("Failed to submit registration. Please try again.");
          });
    }
  </script>
</body>
</html>
