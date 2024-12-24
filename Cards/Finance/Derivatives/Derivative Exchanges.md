up:: [[Derivatives MOC]]
tags:: #Finance 
# Exchanges
- Exchanges guarantee product exchange (removal of counterparty [[Credit Risk]])
	- Become the counterparty to the agreement
- Guarantee quality
- Modularize commodities (ex: 5000 bushels of corn per future)
## Floor Mechanics
- Pit traders and screen traders communicate real time via headset
	- Companies make trades both in the pit and on electronic venues
- Brokers are outside of the pit to relay orders to "off floor" parties
	- **Off floor parties:** hedge funds, banks, corporate consumers, corporate producers, pension funds, retail investors (includes E-traders), other brokers ([[Market Makers]])
- Local: a market maker that only functions in 1 pit (ex: a guy only trading corn)
## Order Routing, Trading, Checking (The Pits)
- The process:
	1) off floor party gets a quote from broker 
	2) Broker asks market makers in pit for quote, which is both a bid and ask. The intention of whether to sell or not does not have to be disclosed, and it better to not be so he gets a proper quote
	3) Best quote gets relayed to off floor party
	4) Off floor party tells broker to buy or sell at quote
	5) Broker arranges the deal with the traders -> order size can be split among parties so long as the price aligns
	6) Documentation: traders fill in a ticket of their transaction and broker fills on on off market party's behalf
	7) Tickets are collected by reps from each firm to check against one another
	8) After prices are agreed upon, trades are sent to clearing houses (record keeping firms) (see [[Futures Market Mechanics]])
## Electronic Markets
- Features
	- Instant quote
	- Instant documentation
	- Clearing houses are plugged into system
	- Much less room for human error
- How it works:
	- **Exchange matching engine:** server that takes in quotes and matches to generate trades
	- Housed in a co-located server farm (see below)

![[Pasted image 20240628134237.png]]

## Co-Location
- The best trading firms have their servers located as close to the exchange as possible for lowest latency
- Nanoseconds can make a huge difference
- Server sends amending quotes to the **exchanges matching engine**
- Any components that require low latency are housed directly in the co-located server
	- Pre-calculated values
	- IOC orders
	- FPGAs (chips)
- Can interact with the server from anywhere in the world

## OTC Markets
- Neither on trading floor (pit) nor on screen
- Done through direct negotiation
- Significantly more counterparty [[Credit Risk]]