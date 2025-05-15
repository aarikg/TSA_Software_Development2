# Agri-Sphere: Intelligent Farm Management

**Event:** TSA Software Development 2024-2025

**Team:** Aarik Ghosh & Pranav Bhatnagar

**Theme:** Enhance the environment and/or agriculture to be more sustainable and efficient.

---

## 1. Project Overview

Agri-Sphere is a web application build to empower farmers with the data and insights needed for more sustainable, efficient, and profitable farming operations. It moves beyond simple diagnostics to act as an all-in-one, AI-powered advisor for the entire farming lifecycle. By integrating real-time weather, market data, soil science, and financial planning with a powerful AI backend, Agri-Sphere transforms complex variables into simple, actionable intelligence.

## 2. The Problem

Modern agriculture faces a multi-faceted challenge: the need to increase efficiency and profitability while operating more sustainably. Farmers are often forced to make critical decisions with incomplete, disconnected, or purely historical information. This leads to:

* **Resource Inefficiency:** Over-application of water and treatments wastes money and harms the environment.
* **Yield Uncertainty:** Pests, diseases, and poor soil health create unpredictable harvests and financial risk.
* **Fragmented Data:** Critical information about soil health, weather forecasts, and live market prices is scattered across different platforms, making holistic planning nearly impossible.
* **Lack of Proactive Tools:** Most tools are reactive, helping to solve problems *after* they occur, rather than preventing them.

## 3. Our Solution: A Unified AI-Powered Platform

Agri-Sphere addresses these challenges by integrating a full suite of farm management tools into a single, intuitive, and powerful web platform. By leveraging the modern power of AI, we were able to create muliple important features for farmers, ranging from photo plant diagnosis, live crop prices, to profitablity dashboards and a lot more.

## 4. Core Features

Our platform is built around eight deeply interconnected modules:

#### 🧑‍🌾 My Farm Tracker

The core of the application where users digitize their farm. Users can add, manage, and delete planting zones, specifying the crop type, number of plants, soil type, and planting date. This data serves as the foundation for all other AI-powered advisory features.

#### 🩺 AI Crop Doctor

A state-of-the-art diagnostic tool. Users can upload an image of a plant leaf, and the Gemini AI provides an instant diagnosis of diseases or pests, complete with sustainable and organic treatment recommendations.

#### 💧 AI Irrigation Advisor

This module moves beyond simple timers. It takes the specific crop type, plant count, and soil type from the "My Farm" tracker, combines it with a live 3-day weather forecast, and feeds it to the AI. The AI then generates a custom, 3-day watering plan in gallons, optimizing water usage based on all variables.

#### 🌱 AI Soil Health Advisor

A proactive tool for long-term sustainability. The user inputs their soil test results (pH, N, P, K) for a specific planting zone. The AI analyzes this data in the context of the crop being grown and provides tailored, organic recommendations to amend the soil and improve nutrient balance, visualized with a dynamic radar chart.

#### 🗺️ AI Crop Planner

This strategic planning tool helps with long-term farm management. A user inputs the crops they want to grow and the number of zones they have. The AI then generates a multi-year crop rotation and companion planting plan designed to maximize soil health, reduce pests naturally, and improve biodiversity.

#### 📈 AI Market Tracker

Provides a live look at the financial landscape. The user can track any agricultural commodity. The AI fetches the latest market price (normalized to standard units like "per pound" or "per bushel") and provides a brief analysis of the recent price trend, empowering users to decide the best time to sell.

#### 💵 Financials Dashboard

This module connects the farm's physical yield to its financial potential. It uses live market data from the Market Tracker and the user's tracked plants to forecast total estimated revenue. By inputting their costs, users can see a clear projection of their profitability, visualized with a dynamic bar chart.

#### 📊 Unified Dashboard

The central hub that provides an at-a-glance overview of the entire operation. It features dynamic widgets for local weather, a color-coded farm health map, and a list of AI-generated priority alerts, such as upcoming harvests, pest warnings, and irrigation advisories.

## 5. Technical Architecture

Agri-Sphere is a purely client-side application, demonstrating a modern, serverless architecture that is fast, scalable, and respects user privacy.

* **Frontend:**
    * **Languages:** HTML5, CSS3, JavaScript (ES6+ Modules)
    * **Frameworks:** Tailwind CSS for a utility-first, professional design system.
    * **Libraries:** Chart.js for data visualization; Font Awesome for iconography.
* **AI & Services (via API):**
    * **Google Gemini 1.5 Flash:** A single AI model is leveraged for multiple, distinct tasks, showcasing advanced prompt engineering:
        * **Multimodal Vision:** Analyzing plant health from images.
        * **Data Synthesis:** Generating irrigation plans from crop, soil, and weather data.
        * **Strategic Planning:** Creating multi-year crop rotation schedules.
        * **Live Data Retrieval:** Estimating current market prices for commodities.
    * **WeatherAPI.com:** Provides live current and forecasted weather data.
* **Data Storage:**
    * **Browser Local Storage:** User-specific data (tracked plants, farm history, tracked commodities) is stored client-side for speed and privacy.

## 6. How to Run Locally

To run Agri-Sphere on your local machine, please follow these steps:

1.  **Clone or Download:** Get a copy of this repository on your computer.
2.  **Create `config.js`:** In the root directory, create a file named `config.js`. This file will store your API keys and will be ignored by Git. Add the following content to it:
    ```javascript
    const GEMINI_API_KEY = "YOUR_GEMINI_API_KEY_HERE";
    const WEATHER_API_KEY = "YOUR_WEATHER_API_KEY_HERE";
    ```
3.  **Get API Keys:**
    * Replace `YOUR_GEMINI_API_KEY_HERE` with your key from [Google AI Studio](https://aistudio.google.com/app/apikey).
    * Replace `YOUR_WEATHER_API_KEY_HERE` with your key from [WeatherAPI.com](https://www.weatherapi.com/).
4.  **Lastly, run on your local browser!**
