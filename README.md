
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Phoenix Capital Limited - Loan Application</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      max-width: 600px;
      margin: 2rem auto;
      padding: 0 1rem;
      background: #f9f9f9;
      color: #333;
    }
    h1, h2 {
      text-align: center;
      color: #007BFF;
    }
    ul {
      list-style: inside disc;
      margin-bottom: 2rem;
    }
    form {
      background: white;
      padding: 1.5rem;
      border-radius: 8px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.15);
    }
    label {
      display: block;
      margin-bottom: 0.25rem;
      font-weight: bold;
    }
    input, select, textarea, button {
      width: 100%;
      padding: 0.5rem;
      margin-bottom: 1rem;
      border-radius: 4px;
      border: 1px solid #ccc;
      font-size: 1rem;
    }
    button {
      background: #007BFF;
      color: white;
      border: none;
      cursor: pointer;
      font-weight: bold;
    }
    button:hover {
      background: #0056b3;
    }
    .contact {
      text-align: center;
      margin-top: 2rem;
    }
    .contact a {
      color: #25D366;
      font-weight: bold;
      text-decoration: none;
      font-size: 1.2rem;
    }
  </style>
</head>
<body>

  <h1>Phoenix Capital Limited</h1>
  <h2>Loan Services Offered</h2>
  <ul>
    <li>Logbook Loans</li>
    <li>Morti-Fix Loans</li>
    <li>Asset Financing for Vehicles</li>
    <li>Buy Off Loans</li>
  </ul>

  <h2>Loan Application Form</h2>
  <form id="loanForm">
    <label for="fullName">Full Name *</label>
    <input type="text" id="fullName" name="fullName" required />

    <label for="phone">Phone Number *</label>
    <input type="tel" id="phone" name="phone" placeholder="+2547XXXXXXXX" required />

    <label for="loanType">Loan Type *</label>
    <select id="loanType" name="loanType" required>
      <option value="">-- Select Loan Type --</option>
      <option value="Logbook Loan">Logbook Loan</option>
      <option value="Morti-Fix Loan">Morti-Fix Loan</option>
      <option value="Asset Financing for Vehicles">Asset Financing for Vehicles</option>
      <option value="Buy Off Loan">Buy Off Loan</option>
    </select>

    <label for="loanAmount">Loan Amount (KES)</label>
    <input type="number" id="loanAmount" name="loanAmount" min="1" />

    <label for="message">Additional Message</label>
    <textarea id="message" name="message" rows="3" placeholder="Any additional info..."></textarea>

    <button type="submit">Apply via WhatsApp</button>
  </form>

  <div class="contact">
    <p>Or contact us directly on WhatsApp:</p>
    <a href="https://wa.me/254798251509" target="_blank" rel="noopener noreferrer">
      +254 798 251 509
    </a>
  </div>

  <script>
    const form = document.getElementById('loanForm');
    form.addEventListener('submit', function(event) {
      event.preventDefault();

      const fullName = form.fullName.value.trim();
      const phone = form.phone.value.trim();
      const loanType = form.loanType.value;
      const loanAmount = form.loanAmount.value.trim();
      const message = form.message.value.trim();

      if (!fullName || !phone || !loanType) {
        alert('Please fill in all required fields.');
        return;
      }

      // Construct WhatsApp message text
      let waMessage = `Loan Application from *${fullName}*%0A`;
      waMessage += `Phone: ${phone}%0A`;
      waMessage += `Loan Type: ${loanType}%0A`;
      if (loanAmount) {
        waMessage += `Loan Amount: KES ${loanAmount}%0A`;
      }
      if (message) {
        waMessage += `Message: ${message}`;
      }

      // WhatsApp number of Phoenix Capital Limited without "+" and spaces
      const waNumber = '254798251509';

      // Open WhatsApp chat with pre-filled message
      const waURL = `https://wa.me/${waNumber}?text=${waMessage}`;

      window.open(waURL, '_blank');
    });
  </script>
</body>
</html>

      
