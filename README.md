<div align="center">

# 💱 Real-Time Currency Converter

### Convert currencies using exchange-rate data from an external API

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Open%20App-0A7A4B?style=for-the-badge)](https://real-time-currency-converter170.vercel.app/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![REST API](https://img.shields.io/badge/REST%20API-Integrated-2F855A?style=flat-square)](#)

**[Live Application](https://real-time-currency-converter170.vercel.app/) · [Source Code](https://github.com/mdnav/real-time-currency-converter) · [Portfolio](https://portfolio1701.vercel.app/)**

</div>

---

## Overview

Real-Time Currency Converter is a browser-based application that converts an entered amount between supported currencies using exchange-rate data retrieved from ExchangeRate-API. Users can select source and target currencies, view associated country flags, swap currencies, and request a conversion.

The displayed rate depends on the external API response and its availability.

## Features

- **Currency selection:** Choose from the currency codes included in the project.
- **Exchange-rate lookup:** Fetches the latest available rates for the selected base currency.
- **Amount conversion:** Calculates and displays the converted amount to two decimal places.
- **Currency swap:** Switches the source and target currencies and requests the conversion again.
- **Country flags:** Updates flag images based on the selected currency mapping.
- **Default values:** Starts with USD as the source currency and INR as the target.
- **Basic error feedback:** Displays a message if the exchange-rate request fails.

## Conversion Workflow

1. Enter an amount.
2. Select the source currency.
3. Select the destination currency.
4. The application requests rates for the selected base currency.
5. JavaScript reads the target rate from the JSON response.
6. The amount is multiplied by the returned rate and displayed.
7. Use the swap control to reverse the currency pair.

## Technology Stack

| Technology or service | Purpose |
|---|---|
| HTML5 | Application structure |
| CSS3 | Styling and responsive layout |
| JavaScript (ES6) | Conversion logic and UI interactions |
| ExchangeRate-API | Exchange-rate data |
| FlagsAPI | Currency-associated flag images |
| Git and GitHub | Version control and source hosting |
| Vercel | Deployment |

## Run Locally

```bash
git clone https://github.com/mdnav/real-time-currency-converter.git
cd real-time-currency-converter
```

Open `index.html` in a modern browser. An internet connection is required to retrieve exchange-rate data and load flag images.

## Project Structure

```text
real-time-currency-converter/
├── index.html
├── style.css
├── app.js
├── codes.js
└── README.md
```

## Concepts Demonstrated

- Fetch API and HTTP requests
- Promises and asynchronous JavaScript
- JSON response processing
- DOM manipulation and event handling
- Dynamic select options and flag updates
- Input handling and basic error feedback
- Integration with external web services

## Important Notes

- Exchange rates are supplied by the external service and may change.
- Conversion results depend on API responses and network availability.
- This project is for learning and demonstration; it is not a financial or investment service.
- Currency-to-country mappings are maintained in `codes.js`.

## Future Improvements

- Loading and request-status indicators
- Stronger input validation and API response checks
- Improved handling of unsupported currency pairs
- Conversion history and favorite currency pairs
- Historical rate charts

## About the Developer

**Mohammad Naveed** — B.Tech ECE student building web applications and developing skills in Java, Spring Boot, React, REST APIs, databases, and cloud technologies.

- **Portfolio:** https://portfolio1701.vercel.app/
- **GitHub:** https://github.com/mdnav
- **LinkedIn:** https://www.linkedin.com/in/mdnav/

## Contributing

Suggestions are welcome. Fork the repository, create a feature branch, make your changes, and open a pull request.

If you find this project useful, consider giving the repository a ⭐.

<div align="center">

**Built with HTML, CSS, and JavaScript by Mohammad Naveed**

</div>
