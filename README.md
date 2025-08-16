<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>EventSphere | Event Management</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    html {
      scroll-behavior: smooth;
    }
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #83a4d4, #b6fbff);
      color: #222;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 60px 40px 80px;
      font-size: 1.1rem;
    }

    header {
      text-align: center;
      margin-bottom: 20px;
    }

    header h1 {
      font-size: 4.5rem;
      font-weight: 900;
      color: #073b4c;
      letter-spacing: 0.08em;
      margin-bottom: 10px;
      user-select: none;
    }

    header p {
      font-size: 1.3rem;
      font-weight: 600;
      color: #055a8c;
    }

    .contact-info {
      font-size: 1.1rem;
      color: #055a8c;
      margin-bottom: 40px;
    }

    .contact-info a {
      color: #118ab2;
      font-weight: 600;
      margin: 0 10px;
      text-decoration: none;
    }

    .contact-info a:hover {
      text-decoration: underline;
    }

    nav {
      display: flex;
      gap: 40px;
      margin-bottom: 60px;
      flex-wrap: wrap;
      justify-content: center;
    }

    nav button {
      background: #118ab2;
      border: none;
      color: white;
      font-weight: 700;
      font-size: 1.15rem;
      width: 160px;
      height: 160px;
      border-radius: 12px;
      cursor: pointer;
      box-shadow: 0 10px 18px rgba(17, 138, 178, 0.3);
      transition: background 0.3s, transform 0.2s, box-shadow 0.3s;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 20px;
    }

    nav button:hover {
      background: #06aed5;
      transform: translateY(-5px);
      box-shadow: 0 15px 25px rgba(6, 174, 213, 0.5);
    }

    #info-container {
      max-width: 1200px;
      width: 100%;
    }

    section {
      background: white;
      padding: 40px 50px;
      margin-bottom: 60px;
      border-radius: 15px;
      box-shadow: 0 12px 24px rgba(0, 0, 0, 0.12);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    section:hover {
      transform: translateY(-8px);
      box-shadow: 0 24px 36px rgba(0, 0, 0, 0.15);
    }

    h2 {
      color: #073b4c;
      margin-bottom: 20px;
      font-weight: 700;
      font-size: 2rem;
      border-bottom: 3px solid #118ab2;
      padding-bottom: 10px;
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 20px;
      justify-items: center;
    }

    .gallery-item {
      text-align: center;
    }

    .gallery img {
      width: 200px;
      height: 150px;
      border-radius: 12px;
      box-shadow: 0 6px 12px rgba(0,0,0,0.2);
    }

    .gallery p {
      margin-top: 8px;
      font-weight: bold;
      color: #055a8c;
    }

    form input, form textarea, form button {
      display: block;
      margin: 10px 0;
      padding: 12px;
      width: 100%;
      max-width: 500px;
      border: 1px solid #ccc;
      border-radius: 8px;
      font-size: 1rem;
    }

    form button {
      background: #ffb3b3;
      color: #fff;
      border: none;
      font-weight: bold;
      cursor: pointer;
      transition: 0.3s;
    }

    form button:hover {
      background: #06aed5;
    }

    .thank-you {
      font-size: 1.4rem;
      font-weight: bold;
      color: green;
      margin-top: 20px;
    }

    @media (max-width: 768px) {
      header h1 {
        font-size: 3rem;
      }

      nav button {
        width: 130px;
        height: 130px;
        font-size: 1rem;
      }

      section {
        padding: 30px 20px;
      }

      h2 {
        font-size: 1.6rem;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>EventSphere</h1>
    <p>Creating Memories That Last Forever</p>
    <div class="contact-info">
      <a href="mailto:manyamanya59893@gmail.com">manyamanya59893@gmail.com</a> | 
      <span>📞 6362991383</span> | 
      <span>📍 Bangalore - 56007</span>
    </div>
  </header>

  <nav>
    <button onclick="showSection('home')">Home</button>
    <button onclick="showSection('about')">About Us</button>
    <button onclick="showSection('gallery')">Gallery</button>
    <button onclick="showSection('contact')">Contact</button>
    <button onclick="showSection('book')">Book Events</button>
  </nav>

  <div id="info-container"></div>

  <script>
    const sectionsContent = {
      home: `
        <section>
          <h2>Welcome to EventSphere</h2>
          <p>
            We organize weddings, corporate functions, birthdays, concerts, and more.  
            Our mission is to craft unforgettable experiences and moments that you’ll cherish forever.
          </p>
        </section>
      `,
      about: `
        <section>
          <h2>About Us</h2>
          <p>
            At EventSphere, we believe every occasion deserves to be celebrated in style.  
            From intimate gatherings to grand celebrations, our experienced team ensures flawless execution.  
            Creativity, professionalism, and passion are at the heart of what we do.
          </p>
        </section>
      `,
      gallery: `
        <section>
          <h2>Our Gallery</h2>
          <div class="gallery">
            <div class="gallery-item">
              <img src="wedding.jpg" alt="Wedding">
              <p>Wedding Ceremony</p>
            </div>
            <div class="gallery-item">
              <img src="birthday.jpg" alt="Birthday">
              <p>Birthday Celebration</p>
            </div>
            <div class="gallery-item">
              <img src="corprote.jpg" alt="Corporate Event">
              <p>Corporate Event</p>
            </div>
            <div class="gallery-item">
              <img src="concert.jpg" alt="Concert">
              <p>Music Concert</p>
            </div>
           
            <div class="gallery-item">
              <img src="baby.jpg" alt="Baby Shower">
              <p>Baby Shower</p>
              </div>
            <div class="gallery-item">
              <img src="party.jpg" alt="Party">
              <p>Private Party</p>
            </div>
          </div>
        </section>
      `,
      contact: `
        <section>
          <h2>Contact Us</h2>
          <p><strong>Phone:</strong> 6362991383</p>
          <p><strong>Email:</strong> manyamanya59893@gmail.com</p>
          <p><strong>Address:</strong> Bangalore - 56007</p>
        </section>
      `,
      book: `
        <section>
          <h2>Book Your Event</h2>
          <form id="bookingForm" onsubmit="submitBooking(event)">
            <input type="text" placeholder="Your Name" required>
            <input type="email" placeholder="Your Email" required>
            <input type="text" placeholder="Event Type (Wedding, Birthday...)" required>
            <textarea placeholder="Additional Details"></textarea>
            <button type="submit">Book Now</button>
          </form>
          <p class="thank-you" id="thankYouMsg" style="display:none;">
            🎉 Thank you for booking with us! We will contact you soon.
          </p>
        </section>
      `
    };

    function showSection(sectionKey) {
      const container = document.getElementById('info-container');
      container.innerHTML = sectionsContent[sectionKey] || '';
      container.scrollIntoView({ behavior: 'smooth' });
    }

    function submitBooking(event) {
      event.preventDefault();
      document.getElementById("bookingForm").style.display = "none";
      document.getElementById("thankYouMsg").style.display = "block";
    }

    window.onload = () => {
      showSection('home'); // default section
    };
  </script>

</body>
</html>
