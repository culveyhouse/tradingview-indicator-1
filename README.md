# tradingview-indicator-1
This is a TradingView strategy/indicator in Pine v6 called "Impulse-Pullback Replay"

## Usage

1. Open [TradingView](https://www.tradingview.com/)
2. Navigate to **Pine Editor** (bottom panel)
3. Copy the contents of `impulse_pullback_replay.pine` into the editor
4. Click **Add to Chart** to apply the strategy
5. Adjust the inputs to taste (defaults are designed for 1m futures charts):
   - **Volume lookback (days)**: rolling window for average volume when evaluating 3x impulse volume (default `90`, capped internally to 1000 bars for efficiency).
   - **Max bars in trade**: hard time stop in bars (default `60`).
   - **Risk/Reward target (R)**: single target in R multiples (default `1.5`).
6. Run **Add Alert** with the built-in alertconditions for automated notifications.

## File Structure

- `impulse_pullback_replay.pine` - Main Pine Script v6 strategy file

## Pine Script v6 Features

This skeleton uses Pine Script v6 syntax and includes sections for:
- **Inputs** - User-configurable parameters
- **Calculations** - Indicator logic and computations
- **Conditions** - Entry/exit signal definitions
- **Strategy Entries & Exits** - Trade execution logic
- **Plots** - Visual chart elements
- **Alerts** - Alert condition definitions
