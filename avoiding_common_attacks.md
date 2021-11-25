Contract security measures
SWC-103 (Floating pragma)
Specific compiler pragma 0.8.3 used in the final project.

SWC-105 (Unprotected Ether Withdrawal)
- The Withdraw is protected with OpenZeppelin Ownable's onlyOwner modifier with other modifiers such as nonReentrant.
- The custom modifier IsRefundable is to ensure the existance of the driver.

SWC-104 (Unchecked Call Return Value)
- The Withdraw payanel shall return a boolean value to determine the withdraw  status, whether is succeed or failed. 

Modifiers used only for validation
All modifiers in contract(s) only validate data with require statements.
There are some custom modifiers to ensure the data and process are legitimate. 
- PaidEnough - Ensure Driver has sufficient fund
- IsRefundable - Ensure the existance of the driver
- isNotOnwner - Owner is not allowed booking
- canBook - No double booking is allowed. (Proposal enhancement in future  will allow to have multiple booking)


Pull over push
All functions that modify state are based on receiving calls rather than making contract calls.