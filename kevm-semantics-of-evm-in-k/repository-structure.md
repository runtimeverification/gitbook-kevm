# Repository Structure

### Repository Structure

The following files constitute the KEVM semantics:

* network.md provides the status codes reported to an Ethereum client on execution exceptions.
* json-rpc.md is an implementation of JSON RPC in K.
* evm-types.md provides the (functional) data of EVM (256-bit words, wordstacks, etc...).
* serialization.md provides helpers for parsing and unparsing data (hex strings, recursive-length prefix, Merkle trees, etc.).
* evm.md is the main KEVM semantics, containing EVM’s configuration and transition rules.

These additional files extend the semantics to make the repository more useful:

* buf.md defines the `#buf` byte-buffer abstraction for use during symbolic execution.
* abi.md defines the [Contract ABI Specification](https://docs.soliditylang.org/en/v0.8.1/abi-spec.html) for use in proofs and easy contract/function specification.
* hashed-locations.md defines the `#hashedLocation` abstraction used to specify Solidity-generated storage layouts.
* edsl.md combines the previous three abstractions for ease-of-use.
* foundry.md adds Foundry capabilities to KEVM.

These files are used for testing the semantics itself:

* state-utils.md provides functionality for EVM initialization, setup, and querying.
* driver.md is an execution harness for KEVM, providing a simple language for describing tests/programs.
