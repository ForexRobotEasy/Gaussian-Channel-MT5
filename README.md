# Gaussian Channel ReadMe

This ReadMe provides information about the code for the 'Gaussian Channel' indicator developed by the Forex Robot Easy Team. This indicator is designed for trend analysis in the Forex market. The code is written in MQL5 language.

## Description

The 'Gaussian Channel' indicator calculates the Gaussian Channel using the Ehlers Gaussian Filter method. It identifies the trend strength and detects bearish phases in the market. Based on the trend identification, the indicator generates trading decisions to either place buy or sell orders or close existing orders.

## Input Parameters

The indicator has one input parameter:

- FilterPeriod: Filter period for the Ehlers Gaussian Filter method. The default value is set to 10.

## Initialization

The `OnInit()` function is responsible for initializing the indicator. It sets the indicator's short name and defines the style and buffer for drawing the indicator line.

## Calculation

The `OnCalculate()` function is the main calculation function of the indicator. It calculates the Gaussian Channel using the Ehlers Gaussian Filter method. It iterates through the price data and applies the filter to calculate the Gaussian value for each bar. The calculated Gaussian values are stored in the `ExtMapBuffer1` array.

After calculating the Gaussian Channel, the function determines the trend strength and identifies bearish phases. It compares the current Gaussian value with the previous one and calculates the trend strength as the absolute difference between them. It also checks if the current Gaussian value is lower than the previous one to identify a bearish phase.

## Trading Decisions

Based on the trend identification, the `OnCalculate()` function generates trading decisions. If a bearish phase is detected, it sends a sell order or closes existing buy orders. If no bearish phase is detected, it sends a buy order or closes existing sell orders. The trading decisions are executed using the `CTrade` class from the Trade library.

## Deinitialization

The `OnDeinit()` function is responsible for cleaning up any resources or open trades when the indicator is removed or the terminal is closed. It calls the `PositionCloseAll()` function of the `CTrade` class to close all open positions.

## Product Description

The Gaussian Channel indicator developed by the Forex Robot Easy Team is a powerful Forex software designed for trend analysis. It uses the Ehlers Gaussian Filter method to calculate the Gaussian Channel, which helps traders identify trend strength and detect bearish phases in the market.

This indicator provides valuable information for making trading decisions. It can be used to determine the optimal time to enter or exit trades, as well as to manage existing positions. By analyzing the trend strength and identifying bearish phases, traders can take advantage of potential profit opportunities in the Forex market.

Please note that ForexRobotEasy is not the official developer of this product. We are only showcasing a sample code that can work as described in the product. To find the official developer of this product, please refer to MQL5.

For detailed reviews and trading results of this product, please visit [Forex Robot Easy - Gaussian Channel MT5](https://forexroboteasy.com/forex-robot-review/review-gaussian-channel-mt5-a-powerful-forex-software-for-trend-analysis/).
