# SimpleBank.sol
SimpleBank.sol
pragma solidity ^0.8.20;
contract SimpleBank {
    mapping(address => uint) public balance;

    function deposit() public payable {
        balance[msg.sender] += msg.value;
    }

    function getBalance() public view returns(uint){
        return balance[msg.sender];
    }
}
