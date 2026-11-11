<div align="center">

# Real-Time Currency Converter

**Convert an amount between supported currencies using exchange-rate data from an external API.**

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Open%20Converter-176B4D?style=for-the-badge)](https://real-time-currency-converter170.vercel.app/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![REST API](https://img.shields.io/badge/REST%20API-Integrated-6B7280?style=flat-square)](#)

[Live Demo](https://real-time-currency-converter170.vercel.app/) · [Source Code](https://github.com/mdnav/real-time-currency-converter) · [Portfolio](https://portfolio1701.vercel.app/)

</div>

---

## Project Overview

Real-Time Currency Converter is a lightweight web application that retrieves exchange-rate data from **ExchangeRate-API** and converts a user-entered amount between supported currencies.

Users can choose a base currency and a target currency, view the associated country flags, swap the currency pair, and request a conversion. The interface is implemented with HTML, CSS, and vanilla JavaScript.

## Live Application

Try the deployed application: **[Open Currency Converter](https://real-time-currency-converter170.vercel.app/)**

## Key Features

- **Currency selection:** Choose from the currency codes defined in the project.
- **Exchange-rate retrieval:** Requests rates for the selected base currency.
- **Amount conversion:** Multiplies the entered amount by the returned target-currency rate.
- **Currency swap:** Exchanges the selected source and destination currencies.
- **Country flag updates:** Displays flag images based on the currency-to-country mapping.
- **Default currency pair:** Loads with USD as the source and INR as the destination.
- **Request feedback:** Displays a loading message and a basic error message if the request fails.

## Conversion Workflow

1. Enter the amount to convert.
2. Select the source and destination currencies.
3. The application requests the latest available rates for the source currency.
4. JavaScript reads the destination currency's rate from the JSON response.
5. The application calculates and displays the converted amount.
6. Use the swap control to reverse the currency pair.

```text
Amount + Currency Pair
         |
         v
Request Exchange Rates
         |
         v
ExchangeRate-API
         |
         v
Read Target Currency Rate
         |
         v
Calculate Converted Amount
         |
         v
Display Conversion Result
```

## Technology Stack

| Technology / Service | Role |
|---|---|
| HTML5 | Application structure |
| CSS3 | Layout and visual styling |
| JavaScript (ES6) | API requests, conversion logic, and DOM updates |
| ExchangeRate-API | Exchange-rate data source |
| FlagsAPI | Country flag images |
| Git & GitHub | Version control and source hosting |
| Vercel | Deployment |

## Run Locally

```bash
git clone https://github.com/mdnav/real-time-currency-converter.git
cd real-time-currency-converter
```

Open `index.html` in a modern web browser. An internet connection is required for exchange-rate requests and flag images.

## Project Structure

```text
real-time-currency-converter/
├── index.html       # Converter form and interface
├── style.css        # Layout and visual styling
├── app.js           # Currency selection, API request, and conversion
├── codes.js         # Currency-code to country-code mapping
└── README.md        # Project documentation
```

## API and Data

### Exchange-rate service

The application requests rates from the following endpoint pattern:

```text
https://api.exchangerate-api.com/v4/latest/{BASE_CURRENCY}
```

The `{BASE_CURRENCY}` segment is replaced with the selected source currency code. The application reads the requested destination rate from the JSON response.

### Country flags

Currency codes are mapped to country codes in `codes.js`. The selected country code is used to load a flag image from FlagsAPI.

> Exchange rates are supplied by an external service. Availability, supported currencies, and update frequency depend on that provider. The project does not guarantee tick-by-tick market rates.

## Engineering Concepts

- Fetch API and asynchronous JavaScript
- Promises and JSON response handling
- Dynamic select-option generation
- DOM manipulation and event listeners
- Currency-to-country data mapping
- Calculating conversions from API-provided rates
- Handling failed network requests

## Current Behavior and Limitations

- The default pair is USD to INR.
- Empty or zero amounts are reset to 1 before the request.
- The application displays a general error message if the request fails.
- Exchange-rate data requires network access.
- This is an educational converter and is not intended for financial, trading, or investment decisions.

## Roadmap

- Validate amount input and API response status more thoroughly
- Add a clear loading state and more descriptive error messages
- Support conversion history and favorite currency pairs
- Display historical exchange-rate charts
- Add improved formatting for currency values

## About the Developer

**Mohammad Naveed**  
B.Tech ECE student focused on software development, Java full-stack engineering, and building practical web applications.

- **Portfolio:** [portfolio1701.vercel.app](https://portfolio1701.vercel.app/)
- **GitHub:** [github.com/mdnav](https://github.com/mdnav)
- **LinkedIn:** [linkedin.com/in/mdnav](https://www.linkedin.com/in/mdnav/)

## Contributing

Suggestions and improvements are welcome. Fork the repository, create a feature branch, commit your changes, and open a pull request.

If you find this project useful, consider giving it a ⭐.

<div align="center">

**Designed and developed by Mohammad Naveed**

</div>
