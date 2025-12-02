# tradingview-indicator-1
This is a TradingView strategy/indicator in Pine v6 called "Impulse-Pullback Replay". It hunts for a large impulse candle with elevated volume, then waits for a pullback into the 50–70% zone of that candle before entering in the impulse direction.

## Usage

1. Open [TradingView](https://www.tradingview.com/)
2. Navigate to **Pine Editor** (bottom panel)
3. Copy the contents of `impulse_pullback_replay.pine` into the editor
4. Click **Add to Chart** to apply the strategy
5. Use the **Settings** gear to adjust inputs (backtest lookback, impulse multipliers, pullback band, timeout bars, R:R target, chop filter, and visualization toggles)

## File Structure

- `impulse_pullback_replay.pine` - Main Pine Script v6 strategy file

## Pine Script v6 Features

Key highlights:
- **Impulse detection** using outsized candle bodies and volume relative to configurable lookbacks.
- **Pullback trigger** that waits for a closing bar inside the 50–70% retrace of the impulse candle.
- **Risk controls** with stop at the opposite wick, configurable R:R target (default 1.5R), optional chop filter, setup timeout, and max hold bars for quick exits.
- **Visuals & alerts** that plot the pullback band, stops/targets, and emit alertconditions for long/short entries.
