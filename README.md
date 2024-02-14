# Regal Spear MT4

This code is a forex trading robot designed to trade the EURUSD currency pair. It is developed by the Forex Robot Easy Team and can be found on their website [forexroboteasy.com](https://forexroboteasy.com). The program is called Regal Spear MT4.

## Requirements

To run this code, you need to include the necessary library called 'Trade' which enables trading functions.

## Parameters

The code includes several input parameters that can be adjusted according to the user's preferences:

- `minimumDeposit`: Minimum deposit required for trading (default: 100)
- `stopLoss`: Stop loss in pips (default: 50)
- `takeProfit`: Take profit in pips (default: 100)
- `lotSize`: Lot size (default: 0.01)
- `slippage`: Slippage in pips (default: 3)

## Trading Function

The main trading function in this code is called `TradeEURUSD()`. Here is how it works:

1. It first retrieves the current account balance using the `AccountInfoDouble()` function.

2. It checks if the account balance meets the minimum deposit requirement. If not, it prints an error message and exits the function.

3. It checks if there are any open positions. If there are, it prints an error message and exits the function.

4. It retrieves the current market data for the EURUSD pair using the `CopyRates()` function.

5. It performs analysis to determine potential entry points for trading. This part is left blank in the code and needs to be implemented by the user. The `signal` variable should be set to true if there is a valid entry point.

6. If there is a valid entry point, it opens a new position using the `OrderSend()` function. It calculates the entry price, stop loss level, and take profit level based on the input parameters.

7. If the position is opened successfully, it prints a success message. Otherwise, it prints an error message.

8. If there are no valid entry points, it prints a message indicating that no entry points were found.

## Entry Point

The entry point of the program is the `OnTick()` function, which is called on every tick of the market. It calls the `TradeEURUSD()` function to execute the trading logic.

## Conclusion

The `OnDeinit()` function is called when the program is stopped. It simply prints a message indicating that the robot has been stopped.

Please note that ForexRobotEasy is not the official developer of this product. This code is provided as a sample that can work as described in the product. To find the official developer of this product, please use MQL5.

For detailed reviews and trading results of this product, please visit [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/regal-spear-mt4-review-automated-forex-trading-perfected/).
