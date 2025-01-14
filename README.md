# Azure Keyvault Encryption/Decryption in C++ and Rust

This repo has programs which retrieve a key from an Azure Key Vault and then encrypt or decrypt messages with it.

The encryption program is written in C++ and is in the `encrypt` folder. The decryption program is written in Rust and is in the `decrypt` folder.

## Building

### `encrypt`

Install [vcpkg](https://vcpkg.io/), then:

```
$ vcpkg install azure-identity-cpp:x64-windows-static azure-security-keyvault-keys-cpp:x64-windows-static
```

Then build with CMake using your prefered method.


### `decrypt`

```
$ cargo build
```
