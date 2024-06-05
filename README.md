**Project title: Token Smart Contract**

**Introduction:**

This Ethereum smart contract is coded in Solidity and  establishes a unique token. It allows for the creation of new tokens and the removal of existing ones. The contract guarantees that tokens cannot be removed if the sender's balance is too low.

**Characteristics:**

- Accessible variables for storing token details like name, abbreviation, and total supply.

- Mapping for monitoring each address's token balance.

- Function for generating new tokens and eliminating current tokens with necessary validations.

Contract Details


Variables

tokenName: The name of the token.

tokenAbbrv: The abbreviation for the token.

totalSupply: The total amount of token in circulation.

Mappings

balances: A mapping that links addresses to their respective token balances.

Functions

mint(address _add, uint _amount): This function increases the overall token supply and adds the specified amount to the balance of the provided address.

burn(address_add, uint_amount): This function decreases the overall token supply and substract the specific amount from the balance of the given address. It ensure that the address's balance is greater or euqal to the burned before proceeding

Usage


Deployment 

for deploying the contract , we need to provide token name, abbrevation and intial supply during deployment


