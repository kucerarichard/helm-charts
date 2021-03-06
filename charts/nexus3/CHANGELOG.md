# Nexus 3 Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

<!-- ## [UNRELEASED]

### Added

### Changed

### Deprecated

### Removed -->

## v3.2.1 - 2020-09-21

### Changed

- Allow boolean attributes to be set for tasks

## v3.2.0 - 2020-09-04

### Changed

- Upgraded image to _v3.27.0_

## v3.1.3 - 2020-09-02

### Changed

- n/a

## v3.1.2 - 2020-08-17

### Changed

- Upgraded image to _v3.26.1_

## v3.1.1 - 2020-08-11

### Added

- New `envVars.jvmAdditionalOptions` value

### Changed

- Replaced `envVars.jvmMaxDirectMemorySize` with `envVars.jvmAdditionalMemoryOptions`

## v3.1.0 - 2020-08-11

### Changed

- Upgraded image to _v3.26.0_

## v3.0.0 - 2020-08-05

### Added

- Image pull secret support
- Service account creation or selection
- Service account annotations
- Service annotations
- PVC annotations
- Role configuration supported

### Changed

- Upgraded image to _v3.25.1_
- Better documentation of values
- Changed default service port to `8081` which matches the container port
- Changed the way the JVM heap is configured to align with the [Nexus 3 docs](https://help.sonatype.com/repomanager3/installation/system-requirements#SystemRequirements-Memory), use `env.jvmMinHeapSize` & `env.jvmMaxHeapSize`
- Renamed `securityContext` to `podSecurityContext` (`securityContext` now refers to the security context of the main container)
- Require `caCerts.enabled` to be set to `true` to use provided certs
- Configuration updated to use REST API where possible
- LDAP config values have changed
- Cleanup script has been updated to work correctly on _Nexus v3.25.0_
- Repo script has been updated to work correctly on _Nexus v3.25.0_

### Removed

- Support of RAM percentage in the JVM configuration (see changed section above)
