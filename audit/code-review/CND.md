# CND

Source file [../../contracts/CND.sol](../../contracts/CND.sol).

<br />

<hr />

```javascript
// BK Ok
pragma solidity ^0.4.15;


// BK Ok
import "./MiniMeToken.sol";


/**
 * @title Cindicator Token
 *
 * @dev Simple ERC20 Token
 */
// BK Ok
contract CND is MiniMeToken {
  /**
    * @dev Constructor
  */
  // BK Ok
  uint256 public constant IS_CND_CONTRACT_MAGIC_NUMBER = 0x1338;
  // BK Ok
  function CND(address _tokenFactory)
    MiniMeToken(
      _tokenFactory,
      0x0,                      // no parent token
      0,                        // no snapshot block number from parent
      "Cindicator Token",   // Token name
      18,                       // Decimals
      "CND",                    // Symbol
      true                      // Enable transfers
    ) 
    {}

    // BK Ok - Reject all ETH payments
    function() payable {
      // BK Ok
      require(false);
    }
}

```
