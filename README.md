# SET'n'3270

Man in the Middle tn3270 proxy and so much more!

```
usage: SETn3270.py [-h] [-p PORT] [--proxy] [-c COMMANDS] [-g GOODBYE] [--ssl]
                   [-v] [-d] [--altport ALTPORT] [--nossl]
                   [target]

SET'n'3270: The Mainframe TN3270 Social Engineering Tool. This tool can be
used in three ways: 1) Create a fake TSO logon screen as a honey pot. 2)
Mirror a live mainframe, even taking commands you expect users to enter. 3)
MITM a connection and output the input to the console.

positional arguments:
  target                The z/OS Mainframe TN3270 Server IP or Hostname

optional arguments:
  -h, --help            show this help message and exit
  -p PORT, --port PORT  The TN3270 server port. Default is 23
  --proxy               Operates as a MITM proxy
  -c COMMANDS, --commands COMMANDS
                        Typed commands you want to send/expect to receive.
                        Multiple commands can be seperated by a semi-colon
                        ';'. e.g: ./SETn3270.py target.com --commands
                        "logon;netview;tso"
  -g GOODBYE, --goodbye GOODBYE
                        Message disaplayed on targets screen when at the end
  --ssl                 Force SSL connections from the client.
  -v, --verbose         Be verbose
  -d, --debug           Show debug information. Displays A LOT of information
  --altport ALTPORT     Define an alternate port to accept connections to.
                        Note: Most tn3270 clients don't make it easy to change
                        ports so don't expect your targets to do so
  --nossl               Disable server side SSL. Note: Most clients will fail
                        if you do not have SSL enabled when they expect SSL
                        connections.
```
