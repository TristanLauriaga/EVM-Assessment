# EVM-Assessment
This is my work for our subject IT Elect 1 at the National Teachers College. Metacrafters assessed us on making our own token and write a solidity code that mints and burns them on a account and let us see the balance of the said account.

## Description
This solidity program is my 1st ever smart contract this program is a simple token program I made my own token named "Nobel" (derived from the word "Nobel Prize") and this program's functions are minting or adding my token to the given account and burning subtracts my token to the accounts balance. This program is a learning step for me because I am just on the tip of the iceberg when it comes to web 3. It will help me on learning Web 3 much easier in the future.

## Getting Started
### Installing

* We dont have to install anything to our device, we can use Remix, an online solidity, Here is the websire https://remix.ethereum.org/.

### Executing program

* To run this program, I used Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

* I have saved my program by clicking the "+" in the workspaces tab, Then I saved the file as a .sol file (EVM:Assessment.sol) because I usedvsolidity to code this assessment.

```javascript
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    string public tokenName = "NOBEL";
    string public tokenAbrv = "NBL";
    uint public totalSupply = 0;
    
    mapping(address => uint) public balances;

    function mint(address _add, uint _val) public  {
        totalSupply += _val;
        balances[_add] += _val;
    }

    function burn(address _add, uint _val) public  {
        if (balances[_add] >= _val ){
            totalSupply -= _val;
            balances[_add] -= _val;
        }  
    }
}
```
