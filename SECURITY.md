# Security Policy

  ## Supported Versions

  This repository provides Bisq-maintained Tor bindings for Kotlin/Java. It is
  used for Tor connectivity, proxy handling, hidden service support, and native or
  external Tor integration.

  Security fixes are applied to the active development branch and any active
  release line still used by supported Bisq applications.

  | Version / Branch | Supported |
  | --- | --- |
  | `master` | :white_check_mark: |
  | Latest `0.7.x` release line while used by supported Bisq applications | :white_check_mark: |
  | Active maintenance branches used by supported Bisq applications | :white_check_mark: |
  | Older release lines, unsupported forks, or locally modified builds | :x: |

  Vulnerabilities in Tor itself should also be reported to the Tor Project
  according to its own security policy. This policy covers the Bisq-maintained
  code in this repository, including Tor startup/configuration, native Tor
  integration, external Tor integration, proxy/socket handling, and packaging.

  ## Reporting a Vulnerability

  Please do **not** report security vulnerabilities through public pull requests,
  Matrix rooms, forums, or social media.

  Report suspected vulnerabilities privately through GitHub's **Report a
  vulnerability** flow on this repository's Security page. If that option is not
  available, contact Bisq maintainers through the main Bisq project security
  channel and ask for a private reporting path. Do not include exploit details in
  public channels.

  Include as much detail as possible:

  - affected branch, commit, release, operating system, and Tor mode;
  - affected module, such as `tor`, `tor.native`, or `tor.external`;
  - whether the issue affects native Tor startup, external Tor usage, torrc
    generation, SOCKS proxy handling, hidden service publication, control-port
    behavior, file permissions, process lifecycle, or bundled resources;
  - whether the issue can expose user IP addresses, onion service keys, private
    network metadata, traffic destinations, Tor control credentials, or application
    identity;
  - reproduction steps, logs, torrc snippets, environment details, or proof of
    concept code where useful;
  - whether the issue depends on a malicious local process, compromised Tor binary,
    malformed Tor output, unsafe temporary files, weak filesystem permissions, or
    unexpected proxy configuration.

  Bisq is an open-source project maintained by contributors. Response times may
  vary, but reports involving possible IP leakage, Tor bypass, onion service key
  exposure, unsafe Tor control access, or traffic deanonymization are treated as
  urgent security issues and will be triaged as quickly as possible.

  For lower-severity issues, maintainers will respond when contributor capacity is
  available.

  If the report is accepted, maintainers may coordinate a fix privately, prepare a
  patched release or dependency update, notify the Tor Project when appropriate,
  and publish an advisory after users have had a reasonable opportunity to update.
  If the report is declined, maintainers will explain the reason when possible.

  Please give maintainers reasonable time to investigate and release mitigations
  before public disclosure. For severe or actively exploited issues, coordinate
  timing with maintainers so public details do not increase risk to users.

  Bisq does not currently guarantee a bug bounty. Security work may be eligible
  for Bisq DAO compensation if it qualifies under the project's contributor and
  critical-bug processes.
