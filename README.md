# Eth-Swap

The EthSwap smart contract enables users to perform instant token swaps on the Ethereum blockchain. The contract allows users to purchase tokens from the contract by sending Ether and sell tokens to the contract in exchange for Ether. The contract uses a fixed rate to calculate the amount of tokens to be purchased/sold based on the amount of Ether.

## Contract Details

- **Solidity Version Compatibility**: ^0.8.0

## State Variables

- `name` (string): The name of the EthSwap instant exchange.

- `token` (Token): A reference to the Token contract representing the ERC-20 token to be traded.

- `rate` (uint): The fixed rate used to calculate the number of tokens to be purchased/sold based on the amount of Ether.

## Events

1. `TokensPurchased(address account, address token, uint amount, uint rate)`: This event is emitted when a user purchases tokens from the contract using Ether.

2. `TokensSold(address account, address token, uint amount, uint rate)`: This event is emitted when a user sells tokens to the contract in exchange for Ether.

## Functions

1. `constructor(Token _token)`: The constructor function to initialize the EthSwap contract with the Token contract address.

2. `buyTokens() public payable`: Allows users to purchase tokens by sending Ether to the contract. The function calculates the number of tokens based on the sent Ether, transfers tokens to the user, and emits a TokensPurchased event.

3. `sellTokens(uint _amount) public`: Allows users to sell tokens to the contract in exchange for Ether. The function calculates the amount of Ether to be redeemed, transfers tokens from the user to the contract, and sends Ether to the user. It emits a TokensSold event.

## Note

This documentation provides an overview of the EthSwap smart contract and its functionalities. The contract enables instant token swaps on the Ethereum blockchain by allowing users to purchase tokens from the contract with Ether and sell tokens to the contract for Ether. Before deploying or interacting with any smart contract, it is crucial to conduct a thorough code review, audit the contract's security, and understand the implications of each function. The contract uses a fixed rate to perform token swaps, and users should be aware of the conversion rates before interacting with the contract.
