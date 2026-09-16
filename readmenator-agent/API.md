# API

## app.py

### image_to_bash (function) `def image_to_bash(image_path, image_res)`
- Defined: `app.py:27`
- Depends on: `utils.py`

### list_png_files (function) `def list_png_files()`
- Defined: `app.py:44`
- Depends on: `utils.py`

### main (function) `def main()`
- Defined: `app.py:54`
- Depends on: `utils.py`

## utils.py

### parse_ip_mac (function) `def parse_ip_mac(input_string)`
- Defined: `utils.py:128`
- Doc: Extracts IP and MAC addresses from a formatted input string using a regular expression.
- Imported by: `app.py`

### create_arp_packet (function) `def create_arp_packet(src_mac, src_ip, dst_ip, dst_mac)`
- Defined: `utils.py:149`
- Doc: Constructs an ARP packet with the given source and destination IP and MAC addresses.
- Imported by: `app.py`

### send_packet (function) `def send_packet(packet, iface)`
- Defined: `utils.py:186`
- Doc: Sends a raw ARP packet over the specified network interface.
- Imported by: `app.py`

### load_version (function) `def load_version()`
- Defined: `utils.py:203`
- Doc: Load the version number from the 'version.json' file.
- Imported by: `app.py`

### print_error (function) `def print_error(error)`
- Defined: `utils.py:224`
- Doc: Prints an error message to the console.
- Imported by: `app.py`

### print_msg (function) `def print_msg(msg)`
- Defined: `utils.py:239`
- Doc: Prints a message to the console.
- Imported by: `app.py`

### print_warn (function) `def print_warn(warn)`
- Defined: `utils.py:255`
- Doc: Prints a warning message to the console.
- Imported by: `app.py`

### signal_handler (function) `def signal_handler(sig, frame)`
- Defined: `utils.py:271`
- Doc: Handles signals such as Control + C and shows a message on how to exit.
- Imported by: `app.py`

### check_rhost (function) `def check_rhost(rhost)`
- Defined: `utils.py:298`
- Doc: Checks if the remote host (rhost) is defined and shows an error message if it is not.
- Imported by: `app.py`

### check_lhost (function) `def check_lhost(lhost)`
- Defined: `utils.py:320`
- Doc: Checks if the local host (lhost) is defined and shows an error message if it is not.
- Imported by: `app.py`

### check_lport (function) `def check_lport(lport)`
- Defined: `utils.py:342`
- Doc: Checks if the local port (lport) is defined and shows an error message if it is not.
- Imported by: `app.py`

### is_binary_present (function) `def is_binary_present(binary_name)`
- Defined: `utils.py:364`
- Doc: Internal function to verify if a binary is present on the operating system.
- Imported by: `app.py`

### handle_multiple_rhosts (function) `def handle_multiple_rhosts(func)`
- Defined: `utils.py:381`
- Doc: Internal function to handle multiple remote hosts (rhost) for operations.
- Imported by: `app.py`

### check_sudo (function) `def check_sudo()`
- Defined: `utils.py:415`
- Doc: Checks if the script is running with superuser (sudo) privileges, and if not,
- Imported by: `app.py`

### activate_virtualenv (function) `def activate_virtualenv(venv_path)`
- Defined: `utils.py:435`
- Doc: Activates a virtual environment and starts an interactive shell.
- Imported by: `app.py`

### parse_proc_net_file (function) `def parse_proc_net_file(file_path)`
- Defined: `utils.py:460`
- Doc: Internal function to parse a /proc/net file and extract network ports.
- Imported by: `app.py`

### get_open_ports (function) `def get_open_ports()`
- Defined: `utils.py:504`
- Doc: Internal function to get open TCP and UDP ports on the operating system.
- Imported by: `app.py`

### find_credentials (function) `def find_credentials(directory)`
- Defined: `utils.py:523`
- Doc: Searches for potential credentials in files within the specified directory.
- Imported by: `app.py`

### rotate_char (function) `def rotate_char(c, shift)`
- Defined: `utils.py:555`
- Doc: Internal function to rotate characters for ROT cipher.
- Imported by: `app.py`

### get_network_info (function) `def get_network_info()`
- Defined: `utils.py:576`
- Doc: Retrieves network interface information with their associated IP addresses.
- Imported by: `app.py`

### getprompt (function) `def getprompt()`
- Defined: `utils.py:608`
- Doc: Generate a command prompt string with network information and user status.
- Imported by: `app.py`

### copy2clip (function) `def copy2clip(text)`
- Defined: `utils.py:644`
- Doc: Copia el texto proporcionado al portapapeles usando xclip.
- Imported by: `app.py`

### clean_output (function) `def clean_output(output)`
- Defined: `utils.py:663`
- Doc: Elimina secuencias de escape de color y otros caracteres no imprimibles.
- Imported by: `app.py`

### teclado_usuario (function) `def teclado_usuario(filename)`
- Defined: `utils.py:675`
- Doc: Procesa un archivo para extraer y mostrar caracteres desde secuencias de escritura específicas.
- Imported by: `app.py`

### salida_strace (function) `def salida_strace(filename)`
- Defined: `utils.py:712`
- Doc: Lee un archivo, extrae texto desde secuencias de escritura y muestra el contenido reconstruido.
- Imported by: `app.py`

### exploitalert (function) `def exploitalert(content)`
- Defined: `utils.py:748`
- Doc: Process and display results from ExploitAlert.
- Imported by: `app.py`

### packetstormsecurity (function) `def packetstormsecurity(content)`
- Defined: `utils.py:791`
- Doc: Process and display results from PacketStorm Security.
- Imported by: `app.py`

### nvddb (function) `def nvddb(content)`
- Defined: `utils.py:833`
- Doc: Process and display results from the National Vulnerability Database.
- Imported by: `app.py`

### find_ss (function) `def find_ss(keyword)`
- Defined: `utils.py:876`
- Doc: Find CVEs in the National Vulnerability Database based on a keyword.
- Imported by: `app.py`

### find_ea (function) `def find_ea(keyword)`
- Defined: `utils.py:901`
- Doc: Find exploits in ExploitAlert based on a keyword.
- Imported by: `app.py`

### find_ps (function) `def find_ps(keyword)`
- Defined: `utils.py:928`
- Doc: Find exploits in PacketStorm Security based on a keyword.
- Imported by: `app.py`

### xor_encrypt_decrypt (function) `def xor_encrypt_decrypt(data, key)`
- Defined: `utils.py:952`
- Doc: Encrypts or decrypts data using XOR encryption with the provided key.
- Imported by: `app.py`

### run (function) `def run(command)`
- Defined: `utils.py:977`
- Doc: Executes a shell command using the subprocess module, capturing its output.
- Imported by: `app.py`

### is_exist (function) `def is_exist(file)`
- Defined: `utils.py:1019`
- Doc: Check if a file exists.
- Imported by: `app.py`

### get_domain (function) `def get_domain(url)`
- Defined: `utils.py:1047`
- Doc: Extracts the domain from a given URL.
- Imported by: `app.py`

### generate_certificates (function) `def generate_certificates()`
- Defined: `utils.py:1063`
- Doc: Generates a certificate authority (CA), client certificate, and client key.
- Imported by: `app.py`

### generate_emails (function) `def generate_emails(full_name, domain)`
- Defined: `utils.py:1106`
- Doc: Generate email permutations based on the provided full name and domain.
- Imported by: `app.py`

### clean_url (function) `def clean_url(host)`
- Defined: `utils.py:1164`
- Doc: Verifica si el último carácter es una barra y, de ser así, la elimina
- Imported by: `app.py`

### random_string (function) `def random_string(length)`
- Defined: `utils.py:1170`
- Doc: Generates a random alphanumeric string.
- Imported by: `app.py`

### generate_http_req (function) `def generate_http_req(host, port, uri, custom_header, cmd)`
- Defined: `utils.py:1175`
- Doc: Generates an HTTP request with the Shellshock payload.
- Imported by: `app.py`

### format_openssh_key (function) `def format_openssh_key(raw_key)`
- Defined: `utils.py:1202`
- Doc: Formats a raw OpenSSH private key string to the correct OpenSSH format.
- Imported by: `app.py`

### format_rsa_key (function) `def format_rsa_key(raw_key)`
- Defined: `utils.py:1233`
- Doc: Formats a raw RSA private key string to the correct PEM format.
- Imported by: `app.py`

### is_package_installed (function) `def is_package_installed(package_name)`
- Defined: `utils.py:1263`
- Doc: Check if a Python package is installed.
- Imported by: `app.py`

### extract (function) `def extract(string, extract_flag)`
- Defined: `utils.py:1273`
- Doc: Extracts and processes specific hexadecimal sequences from a string based on a flag.
- Imported by: `app.py`

### clean_html (function) `def clean_html(html_string)`
- Defined: `utils.py:1296`
- Doc: Remove HTML tags from a string.
- Imported by: `app.py`

### run_command (function) `def run_command(command)`
- Defined: `utils.py:1309`
- Doc: Run a command, print output in real-time, and store the output in a variable.
- Imported by: `app.py`

### generate_random_cve_id (function) `def generate_random_cve_id()`
- Defined: `utils.py:1357`
- Doc: Generates a random CVE (Common Vulnerabilities and Exposures) ID.
- Imported by: `app.py`

### get_credentials (function) `def get_credentials(file)`
- Defined: `utils.py:1372`
- Doc: Searches for credential files with the pattern 'credentials*.txt' and allows the user to select one.
- Imported by: `app.py`

### obfuscate_payload (function) `def obfuscate_payload(payload)`
- Defined: `utils.py:1411`
- Doc: Obfuscates a payload string by converting its characters into hexadecimal format, 
- Imported by: `app.py`

### read_payloads (function) `def read_payloads(file_path)`
- Defined: `utils.py:1435`
- Doc: Reads a file containing payloads and returns a list of properly formatted strings.
- Imported by: `app.py`

### inject_payloads (function) `def inject_payloads(urls, payload_url, request_timeout)`
- Defined: `utils.py:1456`
- Doc: Sends HTTP requests to a list of URLs with injected payloads for testing XSS vulnerabilities.
- Imported by: `app.py`

### prompt (function) `def prompt(label, default)`
- Defined: `utils.py:1544`
- Doc: Return the prompt in the function do_xss
- Imported by: `app.py`

### is_lower (function) `def is_lower(char)`
- Defined: `utils.py:1551`
- Doc: Checks if a character is lowercase.
- Imported by: `app.py`

### is_upper (function) `def is_upper(char)`
- Defined: `utils.py:1564`
- Doc: Checks if a character is uppercase.
- Imported by: `app.py`

### is_mixed (function) `def is_mixed(s)`
- Defined: `utils.py:1577`
- Doc: Determines if a string contains both lowercase and uppercase characters.
- Imported by: `app.py`

### add (function) `def add(str_part, delimiter, i)`
- Defined: `utils.py:1590`
- Doc: Adds a delimiter between string parts if it's not the first part.
- Imported by: `app.py`

### detect_delimiter (function) `def detect_delimiter(foo_bar)`
- Defined: `utils.py:1607`
- Doc: Detects the delimiter used in the input string (e.g., "-", "_", ".").
- Imported by: `app.py`

### transform (function) `def transform(parts, delimiter, casing)`
- Defined: `utils.py:1626`
- Doc: Transforms a list of string parts based on the chosen casing style.
- Imported by: `app.py`

### handle (function) `def handle(input_str)`
- Defined: `utils.py:1656`
- Doc: Splits the input string into parts based on delimiters or mixed casing.
- Imported by: `app.py`

### get_users_dic (function) `def get_users_dic()`
- Defined: `utils.py:1685`
- Doc: List all .txt files in the 'sessions/' directory and prompt the user to select one by number.
- Imported by: `app.py`

### get_hash (function) `def get_hash(dir)`
- Defined: `utils.py:1717`
- Doc: Searches for hash files with the pattern 'hash*.txt' and allows the user to select one.
- Imported by: `app.py`

### is_digit (function) `def is_digit(the_digit)`
- Defined: `utils.py:1757`
- Doc: Check if the given character is a digit.
- Imported by: `app.py`

### crack_password (function) `def crack_password(crypttext)`
- Defined: `utils.py:1768`
- Doc: Crack a Cisco Type 7 password.
- Imported by: `app.py`

### get_terminal_size (function) `def get_terminal_size()`
- Defined: `utils.py:1807`
- Imported by: `app.py`

### halp (function) `def halp()`
- Defined: `utils.py:1815`
- Doc: Display the help panel for the LazyOwn RedTeam Framework.
- Imported by: `app.py`

### ensure_tmux_session (function) `def ensure_tmux_session(session_name)`
- Defined: `utils.py:1859`
- Doc: Ensure that a tmux session is active.
- Imported by: `app.py`

### wrapper (function) `def wrapper(self)`
- Defined: `utils.py:397`
- Doc: internal wrapper of internal function to implement multiples rhost to operate. 
- Imported by: `app.py`

### send_request (function) `def send_request(raw_url)`
- Defined: `utils.py:1481`
- Imported by: `app.py`

### handle_forms (function) `def handle_forms(content, url)`
- Defined: `utils.py:1512`
- Imported by: `app.py`
