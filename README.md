# SolidityFinalProject

This solidity program is the final project which demonstrates code that creates a simple token contract. This will give Solidity newbies a fast overview of the methods used to produce tokens, to burn, and check the balances. 

# Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The functions in this contract can be used to create tokens and burn them. Once the code is deployed, how the user entered data will determine how the code is executed. The purpose of this program is to impart a little bit of Solidity knowledge to beginners.  

# Getting Started

Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

    pragma solidity 0.8.18;

    contract MyToken {

    string public tokenName = "Cresilda";
    string public tokenAbbrv = "Cres";
    uint public totalSupply = 0;

    mapping(address => uint) public balances;

    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value; 
    }
        function burn(address _address, uint _value) public {
        totalSupply -= _value;
        balances[_address] -= _value; 
    }
    }

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile SolidityProject.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken - SolidityProject.sol" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by expanding the area below the address which is the Deployed Contracts area. Expand your deployed contract by clicking the arrow button at the left side of it.

Once done, you may now interact with your created contruct. Just input the needed data such as address(just copy the Account address), and the value of your token, as well as how many tokens you want to burn. 

You have to start with creating a value in the "mint" to create your tokens, then click transact in order for you to deploy the changes. You may check it by clicking the "balances". Once you're done putting a value in your mint, you may input a value of your tokens you want to burn, then click transact to deploy the changes. 

Note: Everytime you transact in the mint section, the balances and totalSupply of your tokens will increase, it is because of the operation we use(+=). In order for you to decrease the value, you must input a value in the burn section that does not exceed to the current value in the balances or totalSupply.

# Authors

Cresilda Alcansado

# License

This project is licensed under the MIT License - see the LICENSE.md file for details
