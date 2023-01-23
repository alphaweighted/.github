# Welcome

Welcome to the public Github for alphaweighted.  Hosted here are various components for integrating with
services at alphaweighted.com, and a-la-carte modules and utilities for building and running your own
backtesting and trading infrastructure.

These tools are aimed at systematic/algorithmic traders, as well as discretionary traders and investors using
automation tooling to help with research, planning or execution.

They are built and provided under two key philosophies:

1. That **no single platform can provide all the power/flexibility/choice** for you to explore, test and express your strategies -> so they are provided 'a-la-carte'; use the components that are relevant to you and build the rest yourself
2. **Your strategies are your secret sauce** and must be provably confidential on your own infrastructure.  All components include documentation describing how to configure for and verify security, so you can be confident no secrets get leaked.


## Tracer

We believe both that rapid iteration is key, and that the human brain is the best ad-hoc analytics tool.  So, the Tracer exists as a mechanism for instantaneously visualizing a price chart with your algo's indicators and
decision points overlaid on top.

This works via a simple API call to alphaweighted.com to post the instrument, time period, and any points/lines of interest.   Your browser window then automatically updates, usually in <0.5sec, to show the updated visualization.

Submit multiple traces rapidly and quickly page through them to instantly get a better understanding of big wins/losses, where entries are good/bad, or whatever price behaviour you want to analyse further.

** *Coming soon* ** 

## awcli

The `awcli` component is a small command-line utility for a variety of purposes, including:
- testing market data components
- interfacing manually with market data components, e.g. to export CSV data
- live/production market data integration - e.g. by streaming price data to `stdout` as part of a pipeline of tools

For more information, see the [awcli docs](https://github.com/alphaweighted/awcli)

## Market data

Access to market data (i.e. instruments, prices, ticks and candles) happens through downloadable market data modules. Each module runs as a service on your infrastructure and acts as a type of 'smart proxy' between you and an upstream data provider such as Oanda, Polygon.io, Alpaca Markets or others.

Use these modules for reliable, high performance and easy-to-use access to market data for backtesting and live trading.

All modules expose a standard API interface (i.e. it's the same API whether you use Oanda, Polygon, TDA or anyone else), and you can interact using `awcli`, by accessing the gRPC API directly, or by using one of our ready-made client API libraries.

To use a market data module, you must already have an active account with the relevant data provider/broker.


- [marketoanda](https://github.com/alphaweighted/marketoanda) - for [Oanda](https://www.oanda.com) an FX/CFD broker

## Client libraries

Coming soon for Go, Python and other languages
