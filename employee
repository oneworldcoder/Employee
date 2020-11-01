pragma solidity >=0.4.0 <0.7.0;

contract Employee {

    struct employee {
        string name;
        string bloodGroup;
        uint age;
        uint height;
    }
    
    mapping(address => employee) public employees;
    

    function setEmployee(string memory name, string memory bloodGroup, uint age, uint height) public {
        address creator = msg.sender;
        
        employee memory newEmployee;
        newEmployee.name = name;
        newEmployee.bloodGroup = bloodGroup;
        newEmployee.age = age;
        newEmployee.height = height;
        employees[creator] = newEmployee;
    }
    
    function getEmployee() public view returns (string memory name, string memory bloodGroup, uint age, uint height) {
        address creator = msg.sender;
        return (employees[creator].name, employees[creator].bloodGroup, employees[creator].age, employees[creator].height);
    }

    
}
