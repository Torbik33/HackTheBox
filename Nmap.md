# Nmap Command Cheat Sheet

## Target Selection
| Command                           | Description                           |
|-----------------------------------|---------------------------------------|
| `10.10.10.0/24`                   | Target network range.                 |

## Scan Types
| Command                           | Description                           |
|-----------------------------------|---------------------------------------|
| `-sn`                             | Disables port scanning.               |
| `-Pn`                             | Disables ICMP Echo Requests.          |
| `-n`                              | Disables DNS Resolution.              |
| `-PE`                             | Performs the ping scan using ICMP Echo Requests against the target. |
| `--packet-trace`                  | Shows all packets sent and received.  |
| `--reason`                        | Displays the reason for a specific result. |
| `--disable-arp-ping`              | Disables ARP Ping Requests.           |

## Port Scanning
| Command                           | Description                           |
|-----------------------------------|---------------------------------------|
| `--top-ports=<num>`               | Scans the specified top ports that are most frequent. |
| `-p-`                             | Scan all ports.                       |
| `-p22-110`                        | Scan all ports between 22 and 110.    |
| `-p22,25`                         | Scans only the specified ports 22 and 25. |
| `-F`                              | Scans top 100 ports.                  |

## Advanced Scan Types
| Command                           | Description                           |
|-----------------------------------|---------------------------------------|
| `-sS`                             | Performs a TCP SYN-Scan.              |
| `-sA`                             | Performs a TCP ACK-Scan.              |
| `-sU`                             | Performs a UDP Scan.                  |
| `-sV`                             | Scans the discovered services for their versions. |
| `-sC`                             | Perform a Script Scan with "default" scripts. |
| `--script <script>`               | Performs a Script Scan using the specified scripts. |
| `-O`                              | Performs an OS Detection Scan.        |
| `-A`                              | Performs OS Detection, Service Detection, and traceroute scans. |
| `-D RND:5`                        | Sets the number of random Decoys used to scan the target. |
| `-e`                              | Specifies the network interface used for the scan. |
| `-S 10.10.10.200`                 | Specifies the source IP address for the scan. |
| `-g`                              | Specifies the source port for the scan. |
| `--dns-server <ns>`               | DNS resolution using a specified name server. |

---

## Output Options
| Nmap Option                       | Description                           |
|-----------------------------------|---------------------------------------|
| `-oA filename`                    | Stores the results in all formats starting with "filename". |
| `-oN filename`                    | Stores the results in normal format with the name "filename". |
| `-oG filename`                    | Stores the results in "grepable" format with the name "filename". |
| `-oX filename`                    | Stores the results in XML format with the name "filename". |

---

## Performance Options
| Nmap Option                       | Description                           |
|-----------------------------------|---------------------------------------|
| `--max-retries <num>`             | Sets the number of retries for scans of specific ports. |
| `--stats-every=5s`                | Displays scan's status every 5 seconds. |
| `-v`/`-vv`                        | Displays verbose output during the scan. |
| `--initial-rtt-timeout 50ms`      | Sets the initial RTT timeout to the specified time. |
| `--max-rtt-timeout 100ms`         | Sets the maximum RTT timeout to the specified time. |
| `--min-rate 300`                  | Sets the number of packets sent simultaneously. |
| `-T <0-5>`                        | Specifies the timing template.        |
