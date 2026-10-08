# root

*Community 0 | 2 files | cohesion 1.00*

## Definition

This community groups 2 file(s) rooted at `root` with dominant language py (cohesion 1.00). Central symbols: `activate_virtualenv`, `add`, `check_lhost`, `check_lport`, `check_rhost`, `check_sudo`, `clean_html`, `clean_output`. Core file: `utils.py` (69 symbols). Documented purpose: Autor: Gris Iscomeback Correo electrónico: grisiscomeback[at]gmail[dot]com Fecha de creación: 09/06/2024 Licencia: GPL v3  Descripción: Este archivo contiene la.

## Files

| File | Language | Layer | Symbols | Doc |
|------|----------|-------|---------|-----|
| `app.py` | py | utility | 3 | yes |
| `utils.py` | py | utility | 69 | yes |

## Key Symbols

- `image_to_bash` (function, `app.py:27`) `def image_to_bash(image_path, image_res)`
- `list_png_files` (function, `app.py:44`) `def list_png_files()`
- `main` (function, `app.py:54`) `def main()`
- `parse_ip_mac` (function, `utils.py:128`) `def parse_ip_mac(input_string)` - Extracts IP and MAC addresses from a formatted input string using a regular expression.
- `create_arp_packet` (function, `utils.py:149`) `def create_arp_packet(src_mac, src_ip, dst_ip, dst_mac)` - Constructs an ARP packet with the given source and destination IP and MAC addresses.
- `send_packet` (function, `utils.py:186`) `def send_packet(packet, iface)` - Sends a raw ARP packet over the specified network interface.
- `load_version` (function, `utils.py:203`) `def load_version()` - Load the version number from the 'version.json' file.
- `print_error` (function, `utils.py:224`) `def print_error(error)` - Prints an error message to the console.
- `print_msg` (function, `utils.py:239`) `def print_msg(msg)` - Prints a message to the console.
- `print_warn` (function, `utils.py:255`) `def print_warn(warn)` - Prints a warning message to the console.
- `signal_handler` (function, `utils.py:271`) `def signal_handler(sig, frame)` - Handles signals such as Control + C and shows a message on how to exit.
- `check_rhost` (function, `utils.py:298`) `def check_rhost(rhost)` - Checks if the remote host (rhost) is defined and shows an error message if it is not.
- `check_lhost` (function, `utils.py:320`) `def check_lhost(lhost)` - Checks if the local host (lhost) is defined and shows an error message if it is not.
- `check_lport` (function, `utils.py:342`) `def check_lport(lport)` - Checks if the local port (lport) is defined and shows an error message if it is not.
- `is_binary_present` (function, `utils.py:364`) `def is_binary_present(binary_name)` - Internal function to verify if a binary is present on the operating system.
- `handle_multiple_rhosts` (function, `utils.py:381`) `def handle_multiple_rhosts(func)` - Internal function to handle multiple remote hosts (rhost) for operations.
- `wrapper` (function, `utils.py:397`) `def wrapper(self)` - internal wrapper of internal function to implement multiples rhost to operate.
- `check_sudo` (function, `utils.py:415`) `def check_sudo()` - Checks if the script is running with superuser (sudo) privileges, and if not,
- `activate_virtualenv` (function, `utils.py:435`) `def activate_virtualenv(venv_path)` - Activates a virtual environment and starts an interactive shell.
- `parse_proc_net_file` (function, `utils.py:460`) `def parse_proc_net_file(file_path)` - Internal function to parse a /proc/net file and extract network ports.
- `get_open_ports` (function, `utils.py:504`) `def get_open_ports()` - Internal function to get open TCP and UDP ports on the operating system.
- `find_credentials` (function, `utils.py:523`) `def find_credentials(directory)` - Searches for potential credentials in files within the specified directory.
- `rotate_char` (function, `utils.py:555`) `def rotate_char(c, shift)` - Internal function to rotate characters for ROT cipher.
- `get_network_info` (function, `utils.py:576`) `def get_network_info()` - Retrieves network interface information with their associated IP addresses.
- `getprompt` (function, `utils.py:608`) `def getprompt()` - Generate a command prompt string with network information and user status.
- `copy2clip` (function, `utils.py:644`) `def copy2clip(text)` - Copia el texto proporcionado al portapapeles usando xclip.
- `clean_output` (function, `utils.py:663`) `def clean_output(output)` - Elimina secuencias de escape de color y otros caracteres no imprimibles.
- `teclado_usuario` (function, `utils.py:675`) `def teclado_usuario(filename)` - Procesa un archivo para extraer y mostrar caracteres desde secuencias de escritura específicas.
- `salida_strace` (function, `utils.py:712`) `def salida_strace(filename)` - Lee un archivo, extrae texto desde secuencias de escritura y muestra el contenido reconstruido.
- `exploitalert` (function, `utils.py:748`) `def exploitalert(content)` - Process and display results from ExploitAlert.

## Internal vs External Edges

- Internal resolved imports (EXTRACTED): 1
- Cross-boundary resolved imports (EXTRACTED): 0

## Connections

- [INFERRED] shares_context community 0 <-> 1 (strength 0.5): Inferred shared context (layer utility) with no import path between community 0 (root) and community 1 (orphans).

## Risks

- [taint medium] `utils.py` -> `utils.py` via `requests` (0 hops)
- [taint high] `utils.py` -> `utils.py` via `subprocess` (0 hops)
- [taint medium] `utils.py` -> `utils.py` via `urllib.request` (0 hops)
- [dataflow UNCHECKED_ALLOC] `app.py:29` `image_to_bash` `img`: Result of allocator stored in `img` is never checked against NULL.

## Open Questions

- Is the dangerous import `requests` in `utils.py` still required, or can it be isolated?
- What would break if the most connected file in root changed?
- Should root be split, given cohesion 1.00?

## Sources

- `app.py`
- `utils.py`
