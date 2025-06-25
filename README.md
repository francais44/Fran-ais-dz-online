<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>English With Roman</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
    }

    body {
      background: linear-gradient(to right, #f8f9fa, #e0f7fa);
      color: #333;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 2rem;
      min-height: 100vh;
    }

    .container {
      max-width: 800px;
      background: white;
      padding: 2rem 3rem;
      border-radius: 10px;
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
      width: 100%;
    }

    h1 {
      color: #0077b6;
      font-size: 2.5rem;
      margin-bottom: 1rem;
    }

    p {
      font-size: 1.1rem;
      margin-bottom: 2rem;
    }

    form {
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    label {
      font-weight: 600;
      margin-bottom: 0.2rem;
    }

    input,
    textarea {
      padding: 0.8rem;
      border: 1px solid #ccc;
      border-radius: 6px;
      font-size: 1rem;
    }

    button {
      padding: 0.8rem;
      background: #0077b6;
      color: white;
      border: none;
      border-radius: 6px;
      font-size: 1.1rem;
      cursor: pointer;
      transition: background 0.3s;
    }

    button:hover {
      background: #023e8a;
    }

    button:disabled {
      background-color: #7bb5d1;
      cursor: not-allowed;
    }

    @media (max-width: 600px) {
      .container {
        padding: 1.5rem;
      }

      h1 {
        font-size: 2rem;
      }
    }
  </style>
</head>
<body>

<div class="container">
  <h1>English With Roman</h1>
  <p>Start your journey to fluent English today! Join Roman’s modern and interactive lessons. Fill in your details below to get started 👇</p>
  
  <form id="registerForm">
    <label for="name">Full Name</label>
    <input type="text" id="name" name="name" placeholder="Your Full Name" required />

    <label for="email">Email</label>
    <input type="email" id="email" name="email" placeholder="Your Email" required />

    <label for="message">Learning Goals</label>
    <textarea id="message" name="message" placeholder="Tell us your learning goals..." rows="4" required></textarea>

    <button type="submit" id="submitBtn">Register Now</button>
  </form>
</div>

<script>
  const form = document.getElementById("registerForm");
  const button = document.getElementById("submitBtn");

  form.addEventListener("submit", function (e) {
    e.preventDefault();

    const name = form.name.value.trim();
    const email = form.email.value.trim();
    const message = form.message.value.trim();

    if (name && email && message) {
      button.disabled = true;
      alert(`✅ Thanks for registering, ${name}! We'll contact you soon.`);
      form.reset();
      button.disabled = false;
    } else {
      alert("⚠️ Please fill in all fields correctly.");
    }
  });
</script>

</body>
</html>