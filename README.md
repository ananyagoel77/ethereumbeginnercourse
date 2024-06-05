**Project title: Token Smart Contract**

**Introduction:**

This Ethereum smart contract is coded in Solidity and  establishes a unique token. It allows for the creation of new tokens and the removal of existing ones. The contract guarantees that tokens cannot be removed if the sender's balance is too low.

**Characteristics:**

- Accessible variables for storing token details like name, abbreviation, and total supply.

- Mapping for monitoring each address's token balance.

- Function for generating new tokens and eliminating current tokens with necessary validations.

**Contract Details**


- **Variables**

**tokenName(string):** The name of the token.

**tokenAbbrv(string):** The abbreviation for the token.

**totalSupply(uint):** The total amount of token in circulation.

- **Mapping**

**balances:** A mapping that links addresses to their respective token balances.

- **Constructor**

The constructor initializes the token's name, abbreviation, and initial supply. The initial supply is assigned to the contract deployer.

- **Functions**
  
**mint(address _add, uint _amount):** This function increases the overall token supply and adds the specified amount to the balance of the provided address.

**burn(address_add, uint_amount):** This function decreases the overall token supply and substract the specific amount from the balance of the given address. It ensure that the address's balance is greater or euqal to the burned before proceeding

**Usage**


- **Deployment:** for deploying the contract , we need to provide token name, abbrevation and intial supply during deployment
- **Minting Token:** To create new tokens, use the mint function and provide the address and the amount of tokens to be minted. For instance, if you want to add 100 tokens to the address 0xAbc123..., you can call mint(0xAbc123..., 100).
- **Burning token:** To remove token, use the burn function and specified the address and the amount of tokens to be burned. For instance, if you want to substract 50 tokens from the address 0xAbc123....., you can call the burn(0xAbc123...., 50), but only if the balance is enough.

**License**
This contract is licensed under the MIT License. SPDX-License-Identifier: MIT.


