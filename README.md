# ETH-Proof
### Creating a Token

"CREATING A TOKEN" code that showcases the fundamental syntax and features of the Solidity programming language is this Solidity code. With a token name, token abbreviation, and token total supply, this codes aims to create tokens.

## Description

Written in Solidity, a programming language used to create smart contracts on the Ethereum blockchain, this program is a straightforward contract. The contract has minting features as well as a burn function.Two parameters are required for its mint function: an address and a value. The function then raises the address's balance by that amount and the total supply by that number. It features a burn function that destroys tokens, operating in opposition to the mint function. In the same way as the mint operates, it will require an address and value. The amount will then be subtracted from both the address's balance and the total supply. 


## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., myToken.sol). Copy and paste the following code into the file
```javascript
//SPDX-License-Identifier: MIT
pragma solidity 0.8.26;

contract PratikToken
{
    //public variables here
    string public tokenName = "Pratik";
    string public tokenAbbrivation = "Bnerjee";
    uint public totalSupply = 0;

    //mapping variable here
    mapping(address => uint )public balances;

    //mint function
    function mint (address _address,uint _value) public
    {
        totalSupply = totalSupply + _value;
        balances[_address] += _value;

    }

    //burn function
    function burn (address _address,uint _value) public
    {
        if(balances[_address] >= _value)
        {
        totalSupply = totalSupply - _value;
        balances[_address] -= _value;
        }

    }
}

```





To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.26" (or another compatible version), and then click on the "Compile PratikToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "AryanToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint function and burn function. Click on the "PratikToken" contract in the left-hand sidebar, and then click on the "mint" function and put values of address and value. Finally, click on the "transact" button to execute the function will do the changes in totalSupply and value at that particular address. Similarly you can use burn function by giving appropriate paramters of address and value and thus clicking on the "transact" will subtract the given value from the already present value at that particular address. 

## Authors

PRATIK BANERJEE  

[mrbanerjeekajal10@gmail.com]


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
