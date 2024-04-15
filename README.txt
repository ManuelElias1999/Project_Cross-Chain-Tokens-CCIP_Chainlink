# TransferUSDCBasic Smart Contract

This Solidity smart contract facilitates the transfer of USDC tokens from the Avalanche Fuji network to another network, in this case, the Sepolia network (assuming it is properly configured on the CCIP network).

## Functionalities

- Transfer USDC from the Avalanche Fuji network to the Sepolia network.
- Check USDC balances and allowances.
- Withdraw any remaining tokens in the contract by the owner.

## Dependencies

The contract depends on the following Chainlink contracts for its operation:

- `IRouterClient`: Interface for interacting with the CCIP contract.
- `Client`: Library for creating and manipulating CCIP messages.
- `IERC20`: Interface for interacting with ERC20 tokens.
- `SafeERC20`: Library for performing safe ERC20 token transfers.

## Usage

1. Deploy the contract on the Avalanche Fuji network.
2. Users can call the `transferUsdcToSepolia` function by providing the receiver's address and the amount of USDC to transfer.
3. The contract will verify USDC balances and allowances, calculate the CCIP fee, and perform the transfer if all conditions are met.
4. The owner can call the `withdrawToken` function to withdraw any remaining tokens in the contract.

## Important Notes

- This contract is an example and should not be used in production without proper auditing.
- It is assumed that the CCIP contract, LINK, and USDC contract addresses are correctly configured for the specified test networks.
