# Advanced HTML5 Elements and Forms

## Objectives
Implement HTML5 images, lists, tables, forms and input types.
Use form validation attributes.
Apply multimedia elements such as audio and video.

## Instructions

- Create an index.html file.
- Add an ordered list with roman numerals
- Add an external image from pexels.com
- Add a table of 5 contacts with; name, address, mobile and emails
- Add a registration form

>[!NOTE]
>  The registration form should have:
>- Name, email, password, and date fields.
>- A dropdown, radio buttons, and checkboxes.
>- Proper labels and placeholders.
>- Required fields and validation attributes.
>- Ensure proper indentation and commenting.
 
# Tasks
- Create a well-structured HTML5 document.
- Ensure semantic correctness.

Happy Coding! 💻✨

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Awesome Page</title>
  <style>
    
    body {
      font-family: sans-serif;
      margin: 20px;
    }

    h1, h2 {
      margin-bottom: 10px;
    }

    label {
      display: block;
      margin-bottom: 5px;
      font-weight: bold;
    }

    input[type="text"],
    input[type="email"],
    input[type="password"],
    input[type="date"],
    select {
      width: 250px;
      padding: 8px;
      margin-bottom: 10px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }

    textarea {
      width: 250px;
      padding: 8px;
      margin-bottom: 10px;
      border: 1px solid #ccc;
      border-radius: 4px;
      height: 80px; /* Set a default height */
    }


    input[type="radio"],
    input[type="checkbox"] {
      margin-right: 5px;
    }

    button {
      background-color: #4CAF50;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }

    table {
      width: 100%;
      border-collapse: collapse;
      margin-bottom: 20px;
    }

    th, td {
      border: 1px solid #ddd;
      padding: 8px;
      text-align: left;
    }

    th {
      background-color: #f2f2f2;
    }

    .error {
      color: red;
    }
  </style>
</head>
<body>

  <!-- Main Heading -->
  <h1>Welcome to My Page</h1>

  <!-- Ordered List with Roman Numerals -->
  <h2>Things to Do Today</h2>
  <ol type="I">
    <li>Wake up</li>
    <li>Have breakfast</li>
    <li>Work on HTML</li>
    <li>Take a break</li>
    <li>Go for a walk</li>
  </ol>

  <!-- External Image from Pexels -->
  <h2>Beautiful Image</h2>
  <img src="https://images.pexels.com/photos/674010/pexels-photo-674010.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" alt="Nature Image" width="500">

  <!-- Table of Contacts -->
  <h2>Contact Information</h2>
  <table>
    <thead>
      <tr>
        <th>Name</th>
        <th>Address</th>
        <th>Mobile</th>
        <th>Email</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>John Doe</td>
        <td>123 Main St, Anytown</td>
        <td>555-123-4567</td>
        <td>john.doe@example.com</td>
      </tr>
      <tr>
        <td>Jane Smith</td>
        <td>456 Oak Ave, Anytown</td>
        <td>555-987-6543</td>
        <td>jane.smith@example.com</td>
      </tr>
      <tr>
        <td>David Lee</td>
        <td>789 Pine Ln, Anytown</td>
        <td>555-111-2222</td>
        <td>david.lee@example.com</td>
      </tr>
      <tr>
        <td>Emily Brown</td>
        <td>101 Elm Rd, Anytown</td>
        <td>555-333-4444</td>
        <td>emily.brown@example.com</td>
      </tr>
      <tr>
        <td>Michael Davis</td>
        <td>222 Maple Dr, Anytown</td>
        <td>555-555-6666</td>
        <td>michael.davis@example.com</td>
      </tr>
    </tbody>
  </table>

  <!-- Registration Form -->
  <h2>Registration Form</h2>
  <form action="#" method="POST" id="registrationForm">
    <div>
      <label for="name">Name:</label>
      <input type="text" id="name" name="name" placeholder="Your Name" required minlength="2" maxlength="50">
      <span id="nameError" class="error"></span>
    </div>

    <div>
      <label for="email">Email:</label>
      <input type="email" id="email" name="email" placeholder="Your Email" required>
      <span id="emailError" class="error"></span>
    </div>

    <div>
      <label for="password">Password:</label>
      <input type="password" id="password" name="password" placeholder="Your Password" required minlength="8">
      <span id="passwordError" class="error"></span>
    </div>

    <div>
      <label for="birthdate">Date of Birth:</label>
      <input type="date" id="birthdate" name="birthdate" required>
    </div>

    <div>
      <label for="country">Country:</label>
      <select id="country" name="country">
        <option value="">Select a Country</option>
        <option value="usa">United States</option>
        <option value="canada">Canada</option>
        <option value="uk">United Kingdom</option>
        <option value="australia">Australia</option>
        <option value="germany">Germany</option>
      </select>
    </div>

    <div>
      <label>Gender:</label>
      <input type="radio" id="male" name="gender" value="male" required>
      <label for="male">Male</label>

      <input type="radio" id="female" name="gender" value="female">
      <label for="female">Female</label>

      <input type="radio" id="other" name="gender" value="other">
      <label for="other">Other</label>
    </div>

    <div>
      <label>Interests:</label>
      <input type="checkbox" id="sports" name="interests" value="sports">
      <label for="sports">Sports</label>

      <input type="checkbox" id="music" name="interests" value="music">
      <label for="music">Music</label>

      <input type="checkbox" id="reading" name="interests" value="reading">
      <label for="reading">Reading</label>
    </div>

    <div>
        <label for="comments">Comments:</label>
        <textarea id="comments" name="comments" placeholder="Any comments?"></textarea>
    </div>


    <button type="submit">Register</button>
  </form>

  <script>
    // Basic client-side validation (can be enhanced)
    document.getElementById("registrationForm").addEventListener("submit", function(event) {
      let isValid = true;

      // Name Validation
      const nameInput = document.getElementById("name");
      const nameError = document.getElementById("nameError");
      if (nameInput.value.trim() === "") {
        nameError.textContent = "Name is required.";
        isValid = false;
      } else if (nameInput.value.length < 2) {
        nameError.textContent = "Name must be at least 2 characters.";
        isValid = false;
      } else {
        nameError.textContent = ""; // Clear error message
      }

      // Email Validation (basic)
      const emailInput = document.getElementById("email");
      const emailError = document.getElementById("emailError");
      if (emailInput.value.trim() === "") {
        emailError.textContent = "Email is required.";
        isValid = false;
      } else if (!/^\S+@\S+\.\S+$/.test(emailInput.value)) {
        emailError.textContent = "Invalid email format.";
        isValid = false;
      } else {
        emailError.textContent = "";
      }

       // Password Validation
      const passwordInput = document.getElementById("password");
      const passwordError = document.getElementById("passwordError");
      if (passwordInput.value.trim() === "") {
        passwordError.textContent = "Password is required.";
        isValid = false;
      } else if (passwordInput.value.length < 8) {
        passwordError.textContent = "Password must be at least 8 characters.";
        isValid = false;
      } else {
        passwordError.textContent = "";
      }


      if (!isValid) {
        event.preventDefault(); // Prevent form submission if validation fails
      }
    });
  </script>
</body>
</html>
