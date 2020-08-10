# README

This module provides a simple interface to control an Energenie power socket.

Install Python libraries

```
pip install energenie

```

Tested devices:
- EG-PMS2-LAN

The Energenie module is released under the MIT licence. Feel free to copy or modify this module. If you do some
improvements or changes, it would be nice if you would share the changes with me!

## Use the Energenie class directly

energenie = Energenie('192.168.1.10', 'socket password')
energenie.login()
print energenie.get_socket_state()
print energenie.get_socket_state(1)
print energenie.get_socket_state(2)
energenie.set_socket_state(3, False)
print energenie.get_socket_state()
energenie.logout()

## Command line

Get the state of all sockets
```
python energenie.py --ip '192.168.1.10'  -g
{1: True, 2: False, 3: False, 4: False}
```

Get the state of socket 3
```
python energenie.py --ip '192.168.1.10' -s 3 -g
False
```

Enable socket 3
```
python energenie.py --ip '192.168.1.10' -s 3 -e
```

Enable all sockets
```
python energenie.py --ip '192.168.1.10' -e
```

Taken From : https://github.com/schneuwlym/energenie
