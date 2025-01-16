up:: [[Computer Science MOC]]
tags:: #Programming  
# FIX Protocol
- Messaging system used in real time financial market communication
	- [[Trading Processes]]
	- [[Derivatives MOC]]
	- [[FX MOC]]
- **Purpose**:
    - FIX is designed to standardize and streamline the electronic trading process. It facilitates communication for trading and market data dissemination.
    - It is used for various types of financial transactions, including equities, fixed income, foreign exchange, derivatives, and more.
- **Participants**:
    - Investment banks, broker-dealers, institutional investors, exchanges, and electronic communication networks (ECNs) use FIX to execute trades and share market data.
- **Benefits**:
    - **Interoperability**: Allows different systems and platforms to communicate seamlessly, reducing the complexity of integration.
    - **Speed**: Ensures fast and reliable communication, which is crucial for high-frequency trading and real-time market data.
    - **Transparency**: Enhances transparency and regulatory compliance by providing a standardized format for transaction reporting.
- **Message Types** (examples)
	- **New Order - Single (D)**: To submit a new order.
	- **Execution Report (8)**: To provide execution details of an order.
	- **Order Cancel Request (F)**: To request the cancellation of an existing order.

## Example
`8=FIX.4.2|9=176|35=D|49=BUYER|56=SELLER|34=2|52=20240725-09:30:05.000|11=13579|21=1|55=IBM|54=1|38=100|40=2|44=120.50|59=0|10=157|
`
- `8=FIX.4.2` specifies the FIX protocol version.
- `35=D` indicates a New Order - Single message.
- `49=BUYER` and `56=SELLER` are the sender and target identifiers, respectively.
- `55=IBM` is the stock symbol for IBM.
- `54=1` indicates a buy order.
- `38=100` specifies the quantity.
- `44=120.50` sets the price at $120.50.