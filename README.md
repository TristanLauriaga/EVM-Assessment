# EVM-Assessment
This is my work for our subject IT Elect 1 at the National Teachers College. Metacrafters assessed us on making our own token and write a solidity code that mints and burns them on a account and let us see the balance of the said account.

## Description
This solidity program is my 1st ever smart contract this program is a simple token program I made my own token named "Nobel" (derived from the word "Nobel Prize") and this program's functions are minting or adding my token to the given account and burning subtracts my token to the accounts balance. This program is a learning step for me because I am just on the tip of the iceberg when it comes to web 3. It will help me on learning Web 3 much easier in the future.

## Getting Started
### Installing

* We dont have to install anything to our device, we can use Remix, an online solidity, Here is the websire https://remix.ethereum.org/.

### Executing program

* To run this program, I used Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

* I have saved my program by clicking the "+" in the workspaces tab, Then I saved the file as a .sol file (EVM:Assessment.sol) because I usedvsolidity to code this assessment. This is my Code below:

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
I have compiled the code by clicking the "soldity compiler" at the left-hand side of the compiler. I chose the version 0.8.18 version of solidity, (Note: Make sure that the version that is writen in your code is the same as the version of the compiler that you are using).

Once that the code is compiled. I went to the "Deploy and run transactions" at the left-hand side of the compiler, there I deployed my smart contract.

After deploying my smart contract I test it and interacted with all of the functions, I called the variables "tokenName", "TokenAbrv" and "totalSupply" then I test also the mapping variable, then the minting function and the burn function.

After testing and troubleshooting my code, Using Loom I took a video explaining and demonstrating my code, you can watch it here https://www.loom.com/share/3e60ef94a1784da8a79a67f396e3e6aa?sid=923945ce-21a2-46f2-a735-24346a1a1e93.

## Author

Lancetristan B. Lauriaga
[IG: @tristanaenaeeee]
[2.1 BSIT]
[The National Teacher College, Quiapo Manila.]

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
