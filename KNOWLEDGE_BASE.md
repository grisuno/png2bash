# Polyglot Codebase Knowledge Graph

> Generated offline by **readmenator**. Supports C, C++, Python, Go, Rust, JS/TS, Java, C#, Shell, PHP, Dart, GDScript, Nim, ASM, Ruby, Swift, Kotlin, Scala, Lua, Elixir.
> No LLMs. No tokens. Pure static analysis. See more [here](https://github.com/grisuno/ReadMenator)

**Total Files Parsed:** 3 | **Total Symbols Extracted:** 72 | **Total Imports:** 36
 | **Resolved Imports:** 1

<!-- ranking_model: v1.0 | weights: {ppr:0.45,auth:0.2,test:0.15,doc:0.1,fresh:0.1} | alpha:0.85 | commit:f0ae16d | date:2026-07-18 -->


## Table of Contents

1. [Statistics Dashboard](#statistics-dashboard)
2. [Architectural Layers](#architectural-layers)
3. [Ranked Context](#ranked-context)
4. [God Nodes](#god-nodes)
5. [Community Analysis](#community-analysis)
6. [Suggested Questions](#suggested-questions)
7. [Taint Propagation Map](#taint-propagation-map)
8. [Hotspot Analysis](#hotspot-analysis)
9. [Change Impact Analysis](#change-impact-analysis)
10. [Suggested Linting Rules](#suggested-linting-rules)
11. [Orphans](#orphans)
12. [Query Recipes](#query-recipes)
13. [Structural Knowledge Map](#structural-knowledge-map)
14. [UML Class Diagram](#uml-class-diagram)
15. [Code Property Graph](#code-property-graph)
16. [Architecture Reference](#architecture-reference)
    - [PY (2 files)](#py-2-files)
    - [SH (1 files)](#sh-1-files)

---

## Statistics Dashboard

| Metric | Value |
|--------|-------|
| Total Files | 3 |
| Total Symbols | 72 |
| Total Imports | 36 |
| Call Edges | 464 |
| Inheritance Edges | 0 |
| Languages | 2 |
| Avg Symbols/File | 24.0 |
| Avg Imports/File | 12.0 |
| Resolved Imports | 1 |

### Top Files by Import Count (Fan-Out)

| File | Imports | Symbols | Language |
|------|---------|---------|----------|
| `utils.py` | 35 | 69 | py |
| `app.py` | 1 | 3 | py |

---

## Architectural Layers

Auto-detected from path patterns, naming conventions, and imported frameworks.

| Layer | Files |
|-------|-------|
| utility | 3 |

### utility

- `app.py` (py, 3 symbols)
- `install.sh` (sh, 0 symbols)
- `utils.py` (py, 69 symbols)

---

## Ranked Context

Files ranked by composite score for the current query context. The ranking combines Personalized PageRank (query relevance), global authority, test coverage, documentation coverage, and code freshness. Model: v1.0.

| Rank | File | Composite | PPR | Authority | Test | Doc |
|------|------|-----------|-----|-----------|------|-----|
| 1 | `utils.py` | 0.3623 | 0.6491 | 0.6491 | 0.00 | 0.96 |
| 2 | `app.py` | 0.2614 | 0.3509 | 0.3509 | 0.00 | 0.33 |
| 3 | `install.sh` | 0.0000 | 0.0000 | 0.0000 | 0.00 | 0.00 |

---

## God Nodes

Most architecturally central files ranked by combined import/export degree and symbol richness.

| File | Score | Connections | PageRank |
|------|-------|-------------|----------|
| `utils.py` | 8.9 | | 0.6491 |
| `app.py` | 2.3 | | 0.3509 |
| `install.sh` | 0.0 | | 0.0000 |

---

## Community Analysis

Files grouped by import-based community detection. Cohesion measures how tightly connected each community is internally.

### root (Cohesion: 1.00)

**2 files** in this community:

- `app.py` (py, 3 symbols)
- `utils.py` (py, 69 symbols)

---

## Suggested Questions

Auto-generated exploration prompts based on graph structure:

- What does utils.py depend on, and what depends on it? (1 connections)
- What does app.py depend on, and what depends on it? (1 connections)
- What does install.sh depend on, and what depends on it? (0 connections)
- What is the overall architecture of this codebase?

---

## Taint Propagation Map

Taint analysis traces how dangerous imports propagate through the codebase via transitive dependencies. Source files import dangerous modules directly; sink files receive the danger indirectly.

**Taint Sources:** 1 | **Taint Sinks:** 1 | **Propagation Paths:** 3

- `utils.py` imports `requests` (0 hop to `utils.py`) [medium]
  Path: utils.py
- `utils.py` imports `subprocess` (0 hop to `utils.py`) [high]
  Path: utils.py
- `utils.py` imports `urllib.request` (0 hop to `utils.py`) [medium]
  Path: utils.py

---

## Hotspot Analysis

Files ranked by combined complexity (symbol count) and centrality (connection count). High-scoring files are architecturally critical and may need refactoring attention.

| File | Complexity | Centrality | Combined | Symbols | Connections |
|------|-----------|------------|----------|---------|-------------|
| `utils.py` | 1.000 | 1.000 | 1.000 | 69 | 36 |
| `app.py` | 0.043 | 0.056 | 0.051 | 3 | 2 |
| `install.sh` | 0.000 | 0.000 | 0.000 | 0 | 0 |

---

## Change Impact Analysis

Files sorted by how many other files would be affected if they changed. High-impact files should be changed with caution.

| File | Direct Dependents | Transitive Dependents | Total Impact |
|------|------------------|----------------------|--------------|
| `utils.py` | 1 | 0 | 1 |
| `app.py` | 0 | 0 | 0 |
| `install.sh` | 0 | 0 | 0 |

---

## Suggested Linting Rules

Automatically suggested linting and security rules based on patterns detected in the codebase. These can be exported as Semgrep rules using the `--export-rules` flag.

| Rule ID | Severity | Description | Language | Matches |
|---------|----------|-------------|----------|---------|
| `RM002` | warning | Bare except clause catches all exceptions including SystemExit | python | 4 |
| `RM001` | info | Large number of functions in py: 72 total | py | 72 |
| `RM003` | info | Print statement found (consider logging instead) | python | 27 |

---

## Orphans

Files with no documentation or low connectivity. These are candidates for documentation investment or cleanup.

- `install.sh` (0 symbols, no doc)

---

## Query Recipes

Example queries you can run against this knowledge base using the ranking engine:

```
# Find files most relevant to a concept
readmenator query "Where is the import resolver implemented?"

# Rank files by relevance to a topic
readmenator query "How does documentation generation work?"

# Explain why a file ranks highly
readmenator query "explain readmenator/_documentation.py"

# Trace dependency paths with ranked context
readmenator query "path from CLI to exporter"
```

The ranking model uses the following signals:

- **Personalized PageRank** (45% weight): query-specific relevance via seed propagation
- **Global Authority** (20% weight): structural importance via standard PageRank
- **Test Coverage** (15% weight): fraction of symbols referenced in test files
- **Doc Coverage** (10% weight): presence of docstrings and file-level docs
- **Freshness** (10% weight): recent modification activity

Results include score decomposition and justification paths for each ranked item.

---

## Structural Knowledge Map

```mermaid
graph TD
    classDef mod fill:#1e1e1e,stroke:#ff6666,stroke-width:2px,color:#fff;
    classDef cls fill:#2d2d2d,stroke:#4ec9b0,stroke-width:2px,color:#fff;
    classDef fn fill:#333,stroke:#dcdcaa,stroke-width:1px,color:#dcdcaa;
    classDef ext fill:#111,stroke:#666,stroke-dasharray:5 5,color:#aaa;
    subgraph community_0 ["root"]
    utils_py["utils.py (py)"]
    class utils_py mod;
    utils_py_parse_ip_mac["parse_ip_mac"]
    class utils_py_parse_ip_mac fn;
    utils_py --> utils_py_parse_ip_mac
    utils_py_create_arp_packet["create_arp_packet"]
    class utils_py_create_arp_packet fn;
    utils_py --> utils_py_create_arp_packet
    utils_py_send_packet["send_packet"]
    class utils_py_send_packet fn;
    utils_py --> utils_py_send_packet
    utils_py_load_version["load_version"]
    class utils_py_load_version fn;
    utils_py --> utils_py_load_version
    utils_py_print_error["print_error"]
    class utils_py_print_error fn;
    utils_py --> utils_py_print_error
    app_py["app.py (py)"]
    class app_py mod;
    install_sh["install.sh (sh)"]
    class install_sh mod;
    end
    app_py -- resolved_imports --> utils_py
    ext_utils["utils"]
    class ext_utils ext;
    app_py -.->|imports| ext_utils
    ext_re["re"]
    class ext_re ext;
    utils_py -.->|imports| ext_re
    ext_os["os"]
    class ext_os ext;
    utils_py -.->|imports| ext_os
    ext_csv["csv"]
    class ext_csv ext;
    utils_py -.->|imports| ext_csv
    ext_sys["sys"]
    class ext_sys ext;
    utils_py -.->|imports| ext_sys
    ext_ssl["ssl"]
    class ext_ssl ext;
    utils_py -.->|imports| ext_ssl
    ext_json["json"]
    class ext_json ext;
    utils_py -.->|imports| ext_json
    ext_time["time"]
    class ext_time ext;
    utils_py -.->|imports| ext_time
    ext_glob["glob"]
    class ext_glob ext;
    utils_py -.->|imports| ext_glob
    ext_shlex["shlex"]
    class ext_shlex ext;
    utils_py -.->|imports| ext_shlex
    ext_pickle["pickle"]
    class ext_pickle ext;
    utils_py -.->|imports| ext_pickle
    ext_signal["signal"]
    class ext_signal ext;
    utils_py -.->|imports| ext_signal
    ext_base64["base64"]
    class ext_base64 ext;
    utils_py -.->|imports| ext_base64
    ext_string["string"]
    class ext_string ext;
    utils_py -.->|imports| ext_string
    ext_ctypes["ctypes"]
    class ext_ctypes ext;
    utils_py -.->|imports| ext_ctypes
    ext_socket["socket"]
    class ext_socket ext;
    utils_py -.->|imports| ext_socket
    ext_struct["struct"]
    class ext_struct ext;
    utils_py -.->|imports| ext_struct
    ext_random["random"]
    class ext_random ext;
    utils_py -.->|imports| ext_random
    ext_binascii["binascii"]
    class ext_binascii ext;
    utils_py -.->|imports| ext_binascii
    ext_readline["readline"]
    class ext_readline ext;
    utils_py -.->|imports| ext_readline
    ext_requests["requests"]
    class ext_requests ext;
    utils_py -.->|imports| ext_requests
    ext_tempfile["tempfile"]
    class ext_tempfile ext;
    utils_py -.->|imports| ext_tempfile
    ext_threading["threading"]
    class ext_threading ext;
    utils_py -.->|imports| ext_threading
    ext_subprocess["subprocess"]
    class ext_subprocess ext;
    utils_py -.->|imports| ext_subprocess
    ext_urllib_parse["urllib.parse"]
    class ext_urllib_parse ext;
    utils_py -.->|imports| ext_urllib_parse
    ext_urllib_request["urllib.request"]
    class ext_urllib_request ext;
    utils_py -.->|imports| ext_urllib_request
    ext_importlib_util["importlib.util"]
    class ext_importlib_util ext;
    utils_py -.->|imports| ext_importlib_util
    ext_PIL["PIL"]
    class ext_PIL ext;
    utils_py -.->|imports| ext_PIL
    ext_itertools["itertools"]
    class ext_itertools ext;
    utils_py -.->|imports| ext_itertools
    ext_bs4["bs4"]
    class ext_bs4 ext;
    utils_py -.->|imports| ext_bs4
    ext_pykeepass["pykeepass"]
    class ext_pykeepass ext;
    utils_py -.->|imports| ext_pykeepass
    ext_libnmap_parser["libnmap.parser"]
    class ext_libnmap_parser ext;
    utils_py -.->|imports| ext_libnmap_parser
    ext_libnmap_process["libnmap.process"]
    class ext_libnmap_process ext;
    utils_py -.->|imports| ext_libnmap_process
    ext_concurrent_futures["concurrent.futures"]
    class ext_concurrent_futures ext;
    utils_py -.->|imports| ext_concurrent_futures
    utils_py -.->|imports| ext_urllib_parse
    ext_modules_lazyencoder_decoder["modules.lazyencoder_decoder"]
    class ext_modules_lazyencoder_decoder ext;
    utils_py -.->|imports| ext_modules_lazyencoder_decoder
```

---

## Code Property Graph

Machine-readable Code Property Graph (CPG) in JSON-LD format. This block allows AI agents to parse the full structural graph without additional file reads. Compatible with GraphRAG pipelines.

```json
{"@context": "https://schema.org", "analysis": {"communities": [{"cohesion": 1.0, "id": 0, "label": "root", "size": 2}], "god_nodes": [{"node_id": "utils.py", "score": 8.9}, {"node_id": "app.py", "score": 2.3}, {"node_id": "install.sh", "score": 0.0}], "surprising_connections": []}, "edges": [{"confidence": "EXTRACTED", "relation": "imports", "source": "app.py", "target": "utils"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "re"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "os"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "csv"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "sys"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "ssl"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "json"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "time"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "glob"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "shlex"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "pickle"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "signal"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "base64"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "string"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "ctypes"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "socket"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "struct"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "random"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "binascii"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "readline"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "requests"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "tempfile"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "threading"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "subprocess"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "urllib.parse"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "urllib.request"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "importlib.util"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "PIL"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "itertools"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "bs4"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "pykeepass"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "libnmap.parser"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "libnmap.process"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "concurrent.futures"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "urllib.parse"}, {"confidence": "EXTRACTED", "relation": "imports", "source": "utils.py", "target": "modules.lazyencoder_decoder"}, {"confidence": "EXTRACTED", "relation": "resolved_imports", "source": "app.py", "target": "utils.py"}], "generator": "readmenator", "metadata": {"edge_count": 501, "file_count": 3, "language_count": 2, "symbol_count": 72}, "nodes": [{"doc": "_*_ coding: utf8 _*_", "id": "app.py", "kind": "module", "label": "app.py", "language": "py", "sha256": "0e3ae23274541435", "symbol_count": 3, "symbols": [{"kind": "function", "line": 27, "name": "image_to_bash", "signature": "def image_to_bash(image_path, image_res)"}, {"kind": "function", "line": 44, "name": "list_png_files", "signature": "def list_png_files()"}, {"kind": "function", "line": 54, "name": "main", "signature": "def main()"}]}, {"id": "install.sh", "kind": "module", "label": "install.sh", "language": "sh", "sha256": "c907d80fd6734993", "symbol_count": 0, "symbols": []}, {"id": "utils.py", "kind": "module", "label": "utils.py", "language": "py", "sha256": "f88d77d2cd1d92f1", "symbol_count": 69, "symbols": [{"doc": "Extracts IP and MAC addresses from a formatted input string using a regular expression.\n\nThe input string is expected to be in the format: 'IP: (192.168.1.222) MAC: ec:c3:02:b0:4c:96'.\nThe function uses a regular expression to match and extract the IP address and MAC address from the input.\n\nArgs:\n    input_string (str): The formatted string containing the IP and MAC addresses.\n\nReturns:\n    tuple: A tuple containing the extracted IP address and MAC address. If the format is incorrect, returns (None, None).", "kind": "function", "line": 128, "name": "parse_ip_mac", "signature": "def parse_ip_mac(input_string)"}, {"doc": "Constructs an ARP packet with the given source and destination IP and MAC addresses.\n\nThe function creates both Ethernet and ARP headers, combining them into a complete ARP packet.\n\nArgs:\n    src_mac (str): Source MAC address in the format 'xx:xx:xx:xx:xx:xx'.\n    src_ip (str): Source IP address in dotted decimal format (e.g., '192.168.1.1').\n    dst_ip (str): Destination IP address in dotted decimal format (e.g., '192.168.1.2').\n    dst_mac (str): Destination MAC address in the format 'xx:xx:xx:xx:xx:xx'.\n\nReturns:\n    bytes: The constructed ARP packet containing the Ethernet and ARP headers.", "kind": "function", "line": 149, "name": "create_arp_packet", "signature": "def create_arp_packet(src_mac, src_ip, dst_ip, dst_mac)"}, {"doc": "Sends a raw ARP packet over the specified network interface.\n\nThe function creates a raw socket, binds it to the specified network interface, and sends the given packet.\n\nArgs:\n    packet (bytes): The ARP packet to be sent.\n    iface (str): The name of the network interface to use for sending the packet (e.g., 'eth0').\n\nRaises:\n    OSError: If an error occurs while creating the socket or sending the packet.", "kind": "function", "line": 186, "name": "send_packet", "signature": "def send_packet(packet, iface)"}, {"doc": "Load the version number from the 'version.json' file.\n\nThis function attempts to open the 'version.json' file and load its contents. \nIf the file is found, it retrieves the version number from the JSON data. \nIf the version key does not exist, it returns a default version 'release/v0.0.14'. \nIf the file is not found, it also returns the default version.\n\nReturns:\n- str: The version number from the file or the default version if the file is not found or the version key is missing.", "kind": "function", "line": 203, "name": "load_version", "signature": "def load_version()"}, {"doc": "Prints an error message to the console.\n\nThis function takes an error message as input and prints it to the console\nwith a specific format to indicate that it is an error.\n\n:param error: The error message to be printed.\n:type error: str\n:return: None", "kind": "function", "line": 224, "name": "print_error", "signature": "def print_error(error)"}, {"doc": "Prints a message to the console.\n\nThis function takes a message as input and prints it to the console\nwith a specific format to indicate that it is an informational message.\n\n:param msg: The message to be printed.\n:type msg: str\n:return: None", "kind": "function", "line": 239, "name": "print_msg", "signature": "def print_msg(msg)"}, {"doc": "Prints a warning message to the console.\n\nThis function takes a warning message as input and prints it to the console\nwith a specific format to indicate that it is a warning.\n\n:param warn: The warning message to be printed.\n:type warn: str\n:return: None", "kind": "function", "line": 255, "name": "print_warn", "signature": "def print_warn(warn)"}, {"doc": "Handles signals such as Control + C and shows a message on how to exit.\n\nThis function is used to handle signals like Control + C (SIGINT) and prints\na warning message instructing the user on how to exit the program using the\ncommands 'exit', 'q', or 'qa'.\n\n:param sig: The signal number.\n:type sig: int\n:param frame: The current stack frame.\n:type frame: frame\n:return: None", "kind": "function", "line": 271, "name": "signal_handler", "signature": "def signal_handler(sig, frame)"}, {"doc": "Checks if the remote host (rhost) is defined and shows an error message if it is not.\n\nThis function verifies if the `rhost` parameter is set. If it is not defined,\nan error message is printed, providing an example and directing the user to\nadditional help.\n\n:param rhost: The remote host to be checked.\n:type rhost: str\n:return: True if rhost is defined, False otherwise.\n:rtype: bool", "kind": "function", "line": 298, "name": "check_rhost", "signature": "def check_rhost(rhost)"}, {"doc": "Checks if the local host (lhost) is defined and shows an error message if it is not.\n\nThis function verifies if the `lhost` parameter is set. If it is not defined,\nan error message is printed, providing an example and directing the user to\nadditional help.\n\n:param lhost: The local host to be checked.\n:type lhost: str\n:return: True if lhost is defined, False otherwise.\n:rtype: bool", "kind": "function", "line": 320, "name": "check_lhost", "signature": "def check_lhost(lhost)"}, {"doc": "Checks if the local port (lport) is defined and shows an error message if it is not.\n\nThis function verifies if the `lport` parameter is set. If it is not defined,\nan error message is printed, providing an example and directing the user to\nadditional help.\n\n:param lport: The local port to be checked.\n:type lport: int or str\n:return: True if lport is defined, False otherwise.\n:rtype: bool", "kind": "function", "line": 342, "name": "check_lport", "signature": "def check_lport(lport)"}, {"doc": "Internal function to verify if a binary is present on the operating system.\n\nThis function checks if a specified binary is available in the system's PATH\nby using the `which` command. It returns True if the binary is found and False\notherwise.\n\n:param binary_name: The name of the binary to be checked.\n:type binary_name: str\n:return: True if the binary is present, False otherwise.\n:rtype: bool", "kind": "function", "line": 364, "name": "is_binary_present", "signature": "def is_binary_present(binary_name)"}, {"doc": "Internal function to handle multiple remote hosts (rhost) for operations.\n\nThis function is a decorator that allows an operation to be performed across\nmultiple remote hosts specified in `self.params[\"rhost\"]`. It converts a single\nremote host into a list if necessary, and then iterates over each host,\nperforming the given function with each host. After the operation, it restores\nthe original remote host value.\n\n:param func: The function to be decorated and executed for each remote host.\n:type func: function\n:return: The decorated function.\n:rtype: function", "kind": "function", "line": 381, "name": "handle_multiple_rhosts", "signature": "def handle_multiple_rhosts(func)"}, {"doc": "Checks if the script is running with superuser (sudo) privileges, and if not,\nrestarts the script with sudo privileges.\n\nThis function verifies if the script is being executed with root privileges\nby checking the effective user ID. If the script is not running as root,\nit prints a warning message and restarts the script using sudo.\n\n:return: None", "kind": "function", "line": 415, "name": "check_sudo", "signature": "def check_sudo()"}, {"doc": "Activates a virtual environment and starts an interactive shell.\n\nThis function activates a virtual environment located at `venv_path` and then\nlaunches an interactive bash shell with the virtual environment activated.\n\n:param venv_path: The path to the virtual environment directory.\n:type venv_path: str\n:return: None", "kind": "function", "line": 435, "name": "activate_virtualenv", "signature": "def activate_virtualenv(venv_path)"}, {"doc": "Internal function to parse a /proc/net file and extract network ports.\n\nThis function reads a file specified by `file_path`, processes each line to\nextract local addresses and ports, and converts them from hexadecimal to decimal.\nThe IP addresses are converted from hexadecimal format to standard dot-decimal\nnotation. The function returns a list of tuples, each containing an IP address\nand a port number.\n\n:param file_path: The path to the /proc/net file to be parsed.\n:type file_path: str\n:return: A list of tuples, each containing an IP address and a port number.\n:rtype: list of tuple", "kind": "function", "line": 460, "name": "parse_proc_net_file", "signature": "def parse_proc_net_file(file_path)"}, {"doc": "Internal function to get open TCP and UDP ports on the operating system.\n\nThis function uses the `parse_proc_net_file` function to extract open TCP and UDP\nports from the corresponding /proc/net files. It returns two lists: one for TCP\nports and one for UDP ports.\n\n:return: A tuple containing two lists: the first list with open TCP ports and\n        the second list with open UDP ports.\n:rtype: tuple of (list of tuple, list of tuple)", "kind": "function", "line": 504, "name": "get_open_ports", "signature": "def get_open_ports()"}, {"doc": "Searches for potential credentials in files within the specified directory.\n\nThis function uses a regular expression to find possible credentials such as\npasswords, secrets, API keys, and tokens in files within the given directory.\nIt iterates through all files in the directory and prints any matches found.\n\n:param directory: The directory to search for files containing credentials.\n:type directory: str\n:return: None", "kind": "function", "line": 523, "name": "find_credentials", "signature": "def find_credentials(directory)"}, {"doc": "Internal function to rotate characters for ROT cipher.\n\nThis function takes a character and a shift value, and rotates the character\nby the specified shift amount. It only affects alphabetical characters, leaving\nnon-alphabetical characters unchanged.\n\n:param c: The character to be rotated.\n:type c: str\n:param shift: The number of positions to shift the character.\n:type shift: int\n:return: The rotated character.\n:rtype: str", "kind": "function", "line": 555, "name": "rotate_char", "signature": "def rotate_char(c, shift)"}, {"doc": "Retrieves network interface information with their associated IP addresses.\n\nThis function executes a shell command to gather network interface details, \nparses the output to extract interface names and their corresponding IP addresses, \nand returns this information in a dictionary format. The dictionary keys are\ninterface names, and the values are IP addresses.\n\n:return: A dictionary where the keys are network interface names and the values\n         are their associated IP addresses.\n:rtype: dict", "kind": "function", "line": 576, "name": "get_network_info", "signature": "def get_network_info()"}, {"doc": "Generate a command prompt string with network information and user status.\n\n:param: None\n\n:returns: A string representing the command prompt with network information and user status.\n\nManual execution:\nTo manually get a prompt string with network information and user status, ensure you have `get_network_info()` implemented to return a dictionary of network interfaces and their IPs. Then use the function to create a prompt string based on the current user and network info.\n\nExample:\nIf the function `get_network_info()` returns:\n    {\n        'tun0': '10.0.0.1',\n        'eth0': '192.168.1.2'\n    }\n\nAnd the user is root, the prompt string generated might be:\n    [LazyOwn👽10.0.0.1]# \nIf the user is not root, it would be:\n    [LazyOwn👽10.0.0.1]$ \n\nIf no 'tun' interface is found, the function will use the first available IP or fallback to '127.0.0.1'.", "kind": "function", "line": 608, "name": "getprompt", "signature": "def getprompt()"}, {"doc": "Copia el texto proporcionado al portapapeles usando xclip.\n\nArgs:\n    text (str): El texto que se desea copiar al portapapeles.\n\nExample:\n    copy2clip(\"Hello, World!\")", "kind": "function", "line": 644, "name": "copy2clip", "signature": "def copy2clip(text)"}, {"doc": "Elimina secuencias de escape de color y otros caracteres no imprimibles.", "kind": "function", "line": 663, "name": "clean_output", "signature": "def clean_output(output)"}, {"doc": "Procesa un archivo para extraer y mostrar caracteres desde secuencias de escritura específicas.\n\nArgs:\n    filename (str): El nombre del archivo a leer.\n\nRaises:\n    FileNotFoundError: Si el archivo no se encuentra.\n    Exception: Para otros errores que puedan ocurrir.", "kind": "function", "line": 675, "name": "teclado_usuario", "signature": "def teclado_usuario(filename)"}, {"doc": "Lee un archivo, extrae texto desde secuencias de escritura y muestra el contenido reconstruido.\n\nArgs:\n    filename (str): El nombre del archivo a leer.\n\nRaises:\n    FileNotFoundError: Si el archivo no se encuentra.\n    Exception: Para otros errores que puedan ocurrir.", "kind": "function", "line": 712, "name": "salida_strace", "signature": "def salida_strace(filename)"}, {"doc": "Process and display results from ExploitAlert.\n\nThis function checks if the provided content contains any results. \nIf results are present, it prints the title and link for each exploit found, \nand appends the results to a predata list. If no results are found, \nit prints an error message.\n\nParameters:\n- content (list): A list of dictionaries containing exploit information.\n\nReturns:\nNone\nThanks to Sicat 🐈\nAn excellent tool for CVE detection, I implemented only the keyword search as I had to change some libraries. Soon also for XML generated by nmap :) Total thanks to justakazh. https://github.com/justakazh/sicat/", "kind": "function", "line": 748, "name": "exploitalert", "signature": "def exploitalert(content)"}, {"doc": "Process and display results from PacketStorm Security.\n\nThis function extracts exploit data from the provided content using regex. \nIf any results are found, it prints the title and link for each exploit, \nand appends the results to a predata list. If no results are found, \nit prints an error message.\n\nParameters:\n- content (str): The HTML content from PacketStorm Security.\n\nReturns:\nNone\nThanks to Sicat 🐈\nAn excellent tool for CVE detection, I implemented only the keyword search as I had to change some libraries. Soon also for XML generated by nmap :) Total thanks to justakazh. https://github.com/justakazh/sicat/", "kind": "function", "line": 791, "name": "packetstormsecurity", "signature": "def packetstormsecurity(content)"}, {"doc": "Process and display results from the National Vulnerability Database.\n\nThis function checks if there are any vulnerabilities in the provided content. \nIf vulnerabilities are present, it prints the ID, description, and link \nfor each CVE found, and appends the results to a predata list. \nIf no results are found, it prints an error message.\n\nParameters:\n- content (dict): A dictionary containing vulnerability data.\n\nReturns:\nNone\nThanks to Sicat 🐈\nAn excellent tool for CVE detection, I implemented only the keyword search as I had to change some libraries. Soon also for XML generated by nmap :) Total thanks to justakazh. https://github.com/justakazh/sicat/", "kind": "function", "line": 833, "name": "nvddb", "signature": "def nvddb(content)"}, {"doc": "Find CVEs in the National Vulnerability Database based on a keyword.\n\nThis function takes a keyword, formats it for the API request, \nand sends a GET request to the NVD API. If the request is successful, \nit returns the JSON response containing CVE data; otherwise, \nit returns False.\n\nParameters:\n- keyword (str): The keyword to search for in CVEs.\n\nReturns:\n- dict or bool: The JSON response containing CVE data or False on failure.\nThanks to Sicat 🐈\nAn excellent tool for CVE detection, I implemented only the keyword search as I had to change some libraries. Soon also for XML generated by nmap :) Total thanks to justakazh. https://github.com/justakazh/sicat/", "kind": "function", "line": 876, "name": "find_ss", "signature": "def find_ss(keyword)"}, {"doc": "Find exploits in ExploitAlert based on a keyword.\n\nThis function takes a keyword, formats it for the API request, \nand sends a GET request to the ExploitAlert API. If the request is successful, \nit returns the JSON response containing exploit data; otherwise, \nit returns False.\n\nParameters:\n- keyword (str): The keyword to search for exploits.\n\nReturns:\n- dict or bool: The JSON response containing exploit data or False on failure.\nThanks to Sicat 🐈\nAn excellent tool for CVE detection, I implemented only the keyword search as I had to change some libraries. Soon also for XML generated by nmap :) Total thanks to justakazh. https://github.com/justakazh/sicat/", "kind": "function", "line": 901, "name": "find_ea", "signature": "def find_ea(keyword)"}, {"doc": "Find exploits in PacketStorm Security based on a keyword.\n\nThis function takes a keyword, formats it for the search request, \nand sends a GET request to the PacketStorm Security website. \nIf the request is successful, it returns the HTML response; otherwise, \nit returns False.\n\nParameters:\n- keyword (str): The keyword to search for exploits.\n\nReturns:\n- str or bool: The HTML response containing exploit data or False on failure.\nThanks to Sicat 🐈\nAn excellent tool for CVE detection, I implemented only the keyword search as I had to change some libraries. Soon also for XML generated by nmap :) Total thanks to justakazh. https://github.com/justakazh/sicat/", "kind": "function", "line": 928, "name": "find_ps", "signature": "def find_ps(keyword)"}, {"doc": "Encrypts or decrypts data using XOR encryption with the provided key.\n\nParameters:\ndata (bytes or bytearray): The input data to be encrypted or decrypted.\nkey (str): The encryption key as a string.\n\nReturns:\nbytearray: The result of the XOR operation, which can be either the encrypted or decrypted data.\n\nExample:\nencrypted_data = xor_encrypt_decrypt(b\"Hello, World!\", \"key\")\ndecrypted_data = xor_encrypt_decrypt(encrypted_data, \"key\")\nprint(decrypted_data.decode(\"utf-8\"))  # Outputs: Hello, World!\n\nAdditional Notes:\n- XOR encryption is symmetric, meaning that the same function is used for both encryption and decryption.\n- The key is repeated cyclically to match the length of the data if necessary.\n- This method is commonly used for simple encryption tasks, but it is not secure for protecting sensitive information.", "kind": "function", "line": 952, "name": "xor_encrypt_decrypt", "signature": "def xor_encrypt_decrypt(data, key)"}, {"doc": "Executes a shell command using the subprocess module, capturing its output.\n\nParameters:\ncommand (str): The command to execute.\n\nReturns:\nstr: The output of the command if successful, or an error message if an exception occurs.\n\nExceptions:\n- FileNotFoundError: Raised if the command is not found.\n- subprocess.CalledProcessError: Raised if the command exits with a non-zero status.\n- subprocess.TimeoutExpired: Raised if the command times out.\n- Exception: Catches any other unexpected exceptions.\n\nExample:\noutput = run(\"ls -la\")\nprint(output)\n\nAdditional Notes:\nThe function attempts to execute the provided command, capturing its output.\nIt also handles common exceptions that may occur during command execution.", "kind": "function", "line": 977, "name": "run", "signature": "def run(command)"}, {"doc": "Check if a file exists.\n\nThis function checks whether a given file exists on the filesystem. If the file \ndoes not exist, it prints an error message and returns False. Otherwise, it returns True.\n\nArguments:\nfile (str): The path to the file that needs to be checked.\n\nReturns:\nbool: Returns True if the file exists, False otherwise.\n\nExample:\n>>> is_exist('/path/to/file.txt')\nTrue\n>>> is_exist('/non/existent/file.txt')\nFalse\n\nNotes:\nThis function uses os.path.isfile to determine the existence of the file. \nEnsure that the provided path is correct and accessible.", "kind": "function", "line": 1019, "name": "is_exist", "signature": "def is_exist(file)"}, {"doc": "Extracts the domain from a given URL.\n\nParameters:\nurl (str): The full URL from which to extract the domain.\n\nReturns:\nstr: The extracted domain from the URL, or None if it cannot be extracted.", "kind": "function", "line": 1047, "name": "get_domain", "signature": "def get_domain(url)"}, {"doc": "Generates a certificate authority (CA), client certificate, and client key.\n\nReturns:\n    str: Paths to the generated CA certificate, client certificate, and client key.", "kind": "function", "line": 1063, "name": "generate_certificates", "signature": "def generate_certificates()"}, {"doc": "Generate email permutations based on the provided full name and domain.\n\nThis function takes a full name and domain as input, splits the full name into\ncomponents, and creates a list of potential email addresses.\n\nParameters:\nfull_name (str): The full name to base the email addresses on.\ndomain (str): The domain to use for the generated email addresses.\n\nInternal Variables:\nnames (list): A list of the name components extracted from the full name.\nfirst_name (str): The first name component.\nlast_name (str): The last name component.\nfirst_initial (str): The first initial of the first name.\nlast_initial (str): The first initial of the last name.\n\nReturns:\nlist: A list of generated email permutations.\n\nNote:\n- At least two parts of the name are required to generate valid email addresses.", "kind": "function", "line": 1106, "name": "generate_emails", "signature": "def generate_emails(full_name, domain)"}, {"doc": "Verifica si el último carácter es una barra y, de ser así, la elimina", "kind": "function", "line": 1164, "name": "clean_url", "signature": "def clean_url(host)"}, {"doc": "Generates a random alphanumeric string.", "kind": "function", "line": 1170, "name": "random_string", "signature": "def random_string(length)"}, {"doc": "Generates an HTTP request with the Shellshock payload.", "kind": "function", "line": 1175, "name": "generate_http_req", "signature": "def generate_http_req(host, port, uri, custom_header, cmd)"}, {"doc": "Formats a raw OpenSSH private key string to the correct OpenSSH format.\n\nThis function takes a raw OpenSSH private key string, cleans it by removing any unnecessary \ncharacters (such as newlines, spaces, and headers/footers), splits the key content into lines \nof 64 characters, and then reassembles the key with the standard OpenSSH header and footer. \nIt ensures the key follows the correct OpenSSH format.\n\nParameters:\n    raw_key (str): The raw OpenSSH private key string to format.\n\nReturns:\n    str: The formatted OpenSSH private key with proper headers, footers, and 64-character lines.", "kind": "function", "line": 1202, "name": "format_openssh_key", "signature": "def format_openssh_key(raw_key)"}, {"doc": "Formats a raw RSA private key string to the correct PEM format.\n\nThis function takes a raw RSA private key string, cleans it by removing any unnecessary\ncharacters (such as newlines, spaces, and headers/footers), splits the key content into lines \nof 64 characters, and then reassembles the key with the standard PEM header and footer. \nIt ensures the key follows the correct RSA format.\n\nParameters:\n    raw_key (str): The raw RSA private key string to format.\n\nReturns:\n    str: The formatted RSA private key with proper headers, footers, and 64-character lines.", "kind": "function", "line": 1233, "name": "format_rsa_key", "signature": "def format_rsa_key(raw_key)"}, {"doc": "Check if a Python package is installed.\n\n:param package_name: Name of the package to check.\n:returns: True if installed, False otherwise.", "kind": "function", "line": 1263, "name": "is_package_installed", "signature": "def is_package_installed(package_name)"}, {"doc": "Extracts and processes specific hexadecimal sequences from a string based on a flag.\n\nIf the `extract_flag` is set to True, the function extracts all sequences of the form 'x[a-f0-9][a-f0-9]' \n(where 'x' is followed by two hexadecimal digits), removes the 'x' from the extracted sequences, \nand returns the processed string. If `extract_flag` is False, the function returns the original string.\n\nParameters:\n    string (str): The input string from which hexadecimal sequences are to be extracted.\n    extract_flag (bool): A flag indicating whether to perform the extraction (True) or not (False).\n\nReturns:\n    str: The processed string with the extracted hexadecimal sequences if `extract_flag` is True, \n         or the original string if `extract_flag` is False.", "kind": "function", "line": 1273, "name": "extract", "signature": "def extract(string, extract_flag)"}, {"doc": "Remove HTML tags from a string.\n\nThis function uses a regular expression to strip HTML tags and return plain text.\n\n:param html_string: A string containing HTML content.\n:returns: A cleaned string with HTML tags removed.", "kind": "function", "line": 1296, "name": "clean_html", "signature": "def clean_html(html_string)"}, {"doc": "Run a command, print output in real-time, and store the output in a variable.\n\nThis method executes a given command using `subprocess.Popen`, streams both the standard \noutput and standard error to the console in real-time, and stores the full output (stdout \nand stderr) in a variable. If interrupted, the process is terminated gracefully.\n\n:param command: The command to be executed as a string.\n:type command: str\n\n:returns: The full output of the command (stdout and stderr).\n:rtype: str\n\nExample:\n    To execute a command, call `run_command(\"ls -l\")`.", "kind": "function", "line": 1309, "name": "run_command", "signature": "def run_command(command)"}, {"doc": "Generates a random CVE (Common Vulnerabilities and Exposures) ID.\n\nThis function creates a random CVE ID by selecting a random year between 2020 and 2024,\nand a random code between 1000 and 9999. The CVE ID is returned in the format 'CVE-{year}-{code}'.\n\nReturns:\n    str: A randomly generated CVE ID in the format 'CVE-{year}-{code}'.", "kind": "function", "line": 1357, "name": "generate_random_cve_id", "signature": "def generate_random_cve_id()"}, {"doc": "Searches for credential files with the pattern 'credentials*.txt' and allows the user to select one.\n\nThe function lists all matching files and prompts the user to select one. It then reads the selected file\nand returns a list of tuples with the format (username, password) for each line in the file.\n\nReturns:\nlist of tuples: A list containing tuples with (username, password) for each credential found in the file.\n                If no files are found or an invalid selection is made, an empty list is returned.", "kind": "function", "line": 1372, "name": "get_credentials", "signature": "def get_credentials(file)"}, {"doc": "Obfuscates a payload string by converting its characters into hexadecimal format, \nwith additional comments for every third character.\n\nFor every character in the payload, the function converts it to its hexadecimal representation.\nEvery third character (after the first) is enclosed in a comment `/*hex_value*/`, while the rest \nare prefixed with `\\x`.\n\nParameters:\n    payload (str): The input string that needs to be obfuscated.\n\nReturns:\n    str: The obfuscated string where characters are replaced by their hexadecimal representations, \n         with every third character wrapped in a comment.", "kind": "function", "line": 1411, "name": "obfuscate_payload", "signature": "def obfuscate_payload(payload)"}, {"doc": "Reads a file containing payloads and returns a list of properly formatted strings.\n\nThis function opens a specified file, reads each line, and checks if the line starts with a \ndouble quote. If it does not, it adds double quotes around the line. Each line is stripped \nof leading and trailing whitespace before being added to the list.\n\nParameters:\n    file_path (str): The path to the file containing payloads.\n\nReturns:\n    list: A list of strings, each representing a payload from the file, formatted with \n          leading and trailing double quotes if necessary.", "kind": "function", "line": 1435, "name": "read_payloads", "signature": "def read_payloads(file_path)"}, {"doc": "Sends HTTP requests to a list of URLs with injected payloads for testing XSS vulnerabilities.\n\nThis function reads payloads from a specified file and sends GET requests to the provided URLs,\ninjecting obfuscated payloads into the query parameters or form fields to test for cross-site \nscripting (XSS) vulnerabilities. It handles both URLs with existing query parameters and those \nwithout. If forms are found in the response, it submits them with the payloads as well.\n\nParameters:\n    urls (list): A list of URLs to test for XSS vulnerabilities.\n    payload_url (str): A placeholder string within the payloads that will be replaced with \n                       the actual URL for testing.\n    request_timeout (int, optional): The timeout for each request in seconds. Defaults to 15.\n\nReturns:\n    None: This function does not return any value but prints the status of each request and \n          form submission to the console.\n\nRaises:\n    requests.RequestException: Raises an exception if any HTTP request fails, which is handled\n                               by printing a warning message.", "kind": "function", "line": 1456, "name": "inject_payloads", "signature": "def inject_payloads(urls, payload_url, request_timeout)"}, {"doc": "Return the prompt in the function do_xss", "kind": "function", "line": 1544, "name": "prompt", "signature": "def prompt(label, default)"}, {"doc": "Checks if a character is lowercase.\n\nParameters:\n    char (str): The character to check.\n\nReturns:\n    bool: True if the character is lowercase, False otherwise.", "kind": "function", "line": 1551, "name": "is_lower", "signature": "def is_lower(char)"}, {"doc": "Checks if a character is uppercase.\n\nParameters:\n    char (str): The character to check.\n\nReturns:\n    bool: True if the character is uppercase, False otherwise.", "kind": "function", "line": 1564, "name": "is_upper", "signature": "def is_upper(char)"}, {"doc": "Determines if a string contains both lowercase and uppercase characters.\n\nParameters:\n    s (str): The string to check.\n\nReturns:\n    bool: True if the string has mixed casing, False otherwise.", "kind": "function", "line": 1577, "name": "is_mixed", "signature": "def is_mixed(s)"}, {"doc": "Adds a delimiter between string parts if it's not the first part.\n\nParameters:\n    str_part (str): The string part to add.\n    delimiter (str): The delimiter to insert between parts.\n    i (int): The index of the part.\n\nReturns:\n    str: The string part with delimiter if applicable.", "kind": "function", "line": 1590, "name": "add", "signature": "def add(str_part, delimiter, i)"}, {"doc": "Detects the delimiter used in the input string (e.g., \"-\", \"_\", \".\").\n\nParameters:\n    foo_bar (str): The input string.\n\nReturns:\n    str: The detected delimiter.", "kind": "function", "line": 1607, "name": "detect_delimiter", "signature": "def detect_delimiter(foo_bar)"}, {"doc": "Transforms a list of string parts based on the chosen casing style.\n\nParameters:\n    parts (list): List of string parts.\n    delimiter (str): Delimiter to use between parts.\n    casing (str): Casing style ('l', 'u', 'c', 'p').\n\nReturns:\n    str: The transformed string.", "kind": "function", "line": 1626, "name": "transform", "signature": "def transform(parts, delimiter, casing)"}, {"doc": "Splits the input string into parts based on delimiters or mixed casing.\n\nParameters:\n    input_str (str): The input string to split.\n\nReturns:\n    list: A list of string parts.", "kind": "function", "line": 1656, "name": "handle", "signature": "def handle(input_str)"}, {"doc": "List all .txt files in the 'sessions/' directory and prompt the user to select one by number.\n\n:returns: The path of the selected .txt file.", "kind": "function", "line": 1685, "name": "get_users_dic", "signature": "def get_users_dic()"}, {"doc": "Searches for hash files with the pattern 'hash*.txt' and allows the user to select one.\n\nThe function lists all matching files and prompts the user to select one. It then reads the selected file\nand returns the hash content as a single string, without any newline characters or extra formatting.\n\nReturns:\nstr: The hash content from the selected file as a single string. If no files are found or an invalid\n     selection is made, an empty string is returned.", "kind": "function", "line": 1717, "name": "get_hash", "signature": "def get_hash(dir)"}, {"doc": "Check if the given character is a digit.\n\nArgs:\n    the_digit (str): The character to check.\n\nReturns:\n    bool: True if the character is a digit, False otherwise.", "kind": "function", "line": 1757, "name": "is_digit", "signature": "def is_digit(the_digit)"}, {"doc": "Crack a Cisco Type 7 password.\n\nArgs:\n    crypttext (str): The encrypted password in Type 7 format.\n\nReturns:\n    str: The cracked plaintext password or an empty string if invalid.", "kind": "function", "line": 1768, "name": "crack_password", "signature": "def crack_password(crypttext)"}, {"kind": "function", "line": 1807, "name": "get_terminal_size", "signature": "def get_terminal_size()"}, {"doc": "Display the help panel for the LazyOwn RedTeam Framework.\n\nThis function prints usage instructions, options, and descriptions for \nrunning the LazyOwn framework. It provides users with an overview of \ncommand-line options that can be used when executing the `./run` command.\n\nThe output includes the current version of the framework and various \noptions available for users, along with a brief description of each option.\n\nOptions include:\n    - `--help`: Displays the help panel.\n    - `-v`: Shows the version of the framework.\n    - `-p <payloadN.json>`: Executes the framework with a specified payload \n      JSON file. This option is particularly useful for Red Teams.\n    - `-c <command>`: Executes a specific command using LazyOwn, for \n      example, `ping`.\n    - `--no-banner`: Runs the framework without displaying the banner.\n    - `-s`: Runs the framework with root privileges.\n    - `--old-banner`: Displays the old banner.\n\nExample:\n    To see the help panel, call the function as follows:\n    \n    >>> halp()\n\nNote:\n    - This function exits the program after displaying the help information,\n      using `sys.exit(0)`.", "kind": "function", "line": 1815, "name": "halp", "signature": "def halp()"}, {"doc": "Ensure that a tmux session is active.\n\nThis function checks whether a specified tmux session is currently running.\nIf the session does not exist, it creates a new tmux session with the specified\nname and executes the command to run the LazyOwn RedTeam Framework script.\n\nThe function uses the `tmux has-session` command to check for the existence\nof the session. If the session is not found (i.e., the return code is not zero),\nit will create a new tmux session in detached mode and run the command \n`./run --no-banner` within that session.\n\nArgs:\n    session_name (str): The name of the tmux session to check or create.\n\nExample:\n    To ensure that a tmux session named 'lazyown_sessions' is active,\n    call the function as follows:\n    \n    >>> ensure_tmux_session('lazyown_sessions')\n\nNote:\n    - Ensure that tmux is installed and properly configured on the system.\n    - The command executed within the tmux session must be valid and\n      accessible in the current environment.", "kind": "function", "line": 1859, "name": "ensure_tmux_session", "signature": "def ensure_tmux_session(session_name)"}, {"doc": "internal wrapper of internal function to implement multiples rhost to operate. ", "kind": "function", "line": 397, "name": "wrapper", "signature": "def wrapper(self)"}, {"kind": "function", "line": 1481, "name": "send_request", "signature": "def send_request(raw_url)"}, {"kind": "function", "line": 1512, "name": "handle_forms", "signature": "def handle_forms(content, url)"}]}], "type": "CodePropertyGraph", "version": "1.0"}
```

---

## Architecture Reference

### PY (2 files)

#### `app.py`
**Path:** `app.py`
**File Doc:** *_*_ coding: utf8 _*_*

**Functions:**
- `image_to_bash` (line 27) `def image_to_bash(image_path, image_res)`
- `list_png_files` (line 44) `def list_png_files()`
- `main` (line 54) `def main()`

#### `utils.py`
**Path:** `utils.py`

**Functions:**
- `parse_ip_mac` (line 128) `def parse_ip_mac(input_string)` - *Extracts IP and MAC addresses from a formatted input string using a regular expression.

The input string is expected to be in the format: 'IP: (192.168.1.222) MAC: ec:c3:02:b0:4c:96'.
The function uses a regular expression to match and extract the IP address and MAC address from the input.

Args:
    input_string (str): The formatted string containing the IP and MAC addresses.

Returns:
    tuple: A tuple containing the extracted IP address and MAC address. If the format is incorrect, returns (None, None).*
- `create_arp_packet` (line 149) `def create_arp_packet(src_mac, src_ip, dst_ip, dst_mac)` - *Constructs an ARP packet with the given source and destination IP and MAC addresses.

The function creates both Ethernet and ARP headers, combining them into a complete ARP packet.

Args:
    src_mac (str): Source MAC address in the format 'xx:xx:xx:xx:xx:xx'.
    src_ip (str): Source IP address in dotted decimal format (e.g., '192.168.1.1').
    dst_ip (str): Destination IP address in dotted decimal format (e.g., '192.168.1.2').
    dst_mac (str): Destination MAC address in the format 'xx:xx:xx:xx:xx:xx'.

Returns:
    bytes: The constructed ARP packet containing the Ethernet and ARP headers.*
- `send_packet` (line 186) `def send_packet(packet, iface)` - *Sends a raw ARP packet over the specified network interface.

The function creates a raw socket, binds it to the specified network interface, and sends the given packet.

Args:
    packet (bytes): The ARP packet to be sent.
    iface (str): The name of the network interface to use for sending the packet (e.g., 'eth0').

Raises:
    OSError: If an error occurs while creating the socket or sending the packet.*
- `load_version` (line 203) `def load_version()` - *Load the version number from the 'version.json' file.

This function attempts to open the 'version.json' file and load its contents. 
If the file is found, it retrieves the version number from the JSON data. 
If the version key does not exist, it returns a default version 'release/v0.0.14'. 
If the file is not found, it also returns the default version.

Returns:
- str: The version number from the file or the default version if the file is not found or the version key is missing.*
- `print_error` (line 224) `def print_error(error)` - *Prints an error message to the console.

This function takes an error message as input and prints it to the console
with a specific format to indicate that it is an error.

:param error: The error message to be printed.
:type error: str
:return: None*
- `print_msg` (line 239) `def print_msg(msg)` - *Prints a message to the console.

This function takes a message as input and prints it to the console
with a specific format to indicate that it is an informational message.

:param msg: The message to be printed.
:type msg: str
:return: None*
- `print_warn` (line 255) `def print_warn(warn)` - *Prints a warning message to the console.

This function takes a warning message as input and prints it to the console
with a specific format to indicate that it is a warning.

:param warn: The warning message to be printed.
:type warn: str
:return: None*
- `signal_handler` (line 271) `def signal_handler(sig, frame)` - *Handles signals such as Control + C and shows a message on how to exit.

This function is used to handle signals like Control + C (SIGINT) and prints
a warning message instructing the user on how to exit the program using the
commands 'exit', 'q', or 'qa'.

:param sig: The signal number.
:type sig: int
:param frame: The current stack frame.
:type frame: frame
:return: None*
- `check_rhost` (line 298) `def check_rhost(rhost)` - *Checks if the remote host (rhost) is defined and shows an error message if it is not.

This function verifies if the `rhost` parameter is set. If it is not defined,
an error message is printed, providing an example and directing the user to
additional help.

:param rhost: The remote host to be checked.
:type rhost: str
:return: True if rhost is defined, False otherwise.
:rtype: bool*
- `check_lhost` (line 320) `def check_lhost(lhost)` - *Checks if the local host (lhost) is defined and shows an error message if it is not.

This function verifies if the `lhost` parameter is set. If it is not defined,
an error message is printed, providing an example and directing the user to
additional help.

:param lhost: The local host to be checked.
:type lhost: str
:return: True if lhost is defined, False otherwise.
:rtype: bool*
- `check_lport` (line 342) `def check_lport(lport)` - *Checks if the local port (lport) is defined and shows an error message if it is not.

This function verifies if the `lport` parameter is set. If it is not defined,
an error message is printed, providing an example and directing the user to
additional help.

:param lport: The local port to be checked.
:type lport: int or str
:return: True if lport is defined, False otherwise.
:rtype: bool*
- `is_binary_present` (line 364) `def is_binary_present(binary_name)` - *Internal function to verify if a binary is present on the operating system.

This function checks if a specified binary is available in the system's PATH
by using the `which` command. It returns True if the binary is found and False
otherwise.

:param binary_name: The name of the binary to be checked.
:type binary_name: str
:return: True if the binary is present, False otherwise.
:rtype: bool*
- `handle_multiple_rhosts` (line 381) `def handle_multiple_rhosts(func)` - *Internal function to handle multiple remote hosts (rhost) for operations.

This function is a decorator that allows an operation to be performed across
multiple remote hosts specified in `self.params["rhost"]`. It converts a single
remote host into a list if necessary, and then iterates over each host,
performing the given function with each host. After the operation, it restores
the original remote host value.

:param func: The function to be decorated and executed for each remote host.
:type func: function
:return: The decorated function.
:rtype: function*
- `check_sudo` (line 415) `def check_sudo()` - *Checks if the script is running with superuser (sudo) privileges, and if not,
restarts the script with sudo privileges.

This function verifies if the script is being executed with root privileges
by checking the effective user ID. If the script is not running as root,
it prints a warning message and restarts the script using sudo.

:return: None*
- `activate_virtualenv` (line 435) `def activate_virtualenv(venv_path)` - *Activates a virtual environment and starts an interactive shell.

This function activates a virtual environment located at `venv_path` and then
launches an interactive bash shell with the virtual environment activated.

:param venv_path: The path to the virtual environment directory.
:type venv_path: str
:return: None*
- `parse_proc_net_file` (line 460) `def parse_proc_net_file(file_path)` - *Internal function to parse a /proc/net file and extract network ports.

This function reads a file specified by `file_path`, processes each line to
extract local addresses and ports, and converts them from hexadecimal to decimal.
The IP addresses are converted from hexadecimal format to standard dot-decimal
notation. The function returns a list of tuples, each containing an IP address
and a port number.

:param file_path: The path to the /proc/net file to be parsed.
:type file_path: str
:return: A list of tuples, each containing an IP address and a port number.
:rtype: list of tuple*
- `get_open_ports` (line 504) `def get_open_ports()` - *Internal function to get open TCP and UDP ports on the operating system.

This function uses the `parse_proc_net_file` function to extract open TCP and UDP
ports from the corresponding /proc/net files. It returns two lists: one for TCP
ports and one for UDP ports.

:return: A tuple containing two lists: the first list with open TCP ports and
        the second list with open UDP ports.
:rtype: tuple of (list of tuple, list of tuple)*
- `find_credentials` (line 523) `def find_credentials(directory)` - *Searches for potential credentials in files within the specified directory.

This function uses a regular expression to find possible credentials such as
passwords, secrets, API keys, and tokens in files within the given directory.
It iterates through all files in the directory and prints any matches found.

:param directory: The directory to search for files containing credentials.
:type directory: str
:return: None*
- `rotate_char` (line 555) `def rotate_char(c, shift)` - *Internal function to rotate characters for ROT cipher.

This function takes a character and a shift value, and rotates the character
by the specified shift amount. It only affects alphabetical characters, leaving
non-alphabetical characters unchanged.

:param c: The character to be rotated.
:type c: str
:param shift: The number of positions to shift the character.
:type shift: int
:return: The rotated character.
:rtype: str*
- `get_network_info` (line 576) `def get_network_info()` - *Retrieves network interface information with their associated IP addresses.

This function executes a shell command to gather network interface details, 
parses the output to extract interface names and their corresponding IP addresses, 
and returns this information in a dictionary format. The dictionary keys are
interface names, and the values are IP addresses.

:return: A dictionary where the keys are network interface names and the values
         are their associated IP addresses.
:rtype: dict*
- `getprompt` (line 608) `def getprompt()` - *Generate a command prompt string with network information and user status.

:param: None

:returns: A string representing the command prompt with network information and user status.

Manual execution:
To manually get a prompt string with network information and user status, ensure you have `get_network_info()` implemented to return a dictionary of network interfaces and their IPs. Then use the function to create a prompt string based on the current user and network info.

Example:
If the function `get_network_info()` returns:
    {
        'tun0': '10.0.0.1',
        'eth0': '192.168.1.2'
    }

And the user is root, the prompt string generated might be:
    [LazyOwn👽10.0.0.1]# 
If the user is not root, it would be:
    [LazyOwn👽10.0.0.1]$ 

If no 'tun' interface is found, the function will use the first available IP or fallback to '127.0.0.1'.*
- `copy2clip` (line 644) `def copy2clip(text)` - *Copia el texto proporcionado al portapapeles usando xclip.

Args:
    text (str): El texto que se desea copiar al portapapeles.

Example:
    copy2clip("Hello, World!")*
- `clean_output` (line 663) `def clean_output(output)` - *Elimina secuencias de escape de color y otros caracteres no imprimibles.*
- `teclado_usuario` (line 675) `def teclado_usuario(filename)` - *Procesa un archivo para extraer y mostrar caracteres desde secuencias de escritura específicas.

Args:
    filename (str): El nombre del archivo a leer.

Raises:
    FileNotFoundError: Si el archivo no se encuentra.
    Exception: Para otros errores que puedan ocurrir.*
- `salida_strace` (line 712) `def salida_strace(filename)` - *Lee un archivo, extrae texto desde secuencias de escritura y muestra el contenido reconstruido.

Args:
    filename (str): El nombre del archivo a leer.

Raises:
    FileNotFoundError: Si el archivo no se encuentra.
    Exception: Para otros errores que puedan ocurrir.*
- `exploitalert` (line 748) `def exploitalert(content)` - *Process and display results from ExploitAlert.

This function checks if the provided content contains any results. 
If results are present, it prints the title and link for each exploit found, 
and appends the results to a predata list. If no results are found, 
it prints an error message.

Parameters:
- content (list): A list of dictionaries containing exploit information.

Returns:
None
Thanks to Sicat 🐈
An excellent tool for CVE detection, I implemented only the keyword search as I had to change some libraries. Soon also for XML generated by nmap :) Total thanks to justakazh. https://github.com/justakazh/sicat/*
- `packetstormsecurity` (line 791) `def packetstormsecurity(content)` - *Process and display results from PacketStorm Security.

This function extracts exploit data from the provided content using regex. 
If any results are found, it prints the title and link for each exploit, 
and appends the results to a predata list. If no results are found, 
it prints an error message.

Parameters:
- content (str): The HTML content from PacketStorm Security.

Returns:
None
Thanks to Sicat 🐈
An excellent tool for CVE detection, I implemented only the keyword search as I had to change some libraries. Soon also for XML generated by nmap :) Total thanks to justakazh. https://github.com/justakazh/sicat/*
- `nvddb` (line 833) `def nvddb(content)` - *Process and display results from the National Vulnerability Database.

This function checks if there are any vulnerabilities in the provided content. 
If vulnerabilities are present, it prints the ID, description, and link 
for each CVE found, and appends the results to a predata list. 
If no results are found, it prints an error message.

Parameters:
- content (dict): A dictionary containing vulnerability data.

Returns:
None
Thanks to Sicat 🐈
An excellent tool for CVE detection, I implemented only the keyword search as I had to change some libraries. Soon also for XML generated by nmap :) Total thanks to justakazh. https://github.com/justakazh/sicat/*
- `find_ss` (line 876) `def find_ss(keyword)` - *Find CVEs in the National Vulnerability Database based on a keyword.

This function takes a keyword, formats it for the API request, 
and sends a GET request to the NVD API. If the request is successful, 
it returns the JSON response containing CVE data; otherwise, 
it returns False.

Parameters:
- keyword (str): The keyword to search for in CVEs.

Returns:
- dict or bool: The JSON response containing CVE data or False on failure.
Thanks to Sicat 🐈
An excellent tool for CVE detection, I implemented only the keyword search as I had to change some libraries. Soon also for XML generated by nmap :) Total thanks to justakazh. https://github.com/justakazh/sicat/*
- `find_ea` (line 901) `def find_ea(keyword)` - *Find exploits in ExploitAlert based on a keyword.

This function takes a keyword, formats it for the API request, 
and sends a GET request to the ExploitAlert API. If the request is successful, 
it returns the JSON response containing exploit data; otherwise, 
it returns False.

Parameters:
- keyword (str): The keyword to search for exploits.

Returns:
- dict or bool: The JSON response containing exploit data or False on failure.
Thanks to Sicat 🐈
An excellent tool for CVE detection, I implemented only the keyword search as I had to change some libraries. Soon also for XML generated by nmap :) Total thanks to justakazh. https://github.com/justakazh/sicat/*
- `find_ps` (line 928) `def find_ps(keyword)` - *Find exploits in PacketStorm Security based on a keyword.

This function takes a keyword, formats it for the search request, 
and sends a GET request to the PacketStorm Security website. 
If the request is successful, it returns the HTML response; otherwise, 
it returns False.

Parameters:
- keyword (str): The keyword to search for exploits.

Returns:
- str or bool: The HTML response containing exploit data or False on failure.
Thanks to Sicat 🐈
An excellent tool for CVE detection, I implemented only the keyword search as I had to change some libraries. Soon also for XML generated by nmap :) Total thanks to justakazh. https://github.com/justakazh/sicat/*
- `xor_encrypt_decrypt` (line 952) `def xor_encrypt_decrypt(data, key)` - *Encrypts or decrypts data using XOR encryption with the provided key.

Parameters:
data (bytes or bytearray): The input data to be encrypted or decrypted.
key (str): The encryption key as a string.

Returns:
bytearray: The result of the XOR operation, which can be either the encrypted or decrypted data.

Example:
encrypted_data = xor_encrypt_decrypt(b"Hello, World!", "key")
decrypted_data = xor_encrypt_decrypt(encrypted_data, "key")
print(decrypted_data.decode("utf-8"))  # Outputs: Hello, World!

Additional Notes:
- XOR encryption is symmetric, meaning that the same function is used for both encryption and decryption.
- The key is repeated cyclically to match the length of the data if necessary.
- This method is commonly used for simple encryption tasks, but it is not secure for protecting sensitive information.*
- `run` (line 977) `def run(command)` - *Executes a shell command using the subprocess module, capturing its output.

Parameters:
command (str): The command to execute.

Returns:
str: The output of the command if successful, or an error message if an exception occurs.

Exceptions:
- FileNotFoundError: Raised if the command is not found.
- subprocess.CalledProcessError: Raised if the command exits with a non-zero status.
- subprocess.TimeoutExpired: Raised if the command times out.
- Exception: Catches any other unexpected exceptions.

Example:
output = run("ls -la")
print(output)

Additional Notes:
The function attempts to execute the provided command, capturing its output.
It also handles common exceptions that may occur during command execution.*
- `is_exist` (line 1019) `def is_exist(file)` - *Check if a file exists.

This function checks whether a given file exists on the filesystem. If the file 
does not exist, it prints an error message and returns False. Otherwise, it returns True.

Arguments:
file (str): The path to the file that needs to be checked.

Returns:
bool: Returns True if the file exists, False otherwise.

Example:
>>> is_exist('/path/to/file.txt')
True
>>> is_exist('/non/existent/file.txt')
False

Notes:
This function uses os.path.isfile to determine the existence of the file. 
Ensure that the provided path is correct and accessible.*
- `get_domain` (line 1047) `def get_domain(url)` - *Extracts the domain from a given URL.

Parameters:
url (str): The full URL from which to extract the domain.

Returns:
str: The extracted domain from the URL, or None if it cannot be extracted.*
- `generate_certificates` (line 1063) `def generate_certificates()` - *Generates a certificate authority (CA), client certificate, and client key.

Returns:
    str: Paths to the generated CA certificate, client certificate, and client key.*
- `generate_emails` (line 1106) `def generate_emails(full_name, domain)` - *Generate email permutations based on the provided full name and domain.

This function takes a full name and domain as input, splits the full name into
components, and creates a list of potential email addresses.

Parameters:
full_name (str): The full name to base the email addresses on.
domain (str): The domain to use for the generated email addresses.

Internal Variables:
names (list): A list of the name components extracted from the full name.
first_name (str): The first name component.
last_name (str): The last name component.
first_initial (str): The first initial of the first name.
last_initial (str): The first initial of the last name.

Returns:
list: A list of generated email permutations.

Note:
- At least two parts of the name are required to generate valid email addresses.*
- `clean_url` (line 1164) `def clean_url(host)` - *Verifica si el último carácter es una barra y, de ser así, la elimina*
- `random_string` (line 1170) `def random_string(length)` - *Generates a random alphanumeric string.*
- `generate_http_req` (line 1175) `def generate_http_req(host, port, uri, custom_header, cmd)` - *Generates an HTTP request with the Shellshock payload.*
- `format_openssh_key` (line 1202) `def format_openssh_key(raw_key)` - *Formats a raw OpenSSH private key string to the correct OpenSSH format.

This function takes a raw OpenSSH private key string, cleans it by removing any unnecessary 
characters (such as newlines, spaces, and headers/footers), splits the key content into lines 
of 64 characters, and then reassembles the key with the standard OpenSSH header and footer. 
It ensures the key follows the correct OpenSSH format.

Parameters:
    raw_key (str): The raw OpenSSH private key string to format.

Returns:
    str: The formatted OpenSSH private key with proper headers, footers, and 64-character lines.*
- `format_rsa_key` (line 1233) `def format_rsa_key(raw_key)` - *Formats a raw RSA private key string to the correct PEM format.

This function takes a raw RSA private key string, cleans it by removing any unnecessary
characters (such as newlines, spaces, and headers/footers), splits the key content into lines 
of 64 characters, and then reassembles the key with the standard PEM header and footer. 
It ensures the key follows the correct RSA format.

Parameters:
    raw_key (str): The raw RSA private key string to format.

Returns:
    str: The formatted RSA private key with proper headers, footers, and 64-character lines.*
- `is_package_installed` (line 1263) `def is_package_installed(package_name)` - *Check if a Python package is installed.

:param package_name: Name of the package to check.
:returns: True if installed, False otherwise.*
- `extract` (line 1273) `def extract(string, extract_flag)` - *Extracts and processes specific hexadecimal sequences from a string based on a flag.

If the `extract_flag` is set to True, the function extracts all sequences of the form 'x[a-f0-9][a-f0-9]' 
(where 'x' is followed by two hexadecimal digits), removes the 'x' from the extracted sequences, 
and returns the processed string. If `extract_flag` is False, the function returns the original string.

Parameters:
    string (str): The input string from which hexadecimal sequences are to be extracted.
    extract_flag (bool): A flag indicating whether to perform the extraction (True) or not (False).

Returns:
    str: The processed string with the extracted hexadecimal sequences if `extract_flag` is True, 
         or the original string if `extract_flag` is False.*
- `clean_html` (line 1296) `def clean_html(html_string)` - *Remove HTML tags from a string.

This function uses a regular expression to strip HTML tags and return plain text.

:param html_string: A string containing HTML content.
:returns: A cleaned string with HTML tags removed.*
- `run_command` (line 1309) `def run_command(command)` - *Run a command, print output in real-time, and store the output in a variable.

This method executes a given command using `subprocess.Popen`, streams both the standard 
output and standard error to the console in real-time, and stores the full output (stdout 
and stderr) in a variable. If interrupted, the process is terminated gracefully.

:param command: The command to be executed as a string.
:type command: str

:returns: The full output of the command (stdout and stderr).
:rtype: str

Example:
    To execute a command, call `run_command("ls -l")`.*
- `generate_random_cve_id` (line 1357) `def generate_random_cve_id()` - *Generates a random CVE (Common Vulnerabilities and Exposures) ID.

This function creates a random CVE ID by selecting a random year between 2020 and 2024,
and a random code between 1000 and 9999. The CVE ID is returned in the format 'CVE-{year}-{code}'.

Returns:
    str: A randomly generated CVE ID in the format 'CVE-{year}-{code}'.*
- `get_credentials` (line 1372) `def get_credentials(file)` - *Searches for credential files with the pattern 'credentials*.txt' and allows the user to select one.

The function lists all matching files and prompts the user to select one. It then reads the selected file
and returns a list of tuples with the format (username, password) for each line in the file.

Returns:
list of tuples: A list containing tuples with (username, password) for each credential found in the file.
                If no files are found or an invalid selection is made, an empty list is returned.*
- `obfuscate_payload` (line 1411) `def obfuscate_payload(payload)` - *Obfuscates a payload string by converting its characters into hexadecimal format, 
with additional comments for every third character.

For every character in the payload, the function converts it to its hexadecimal representation.
Every third character (after the first) is enclosed in a comment `/*hex_value*/`, while the rest 
are prefixed with `\x`.

Parameters:
    payload (str): The input string that needs to be obfuscated.

Returns:
    str: The obfuscated string where characters are replaced by their hexadecimal representations, 
         with every third character wrapped in a comment.*
- `read_payloads` (line 1435) `def read_payloads(file_path)` - *Reads a file containing payloads and returns a list of properly formatted strings.

This function opens a specified file, reads each line, and checks if the line starts with a 
double quote. If it does not, it adds double quotes around the line. Each line is stripped 
of leading and trailing whitespace before being added to the list.

Parameters:
    file_path (str): The path to the file containing payloads.

Returns:
    list: A list of strings, each representing a payload from the file, formatted with 
          leading and trailing double quotes if necessary.*
- `inject_payloads` (line 1456) `def inject_payloads(urls, payload_url, request_timeout)` - *Sends HTTP requests to a list of URLs with injected payloads for testing XSS vulnerabilities.

This function reads payloads from a specified file and sends GET requests to the provided URLs,
injecting obfuscated payloads into the query parameters or form fields to test for cross-site 
scripting (XSS) vulnerabilities. It handles both URLs with existing query parameters and those 
without. If forms are found in the response, it submits them with the payloads as well.

Parameters:
    urls (list): A list of URLs to test for XSS vulnerabilities.
    payload_url (str): A placeholder string within the payloads that will be replaced with 
                       the actual URL for testing.
    request_timeout (int, optional): The timeout for each request in seconds. Defaults to 15.

Returns:
    None: This function does not return any value but prints the status of each request and 
          form submission to the console.

Raises:
    requests.RequestException: Raises an exception if any HTTP request fails, which is handled
                               by printing a warning message.*
- `prompt` (line 1544) `def prompt(label, default)` - *Return the prompt in the function do_xss*
- `is_lower` (line 1551) `def is_lower(char)` - *Checks if a character is lowercase.

Parameters:
    char (str): The character to check.

Returns:
    bool: True if the character is lowercase, False otherwise.*
- `is_upper` (line 1564) `def is_upper(char)` - *Checks if a character is uppercase.

Parameters:
    char (str): The character to check.

Returns:
    bool: True if the character is uppercase, False otherwise.*
- `is_mixed` (line 1577) `def is_mixed(s)` - *Determines if a string contains both lowercase and uppercase characters.

Parameters:
    s (str): The string to check.

Returns:
    bool: True if the string has mixed casing, False otherwise.*
- `add` (line 1590) `def add(str_part, delimiter, i)` - *Adds a delimiter between string parts if it's not the first part.

Parameters:
    str_part (str): The string part to add.
    delimiter (str): The delimiter to insert between parts.
    i (int): The index of the part.

Returns:
    str: The string part with delimiter if applicable.*
- `detect_delimiter` (line 1607) `def detect_delimiter(foo_bar)` - *Detects the delimiter used in the input string (e.g., "-", "_", ".").

Parameters:
    foo_bar (str): The input string.

Returns:
    str: The detected delimiter.*
- `transform` (line 1626) `def transform(parts, delimiter, casing)` - *Transforms a list of string parts based on the chosen casing style.

Parameters:
    parts (list): List of string parts.
    delimiter (str): Delimiter to use between parts.
    casing (str): Casing style ('l', 'u', 'c', 'p').

Returns:
    str: The transformed string.*
- `handle` (line 1656) `def handle(input_str)` - *Splits the input string into parts based on delimiters or mixed casing.

Parameters:
    input_str (str): The input string to split.

Returns:
    list: A list of string parts.*
- `get_users_dic` (line 1685) `def get_users_dic()` - *List all .txt files in the 'sessions/' directory and prompt the user to select one by number.

:returns: The path of the selected .txt file.*
- `get_hash` (line 1717) `def get_hash(dir)` - *Searches for hash files with the pattern 'hash*.txt' and allows the user to select one.

The function lists all matching files and prompts the user to select one. It then reads the selected file
and returns the hash content as a single string, without any newline characters or extra formatting.

Returns:
str: The hash content from the selected file as a single string. If no files are found or an invalid
     selection is made, an empty string is returned.*
- `is_digit` (line 1757) `def is_digit(the_digit)` - *Check if the given character is a digit.

Args:
    the_digit (str): The character to check.

Returns:
    bool: True if the character is a digit, False otherwise.*
- `crack_password` (line 1768) `def crack_password(crypttext)` - *Crack a Cisco Type 7 password.

Args:
    crypttext (str): The encrypted password in Type 7 format.

Returns:
    str: The cracked plaintext password or an empty string if invalid.*
- `get_terminal_size` (line 1807) `def get_terminal_size()`
- `halp` (line 1815) `def halp()` - *Display the help panel for the LazyOwn RedTeam Framework.

This function prints usage instructions, options, and descriptions for 
running the LazyOwn framework. It provides users with an overview of 
command-line options that can be used when executing the `./run` command.

The output includes the current version of the framework and various 
options available for users, along with a brief description of each option.

Options include:
    - `--help`: Displays the help panel.
    - `-v`: Shows the version of the framework.
    - `-p <payloadN.json>`: Executes the framework with a specified payload 
      JSON file. This option is particularly useful for Red Teams.
    - `-c <command>`: Executes a specific command using LazyOwn, for 
      example, `ping`.
    - `--no-banner`: Runs the framework without displaying the banner.
    - `-s`: Runs the framework with root privileges.
    - `--old-banner`: Displays the old banner.

Example:
    To see the help panel, call the function as follows:
    
    >>> halp()

Note:
    - This function exits the program after displaying the help information,
      using `sys.exit(0)`.*
- `ensure_tmux_session` (line 1859) `def ensure_tmux_session(session_name)` - *Ensure that a tmux session is active.

This function checks whether a specified tmux session is currently running.
If the session does not exist, it creates a new tmux session with the specified
name and executes the command to run the LazyOwn RedTeam Framework script.

The function uses the `tmux has-session` command to check for the existence
of the session. If the session is not found (i.e., the return code is not zero),
it will create a new tmux session in detached mode and run the command 
`./run --no-banner` within that session.

Args:
    session_name (str): The name of the tmux session to check or create.

Example:
    To ensure that a tmux session named 'lazyown_sessions' is active,
    call the function as follows:
    
    >>> ensure_tmux_session('lazyown_sessions')

Note:
    - Ensure that tmux is installed and properly configured on the system.
    - The command executed within the tmux session must be valid and
      accessible in the current environment.*
- `wrapper` (line 397) `def wrapper(self)` - *internal wrapper of internal function to implement multiples rhost to operate. *
- `send_request` (line 1481) `def send_request(raw_url)`
- `handle_forms` (line 1512) `def handle_forms(content, url)`

### SH (1 files)

#### `install.sh`
**Path:** `install.sh`

*No symbols extracted*
