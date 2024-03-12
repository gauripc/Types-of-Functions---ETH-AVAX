# ERC20 FUNGIBLE TOKEN
This Solidity program is a "fungible token" creator program that demonstrates how ERC20 contract is extended and used to create customized fungible tokens in Solidity programming language. The purpose of this program is display how fungible tokens are created in EVMs

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. This contract has multiple functions to interact with the Fungible token contract. We use mint to mint tokens which can only be called by the owner of the contract. Also multiple other functions like transfer, approve are present.

## Getting Started

### Executing program

Executing program To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: UNLICENSED
pragma solidity ^0.8.9;
import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
contract Token is ERC20{
    address public owner;
    constructor(string memory name,string memory symbol) ERC20(name,symbol){
        owner=msg.sender;
    }

    modifier onlyOwner{
        require(msg.sender==owner,"Only owner can do this");
        _;
    }

    function mint(address _to,uint a mount) public onlyOwner {
        _mint(_to,amount);
    }

}
```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.9" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Token" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the sayHello function. Click on the "HelloWorld" contract in the left-hand sidebar, and then click on multiple functions available. Finally, click on the "transact" button to execute the function and retrieve the appropriate messages.

## Authors

Gauri Gupta 
[@gauripc](https://github.com/gauripc)
