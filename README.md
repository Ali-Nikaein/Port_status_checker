# Port_status_checker
The purpose of this code is to check a range of ports on a host and report which ports are open. Additionally, it identifies the services running on those open ports.

## Purpose of Code
The purpose of this code is to check a range of ports on a host and report which ports are open. Additionally, it identifies the services running on those open ports.

## How to Use
1. Clone the repository to your local machine.
   ```bash
   [git clone <repository-url>](https://github.com/Ali-Nikaein/Port_status_checker.git)
   ```
2. Compile the code :
   ```bash
   gcc port_status.c -o port_checker -lws2_32
   ```
3. Run the executable with the host IP address and a list of ports to check.
   ```bash
   ./port_checker <host> <port1> <port2> ... <portN>
   ```

## Example
```bash
./port_checker 127.0.0.1 80 443 8080 8081
```

## Dependencies
- Windows Socket API (winsock2.h)
- Standard Input/Output functions (stdio.h)
- Standard Library functions (stdlib.h)
- String manipulation functions (string.h)

## Code Explanation
The code initializes the Winsock library, creates a socket for each specified port, and attempts to connect to the host on that port. If the connection is successful, it prints that the port is open and identifies the service running on that port. If the connection fails, it indicates that the port is closed.

## Error Handling
The code includes basic error handling, such as checking if the correct number of command-line arguments is provided and handling socket creation failures.

## Disclaimer
This tool is intended for educational and testing purposes only. Unauthorized port scanning of systems without permission is illegal and unethical. Ensure you have the appropriate authorization before using this tool on any network. The developers are not responsible for any misuse or consequences arising from the use of this tool.
