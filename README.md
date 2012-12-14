## Simple SMTP Sink Server

This is an extremely Simple SMTP sink server written in Python. Message are neither validated, proxied nor delivered to any recepient. 

The server comes with a web based interface for viewing all messages passing through this mail server.

Useful for testing out smtp/emails of your project.


## Instructions

### Usage

Run

```
$ python smtp_server.py
```

open web interface at

```
http://localhost:8080/
```

### Config

1. Default web url : http://localhost:8080/
2. Default SMTP host: http://localhost:1130/
3. Edit `server = SMTPServerThread(('127.0.0.1', 1130) )` to your desired SMTP ip & port.
4. Edit `bottle.run(app, host='localhost', port=8080, reloader=(not runServer))` to your desired web ip & port

### Pre-requisits

- Django >= 1.4 (for templating)
- python >= 2.5

Comes package with bottle.py

### Note

All data is stored in pickled format and is loaded into memory. You may want to delete the data file from time to time.

### Todo:

 - Allow deletion of messages
 - Render HTML email content