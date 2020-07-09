# MyPublicIP
A simple automation tool that reports your public IP address to you via email, It must be executed on a Windows or a Linux/Unix box in your LAN, It reports the IP address based on a time interval that the user inserts (optional). It also connects to a local database to store the past IP addresses and avoid duplicate reports. The tool is useful for people that are with ISPs that don't provide static public IP addresses.

Command line examples:

- sudo python3 MyPublicip.py --re ExampleReceiverEmail@ExampleDomain.com --o linux --se ExampleSenderEmail2@gmail.com --pw ExampleSenderPassword --t 24
- python MyPublicip.py --re ExampleReceiverEmail@ExampleDomain.com --o windows --se ExampleSenderEmail2@gmail.com --pw ExampleSenderPassword --t 24



Usage:

MyPublicIp.py [-h] --re RE --o O --se SE --pw PW [--t T]

[Example 1]: python MyPublicip.py --re ExampleReceiverEmail@ExampleDomain.com
--o windows --se ExampleSenderEmail2@gmail.com --pw ExampleSenderPassword --t
24 [Example 2]: python3 MyPublicip.py --re
ExampleReceiverEmail@ExampleDomain.com --o linux --se
ExampleSenderEmail2@gmail.com --pw ExampleSenderPassword --t 24

optional arguments:
  -h, --help            show this help message and exit
  --re RE, --receiver_email RE
                        Email that the IP address will be sent to
  --o O, --os O         OS to be specified so the accurate command can get
                        executed (Available options: Windows/Linux)
  --se SE, --sender_email SE
                        Email address that will be used to send the results
                        (Less secure apps must be enabled on your account)
  --pw PW, --sender_password PW
                        Email password that will be used to login to the
                        sender's email (Will appear in plain text on this
                        terminal)
  --t T, --time T       Wait time until IP address is obtained and sent again
                        (time should be in hours)
