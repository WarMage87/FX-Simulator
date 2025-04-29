# FX Trading Simulator V2.9.2

A web-based simulator designed to help assess the robustness of FX trading strategies by running simulations with adjustable parameters and Monte Carlo analysis. Built with HTML, Tailwind CSS, and JavaScript (using Chart.js for charts and jsPDF for reporting).

## Features

*   **Single Simulation:** Run individual trading simulations with visual feedback (capital chart, trade log).
*   **Monte Carlo Analysis:** Perform batch simulations (up to 1,000,000 runs) to analyse the distribution of final outcomes and calculate extensive statistics.
*   **Configurable Parameters:**
    *   Total Bankroll & Initial Active Capital (implements Active/Reserve capital concept).
    *   Target Expected Value (EV) and configurable Win/Loss Ranges (% profit/loss per trade).
    *   Bet Sizing Modes: Fixed Dollar Amount ($) or Percentage (%) of **Total Capital**.
    *   Variable bet sizing using Min/Max/Avg parameters within the selected mode.
    *   Optional Black Swan events (configurable probability).
    *   Optional automatic profit banking from Active to Reserve Capital (configurable frequency).
    *   Optional automatic Active Capital top-up from Reserve if needed.
*   **Detailed Statistics:**
    *   **Single Run:** Win Rate, Profit Factor, Max Drawdown, Estimated RoR, etc.
    *   **Monte Carlo:** Histogram of final capital, Mean/Median/Mode, Skewness/Kurtosis, Confidence Intervals, Percentiles (P1-P99), Aggregated Max Drawdown, CVaR (95%/99%), IQR, Return %, Simplified Sharpe Ratio, Probability of Profit/Ruin, and more.
*   **Preset Management:** Save, load, and delete entire configuration presets locally in your browser.
*   **Results Export:** Download single run results or Monte Carlo summaries as detailed PDF reports (including the histogram chart in the MC summary).

## How to Use

1.  **Download:** Get the `49.html` file from this repository.
    *   Click on the `49.html` file name in the file list above.
    *   On the file view page, find the "Raw" button.
    *   Right-click the "Raw" button and select "Save Link As..." (or similar wording depending on your browser) to save the `49.html` file to your computer.
2.  **Open:** Open the downloaded `49.html` file directly in a modern web browser (e.g., Google Chrome, Mozilla Firefox, Microsoft Edge). No installation or web server is needed.
3.  **Configure:** Adjust the simulation parameters in the different sections (Core Settings, Win/Loss Ranges, Optional Features, Auto Trade, Monte Carlo). Hover over labels or icons for tooltips explaining each setting.
4.  **Run:**
    *   Use "Place Trade" for manual steps (enter size first).
    *   Configure "Auto Trade" settings (Fixed $ or Percent %) and click "Start / Resume Auto" for a single visualized simulation run.
    *   Configure "Monte Carlo" settings (number of runs, bet sizing method) and click "Run Monte Carlo Batch" for statistical analysis over many runs.
5.  **Analyse:** Review the results:
    *   **Single Run:** Observe the Trade Log and Capital Chart in real-time (or after completion). Final stats appear in a modal and are stored locally for review/download via the "Single Results" section.
    *   **Monte Carlo:** View the comprehensive statistics and histogram chart in the Summary Modal that appears upon completion or abortion. Download the summary PDF from the modal.

## Key Differences: Single Run vs. Monte Carlo

*   **Purpose:** Single run shows one specific outcome path. Monte Carlo shows the *distribution* of outcomes over many runs for statistical robustness checks.
*   **Visualization:** Single run updates the Chart/Log live (affected by Speed setting). Monte Carlo runs much faster *without* live visualization (shows progress bar instead).
*   **Bet Sizing:** Single Auto runs use variable sizing based on Min/Max/Avg settings. Monte Carlo runs can use either a *fixed* dollar amount (derived from the Avg setting at the start) OR *variable* sizing (like single auto runs), selectable via a toggle.
*   **Results:** Single run results are saved persistently in browser storage and can be navigated/downloaded individually. Monte Carlo results are aggregated into a summary modal (with its own PDF download) and are *not* stored individually in the persistent results area.

## Version History

*   **V2.9.2 (Current):** Code refactoring for maintainability. Renamed "Reset Simulation Config" button to "Restart Single Simulation". Moved PDF attribution to the end of reports.
*   **V2.9.1:** Added advanced Monte Carlo stats (Conditional CIs, Percentiles P1-P99, Aggregated Max Drawdown stats, CVaR 95%/99%, IQR, Return on Initial Capital % Avg/Median, Simplified Sharpe Ratio). Included histogram chart in MC summary PDF. Updated modal layouts.

## License & Attribution

This FX Trading Simulator (V2.9.2) is licensed under the [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

You are free to Share and Adapt the material for any purpose, even commercially, under the condition of **Attribution**.

**Please attribute the original creator:**
*   **Creator:** Winston Koh
*   **Organisation:** Founder & Chief Trader of ZenithFX Trading Academy
