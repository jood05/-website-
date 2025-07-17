<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>المهندسة جود المومني</title>
  <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;700&display=swap" rel="stylesheet"/>

  <style>
    body {
      margin: 0;
      font-family: 'Tajawal', sans-serif;
      color: #333;
background: linear-gradient(135deg, #e5d4ed, #a65e5e, #890303);
 background-size: 400% 400%;
 animation: gradientMove 15s ease infinite;
    }
 @keyframes gradientMove {
   0% { background-position: 0% 50%; }
   50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
    }
    header {
      height: 100vh;
      background: url('https://images.pexels.com/photos/7953420/pexels-photo-7953420.jpeg') center/cover no-repeat;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      position: relative;
    }

    header::after {
      content: '';
      position: absolute;
      inset: 0;
      background: rgba(0, 0, 0, 0.4);
    }
    header h1 {
      font-size: 3rem;
      color: #fff;
      margin: 0;
      z-index: 1;
    }

    header .intro {
      text-align: center;
      z-index: 1;
    }
    header .intro h2,
    header .intro p {
      color: #fff;
      animation: fadeInUp 1s ease-out both;
    }

    header .intro button {
      padding: 12px 24px;
      margin-top: 20px;
      font-size: 1rem;
      border: none;
      border-radius: 4px;
      background: linear-gradient(45deg, #6c63ff, #42a5f5);
      color: #fff;
      cursor: pointer;
      transition: transform 0.3s;
    }
    header .intro button:hover {
      transform: scale(1.05);
    }
    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
    .section {
      padding: 80px 20px;
      text-align: center;
    }
    .section h2 {
      margin-bottom: 40px;
      font-size: 2rem;
      position: relative;
    }
    .section h2::after {
      content: '';
      width: 60px;
      height: 4px;
      background: #6c63ff;
      display: block;
      margin: 12px auto 0;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 20px;
      max-width: 800px;
      margin: auto;
    }

    .card {
      padding: 20px;
      background: #fff;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s, box-shadow 0.3s;
      opacity: 0;
    }

    .card.visible {
      opacity: 1;
      transition: opacity 0.6s ease-out, transform 0.3s;
    }
    .card:hover {
      transform: translateY(-8px);
      box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
    }

    footer {
      padding: 20px;
     background: linear-gradient(135deg, #890303, #a65e5e, #e5d4ed);
     background-size: 400% 400%;
  animation: gradientMove 15s ease infinite;
      color: #fff;
      text-align: center;
    }

    @media (max-width: 600px) {
      header h1 {
        font-size: 2rem;
      }

      header .intro h2 {
        font-size: 1.2rem;
      }

      .cards {
        grid-template-columns: 1fr;
      }

      #email p {
        font-size: 1rem;
      }
    }
  </style>
</head>
<body dir="rtl">

  <header id="hero">
    <nav>
      <h1>جود المومني</h1>
    </nav>
    <div class="intro">
      <p>مرحباً بكم في موقعي الشخصي</p>
      <button onclick="scrollToSection('skills')">مهاراتي</button>
    </div>
  </header>

  <section id="skills" class="section">
    <h2>مهاراتي</h2>
    <div class="cards">
      <div class="card">Python</div>
      <div class="card">++C</div>
      <div class="card">HTML </div>
      <div class="card">Databases</div>
    </div>
  </section>

  <section id="about" class="section">
    <h2>حول</h2>
    <p>طالبة علم بيانات و ذكاء اصطناعي في جامعة عجلون الوطنية، أهوى تطوير الحلول باستخدام أحدث التقنيات.</p>
  </section>

  <section id="projects" class="section">
    <h2>مشاريعي</h2>
    <div class="cards">
            <div class="card">
        <h3>موقع شخصي تفاعلي</h3>
        <p>مبني بـ HTML و CSS مع تأثيرات وانيميشن لإظهار المهارات.</p>
      </div>
    </div>
  </section>

  <section id="email" class="section">
    <h2>راسلني</h2>
    <p>البريد الإلكتروني: <a href="mailto:jood2005almomani@gmail.com">jood2005almomani@gmail.com</a></p>
  </section>

  <footer>
    <p>© 2025 جود المومني</p>
  </footer>

  <script>
    function scrollToSection(id) {
      document.getElementById(id).scrollIntoView({ behavior: 'smooth' });
    }

    document.addEventListener('DOMContentLoaded', () => {
      const cards = document.querySelectorAll('.card');

      const observer = new IntersectionObserver(entries => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.add('visible');
            observer.unobserve(entry.target);
          }
        });
      }, { threshold: 0.2 });

      cards.forEach(card => observer.observe(card));
    });
  </script>
</body>
</html>![Untitled Diagram drawio (1)](https://github.com/user-attachments/assets/86a335c9-d667-440f-8299-a252eac37f9c)
