# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [15.2.0] - 2020-03-25
### Added
- Support bootstrap ceph config (#129)
- Run "cephadm check-host" on all minions (#137)
### Fixed
- Improve descriptions of stages and steps (#144)
- Do not omit bootstrap MGR from "ceph orch apply mgr" (#136)
- Use new OSD creation syntax (#133)
- Work around podman/runc bug (#134)

## [15.1.1] - 2020-03-18
### Added
- Add "Admin" role (#121)
- Support config export and import (#90)
- Add "status" command (#112)
- Automatically set chooseleaf type if needed (#105)
- Improve error handling when calling salt commands (#89)
- Rename ceph-bootstrap to ceph-salt (#93)
### Fixed
- Use `cephadm pull` instead of `podman pull` (#122)
- Handle execution errors (#126)
- Fix error when deploying additional mgrs (#119)
- Bump PyYAML dependency (#117)
- No default value for Ceph container image path (#115)
- Work around timing issue in cephadm device list (#109)
- Renamed "host" field to "hostname" (#111)
- Use "ceph orch daemon add mon" to add remaining MONs (#108)
- Tell ceph orch the right number of mgrs (#106)
- Add `--skip-prepare-host` to `cephadm bootstrap` (#98)
- Fix salt job return event processing (#95)
- Check os_family before executing zypper command (#92)
- Eliminate implicit dependency on which (#85)
### Removed
- Migrate ceph-bootstrap-qa to sesdev (#88)

## [15.1.0] - 2020-02-17
### Added
- System update and reboot during deployment (#11)
- Ensure ceph-salt-formula is loaded by the salt-master before deploy (#65)
- Automatic pillar setup (#8)
- Check salt-master is up and running (#61)
- Wait more verbosely on QA ceph_health_test (#62)
### Fixed
- Rename calls to Ceph Orchestrator Apply (#80)
- Rename calls to Ceph Orchestrator (#73)
- Explicitly install podman (#72)

## [15.0.2] - 2020-01-29
### Added
- New "deploy" command with real-time feedback (#9)
- Use salt-event bus to notify about execution progress (#30)
- Initial integration testing (#33)
### Fixed
- Require root privileges (#18)
- Remove salt python API terminal output (#10)
- Hide Dashboard password (#48)
- Fixed error when deploying without any role (#45)
- Fixed error when deploying without any time server (#40)
- Fixed bootstrap help message (#36)

## [15.0.1] - 2020-01-17
### Added
- Each config shell command now returns a success or error message (#13)
- Moved ceph-salt-formula into ceph-bootstrap project as a subpackage (#26)
### Fixed
- Check if minion FQDN resolves to loopback IP address (#21)
- Fixed "help" command when help text is not provided (#14)
- Fixed "bootstrap_mon" update when the last MON is removed (#17)
- Minions without role are also added to "ceph-salt:minions:all" (#22)
- Fix minion removal upon error (#24)

## [0.1.0] - 2019-12-12
### Added
- Mgr/Mon roles configuration
- Configuration of drive groups specifications to be used in OSD deployment
- Ceph-dashboard credentials configuration
- Ceph daemon container image path configuration
- Control Mon/Mgr/OSD deployment with enable/disable flags

## [0.0.1] - 2019-12-03
### Added
- `sesboot`: CLI tool
- RPM spec file.
- Minimal README.
- The CHANGELOG file.

[Unreleased]: https://github.com/ceph/ceph-salt/compare/v15.2.0...HEAD
[15.2.0]: https://github.com/ceph/ceph-salt/releases/tag/v15.2.0
[15.1.1]: https://github.com/ceph/ceph-salt/releases/tag/v15.1.1
[15.1.0]: https://github.com/ceph/ceph-salt/releases/tag/v15.1.0
[15.0.2]: https://github.com/ceph/ceph-salt/releases/tag/v15.0.2
[15.0.1]: https://github.com/ceph/ceph-salt/releases/tag/v15.0.1
[0.1.0]: https://github.com/ceph/ceph-salt/releases/tag/v0.1.0
[0.0.1]: https://github.com/ceph/ceph-salt/releases/tag/v0.0.1
