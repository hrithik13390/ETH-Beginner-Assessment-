Driving License Smart Contract

Overview

> This Solidity program is a simple contract that checks the eligibility for a driving license based on the user's age. The purpose of this program is to demonstrate basic conditional checks, error handling using require, assert, and revert, and provide a foundation for more complex Solidity programming tasks.

Description
> This program consists of a smart contract written in Solidity, used for developing smart contracts on the Ethereum blockchain. The contract has two main functions:

checkEligibility: Checks if a person is eligible for a driving license based on their age.
applyForLicense: Demonstrates the use of revert to handle the case where the applicant's age is below 18.
> The checkEligibility function uses require to ensure the applicant's age is 18 or above, assert to perform an additional check that the age is exactly 18, and returns appropriate messages based on the age. The applyForLicense function uses revert to handle cases where the applicant is too young to apply.

Getting Started

Executing Program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website.

1. Create a New File:

> Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar.

> Save the file with a .sol extension (e.g., DrivingLicense.sol).

> Copy and paste the following code into the file:
solidity
Copy code
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract DrivingLicense {
    // Function to check eligibility for driving license
    function checkEligibility(uint _age) public pure returns (string memory) {
        // Check if age is 18 or above
        require(_age >= 18, "You must be 18 or above to drive");

        // If age is 18, congratulate the applicant and assert age is exactly 18
        if (_age == 18) {
            assert(_age == 18);
            return "Congratulations! You are now eligible for a driving license";
        }

        // If age is above 18, return eligibility message
        return "You are eligible to drive";
    }

    // Function to demonstrate revert if age is below 18
    function applyForLicense(uint _age) public pure returns (string memory) {
        // Revert if age is below 18
        if (_age < 18) {
            revert("You are not eligible to drive, age must be 18 or above");
        }

        // Return eligibility message
        return "You are eligible to apply for a driving license";
    }
}
2. Compile the Code:

> Click on the "Solidity Compiler" tab in the left-hand sidebar.

> Make sure the "Compiler" option is set to a compatible version, such as "0.8.0".

> Click on the "Compile DrivingLicense.sol" button.

3. Deploy the Contract:

> Once the code is compiled, go to the "Deploy & Run Transactions" tab in the left-hand sidebar.

> Select the "DrivingLicense" contract from the dropdown menu.

> Click on the "Deploy" button.

4. Interact with the Contract

> Once the contract is deployed, you can interact with it by calling the checkEligibility and applyForLicense functions.

> Click on the "DrivingLicense" contract in the left-hand sidebar.

> Click on the checkEligibility function, enter an age, and click "transact" to see if the person is eligible for a driving license.

> Click on the applyForLicense function, enter an age, and click "transact" to see if the person can apply for a driving license.

Authors

HRITHIK

@HRITHIK RANJAN

License

This project is licensed under the MIT License - see the LICENSE.md file for details.
