# solidity

This Solidity program is a coin that store the detail of the coin, it demonstrates the function of parameters and contract

## Description

The program is a simple contract written in Solidity, a programming language used for developing smart function on the Ethereum blockchain. This program serves as a simple and straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

contract MyToken {


string public tokenName = "Meta";
string public tokenAbrrv = "MTA";
uint public totalSupply = 0;
 
mapping (address => uint) public balances;
  
function mint (address _address, uint _value) public  {
  totalSupply += _value;
  balances[_address] += _value;
}
    
function burn (address _address, uint _value) public {
  if (balances[_address] >= _value){
    totalSupply -= _value;
    balances[_address] -= _value;
  }
}
}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "HelloWorld" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the sayHello function. Click on the "HelloWorld" contract in the left-hand sidebar, and then click on the "sayHello" function. Finally, click on the "transact" button to execute the function and retrieve the "Hello World!" message.

## Authors

NTC Patrick Ibabao


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
