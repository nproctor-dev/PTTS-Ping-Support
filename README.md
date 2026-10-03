# PTTS Ping 1.1.0

PTTS Ping is a prebuilt native Qt6 desktop application for monitoring multiple
hosts on Linux. It is **Proprietary Freeware**.

## Download

### Latest Linux release

**[Download PTTS Ping for Ubuntu / Debian (.deb)](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/latest/download/ptts-ping_amd64.deb)**

[SHA256 checksum](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/latest/download/ptts-ping_amd64.deb.sha256)

[Latest release notes](https://github.com/nproctor-dev/PTTS-Ping-Support/releases/latest) | [PTTS Ping website](https://pttsllc.com/software/ptts-ping/) | [Support](https://github.com/nproctor-dev/PTTS-Ping-Support/issues)

### Easy installation

1. Download `ptts-ping_amd64.deb`.
2. Open the downloaded file with your Linux software installer.
3. Click **Install**.
4. Launch **PTTS Ping** from your application menu.

Or from a terminal:

```sh
sudo apt install ./ptts-ping_amd64.deb
```

No development tools or manual Qt installation are required.

![PTTS Ping monitoring overview](screenshots/ptts-ping-overview.png)

## Monitoring

- Continuous monitoring of IP addresses and hostnames, with latency and
  success/failure/packet-loss counters. Interval changes take effect immediately;
  unfinished batches prevent overlapping cycles. Large lists update progressively.
- **Last Failure** records the latest applied failed result in local time.
- **Failure Duration** shows the current continuous outage using monotonic time;
  recovery clears the duration but preserves Last Failure.
- **Flapping** highlights unstable hosts using recent results and configurable
  window/threshold controls, as illustrated below.
- Clear Counters resets counters and flap history while preserving Last Failure,
  current status, and active outage timing. Changing Flap Window restarts only
  flap history; changing the threshold reevaluates retained samples immediately.
- Reverse DNS enriches unnamed IP entries without occupying ping workers.
  Resolver calls have no application-controlled timeout and may delay process
  exit after the window closes.
- Numeric IP sorting, read-only results, user-resizable columns, horizontal
  scrolling, and a draggable vertical host-input/results splitter.
- Save List / Load List use UTF-8; saves replace files atomically. The last host
  list and window size/state, splitter allocation, and column widths are remembered.
  Under Wayland, exact top-level window placement may remain controlled by the
  compositor/window manager.

Each new Start begins a fresh monitoring session. Stopped or superseded results
cannot update the new session. Unknown latency is displayed as `--`.

## Flapping detection

Flapping requires both successful and failed samples, at least two UP/DOWN
transitions, and a failure percentage at or above the selected threshold within
the rolling Flap Window. **YES** appears yellow with black text and can occur
while the host is currently UP or DOWN. Expired history clears the indication
automatically without requiring a new ping.

| Flapping while currently UP | Flapping while currently DOWN |
| --- | --- |
| ![Flapping detected on an UP host](screenshots/ptts-ping-flapping-up.png) | ![Flapping detected on a DOWN host](screenshots/ptts-ping-flapping-down.png) |

## Monitoring controls

**Interval** controls how often a new ping cycle starts; unfinished cycles never
overlap. **Flap Window** selects how far back results are retained (default
5 minutes, range 1–60). **Failure threshold** sets the minimum failed-ping
percentage needed for flapping (default 20%, range 1–100); the transition and
mixed-result requirements still apply.

Hover over a control label or value for help contained within the PTTS Ping window.

![In-application hover help for monitoring controls](screenshots/ptts-ping-hover-help.png)

## Host input

Enter one target or named entry per line:

```text
192.0.2.10
example.com
server01<TAB>198.51.100.20
server01,198.51.100.20
server01 198.51.100.20
203.0.113.10-203.0.113.20
```

Replace `<TAB>` with an actual tab. A tab/comma row must have exactly two fields;
its target must be nonempty. An empty name uses the target as its display name.
Whitespace-separated rows accept a single target or `Name Target`.

IPv4 ranges allow whitespace around `-` and at most **4096 addresses**.
Reversed or malformed numeric ranges are rejected. Ordinary hyphenated hostnames
remain supported. Malformed input is rejected before monitoring starts, with a
line-numbered warning. Option-like targets beginning with `-` are rejected.

## Requirements

The native amd64 package is package-tested on Ubuntu 24.04 LTS and Ubuntu 26.04.
APT installs the required Qt6 runtime libraries and `iputils-ping` automatically.
No development tools or manual Qt setup are required. Other distributions require
their own testing.

## Install, upgrade, and uninstall

Download `ptts-ping_amd64.deb`, then install or upgrade from its directory:

```sh
sudo apt install ./ptts-ping_amd64.deb
```

Uninstall:

```sh
sudo apt remove ptts-ping
```

Monitoring preferences are stored in portable `settings.ini`; the UTF-8 host
list remains in `last_hosts.txt`. Window/splitter/header and sort state belong
to machine/display-local `ui.ini`. Per-user runtime files are separate from the
package; upgrades do not overwrite them:

```text
~/.config/ptts-ping/settings.ini
~/.config/ptts-ping/last_hosts.txt
~/.config/ptts-ping/ui.ini
```

Optional user-state removal:

```sh
rm -rf ~/.config/ptts-ping
```

This deletes saved monitoring preferences, host input, and UI layout state. Removing the package alone
leaves that user state intact. Storage failures do not prevent monitoring.

## Support

For bugs, installation problems, questions, or feature requests:

**[Open a GitHub issue](https://github.com/nproctor-dev/PTTS-Ping-Support/issues/new/choose)**

Please include your PTTS Ping version, Linux distribution/version, what you expected,
what happened instead, and steps to reproduce the problem.

## License

PTTS Ping is **Proprietary Freeware**, not open source. Free personal, educational,
and internal commercial use is permitted. The complete official unmodified
package may be redistributed free of charge under [LICENSE](LICENSE).
Modified/derivative redistribution, sublicensing, and resale are not permitted.
All rights not expressly granted are reserved.

On first launch, missing config files are copied from the development-era
`~/.config/pingview/` directory. Existing PTTS Ping files win; legacy files remain.

Project website: https://pttsllc.com/software/ptts-ping/
