# Polyglot Codebase Knowledge Graph

> Generated offline by **readmenator**. Supports C, C++, Python, Go, Rust, JS/TS, Java, C#, Shell, PHP, Dart, GDScript, Nim, ASM.
> No LLMs. No tokens. Pure static analysis.

**Total Files Parsed:** 3 | **Total Symbols Extracted:** 72 | **Total Imports:** 36

## Structural Knowledge Map
```mermaid
graph TD
    classDef mod fill:#1e1e1e,stroke:#ff6666,stroke-width:2px,color:#fff;
    classDef cls fill:#2d2d2d,stroke:#4ec9b0,stroke-width:2px,color:#fff;
    classDef fn fill:#333,stroke:#dcdcaa,stroke-width:1px,color:#dcdcaa;
    classDef ext fill:#111,stroke:#666,stroke-dasharray: 5 5,color:#aaa;
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
    app_py_image_to_bash["image_to_bash"]
    class app_py_image_to_bash fn;
    app_py --> app_py_image_to_bash
    app_py_list_png_files["list_png_files"]
    class app_py_list_png_files fn;
    app_py --> app_py_list_png_files
    app_py_main["main"]
    class app_py_main fn;
    app_py --> app_py_main
    install_sh["install.sh (sh)"]
    class install_sh mod;
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

## Architecture Reference

### PY (2 files)

#### `app.py`
**Path:** `app.py`

**Functions:**
- `image_to_bash` (line 27)
- `list_png_files` (line 44)
- `main` (line 54)

#### `utils.py`
**Path:** `utils.py`

**Functions:**
- `parse_ip_mac` (line 128) - *Extracts IP and MAC addresses from a formatted input string using a regular expression.

The input string is expected to be in the format: 'IP: (192.168.1.222) MAC: ec:c3:02:b0:4c:96'.
The function uses a regular expression to match and extract the IP address and MAC address from the input.

Args:
    input_string (str): The formatted string containing the IP and MAC addresses.

Returns:
    tuple: A tuple containing the extracted IP address and MAC address. If the format is incorrect, returns (None, None).*
- `create_arp_packet` (line 149) - *Constructs an ARP packet with the given source and destination IP and MAC addresses.

The function creates both Ethernet and ARP headers, combining them into a complete ARP packet.

Args:
    src_mac (str): Source MAC address in the format 'xx:xx:xx:xx:xx:xx'.
    src_ip (str): Source IP address in dotted decimal format (e.g., '192.168.1.1').
    dst_ip (str): Destination IP address in dotted decimal format (e.g., '192.168.1.2').
    dst_mac (str): Destination MAC address in the format 'xx:xx:xx:xx:xx:xx'.

Returns:
    bytes: The constructed ARP packet containing the Ethernet and ARP headers.*
- `send_packet` (line 186) - *Sends a raw ARP packet over the specified network interface.

The function creates a raw socket, binds it to the specified network interface, and sends the given packet.

Args:
    packet (bytes): The ARP packet to be sent.
    iface (str): The name of the network interface to use for sending the packet (e.g., 'eth0').

Raises:
    OSError: If an error occurs while creating the socket or sending the packet.*
- `load_version` (line 203) - *Load the version number from the 'version.json' file.

This function attempts to open the 'version.json' file and load its contents. 
If the file is found, it retrieves the version number from the JSON data. 
If the version key does not exist, it returns a default version 'release/v0.0.14'. 
If the file is not found, it also returns the default version.

Returns:
- str: The version number from the file or the default version if the file is not found or the version key is missing.*
- `print_error` (line 224) - *Prints an error message to the console.

This function takes an error message as input and prints it to the console
with a specific format to indicate that it is an error.

:param error: The error message to be printed.
:type error: str
:return: None*
- `print_msg` (line 239) - *Prints a message to the console.

This function takes a message as input and prints it to the console
with a specific format to indicate that it is an informational message.

:param msg: The message to be printed.
:type msg: str
:return: None*
- `print_warn` (line 255) - *Prints a warning message to the console.

This function takes a warning message as input and prints it to the console
with a specific format to indicate that it is a warning.

:param warn: The warning message to be printed.
:type warn: str
:return: None*
- `signal_handler` (line 271) - *Handles signals such as Control + C and shows a message on how to exit.

This function is used to handle signals like Control + C (SIGINT) and prints
a warning message instructing the user on how to exit the program using the
commands 'exit', 'q', or 'qa'.

:param sig: The signal number.
:type sig: int
:param frame: The current stack frame.
:type frame: frame
:return: None*
- `check_rhost` (line 298) - *Checks if the remote host (rhost) is defined and shows an error message if it is not.

This function verifies if the `rhost` parameter is set. If it is not defined,
an error message is printed, providing an example and directing the user to
additional help.

:param rhost: The remote host to be checked.
:type rhost: str
:return: True if rhost is defined, False otherwise.
:rtype: bool*
- `check_lhost` (line 320) - *Checks if the local host (lhost) is defined and shows an error message if it is not.

This function verifies if the `lhost` parameter is set. If it is not defined,
an error message is printed, providing an example and directing the user to
additional help.

:param lhost: The local host to be checked.
:type lhost: str
:return: True if lhost is defined, False otherwise.
:rtype: bool*
- `check_lport` (line 342) - *Checks if the local port (lport) is defined and shows an error message if it is not.

This function verifies if the `lport` parameter is set. If it is not defined,
an error message is printed, providing an example and directing the user to
additional help.

:param lport: The local port to be checked.
:type lport: int or str
:return: True if lport is defined, False otherwise.
:rtype: bool*
- `is_binary_present` (line 364) - *Internal function to verify if a binary is present on the operating system.

This function checks if a specified binary is available in the system's PATH
by using the `which` command. It returns True if the binary is found and False
otherwise.

:param binary_name: The name of the binary to be checked.
:type binary_name: str
:return: True if the binary is present, False otherwise.
:rtype: bool*
- `handle_multiple_rhosts` (line 381) - *Internal function to handle multiple remote hosts (rhost) for operations.

This function is a decorator that allows an operation to be performed across
multiple remote hosts specified in `self.params["rhost"]`. It converts a single
remote host into a list if necessary, and then iterates over each host,
performing the given function with each host. After the operation, it restores
the original remote host value.

:param func: The function to be decorated and executed for each remote host.
:type func: function
:return: The decorated function.
:rtype: function*
- `check_sudo` (line 415) - *Checks if the script is running with superuser (sudo) privileges, and if not,
restarts the script with sudo privileges.

This function verifies if the script is being executed with root privileges
by checking the effective user ID. If the script is not running as root,
it prints a warning message and restarts the script using sudo.

:return: None*
- `activate_virtualenv` (line 435) - *Activates a virtual environment and starts an interactive shell.

This function activates a virtual environment located at `venv_path` and then
launches an interactive bash shell with the virtual environment activated.

:param venv_path: The path to the virtual environment directory.
:type venv_path: str
:return: None*
- `parse_proc_net_file` (line 460) - *Internal function to parse a /proc/net file and extract network ports.

This function reads a file specified by `file_path`, processes each line to
extract local addresses and ports, and converts them from hexadecimal to decimal.
The IP addresses are converted from hexadecimal format to standard dot-decimal
notation. The function returns a list of tuples, each containing an IP address
and a port number.

:param file_path: The path to the /proc/net file to be parsed.
:type file_path: str
:return: A list of tuples, each containing an IP address and a port number.
:rtype: list of tuple*
- `get_open_ports` (line 504) - *Internal function to get open TCP and UDP ports on the operating system.

This function uses the `parse_proc_net_file` function to extract open TCP and UDP
ports from the corresponding /proc/net files. It returns two lists: one for TCP
ports and one for UDP ports.

:return: A tuple containing two lists: the first list with open TCP ports and
        the second list with open UDP ports.
:rtype: tuple of (list of tuple, list of tuple)*
- `find_credentials` (line 523) - *Searches for potential credentials in files within the specified directory.

This function uses a regular expression to find possible credentials such as
passwords, secrets, API keys, and tokens in files within the given directory.
It iterates through all files in the directory and prints any matches found.

:param directory: The directory to search for files containing credentials.
:type directory: str
:return: None*
- `rotate_char` (line 555) - *Internal function to rotate characters for ROT cipher.

This function takes a character and a shift value, and rotates the character
by the specified shift amount. It only affects alphabetical characters, leaving
non-alphabetical characters unchanged.

:param c: The character to be rotated.
:type c: str
:param shift: The number of positions to shift the character.
:type shift: int
:return: The rotated character.
:rtype: str*
- `get_network_info` (line 576) - *Retrieves network interface information with their associated IP addresses.

This function executes a shell command to gather network interface details, 
parses the output to extract interface names and their corresponding IP addresses, 
and returns this information in a dictionary format. The dictionary keys are
interface names, and the values are IP addresses.

:return: A dictionary where the keys are network interface names and the values
         are their associated IP addresses.
:rtype: dict*
- `getprompt` (line 608) - *Generate a command prompt string with network information and user status.

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
- `copy2clip` (line 644) - *Copia el texto proporcionado al portapapeles usando xclip.

Args:
    text (str): El texto que se desea copiar al portapapeles.

Example:
    copy2clip("Hello, World!")*
- `clean_output` (line 663) - *Elimina secuencias de escape de color y otros caracteres no imprimibles.*
- `teclado_usuario` (line 675) - *Procesa un archivo para extraer y mostrar caracteres desde secuencias de escritura específicas.

Args:
    filename (str): El nombre del archivo a leer.

Raises:
    FileNotFoundError: Si el archivo no se encuentra.
    Exception: Para otros errores que puedan ocurrir.*
- `salida_strace` (line 712) - *Lee un archivo, extrae texto desde secuencias de escritura y muestra el contenido reconstruido.

Args:
    filename (str): El nombre del archivo a leer.

Raises:
    FileNotFoundError: Si el archivo no se encuentra.
    Exception: Para otros errores que puedan ocurrir.*
- `exploitalert` (line 748) - *Process and display results from ExploitAlert.

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
- `packetstormsecurity` (line 791) - *Process and display results from PacketStorm Security.

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
- `nvddb` (line 833) - *Process and display results from the National Vulnerability Database.

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
- `find_ss` (line 876) - *Find CVEs in the National Vulnerability Database based on a keyword.

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
- `find_ea` (line 901) - *Find exploits in ExploitAlert based on a keyword.

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
- `find_ps` (line 928) - *Find exploits in PacketStorm Security based on a keyword.

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
- `xor_encrypt_decrypt` (line 952) - *Encrypts or decrypts data using XOR encryption with the provided key.

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
- `run` (line 977) - *Executes a shell command using the subprocess module, capturing its output.

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
- `is_exist` (line 1019) - *Check if a file exists.

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
- `get_domain` (line 1047) - *Extracts the domain from a given URL.

Parameters:
url (str): The full URL from which to extract the domain.

Returns:
str: The extracted domain from the URL, or None if it cannot be extracted.*
- `generate_certificates` (line 1063) - *Generates a certificate authority (CA), client certificate, and client key.

Returns:
    str: Paths to the generated CA certificate, client certificate, and client key.*
- `generate_emails` (line 1106) - *Generate email permutations based on the provided full name and domain.

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
- `clean_url` (line 1164) - *Verifica si el último carácter es una barra y, de ser así, la elimina*
- `random_string` (line 1170) - *Generates a random alphanumeric string.*
- `generate_http_req` (line 1175) - *Generates an HTTP request with the Shellshock payload.*
- `format_openssh_key` (line 1202) - *Formats a raw OpenSSH private key string to the correct OpenSSH format.

This function takes a raw OpenSSH private key string, cleans it by removing any unnecessary 
characters (such as newlines, spaces, and headers/footers), splits the key content into lines 
of 64 characters, and then reassembles the key with the standard OpenSSH header and footer. 
It ensures the key follows the correct OpenSSH format.

Parameters:
    raw_key (str): The raw OpenSSH private key string to format.

Returns:
    str: The formatted OpenSSH private key with proper headers, footers, and 64-character lines.*
- `format_rsa_key` (line 1233) - *Formats a raw RSA private key string to the correct PEM format.

This function takes a raw RSA private key string, cleans it by removing any unnecessary
characters (such as newlines, spaces, and headers/footers), splits the key content into lines 
of 64 characters, and then reassembles the key with the standard PEM header and footer. 
It ensures the key follows the correct RSA format.

Parameters:
    raw_key (str): The raw RSA private key string to format.

Returns:
    str: The formatted RSA private key with proper headers, footers, and 64-character lines.*
- `is_package_installed` (line 1263) - *Check if a Python package is installed.

:param package_name: Name of the package to check.
:returns: True if installed, False otherwise.*
- `extract` (line 1273) - *Extracts and processes specific hexadecimal sequences from a string based on a flag.

If the `extract_flag` is set to True, the function extracts all sequences of the form 'x[a-f0-9][a-f0-9]' 
(where 'x' is followed by two hexadecimal digits), removes the 'x' from the extracted sequences, 
and returns the processed string. If `extract_flag` is False, the function returns the original string.

Parameters:
    string (str): The input string from which hexadecimal sequences are to be extracted.
    extract_flag (bool): A flag indicating whether to perform the extraction (True) or not (False).

Returns:
    str: The processed string with the extracted hexadecimal sequences if `extract_flag` is True, 
         or the original string if `extract_flag` is False.*
- `clean_html` (line 1296) - *Remove HTML tags from a string.

This function uses a regular expression to strip HTML tags and return plain text.

:param html_string: A string containing HTML content.
:returns: A cleaned string with HTML tags removed.*
- `run_command` (line 1309) - *Run a command, print output in real-time, and store the output in a variable.

This method executes a given command using `subprocess.Popen`, streams both the standard 
output and standard error to the console in real-time, and stores the full output (stdout 
and stderr) in a variable. If interrupted, the process is terminated gracefully.

:param command: The command to be executed as a string.
:type command: str

:returns: The full output of the command (stdout and stderr).
:rtype: str

Example:
    To execute a command, call `run_command("ls -l")`.*
- `generate_random_cve_id` (line 1357) - *Generates a random CVE (Common Vulnerabilities and Exposures) ID.

This function creates a random CVE ID by selecting a random year between 2020 and 2024,
and a random code between 1000 and 9999. The CVE ID is returned in the format 'CVE-{year}-{code}'.

Returns:
    str: A randomly generated CVE ID in the format 'CVE-{year}-{code}'.*
- `get_credentials` (line 1372) - *Searches for credential files with the pattern 'credentials*.txt' and allows the user to select one.

The function lists all matching files and prompts the user to select one. It then reads the selected file
and returns a list of tuples with the format (username, password) for each line in the file.

Returns:
list of tuples: A list containing tuples with (username, password) for each credential found in the file.
                If no files are found or an invalid selection is made, an empty list is returned.*
- `obfuscate_payload` (line 1411) - *Obfuscates a payload string by converting its characters into hexadecimal format, 
with additional comments for every third character.

For every character in the payload, the function converts it to its hexadecimal representation.
Every third character (after the first) is enclosed in a comment `/*hex_value*/`, while the rest 
are prefixed with `\x`.

Parameters:
    payload (str): The input string that needs to be obfuscated.

Returns:
    str: The obfuscated string where characters are replaced by their hexadecimal representations, 
         with every third character wrapped in a comment.*
- `read_payloads` (line 1435) - *Reads a file containing payloads and returns a list of properly formatted strings.

This function opens a specified file, reads each line, and checks if the line starts with a 
double quote. If it does not, it adds double quotes around the line. Each line is stripped 
of leading and trailing whitespace before being added to the list.

Parameters:
    file_path (str): The path to the file containing payloads.

Returns:
    list: A list of strings, each representing a payload from the file, formatted with 
          leading and trailing double quotes if necessary.*
- `inject_payloads` (line 1456) - *Sends HTTP requests to a list of URLs with injected payloads for testing XSS vulnerabilities.

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
- `prompt` (line 1544) - *Return the prompt in the function do_xss*
- `is_lower` (line 1551) - *Checks if a character is lowercase.

Parameters:
    char (str): The character to check.

Returns:
    bool: True if the character is lowercase, False otherwise.*
- `is_upper` (line 1564) - *Checks if a character is uppercase.

Parameters:
    char (str): The character to check.

Returns:
    bool: True if the character is uppercase, False otherwise.*
- `is_mixed` (line 1577) - *Determines if a string contains both lowercase and uppercase characters.

Parameters:
    s (str): The string to check.

Returns:
    bool: True if the string has mixed casing, False otherwise.*
- `add` (line 1590) - *Adds a delimiter between string parts if it's not the first part.

Parameters:
    str_part (str): The string part to add.
    delimiter (str): The delimiter to insert between parts.
    i (int): The index of the part.

Returns:
    str: The string part with delimiter if applicable.*
- `detect_delimiter` (line 1607) - *Detects the delimiter used in the input string (e.g., "-", "_", ".").

Parameters:
    foo_bar (str): The input string.

Returns:
    str: The detected delimiter.*
- `transform` (line 1626) - *Transforms a list of string parts based on the chosen casing style.

Parameters:
    parts (list): List of string parts.
    delimiter (str): Delimiter to use between parts.
    casing (str): Casing style ('l', 'u', 'c', 'p').

Returns:
    str: The transformed string.*
- `handle` (line 1656) - *Splits the input string into parts based on delimiters or mixed casing.

Parameters:
    input_str (str): The input string to split.

Returns:
    list: A list of string parts.*
- `get_users_dic` (line 1685) - *List all .txt files in the 'sessions/' directory and prompt the user to select one by number.

:returns: The path of the selected .txt file.*
- `get_hash` (line 1717) - *Searches for hash files with the pattern 'hash*.txt' and allows the user to select one.

The function lists all matching files and prompts the user to select one. It then reads the selected file
and returns the hash content as a single string, without any newline characters or extra formatting.

Returns:
str: The hash content from the selected file as a single string. If no files are found or an invalid
     selection is made, an empty string is returned.*
- `is_digit` (line 1757) - *Check if the given character is a digit.

Args:
    the_digit (str): The character to check.

Returns:
    bool: True if the character is a digit, False otherwise.*
- `crack_password` (line 1768) - *Crack a Cisco Type 7 password.

Args:
    crypttext (str): The encrypted password in Type 7 format.

Returns:
    str: The cracked plaintext password or an empty string if invalid.*
- `get_terminal_size` (line 1807)
- `halp` (line 1815) - *Display the help panel for the LazyOwn RedTeam Framework.

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
- `ensure_tmux_session` (line 1859) - *Ensure that a tmux session is active.

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
- `wrapper` (line 397) - *internal wrapper of internal function to implement multiples rhost to operate. *
- `send_request` (line 1481)
- `handle_forms` (line 1512)

### SH (1 files)

#### `install.sh`
**Path:** `install.sh`

*No symbols extracted*
