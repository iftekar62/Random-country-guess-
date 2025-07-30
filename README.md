<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Random Country Explorer</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      text-align: center;
      padding: 50px;
      background: #f2f2f2;
    }

    h1 {
      color: #333;
    }

    button {
      background-color: #0066cc;
      color: white;
      border: none;
      padding: 15px 25px;
      font-size: 16px;
      cursor: pointer;
      border-radius: 5px;
      margin-bottom: 20px;
    }

    button:hover {
      background-color: #0052a3;
    }

    #country-info {
      margin-top: 20px;
      background: white;
      padding: 20px;
      border-radius: 10px;
      display: inline-block;
      box-shadow: 0px 2px 10px rgba(0, 0, 0, 0.1);
    }
  </style>
</head>
<body>
  <h1>🌍 Random Country Explorer</h1>
  <button onclick="showRandomCountry()">Choose a Random Country</button>

  <div id="country-info"></div>

  <script>
    const countries = [
      "Algeria", "Angola", "Benin", "Botswana", "Burkina Faso", "Burundi", "Cabo Verde", "Cameroon",
      "Central African Republic", "Chad", "Comoros", "Congo (Congo-Brazzaville)", "Democratic Republic of the Congo", "Djibouti", "Egypt",
      "Equatorial Guinea", "Eritrea", "Eswatini (fmr. Swaziland)", "Ethiopia", "Gabon", "Gambia", "Ghana", "Guinea",
      "Guinea-Bissau", "Ivory Coast", "Kenya", "Lesotho", "Liberia", "Libya", "Madagascar", "Malawi", "Mali", "Mauritania", "Mauritius",
      "Morocco", "Mozambique", "Namibia", "Niger", "Nigeria", "Rwanda", "Sao Tome and Principe", "Senegal", "Seychelles", "Sierra Leone",
      "Somalia", "South Africa", "South Sudan", "Sudan", "Tanzania", "Togo", "Tunisia", "Uganda", "Zambia", "Zimbabwe", "Afghanistan",
      "Armenia", "Azerbaijan", "Bahrain", "Bangladesh", "Bhutan", "Brunei", "Cambodia", "China", "Cyprus", "Georgia", "India",
      "Indonesia", "Iran", "Iraq", "Japan", "Jordan", "Kazakhstan", "Kuwait", "Kyrgyzstan", "Laos", "Lebanon", "Malaysia", "Maldives",
      "Mongolia", "Myanmar", "Nepal", "North Korea", "Oman", "Pakistan", "Palestine", "Philippines", "Qatar", "Saudi Arabia", "Singapore",
      "South Korea", "Sri Lanka", "Syria", "Taiwan", "Tajikistan", "Thailand", "Timor-Leste", "Turkey", "Turkmenistan",
      "United Arab Emirates", "Uzbekistan", "Vietnam", "Yemen", "Albania", "Andorra", "Austria", "Belarus", "Belgium",
      "Bosnia and Herzegovina", "Bulgaria", "Croatia", "Czech Republic", "Denmark", "Estonia", "Finland", "France", "Germany",
      "Greece", "Hungary", "Iceland", "Ireland", "Italy", "Kosovo", "Latvia", "Liechtenstein", "Lithuania", "Luxembourg", "Malta",
      "Moldova", "Monaco", "Montenegro", "Netherlands", "North Macedonia", "Norway", "Poland", "Portugal", "Romania", "Russia",
      "San Marino", "Serbia", "Slovakia", "Slovenia", "Spain", "Sweden", "Switzerland", "Ukraine", "United Kingdom", "Vatican City",
      "Antigua and Barbuda", "Bahamas", "Barbados", "Belize", "Canada", "Costa Rica", "Cuba", "Dominica", "Dominican Republic",
      "El Salvador", "Grenada", "Guatemala", "Haiti", "Honduras", "Jamaica", "Mexico", "Nicaragua", "Panama", "Saint Kitts and Nevis",
      "Saint Lucia", "Saint Vincent and the Grenadines", "Trinidad and Tobago", "United States", "Argentina", "Bolivia", "Brazil",
      "Chile", "Colombia", "Ecuador", "Guyana", "Paraguay", "Peru", "Suriname", "Uruguay", "Venezuela", "Australia", "Fiji",
      "Kiribati", "Marshall Islands", "Micronesia", "Nauru", "New Zealand", "Palau", "Papua New Guinea", "Samoa", "Solomon Islands",
      "Tonga", "Tuvalu", "Vanuatu", "Antarctica"
    ];

    function showRandomCountry() {
      const randomIndex = Math.floor(Math.random() * countries.length);
      const countryName = countries[randomIndex];

      const infoHTML = `
        <h2>${countryName}</h2>
        <p><strong>Note:</strong> This version shows only the name. Flag, capital, etc., will need internet or data setup later.</p>
      `;

      document.getElementById("country-info").innerHTML = infoHTML;
    }
  </script>
</body>
</html>
