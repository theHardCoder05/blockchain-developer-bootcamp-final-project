Design patterns used
Access Control Design Pattern
Ownable design pattern used in three functions:  Withdraw() and addCar(). The key idea is ONLY the Owner can perform the withdraw or refund the deposit back to the driver. Ideally, the addCar function should defer to an address(operator) who has the "Operator" Role.
Inheritance and Interfaces
- Import Openzepplin Smart Contracts for all kind of security best pratices and folllowing the guideline.
- Created custom intfaces to implement interface design pattern (SOLID) principle.
External Call design pattern
- Created an external call deisgn pattern contract to act as a Ochestration layer to absctract the business logics contracts.
