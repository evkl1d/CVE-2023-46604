# CVE-2023-46604

This repository contains an exploit script and a Proof of Concept (PoC) XML file for the CVE-2023-46604 vulnerability affecting Apache ActiveMQ. The vulnerability allows for remote code execution due to unsafe deserialization practices within the OpenWire protocol.

## Description

CVE-2023-46604 is a deserialization vulnerability that exists in Apache ActiveMQ's OpenWire protocol. This flaw can be exploited by an attacker to execute arbitrary code on the server where ActiveMQ is running. The exploit script in this repository automates the process of sending a crafted request to the server to trigger the vulnerability.

## Repository Contents

- `exploit.py` - The main Python exploit script that triggers the vulnerability.
- `poc.xml` - An XML file that serves as a proof of concept for the exploit.

## Prerequisites

Before running the exploit script, ensure that you have:

- Python 3.x installed on your system.
- Network access to the vulnerable ActiveMQ server.
- The URL to the `poc.xml` file, which should be accessible by the target ActiveMQ server.

## Usage

To use the exploit script, you need to provide the IP address of the target ActiveMQ server, the port number (default is 61616), and the URL to the `poc.xml` file.

```
python exploit.py -i <target-ip> -p <target-port> -u <url-to-poc.xml>
```

Replace `<target-ip>`, `<target-port>`, and `<url-to-poc.xml>` with the appropriate values for your target environment.

## Credits
The exploit script provided in this repository is based on an original exploit written in Go by [X1r0z](https://github.com/X1r0z/ActiveMQ-RCE). The Python version aims to provide a similar exploit in a different programming language while maintaining the effectiveness of the original exploit.

## Disclaimer

This exploit is provided for educational purposes only. The authors of this repository are not responsible for any misuse or damage caused by this material. Use it at your own risk.

## Contact

If you have any questions or feedback regarding this exploit, please open an issue in this repository.
