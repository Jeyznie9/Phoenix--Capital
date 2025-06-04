<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Phoenix Capital Limited</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      background: #f9f9f9;
      color: #333;
    }

    /* Hide old logo */
    .logo {
      display: none;
    }

    /* Header */
    header.site-header {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 250px;
      background: linear-gradient(135deg, #1e3c72, #2a5298);
      color: white;
      text-align: center;
      padding: 0 20px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.25);
    }

    .hero h1 {
      font-size: 3rem;
      margin: 0;
      letter-spacing: 1.2px;
      font-weight: 700;
    }

    .hero .tagline {
      font-size: 1.5rem;
      margin-top: 12px;
      font-style: italic;
      opacity: 0.85;
      font-weight: 500;
    }

    /* Main container */
    main {
      max-width: 600px;
      margin: 40px auto;
      padding: 0 20px;
      background: white;
      border-radius: 8px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    }

    /* Form styles */
    form {
      display: flex;
      flex-direction: column;
      gap: 20px;
      padding: 30px 20px;
    }

    label {
      font-weight: 600;
      margin-bottom: 6px;
    }

    input[type="text"],
    input[type="email"],
    input[type="tel"],
    input[type="number"],
    textarea {
      padding: 10px;
      border: 1.5px solid #ccc;
      border-radius: 6px;
      font-size: 1rem;
      resize: vertical;
      transition: border-color 0.3s ease;
    }

    input[type="text"]:focus,
    input[type="email"]:focus,
    input[type="tel"]:focus,
    input[type="number"]:focus,
    textarea:focus {
      border-color: #1e3c72;
      outline: none;
    }

    button[type="submit"] {
      background: #1e3c72;
      color: white;
      font-size: 1.2rem;
      font-weight: 700;
      padding: 12px;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      transition: background 0.3s ease;
    }

    button[type="submit"]:hover {
      background: #16325c;
    }
  </style>
</head>
<body>
  <header class="site-header">
    <div class="hero">
      <h1>Phoenix Capital</h1>
      <p class="tagline">Fueling Your Financial Renaissance</p>
    </div>
  </header>

  <main>
    <form action="#" method="post" id="loanForm">
      <h2>Loan Application Form</h2>
      <label for="fullName">Full Name *</label>
      <input type="text" id="fullName" name="fullName" required />

      <label for="email">Email Address *</label>
      <input type="email" id="email" name="email" required />

      <label for="phone">Phone Number *</label>
      <input type="tel" id="phone" name="phone" required />

      <label for="loanAmount">Loan Amount (USD) *</label>
      <input type="number" id="loanAmount" name="loanAmount" min="100" required />

      <label for="message">Additional Information</label>
      <textarea id="message" name="message" rows="4" placeholder="Optional"></textarea>

      <button type="submit">Apply Now</button>
    </form>
  </main>
</body>
</html>
