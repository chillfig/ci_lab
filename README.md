# Core Flight System : Framework : App : Command Ingest Lab

This repository contains NASA's Command Ingest Lab (ci_lab), which is a framework component of the Core Flight System.

This lab application is a non-flight utility to send commands to the cFS Bundle. It is intended to be located in the `apps/ci_lab` subdirectory of a cFS Mission Tree.  The Core Flight System is bundled at https://github.com/nasa/cFS (which includes ci_lab as a submodule), which includes build and execution instructions.

ci_lab is a simple command uplink application that accepts CCSDS telecommand packets over a UDP/IP port. It does not provide a full CCSDS Telecommand stack implementation.

## Version Notes
- 2.3.2: DEVELOPMENT
  - Use OSAL socket API instead of BSD sockets
  - Remove PDU introspection code
  - Update command and telemetry logic
  - Collect globals as a single top-level global structure
  - Minor changes, see https://github.com/nasa/ci_lab/pull/38
- 2.3.1: DEVELOPMENT
  - Code style and enforcement (see https://github.com/nasa/ci_lab/pull/31)
- **2.3.0 OFFICIAL RELEASE**:
  - Minor updates (see https://github.com/nasa/ci_lab/pull/12)
  - Not backwards compatible with OSAL 4.2.1
  - Released as part of cFE 6.7.0, Apache 2.0
- **2.2.0a OFFICIAL RELEASE**:
  - Released as part of cFE 6.6.0a, Apache 2.0

## Known issues

Dependence on cfe platform config header is undesirable, and the check is not endian safe.  As a lab application, extensive testing is not performed prior to release and only minimal functionality is included.

## Getting Help

For best results, submit issues:questions or issues:help wanted requests at https://github.com/nasa/cFS.

Official cFS page: http://cfs.gsfc.nasa.gov
