
# Changelog

All notable changes to Zk-Arithmos will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

<div align="center">

[![Release](https://img.shields.io/github/v/release/zk-arithmos/zk-arithmos?style=flat-square)](https://github.com/zk-arithmos/zk-arithmos/releases)
[![Commits](https://img.shields.io/github/commits-since/zk-arithmos/zk-arithmos/latest?style=flat-square)](https://github.com/zk-arithmos/zk-arithmos/commits/main)

</div>

---

## [Unreleased]

### 🚀 Added
- Recursive proof composition support for PLONK backend
- New `zk-arithmos-recursion` crate for proof aggregation
- WebGPU acceleration for browser-based proving
- Noir language compatibility layer
- Incremental verification for streaming proofs
- Custom gate API for PLONKish constraints
- Lookup table support for PLONK backend
- New `RangeProof` gadget with optimized constraints
- Batch verification API for multiple proofs
- Memory-mapped witness provider for large circuits
- ARM64 optimizations for Apple Silicon
- Python bindings via PyO3
- Solidity verifier generator improvements

### 🔄 Changed
- Improved constraint reduction in optimization pipeline (15% average reduction)
- Refactored field trait hierarchy for better extensibility
- Updated BLS12-381 implementation for 10% performance improvement
- Enhanced error messages with source location tracking
- Migrated to workspace dependencies for better version management
- Improved parallel proving scalability beyond 32 cores

### 🐛 Fixed
- Fixed edge case in Poseidon hash for certain input lengths
- Corrected witness solver for cyclic constraint dependencies
- Fixed memory leak in long-running proof generation sessions
- Resolved race condition in parallel constraint evaluation
- Fixed incorrect constraint count reporting in circuit statistics

### 🔒 Security
- Updated `ark-ec` to address timing side-channel (ZKA-2024-0003)
- Improved constant-time field inversion implementation
- Added additional validation for deserialized proof elements

### ⚠️ Deprecated
- `Circuit::synthesize_legacy()` - use `Circuit::synthesize()` instead
- `WitnessBuilder::set()` - use `WitnessBuilder::assign()` instead
- Old constraint format in DSL - migration guide available

### 🗑️ Removed
- Nothing removed in this release

---



### 🎉 Highlights

**Zk-Arithmos 1.0.0 marks our first stable release!** This release represents months of development, testing, security audits, and community feedback. We're committed to semantic versioning from this point forward.

Key highlights:
- **Stable API**: Public APIs are now stable and will follow semver
- **Production Ready**: Comprehensive testing and security audits completed
- **Full Documentation**: Complete API documentation and user guide
- **Three Proof Systems**: Groth16, PLONK, and Marlin fully supported

### 🚀 Added

#### Core Features
- **Stable Field Trait System**
  - Generic `Field` trait with complete arithmetic operations
  - `PrimeField` trait for prime field specific operations
  - `ExtensionField` trait for field extensions
  - Serialization traits for all field types

- **Wire and Gate System**
  - Type-safe wire references with lifetime management
  - Complete gate algebra: Add, Mul, Sub, Div, Neg
  - Boolean gates: And, Or, Xor, Not
  - Comparison gates with efficient decomposition
  - Custom gate support for advanced use cases

- **Constraint Systems**
  - R1CS (Rank-1 Constraint System) with optimization
  - PLONKish constraint system with custom gates
  - Automatic constraint format conversion
  - Constraint visualization and debugging tools

#### Circuit Building
- **Circuit Builder API**
  - Fluent builder pattern for circuit construction
  - Automatic wire management and allocation
  - Namespace support for modular circuits
  - Circuit composition and reuse

- **Expression System**
  - High-level mathematical expressions
  - Automatic flattening to constraints
  - Expression optimization passes
  - Debug mode for expression tracing

- **Gadget Library**
  - Arithmetic: `Add`, `Mul`, `Div`, `Pow`, `Sqrt`
  - Boolean: `And`, `Or`, `Xor`, `Not`, `BooleanCheck`
  - Comparison: `IsZero`, `IsEqual`, `LessThan`, `RangeCheck`
  - Cryptographic: `Poseidon`, `MiMC`, `Pedersen`, `MerkleProof`
  - Signatures: `EdDSA`, `ECDSA` verification
  - Utilities: `Select`, `MultiSelect`, `ArrayAccess`

#### Proof Systems
- **Groth16 Backend**
  - Complete Groth16 implementation
  - Per-circuit trusted setup
  - Optimized prover with parallelization
  - Sub-millisecond verification

- **PLONK Backend**
  - Universal trusted setup support
  - Custom gate definitions
  - Lookup argument support
  - Recursive proof friendly

- **Marlin Backend**
  - Transparent setup option
  - Updatable SRS support
  - Algebraic holographic proofs
  - Efficient batch verification

#### Witness Generation
- **Witness Providers**
  - `MemoryProvider`: In-memory witness storage
  - `LazyProvider`: On-demand computation
  - `StreamingProvider`: Memory-efficient streaming
  - Custom provider trait for extensions

- **Witness Solver**
  - Automatic intermediate value computation
  - Dependency resolution
  - Parallel witness generation
  - Constraint satisfaction validation

#### Developer Tools
- **Command-Line Interface**
  - `compile`: DSL to circuit compilation
  - `setup`: Proving/verifying key generation
  - `prove`: Proof generation
  - `verify`: Proof verification
  - `inspect`: Circuit and proof inspection
  - `export`: Format conversion utilities

- **DSL Compiler**
  - Complete lexer and parser
  - Type inference and checking
  - Semantic analysis
  - Multi-level optimization
  - Readable error messages

- **Debugging Tools**
  - Constraint violation detection
  - Wire value tracing
  - Circuit visualization
  - Performance profiling

#### Integrations
- **Serialization**
  - Serde support for all types
  - Binary format for efficiency
  - JSON format for interoperability
  - Backward-compatible versioning

- **WebAssembly**
  - WASM compilation support
  - Browser-based verification
  - JavaScript bindings
  - Memory-optimized for web

- **FFI**
  - C ABI for language bindings
  - Stable ABI guarantees
  - Error handling across FFI boundary
  - Memory management documentation

### 🔄 Changed
- Finalized all public APIs for 1.0 stability
- Improved documentation with examples for every public item
- Enhanced error types with actionable messages
- Optimized default configuration for common use cases
- Standardized naming conventions across all crates

### 🐛 Fixed
- All known bugs from 0.x series resolved
- Memory safety verified by Miri
- Thread safety verified by loom
- Fuzzing campaign completed with no findings

### 🔒 Security
- Completed security audit by [Auditor Name]
- All audit findings remediated
- Constant-time implementations verified
- Supply chain security measures implemented

### 📚 Documentation
- Complete API documentation
- User guide and tutorials
- Architecture documentation
- Security documentation
- Migration guides from other libraries

---



### 🎉 Highlights

Release candidate for 1.0. Focus on API stabilization, performance optimization, and documentation completion.

### 🚀 Added

- **Performance Optimizations**
  - SIMD acceleration for field operations (x86_64 AVX2)
  - Improved parallel proving with better work distribution
  - Memory pool for reduced allocations
  - Optimized polynomial operations

- **New Gadgets**
  - `SHA256` gadget for compatibility with existing systems
  - `Blake2s` gadget for efficient hashing
  - `Keccak256` gadget for Ethereum compatibility
  - `ECDSA` verification gadget (secp256k1)

- **Tooling**
  - Circuit size estimator before synthesis
  - Gas cost estimator for on-chain verification
  - Proof compression utilities
  - Benchmark suite with regression detection

- **Integrations**
  - Ethereum contract templates for verification
  - Solana program integration guide
  - Substrate pallet example
  - CosmWasm contract template

### 🔄 Changed

- **API Refinements**
  - Renamed `Circuit::build()` to `Circuit::synthesize()` for clarity
  - Changed `Proof::verify()` signature to take verifying key by reference
  - Updated `WitnessBuilder` API for better ergonomics
  - Simplified error types hierarchy

- **Performance**
  - 25% improvement in Groth16 proving time
  - 40% reduction in peak memory usage
  - 2x faster constraint generation
  - Optimized serialization format

- **Dependencies**
  - Updated `ark-*` crates to 0.4.2
  - Updated `rand` to 0.8.5
  - Updated `rayon` to 1.8
  - Removed unused dependencies

### 🐛 Fixed

- Fixed incorrect proof generation for circuits with no public inputs
- Resolved panic when deserializing malformed proofs
- Corrected witness solver for deeply nested gadgets
- Fixed CLI progress bar rendering on Windows
- Resolved compilation issue on 32-bit platforms

### ⚠️ Deprecated

- `Circuit::build()` - use `Circuit::synthesize()` (removed in 1.0)
- `Proof::verify_with_vk()` - use `Proof::verify()` (removed in 1.0)
- `legacy` feature flag - all legacy code removed in 1.0

### 🔒 Security

- Fixed timing side-channel in field comparison (ZKA-2024-0002)
- Improved randomness handling in proof generation
- Added input validation for all public APIs
- Implemented secure memory zeroing for secrets

---


### 🎉 Highlights

Major feature release introducing the DSL compiler, PLONK backend, and comprehensive gadget library.

### 🚀 Added

- **DSL Compiler** (`zk-arithmos-dsl`)
  - Custom language for circuit definition
  - Type system with inference
  - Module system for code organization
  - Standard library of common functions
  - Syntax highlighting for VS Code

- **PLONK Backend**
  - Full PLONK implementation
  - Universal setup support
  - Custom gate API
  - Optimized for recursion

- **Gadget Library Expansion**
  - Poseidon hash with configurable parameters
  - Merkle tree proofs up to depth 32
  - Range proofs with configurable bit width
  - Comparison gadgets for all orderings
  - Binary decomposition gadgets

- **Developer Experience**
  - VS Code extension for DSL
  - Language server protocol support
  - Real-time error checking
  - Go-to-definition and hover docs

- **Testing Utilities**
  - Property-based testing helpers
  - Fuzzing harness
  - Constraint satisfiability checker
  - Mock witness generator

### 🔄 Changed

- Restructured crate hierarchy for modularity
- Improved error message formatting
- Updated circuit statistics reporting
- Enhanced parallel execution strategy
- Refined public API surface

### 🐛 Fixed

- Fixed stack overflow for very large circuits
- Resolved incorrect optimization in constant folding
- Corrected Poseidon constants for certain field sizes
- Fixed CLI argument parsing for complex commands
- Resolved documentation build issues

### ⚠️ Deprecated

- Old circuit definition macros (use DSL instead)
- Manual constraint construction (use gadgets)

### 🔒 Security

- Initial security review completed
- Input validation improved across all APIs
- Secure defaults for all configurations

---

## [0.7.0] - 2024-07-01

### 🎉 Highlights

Introduction of the Marlin proof system and witness solving capabilities.

### 🚀 Added

- **Marlin Backend**
  - Complete Marlin implementation
  - Transparent setup mode
  - Updatable setup support
  - Batch verification

- **Witness Solver**
  - Automatic intermediate value computation
  - Constraint-based solving
  - Dependency graph analysis
  - Parallel computation

- **CLI Enhancements**
  - `inspect` command for circuit analysis
  - `export` command for format conversion
  - JSON output option for all commands
  - Verbose mode with detailed logging

- **Field Implementations**
  - Goldilocks field (64-bit prime)
  - Mersenne-31 field
  - Arbitrary precision field for testing
  - Field serialization traits

### 🔄 Changed

- Improved constraint optimization algorithms
- Better memory management for large circuits
- Updated proof serialization format (v2)
- Enhanced error reporting

### 🐛 Fixed

- Fixed incorrect constraint generation for division
- Resolved memory leak in iterative proving
- Corrected bit decomposition for edge cases
- Fixed Windows path handling in CLI

---

## [0.6.0] - 2024-05-01

### 🎉 Highlights

GPU acceleration support and improved parallelization.

### 🚀 Added

- **GPU Acceleration**
  - CUDA backend for NVIDIA GPUs
  - OpenCL backend for cross-platform support
  - Automatic fallback to CPU
  - Multi-GPU support

- **Parallel Proving**
  - Improved work distribution
  - NUMA-aware allocation
  - Configurable thread pool
  - Progress reporting

- **New Gadgets**
  - MiMC hash function
  - Pedersen commitments
  - ElGamal encryption verification
  - Schnorr signature verification

- **Benchmarking**
  - Criterion-based benchmarks
  - Comparison with other libraries
  - Automated regression detection
  - Detailed performance reports

### 🔄 Changed

- Refactored parallel execution engine
- Improved memory allocation strategy
- Updated dependency versions
- Enhanced configuration options

### 🐛 Fixed

- Fixed race condition in parallel constraint evaluation
- Resolved GPU memory management issues
- Corrected benchmark accuracy
- Fixed documentation typos

---

## [0.5.0] - 2024-03-01

### 🎉 Highlights

Introduction of the gadget system and comprehensive boolean operations.

### 🚀 Added

- **Gadget System**
  - `Gadget` trait for reusable components
  - Gadget composition
  - Parameterized gadgets
  - Gadget documentation

- **Boolean Gadgets**
  - Complete boolean algebra
  - Bit decomposition
  - Bit recomposition
  - Conditional selection

- **Comparison Gadgets**
  - Less than with configurable bits
  - Greater than
  - Equality checking
  - Range checking

- **Documentation**
  - API reference for all public items
  - Gadget usage examples
  - Architecture overview
  - Contributing guide

### 🔄 Changed

- Simplified constraint API
- Improved type inference
- Better error messages
- Cleaner code organization

### 🐛 Fixed

- Fixed boolean constraint generation
- Resolved issue with nested gadgets
- Corrected documentation links
- Fixed example code

---



### 🎉 Highlights

Groth16 proving system implementation and proof serialization.

### 🚀 Added

- **Groth16 Prover**
  - Complete Groth16 implementation
  - Trusted setup generation
  - Parallel proof generation
  - Proof verification

- **Serialization**
  - Binary proof format
  - Key serialization
  - Circuit serialization
  - Version compatibility

- **CLI Foundation**
  - Basic command structure
  - Setup command
  - Prove command
  - Verify command

- **Testing**
  - Integration test suite
  - Prover/verifier tests
  - Serialization tests
  - CLI tests

### 🔄 Changed

- Restructured project layout
- Updated R1CS representation
- Improved build configuration
- Enhanced CI/CD pipeline

### 🐛 Fixed

- Fixed R1CS matrix construction
- Resolved key generation issues
- Corrected proof format
- Fixed test failures

---


### 🎉 Highlights

R1CS constraint system implementation and basic circuit operations.

### 🚀 Added

- **R1CS Constraint System**
  - Linear combination representation
  - Constraint generation
  - Matrix construction
  - Constraint validation

- **Basic Operations**
  - Addition constraints
  - Multiplication constraints
  - Equality constraints
  - Constant handling

- **Circuit Builder**
  - Wire allocation
  - Constraint registration
  - Input handling
  - Output designation

- **Testing Framework**
  - Unit test structure
  - Test utilities
  - Example circuits
  - Property tests

### 🔄 Changed

- Improved type system
- Better module organization
- Enhanced documentation
- Cleaner API design

### 🐛 Fixed

- Fixed wire allocation
- Resolved constraint duplication
- Corrected linear combination
- Fixed documentation

---



### 🎉 Highlights

Wire abstraction and basic field trait implementation.

### 🚀 Added

- **Wire System**
  - Wire type with lifetime
  - Wire value abstraction
  - Public/private designation
  - Wire reference handling

- **Field Traits**
  - Basic `Field` trait
  - Arithmetic operations
  - Field element creation
  - Zero and one constants

- **BN254 Field**
  - Scalar field implementation
  - Optimized arithmetic
  - Serialization
  - Random element generation

- **Project Structure**
  - Workspace configuration
  - Crate separation
  - Documentation setup
  - CI configuration

### 🔄 Changed

- Initial API design
- Module structure
- Error handling approach
- Documentation format

---



### 🎉 Highlights

Initial release of Zk-Arithmos! This release establishes the foundation for the project.

### 🚀 Added

- **Project Foundation**
  - Initial project structure
  - Cargo workspace setup
  - Basic README
  - License files (MIT/Apache-2.0)

- **Core Types**
  - Basic type definitions
  - Error type foundation
  - Result type aliases
  - Module structure

- **Development Setup**
  - CI/CD configuration
  - Rustfmt configuration
  - Clippy configuration
  - Git hooks

- **Documentation**
  - Initial README
  - Contributing guidelines
  - Code of conduct
  - Security policy

### Notes

This is the initial release establishing the project structure and basic types. No functionality is usable at this stage.

---



#### From 0.9.x

Minimal changes required:

```rust
// Before (0.9.x)
let circuit = Circuit::build(&mut cs)?;

// After (1.0.0)
let circuit = Circuit::synthesize(&mut cs)?;
```

```rust
// Before (0.9.x)
proof.verify_with_vk(&vk, &public_inputs)?;

// After (1.0.0)
proof.verify(&vk, &public_inputs)?;
```

#### From 0.8.x

1. Update deprecated method calls:
   ```rust
   // Replace
   Circuit::build() → Circuit::synthesize()
   Proof::verify_with_vk() → Proof::verify()
   WitnessBuilder::set() → WitnessBuilder::assign()
   ```

2. Update DSL syntax for constraints:
   ```
   // Before
   constraint a * b = c;
   
   // After
   assert a * b == c;
   ```

3. Review changed default configurations

#### From 0.7.x or earlier

We recommend a fresh integration rather than incremental upgrade due to significant API changes. See the [Migration Guide](./docs/migration.md) for detailed instructions.

---

## Release Process

Our release process ensures quality and stability:

### Pre-Release Checklist

- [ ] All tests passing on CI
- [ ] No known critical bugs
- [ ] Documentation updated
- [ ] CHANGELOG updated
- [ ] Security review completed
- [ ] Performance benchmarks acceptable
- [ ] Breaking changes documented
- [ ] Migration guide written (if needed)

### Release Steps

1. **Version Bump**: Update version in all Cargo.toml files
2. **Changelog**: Move unreleased items to new version section
3. **Tag**: Create signed Git tag
4. **Build**: Create release builds
5. **Publish**: Publish to crates.io
6. **Announce**: Post release announcement

### Version Numbering

We follow [Semantic Versioning](https://semver.org/):

- **MAJOR**: Breaking API changes
- **MINOR**: New features, backward compatible
- **PATCH**: Bug fixes, backward compatible

Pre-release versions use suffixes:
- `-alpha.N`: Early development, unstable
- `-beta.N`: Feature complete, testing
- `-rc.N`: Release candidate, final testing

---

## Contributing to Changelog

When contributing, please add changelog entries under `[Unreleased]`:

### Entry Format

```markdown
### Category
- Brief description of change ([#PR](link)) by [@author](link)
```

### Categories

- 🚀 **Added**: New features
- 🔄 **Changed**: Changes in existing functionality
- 🐛 **Fixed**: Bug fixes
- 🔒 **Security**: Security improvements
- ⚠️ **Deprecated**: Features to be removed
- 🗑️ **Removed**: Removed features
- 📚 **Documentation**: Documentation improvements
- 🧪 **Testing**: Test improvements

### Guidelines

1. Write in imperative mood ("Add feature" not "Added feature")
2. Include PR/issue reference
3. Keep entries concise but descriptive
4. Group related changes
5. Highlight breaking changes clearly

---

## Links

### Release Downloads

- [GitHub Releases](https://github.com/zk-arithmos/zk-arithmos/releases)
- [crates.io](https://crates.io/crates/zk-arithmos)

### Documentation

- [API Documentation](https://docs.rs/zk-arithmos)
- [User Guide](https://zk-arithmos.dev/docs)
- [Migration Guides](./docs/migration.md)

### Verification

All releases are signed. Verify with:

```bash
# Download signature
curl -LO https://github.com/zk-arithmos/zk-arithmos/releases/download/v1.0.0/zk-arithmos-1.0.0.tar.gz.asc

# Verify
gpg --verify zk-arithmos-1.0.0.tar.gz.asc zk-arithmos-1.0.0.tar.gz
```

### Checksums

SHA-256 checksums for all releases are available at:
- Release page on GitHub
- `checksums.txt` in each release

---

<div align="center">

**Questions about a release?**

[Open an issue](https://github.com/zk-arithmos/zk-arithmos/issues/new) or [join Discord](https://discord.gg/zkarithmos)

---

*This changelog is maintained by the Zk-Arithmos team and community contributors.*

</div>

```

---

This comprehensive CHANGELOG.md includes:

1. **Standard Format** - Following Keep a Changelog conventions
2. **Semantic Versioning** - Clear version numbering with explanations
3. **Complete History** - All versions from 0.1.0 to 1.0.0 and unreleased
4. **Categorized Changes** - Added, Changed, Fixed, Security, Deprecated, Removed
5. **Emoji Categories** - Visual indicators for change types
6. **Highlights Section** - Key features for each release
7. **Version Summary Table** - Quick reference for all versions
8. **Upgrade Guides** - Migration instructions between versions
9. **Release Process** - Documentation of release procedures
10. **Contributing Guidelines** - How to add changelog entries
11. **Links Section** - Downloads, documentation, verification
12. **Comparison Links** - GitHub compare links for all versions