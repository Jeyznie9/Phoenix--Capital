
     <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Phoenix Capital Limited</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f4;
      color: #333;
      line-height: 1.6;
    }

    .navbar {
      background-color: #2c3e50;
      padding: 10px 20px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
    }

    .logo {
      height: 50px;
    }

    .navbar ul {
      list-style: none;
      display: flex;
      gap: 20px;
    }

    .navbar ul li a {
      color: white;
      text-decoration: none;
      font-size: 16px;
      padding: 8px 12px;
      border-radius: 5px;
      transition: background 0.3s;
    }

    .navbar ul li a:hover {
      background-color: #34495e;
    }

    main {
      padding: 20px;
      max-width: 800px;
      margin: auto;
    }

    section { margin-bottom: 40px; }
    h1, h2 { color: #2c3e50; margin-bottom: 10px; }

    ul.services {
      list-style: square;
      margin-left: 20px;
    }

    a.whatsapp {
      display: inline-block;
      margin-top: 10px;
      padding: 10px 15px;
      background-color: #25D366;
      color: white;
      text-decoration: none;
      border-radius: 5px;
      font-weight: bold;
    }

    a.whatsapp:hover { background-color: #1ebd5a; }

    /* Loan Form Styling */
    #form form {
      background: white;
      padding: 20px;
      margin-top: 20px;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0,0,0,0.05);
      max-width: 500px;
      margin-left: auto;
      margin-right: auto;
    }

    #form label {
      display: block;
      margin-top: 15px;
    }

    #form input, #form select, #form textarea {
      width: 100%;
      padding: 8px;
      margin-top: 5px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    #form button {
      margin-top: 20px;
      background-color: #2c3e50;
      color: white;
      border: none;
      padding: 10px 15px;
      border-radius: 5px;
      cursor: pointer;
    }

    #form button:hover { background-color: #34495e; }

    footer {
      background-color: #2c3e50;
      color: white;
      text-align: center;
      padding: 15px 10px;
    }

    @media (max-width: 600px) {
      .navbar {
        flex-direction: column;
        align-items: center;
      }

      .navbar ul {
        flex-direction: column;
        gap: 10px;
        margin-top: 10px;
      }
    }
  </style>
</head>
<body>

  <header>
    <nav class="navbar">
      <img src="logo.png" alt="Phoenix Capital Logo" class="logo" />
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#services">Our Loans</a></li>
        <li><a href="#form">Apply</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section id="home">
      <h1>Welcome to Phoenix Capital Limited</h1>
      <p>Your trusted partner in financial solutions.</p>
    </section>

    <section id="services">
      <h2>Our Loan Services</h2>
      <ul class="services">
        <li>Logbook Loans</li>
        <li>Morti-Fix Loans</li>
        <li>Asset Financing for Vehicles</li>
        <li>Buy Off Loans</li>
      </ul>
    </section>

    <section id="form">
      <h2>Loan Application Form</h2>
      <form id="loanForm">
        <label for="fullName">Full Name:</label>
        <input type="text" id="fullName" name="fullName" required />

        <label for="phone">Phone Number:</label>
        <input type="tel" id="phone" name="phone" required />

        <label for="email">Email Address:</label>
        <input type="email" id="email" name="email" />

        <label for="loanType">Loan Type:</label>
        <select id="loanType" name="loanType">
          <option value="Logbook Loan">Logbook Loan</option>
          <option value="Morti-Fix Loan">Morti-Fix Loan</option>
          <option value="Asset Financing">Asset Financing</option>
          <option value="Buy Off Loan">Buy Off Loan</option>
        </select>

        <label for="amount">Loan Amount:</label>
        <input type="number" id="amount" name="amount" required />

        <label for="message">Additional Message:</label>
        <textarea id="message" name="message" rows="4"></textarea>

        <button type="submit">Send via WhatsApp</button>
      </form>
    </section>

    <section id="contact">
      <h2>Contact Us</h2>
      <p>Need help or want to apply for a loan? Reach us instantly on WhatsApp:</p>
      <a class="whatsapp" href="https://wa.me/254798251509" target="_blank">Message us on WhatsApp</a>
    </section>
  </main>

  <footer>
    <p>© 2025 Phoenix Capital Limited. All rights reserved.</p>
  </footer>

  <!-- WhatsApp Form Script -->
  <script>
    document.getElementById("loanForm").addEventListener("submit", function(event) {
      event.preventDefault();

      const fullName = document.getElementById("fullName").value;
      const phone = document.getElementById("phone").value;
      const email = document.getElementById("email").value;
      const loanType = document.getElementById("loanType").value;
      const amount = document.getElementById("amount").value;
      const message = document.getElementById("message").value;

      const whatsappMessage = `Loan Application:
Full Name: ${fullName}
Phone Number: ${phone}
Email: ${email}
Loan Type: ${loanType}
Loan Amount: KES ${amount}
Message: ${message}`;

      const encodedMessage = encodeURIComponent(whatsappMessage);
      const whatsappNumber = "254798251509"; // Replace with your number if needed
      const whatsappURL = `https://wa.me/${whatsappNumber}?text=${encodedMessage}`;

      window.open(whatsappURL, "_blank");
    });
  </script>

</body>
</html>
   
