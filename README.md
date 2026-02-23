# EduApplySA-
Secondary schools online application 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Junior Tsiu Portfolio</title>
<style>
:root {
  --bg-dark: #1e1e2f;
  --bg-light: #f0f4f8;
  --card-dark: #2a2a3b;
  --card-light: #fff;
  --text-dark: #eee;
  --text-light: #333;
  --primary: #4facfe;
  --primary-hover: #007BFF;
}

/* Body */
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: var(--bg-dark);
  color: var(--text-dark);
  scroll-behavior: smooth;
}
body.light-mode { background: var(--bg-light); color: var(--text-light); }

/* Navigation */
nav {
  display: flex;
  justify-content: space-around;
  background: var(--card-dark);
  padding: 10px;
  position: sticky;
  top: 0;
  z-index: 100;
}
body.light-mode nav { background: var(--card-light); }
nav a { color: inherit; text-decoration: none; font-weight: bold; padding: 5px 10px; transition: color 0.3s; }
nav a:hover { color: var(--primary); }

/* Containers */
.container {
  max-width: 600px;
  margin: 30px auto;
  padding: 20px;
  background: var(--card-dark);
  border-radius: 15px;
  text-align: center;
  transition: all 0.5s ease;
}
body.light-mode .container { background: var(--card-light); }

img.profile {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  object-fit: cover;
  border: 4px solid var(--primary);
  margin-bottom: 15px;
  animation: float 3s ease-in-out infinite;
}
@keyframes float {
  0% { transform: translateY(0px); }
  50% { transform: translateY(-8px); }
  100% { transform: translateY(0px); }
}

button {
  padding: 12px 20px;
  background: var(--primary);
  color: green;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  margin: 5px;
  transition: background 0.3s, transform 0.2s;
}
button:hover { background: var(--primary-hover); transform: scale(1.05); }

#projects .project-card {
  background: #3a3a4a;
  border-radius: 12px;
  padding: 15px;
  margin: 15px 0;
  text-align: left;
  transition: transform 0.3s, box-shadow 0.3s;
}
body.light-mode #projects .project-card { background: #f5f5f5; }
#projects .project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 20px rgba(0,0,0,0.2);
}

.social-icons a { margin: 0 10px; font-size: 24px; text-decoration: none; color: inherit; }
.social-icons a:hover { color: var(--primary); }

/* Modal */
#modal-overlay {
  position: fixed;
  top:0; left:0; right:0; bottom:0;
  background: rgba(0,0,0,0.7);
  display: none;
  justify-content: center;
  align-items: center;
  z-index: 1000;
  overflow-y: auto;
}
#modal-overlay.show { display: flex; }
#modal {
  width: 95%;
  max-width: 800px;
  background: var(--card-dark);
  border-radius: 15px;
  overflow: hidden;
  position: relative;
  padding: 20px;
}
body.light-mode #modal { background: var(--card-light); }
#modal-close {
  position: absolute;
  top: 10px;
  right: 10px;
  background: #dc3545;
  color: white;
  border: none;
  border-radius: 5px;
  padding: 8px 12px;
  cursor: pointer;
}
#modal-close:hover { background: #a71d2a; }

/* EduApplySA embedded */
#eduapply-container {
  text-align: left;
  max-height: 80vh;
  overflow-y: auto;
  padding: 10px;
  background: #22222f;
  color: #eee;
  border-radius: 12px;
}
body.light-mode #eduapply-container { background: #f5f5f5; color: #333; }
#eduapply-container h2 { text-align: center; margin-top: 0; }
#eduapply-container label { display: block; margin-top: 10px; }
#eduapply-container input, #eduapply-container textarea { width: 100%; margin-top: 5px; padding: 8px; border-radius: 5px; border: 1px solid #ccc; }
#eduapply-container button { width: 100%; margin-top: 15px; }
.final-summary { background: #333; padding: 10px; border-radius: 8px; color: #eee; margin-top: 15px; }
body.light-mode .final-summary { background: #eee; color: #333; }

@media (max-width: 600px){
  .container { margin: 20px 10px; }
}
</style>
</head>
<body>

<!-- NAVIGATION -->
<nav>
  <a href="#about">About</a>
  <a href="#projects">Projects</a>
  <a href="#contact">Contact</a>
  <button id="toggle-mode">Dark/Light</button>
</nav>

<!-- ABOUT ME -->
<div class="container" id="about">
  <img src="https://i.imgur.com/6VBx3io.png" alt="Profile" class="profile">
  <h1>Junior Tsiu</h1>
 
</div>

<!-- PROJECTS -->
<div class="container" id="projects">
  <h2>My Projects</h2>

  <div class="project-card">
    <h3>Portfolio Page</h3>
    <p>My personal portfolio page showcasing projects and skills.</p>
    <button>View Project</button>
  </div>

  <div class="project-card">
    <h3>Interactive Game</h3>
    <p>A simple JavaScript-based game for fun and learning.</p>
    <button>View Project</button>
  </div>

  <div class="project-card">
    <h3>EduApplySA</h3>
    <p>Local school application portal project. Full form and school selection demo.</p>
    <button id="open-eduapply">View Project</button>
  </div>
</div>

<!-- CONTACT -->
<div class="container" id="contact">
  <h2>Contact Me</h2>
  <p>Email: <a href="mailto:junior@example.com">junior@example.com</a></p>
  <p>Phone: +27 600 000 000</p>
  <div class="social-icons">
    <a href="#" target="_blank">🐱 GitHub</a>
    <a href="#" target="_blank">🔗 LinkedIn</a>
    <a href="#" target="_blank">🐦 Twitter</a>
  </div>
</div>

<!-- MODAL -->
<div id="modal-overlay">
  <div id="modal">
    <button id="modal-close">Close</button>

    <!-- EDUAPPLYSA EMBEDDED -->
    <div id="eduapply-container">
      <h2>EduApplySA - School Portal</h2>

      <!-- School selection -->
      <p>Select a school to apply:</p>
      <div>
        <button class="select-school" data-school="Leratong Secondary School">Leratong Secondary School</button>
        <button class="select-school" data-school="Ntemoseng Secondary School">Ntemoseng Secondary School</button>
        <button class="select-school" data-school="Lenyora la Thuto technical school">Lenyora la Thuto technical school</button>
      </div>

      <!-- Application Form -->
      <div id="eduapply-form" style="display:none; margin-top:20px;">
        <h3 id="school-name"></h3>
        <form id="app-form">
          <label>Full Name:</label>
          <input type="text" id="student-name" required>

          <label>Email:</label>
          <input type="email" id="student-email" required>

          <label>Guardian Phone:</label>
          <input type="tel" id="guardian-phone" required>

          <label>Current School:</label>
          <input type="text" id="current-school" required>

          <label>Grade Applying For:</label>
          <input type="text" id="grade" required>

          <label>Residential Address:</label>
          <input type="text" id="address-line1" placeholder="Street/House" required>
          <input type="text" id="address-line2" placeholder="Suburb" required>
          <input type="text" id="address-line3" placeholder="City/Postal Code" required>

          <label>ID Copy of Parent:</label>
          <input type="file" id="id-file" required>

          <label>Proof of Address:</label>
          <input type="file" id="proof-file" required>

          <label>Third Term Report:</label>
          <input type="file" id="learner-file" required>

          <button type="submit">Submit Application</button>
        </form>
        <div class="final-summary" id="final-summary"></div>
      </div>
    </div>
  </div>
</div>

<script>
// Dark/Light Mode
document.getElementById("toggle-mode").addEventListener("click", ()=>{
  document.body.classList.toggle("light-mode");
});

// Modal
const modalOverlay = document.getElementById("modal-overlay");
document.getElementById("open-eduapply").addEventListener("click", ()=> modalOverlay.classList.add("show"));
document.getElementById("modal-close").addEventListener("click", ()=> modalOverlay.classList.remove("show"));

// EduApplySA
let selectedSchool = "";
document.querySelectorAll(".select-school").forEach(btn=>{
  btn.addEventListener("click", ()=>{
    selectedSchool = btn.dataset.school;
    document.getElementById("eduapply-form").style.display = "block";
    document.getElementById("school-name").textContent = `Application Form - ${selectedSchool}`;
    document.getElementById("final-summary").innerHTML = "";
  });
});

// Handle Form Submission
document.getElementById("app-form").addEventListener("submit", function(e){
  e.preventDefault();
  const name = document.getElementById('student-name').value.trim();
  const email = document.getElementById('student-email').value.trim();
  const guardian = document.getElementById('guardian-phone').value.trim();
  const currentSchool = document.getElementById('current-school').value.trim();
  const grade = document.getElementById('grade').value.trim();
  const address1 = document.getElementById('address-line1').value.trim();
  const address2 = document.getElementById('address-line2').value.trim();
  const address3 = document.getElementById('address-line3').value.trim();
  const idFile = document.getElementById('id-file').files[0]?.name || 'No file';
  const proofFile = document.getElementById('proof-file').files[0]?.name || 'No file';
  const learnerFile = document.getElementById('learner-file').files[0]?.name || 'No file';
  const refNum = 'REF' + Math.floor(Math.random()*10000);

  document.getElementById('final-summary').innerHTML = `
    <p><strong>Reference Number:</strong> ${refNum}</p>
    <p><strong>School:</strong> ${selectedSchool}</p>
    <p><strong>Name:</strong> ${name}</p>
    <p><strong>Email:</strong> ${email}</p>
    <p><strong>Guardian Phone:</strong> ${guardian}</p>
    <p><strong>Current School:</strong> ${currentSchool}</p>
    <p><strong>Grade Applying For:</strong> ${grade}</p>
    <p><strong>Residential Address:</strong><br>${address1}<br>${address2}<br>${address3}</p>
    <p><strong>ID File:</strong> ${idFile}</p>
    <p><strong>Proof of Address:</strong> ${proofFile}</p>
    <p><strong>Third Term Report:</strong> ${learnerFile}</p>
  `;
});
</script>

</body>
</html>
