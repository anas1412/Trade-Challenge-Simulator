# Trade Challenge Simulator

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Made with: Vanilla JS](https://img.shields.io/badge/Made%20with-Vanilla%20JS-F7DF1E?logo=javascript&logoColor=black)](https://www.javascript.com)

A sophisticated simulator designed to stress-test trading strategies against the pass/fail conditions of proprietary trading firm challenges.

This tool goes beyond simple win/loss tracking. It leverages a probabilistic model to provide real-time feedback on your strategy's viability, calculating the precise probability of passing or failing from your current equity state.

**[Live Demo](https://anas.cyberia.tn/Trade-Challenge-Simulator/)**

---

![Simulator Screenshot](https://i.imgur.com/your-screenshot.png)
*(Suggestion: Replace the link above with a real screenshot of your application)*

---

## About The Project

Most trading simulators show you a hypothetical equity curve. This one does more. It was built to answer a more critical question: "**Given my current strategy, what are the actual mathematical odds of me passing this challenge?**"

By inputting your challenge's targets (e.g., +6% profit, -6% drawdown) and your strategy's metrics (Risk %, R:R Ratio, Win Rate %), the simulator runs a session where each trade updates not just your P&L, but also your statistical edge and, most importantly, your probability of success.

This allows you to:
-   Objectively assess if a strategy has a positive expectancy (EV).
-   Understand how a string of losses or wins impacts your future odds.
-   Develop a more intuitive feel for risk and probability in a challenge context.

## Key Features

-   **Challenge Configuration**: Set the profit target and maximum drawdown percentages for any prop firm challenge.
-   **Strategy Definition**: Input your core trading parameters:
    -   **Risk % per trade**: How much you risk on each position.
    -   **RR Ratio**: Your strategy's average reward-to-risk ratio.
    -   **Win Rate %**: Your historical (or expected) win rate.
-   **Interactive Simulation**: Manually simulate trades by clicking "Win" or "Loss" to see the immediate impact.
-   **Dynamic Performance Chart**: An auto-updating chart (powered by Chart.js) visualizes your equity curve trade-by-trade.
-   **Advanced Statistical Analysis**:
    -   **System Edge (EV)**: See the calculated Expected Value of your strategy *before* you even start.
    -   **Probabilistic Forecasting**: The core feature. The tool calculates the exact probability of you passing or failing the challenge from your current P&L.
    -   **Live Metrics**: Tracks your trade count and actual win rate as the simulation progresses.

## How It Works

The simulator's core is a probability engine written in JavaScript. For a given state (your current P&L), it solves a system of linear equations derived from a Markov chain model. In simple terms, it calculates the odds of a "random walk" hitting the "pass" boundary before it hits the "fail" boundary.

The results are memoized for performance, allowing for instant feedback as you simulate trades.

## Built With

-   **HTML5**
-   **CSS3**: Styled with a modern, dark-themed UI using CSS variables.
-   **Vanilla JavaScript**: All logic is self-contained and framework-free.
-   **Chart.js**: For rendering the dynamic performance graph.

## Getting Started

No complex setup is required.

1.  Clone the repository:
    ```sh
    git clone https://github.com/your-username/Trade-Challenge-Simulator.git
    ```
2.  Open the `index.html` file in your favorite web browser.

## License

Distributed under the MIT License. See `LICENSE` for more information.