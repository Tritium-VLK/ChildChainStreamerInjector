# periodicRewardsInjector

This contract is meant to be called by chainlink uplink.  It is used in cases where DAOs wish to add extra yields to their Balancer Gaugue emisisons and want more granular control than using the gauge system would allow.


The tests are based on LDO on Arbitrum where a multisig is curerntly doing these operations.


LDO tokens are sent into the contract and are meant to be stored there.

A list is setup with gauges, amounts, and numbers of epochs.

The ChildChainStreamer has its own sense of epochs, this contract waits until the stream says it is ready, and then asks chainlink to trigger it and send in the alotted number of tokens.
