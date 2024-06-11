# Token creation
This project showcases the creation of a custom token on the Ethereum blockchain utilizing Solidity, the main programming language for Ethereum smart contracts. The repository contains the Solidity source code, deployment scripts, and detailed instructions for setting up and deploying your own token.
## Description
This project serves as a comprehensive guide to developing a custom token on the Ethereum blockchain with Solidity. It walks through the entire process, from coding the Solidity contract to deploying the token on the Ethereum network. The goal is to offer a clear grasp of essential concepts related to smart contracts and token creation, empowering developers to create their own tokens for various uses, including Initial Coin Offerings (ICOs), decentralized applications (dApps), and other blockchain-based initiatives.
This project is an in-depth guide to creating a custom token on the Ethereum blockchain using Solidity. It covers the entire process from writing the Solidity code to deploying the token on the Ethereum network. The project aims to provide a clear understanding of the fundamental concepts of smart contracts and token creation, making it easier for developers to create their own tokens for various applications such as Initial Coin Offerings (ICOs), decentralized applications (dApps), and other blockchain-based projects.
## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:
contract MyToken {

    // public variables here
string public tokenName="Abhishek";
string public tokenAbbrv="Abhik";
uint public totalSupply=0;
    // mapping variable here
    mapping (address=>uint)  public remainingBalances;

    // mint function
    function mint (address to,uint value) public{
        totalSupply+= value ;remainingBalances[to] += value ;
    }
 // burn function
    function burn (address from ,uint value) public{
        if (remainingBalances[from]>=value) {
            totalSupply-= value;remainingBalances[from]-= value;
        }
    }

}

   
   



To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can use the deployed contract interface in Remix to call functions like transfer, balanceOf, etc.
## Authors

Abhishek Pratap Singh
[@Abhishek Pratap Singh](https://pratapsinghabhishek671@gmail.com)


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
