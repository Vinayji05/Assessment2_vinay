Project : To Create a Token

In this project we have created a token called 'MyToken' to create and manage a basic cryptocurrency token named "Algo Coin" (AC) on the Ethereum blockchain. The primary functions is to allow users to mint new tokens , increasing the total supply , and to burn existing tokens , decreasing the total supply.

description

The MyToken project is a smart contract implementation on the Ethereum blockchain , designed to create a simple yet functional cryptocurrency token named "Algo Coin" (AC). The project aims to provide a foundational understanding of token creation , supply management , and basic knowledge of tokens within the decentralized ecosystem.

Getting Started

Installing

Their Is No Need To Install Anything.

Executing program

How to run run the program :-

1.Search remix on the browser.

2.Open the remix.

3.Write your code.

4.compile the code.

5.Then deploy the code.

Block of code :-

      SPDX-License-Identifier: MITpragma solidity 0.8.18;
               
       REQUIREMENTS
    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    2. Your contract will have a mapping of addresses to balances (address => uint)
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount
    4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
    5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.
      contract MyToken {

     // public variables here
     string public tokenName ="algo coin";
     string public tokenAbbrv = "AC";
     uint public totalSupply = 1;

     // mapping variable here

     mapping(address => uint) public balances;
     // mint function

     function mint (address _address, uint _value) public {
     totalSupply += _value;
     balances[_address] += _value;
     }
     // burn function

     function burn (address _address, uint _value) public {
     if (balances[_address] >= _value) {
     totalSupply -=_value;
     balances[_address] -= _value;
     }
     }
     } 

Help

Contract Compilation Errors occurs

Advise is that always check your Solidity Version

Auhtor

Name : Vinay

Contract info : vinayseh244@gmail.com

License

This project is licensed under the name Vinay License - see the LICENSE.md file for details.





