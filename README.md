
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Krishna Chetan Portfolio</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
  <style>
  body {
  margin: 0;
  padding-top: 60px;  
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background: linear-gradient(to right, #0f2027, #203a43, #2c5364);
  color: #fff;
}

   nav {
  background: #111;
  padding: 10px;
  position: fixed;   
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000;
  display: flex;
  justify-content: center;
}

    nav a {
      color: #fff;
      margin: 0 15px;
      text-decoration: none;
      font-weight: bold;
      position: relative;
    }
    nav a:hover {
      color: #00e676;
    }
    header {
      text-align: center;
      padding: 50px 20px;
      background-image: url('https://www.transparenttextures.com/patterns/stardust.png');
      background-size: cover;
      background-position: center;
    }
    header h1 {
      font-size: 3rem;
    }
    header p {
      font-size: 1.2rem;
    }
    .profile-image {
      width: 120px;
      height: 120px;
      border-radius: 50%;
      object-fit: cover;
      margin-top: 20px;
      border: 4px solid #00e676;
      box-shadow: 0 4px 20px rgba(0, 255, 136, 0.3);
      transition: transform 0.3s ease;
    }
    .profile-image:hover {
      transform: scale(1.1);
    }
    .channel-image {
      width: 100px;
      height: 100px;
      border-radius: 50%;
      object-fit: cover;
      margin-top: 10px;
      border: 3px solid #ff0000;
      box-shadow: 0 4px 20px rgba(255, 0, 0, 0.3);
      transition: transform 0.3s ease;
    }
    .channel-image:hover {
      transform: scale(1.1);
    }
    section {
      padding: 40px 20px;
      max-width: 1000px;
      margin: auto;
    }
    .card {
      background: #222;
      padding: 20px;
      margin: 20px 0;
      border-radius: 10px;
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .card:hover {
      transform: translateY(-5px);
      box-shadow: 0 12px 25px rgba(0, 255, 136, 0.5);
    }
    .social-icons a {
      margin: 0 10px;
      color: #fff;
      font-size: 1.5rem;
    }
    .social-icons a:hover {
      color: #00e676;
    }
    .edu-card {
      background: #333;
      border-left: 5px solid #00e676;
      margin: 15px 0;
      padding: 15px;
      border-radius: 8px;
      transition: transform 0.3s, background 0.3s;
    }
    .edu-card:hover {
      transform: translateX(5px);
      background: #3a3a3a;
    }
    .edu-card h3 {
      margin: 0 0 10px;
      color: #00e676;
    }
    .edu-card p {
      margin: 5px 0;
    }
    .stars {
      margin-top: 10px;
    }
    .stars i {
      color: gold;
      font-size: 1.2rem;
    }
    .award-card {
      background: linear-gradient(145deg, #1c1c1c, #2c2c2c);
      border-left: 5px solid #00e676;
      margin: 15px 0;
      padding: 15px 20px;
      border-radius: 10px;
      box-shadow: 0 5px 15px rgba(0, 255, 136, 0.2);
      transition: transform 0.3s ease;
    }
    .award-card:hover {
      transform: scale(1.02);
      background: #2a2a2a;
    }
    .award-card h3 {
      margin: 0 0 8px;
      color: #00e676;
    }
    .award-card p {
      margin: 0;
    }
    footer {
      background: #111;
      color: #ccc;
      text-align: center;
      padding: 20px;
      font-size: 0.9rem;
    }
    input, textarea {
      width: 100%;
      padding: 10px;
      margin: 8px 0;
      border: none;
      border-radius: 5px;
    }
    input[type="submit"] {
      background-color: #00e676;
      color: #000;
      font-weight: bold;
      cursor: pointer;
    }
    input[type="submit"]:hover {
      background-color: #00c765;
    }
    .success-message {
      display: none;
      background-color: #d4edda;
      color: #155724;
      padding: 10px;
      margin-top: 10px;
      border-radius: 5px;
      border: 1px solid #c3e6cb;
    }
  </style>
</head>
<body>
    <nav>
    <a href="#about">About</a>
    <a href="#education">Education</a>
    <a href="#awards">Achievements</a>
    <a href="#youtube">YouTube</a>
    <a href="#contact">Contact</a>
  </nav>

  <header>
    <img src="chetan-photo-new.jpg" alt="Krishna Chetan" class="profile-image">
    <h1>Krishna Chetan Paidimarri</h1>
    <p>ICT Student | Developer | Content Creator</p>
    <img src="https://yt3.ggpht.com/U-bb7zeG8MWXBo-4Qv30idLscgiSNGBgd2tS2NHhwNlD2ZJTix9PczKz0SvYAJp5g4ndh4Pj=s600-c-k-c0x00ffffff-no-rj-rp-mo" alt="Sastra Vibes" class="channel-image">
    <div class="social-icons">
      <a href="https://www.linkedin.com/in/paidimarri-krishna-chetan" target="_blank"><i class="fab fa-linkedin"></i></a>
      <a href="https://www.youtube.com/@sastravibes" target="_blank"><i class="fab fa-youtube"></i></a>
      <a href="https://www.instagram.com/paidimarri_krishna_chetan" target="_blank"><i class="fab fa-instagram"></i></a>
      <a href="https://github.com/chetan2007-k" target="_blank"><i class="fab fa-github"></i></a>
    </div>
  </header>

<section id="about">
    <div class="card">
      <h2>About Me</h2>
      <p>Hello! I am Krishna Chetan, a passionate ICT student at SASTRA University. I love exploring new technologies, creating web solutions, and sharing knowledge through my YouTube channel 'Sastra Vibes'.</p>
    </div>
  </section>

  <section id="education">
    <div class="card">
      <h2>Education</h2>
      <div class="edu-card">
        <h3>SASTRA University, Thanjavur</h3>
        <p><strong>Degree:</strong> B.Tech in Information and Communication Technology (2024 – 2028)</p>
        <p><strong>CGPA SEM 1:</strong> 8.84</p>
        <p><strong>Skills:</strong> C, C++</p>
      </div>
      <div class="edu-card">
        <h3>Jaggaiahpet Residential College (JRC)</h3>
        <p><strong>Course:</strong> Intermediate, MPC (2022 – 2024)</p>
        <p><strong>Grade:</strong> 98.4%</p>
      </div>
      <div class="edu-card">
        <h3>CHEGU VIDYALAYAM EM HIGH SCHOOL</h3>
        <p><strong>SSC</strong> – March 2022</p>
        <p><strong>Grade:</strong> 95.83%</p>
      </div>
    </div>
  </section>

  <section id="awards">
    <div class="card">
      <h2>Achievements and Awards</h2>
      <div class="award-card">
        <h3>Bharati Airtel Scholarship</h3>
        <p>Awarded for outstanding academic performance and leadership potential.</p>
      </div>
      <div class="award-card">
        <h3>Social Wellbeing Committee</h3>
        <p>Selected as a member to promote mental wellness and community engagement.</p>
      </div>
      <div class="award-card">
        <h3>Top Performer in Projects</h3>
        <p>Recognized for excellence in multiple technical and creative projects.</p>
      </div>
    </div>
  </section>

  <section id="youtube">
    <div class="card">
      <h2>YouTube Channel</h2>
      <img src="https://yt3.ggpht.com/U-bb7zeG8MWXBo-4Qv30idLscgiSNGBgd2tS2NHhwNlD2ZJTix9PczKz0SvYAJp5g4ndh4Pj=s600-c-k-c0x00ffffff-no-rj-rp-mo" alt="YouTube Channel" class="channel-image">
      <p>Channel: <a href="https://www.youtube.com/@sastravibes" target="_blank">Sastra Vibes</a></p>
      <iframe width="100%" height="315" src="https://www.youtube.com/embed/NAuExe3UKGQ" frameborder="0" allowfullscreen></iframe>
      <p>Subscribers: 382</p>
      <div class="stars">
        <i class="fas fa-star"></i>
        <i class="fas fa-star"></i>
        <i class="fas fa-star"></i>
        <i class="fas fa-star"></i>
        <i class="fas fa-star-half-alt"></i>
      </div>
    </div>
  </section>

  <section id="contact">
    <div class="card">
      <h2>Contact Me</h2>
      <form action="https://formsubmit.co/128014029@sastra.ac.in" method="POST" onsubmit="showMessage()">
        <input type="hidden" name="_captcha" value="false">
        <input type="hidden" name="_next" value="https://thankyou-page-link.com">

        <label for="name">Name:</label>
        <input type="text" id="name" name="name" required>

        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>

        <label for="message">Message:</label>
        <textarea id="message" name="message" rows="5" required></textarea>

        <input type="submit" value="Send Message">
      </form>
      <div class="success-message" id="successMessage">
        Thank you! Your message has been sent.
      </div>
    </div>
  </section>

  <footer>
    <p>&copy; 2025 Krishna Chetan Paidimarri. All rights reserved.</p>
  </footer>

  <script>
    function showMessage() {
      document.getElementById('successMessage').style.display = 'block';
    }
  </script>
</body>
</html>
