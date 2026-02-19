<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Report Freelancer</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    * {
      box-sizing: border-box;
      font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
      background: linear-gradient(135deg, #667eea, #764ba2);
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 20px;
    }

    .form-container {
      background: #ffffff;
      width: 100%;
      max-width: 500px;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
    }

    .form-container h2 {
      text-align: center;
      margin-bottom: 10px;
      color: #333;
    }

    .form-container p {
      text-align: center;
      margin-bottom: 25px;
      color: #666;
      font-size: 14px;
    }

    .form-group {
      margin-bottom: 16px;
    }

    label {
      display: block;
      font-weight: 600;
      margin-bottom: 6px;
      color: #444;
    }

    input, select, textarea {
      width: 100%;
      padding: 12px;
      border-radius: 8px;
      border: 1px solid #ccc;
      font-size: 14px;
      outline: none;
      transition: border 0.2s, box-shadow 0.2s;
    }

    input:focus,
    select:focus,
    textarea:focus {
      border-color: #667eea;
      box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.2);
    }

    textarea {
      resize: vertical;
      min-height: 100px;
    }

    button {
      width: 100%;
      padding: 14px;
      border: none;
      border-radius: 10px;
      background: linear-gradient(135deg, #667eea, #764ba2);
      color: #fff;
      font-size: 16px;
      font-weight: 600;
      cursor: pointer;
      transition: transform 0.2s, box-shadow 0.2s;
    }

    button:hover {
      transform: translateY(-2px);
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
    }

    .hidden {
      display: none;
    }

    @media (max-width: 480px) {
      .form-container {
        padding: 20px;
      }
    }
  </style>
</head>

<body>

  <div class="form-container">
    <h2>Report Freelancer</h2>
    <p>Submit a report if a freelancer violated rules or behaved improperly.</p>

    <form action="https://api.web3forms.com/submit" method="POST">

      <!-- Web3Forms Access Key -->
      <input type="hidden" name="access_key" value="40d37968-d566-4a66-a737-9d946955f6df">

      <!-- Reporter Info -->
      <div class="form-group">
        <label>Your Name</label>
        <input type="text" name="reporter_name" placeholder="Enter your name" required>
      </div>

      <div class="form-group">
        <label>Your Email</label>
        <input type="email" name="reporter_email" placeholder="Enter your email" required>
      </div>

      <!-- Freelancer Info -->
      <div class="form-group">
        <label>Freelancer Name / Username</label>
        <input type="text" name="freelancer_name" placeholder="Freelancer name or username" required>
      </div>

      <div class="form-group">
        <label>Reason for Report</label>
        <select name="report_reason" required>
          <option value="">Select a reason</option>
          <option>Scam / Fraud</option>
          <option>Did not deliver work</option>
          <option>Plagiarism</option>
          <option>Abusive behavior</option>
          <option>Fake profile</option>
          <option>Other</option>
        </select>
      </div>

      <!-- Message -->
      <div class="form-group">
        <label>Detailed Description</label>
        <textarea name="message" placeholder="Explain the issue in detail..." required></textarea>
      </div>

      <!-- Honeypot Spam Protection -->
      <input type="checkbox" name="botcheck" class="hidden">

      <!-- Optional Redirect -->
      <!-- <input type="hidden" name="redirect" value="https://yourwebsite.com/thank-you.html"> -->

      <button type="submit">Submit Report</button>

    </form>
  </div>

</body>
</html>
