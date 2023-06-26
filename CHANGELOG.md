# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.1.2](https://github.com/acquire-project/acquire-core-libs/compare/v0.1.1...v0.1.2) - 2023-05-24

### Added

- Nightly releases.
- Device Properties: Storage property metadata.
- Device Properties: A function to set chunking parameters.
- Device Kit: A function to get property metadata for a storage device.
- Device Kit: A function to reserve image shape for a storage device.
- Device HAL: A function to get storage property metadata.
- Device HAL: A function to reserve image shape for a storage device.

### Changed

- Device Properties: The `storage_properties_init` function no longer accepts a `bytes_per_chunk` parameter.

### Fixed

- Compiles with position-independent code.

## 0.1.1 - 2023-05-11