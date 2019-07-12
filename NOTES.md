Problems:
- How to know whether consensus version of a block is correct before inserting it in the storage? As block would fail insertion if not connected to genesis, perform (potentially lazy) dirty lookups of preceding blocks.
- How to know whether consensus versions of multiple blocks are correct before obtaining connection to chain? (Sync.)

Where is version of block read?
- aec_headers:validate_version
  - TODO Explore.
- In (deletable) assertion in building key block candidate in node.
  - TODO Delete.
- In (deletable) assertion in building micro block candidate in node.

When is version of block written?
- In building block candidate in node.
- In deserializing block from network.
- In deserializing block from user API.
- In deserializing block from DB.
