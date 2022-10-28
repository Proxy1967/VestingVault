# Vesting contract

Vesting is the process of locking and distributing purchased tokens within a given timeframe. A particular timeframe that determines vesting is known as the "Vesting Period" - It basically delays the access to the assets being offered.

This contract handles the vesting of Eth and ERC20 tokens for a given beneficiary. Custody of multiple tokens can be given to this contract, which will release the token to the beneficiary following a given vesting schedule.

### Functions

* constructor 
    * should be owned by the deployer of the contract
    * should be deployed with a set recipient (beneficiery)
* receive()
* getBeneficiary()
* getStart()
* getDuration()
* getReleasedETH()
* getReleasedToken(token)
* release()
* release(token)
* vestedAmount(timestamp)
* vestedAmount(token, timestamp)
* _vestingSchedule(totalAllocation, timestamp)

### Events

* EtherReleased(amount)
* ERC20Released(token, amount)
