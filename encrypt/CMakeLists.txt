﻿cmake_minimum_required (VERSION 3.15)

project ("azure-test")

set(VCPKG_TARGET_TRIPLET "x64-windows-static")

find_package(azure-security-keyvault-keys-cpp CONFIG REQUIRED)
find_package(azure-identity-cpp CONFIG REQUIRED)

add_executable(azure_encrypt "encrypt/azure-encrypt.cpp")
set_property(TARGET azure_encrypt PROPERTY MSVC_RUNTIME_LIBRARY "MultiThreadedDebug")
target_link_libraries(azure_encrypt PRIVATE Azure::azure-identity Azure::azure-security-keyvault-keys)
