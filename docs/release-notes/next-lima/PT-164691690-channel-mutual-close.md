- The [```channel_close_mutual```](https://github.com/aeternity/protocol/blob/master/channels/ON-CHAIN.md#channel_close_mutual) 
transaction can now be performed while the channel is not active (The channel is being closed unilaterally and a dispute may or may not be ongoing), 
this is a consensus breaking change available after the Lima fork.
- The state channel FSM after the Lima fork accepts a shutdown message while the channel is being closed unilaterally.
- If one of the peers refuses signing the closing transaction while the channel is not active then the request may timeout without killing the FSM.
