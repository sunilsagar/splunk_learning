# Installing Splunk Universal Forwarder

## 1. Install Splunk Forwarder

### MacBook:

Download Universal Fowarder : [Splunk Download](https://www.splunk.com/en_us/download/universal-forwarder.html#)

```bash
wget -O splunkforwarder-9.1.1-64e843ea36b1-darwin-universal2.tgz "https://download.splunk.com/products/universalforwarder/releases/9.1.1/osx/splunkforwarder-9.1.1-64e843ea36b1-darwin-universal2.tgz"
```

```bash
./splunk start --accept-license
This appears to be your first time running this version of Splunk.

Splunk software must create an administrator account during startup. Otherwise, you cannot log in.
Create credentials for the administrator account.
Characters do not appear on the screen when you type in credentials.

Please enter an administrator username: sunil
Password must contain at least:
   * 8 total printable ASCII character(s).
Please enter a new password:
Please confirm new password:

Splunk> Needle. Haystack. Found.

Checking prerequisites...
	Checking mgmt port [8089]: not available
ERROR: mgmt port [8089] - port is already bound.  Splunk needs to use this port.
Would you like to change ports? [y/n]: y
Enter a new mgmt port: 8090
Setting mgmt to port: 8090
The server's splunkd port has been changed.
	Checking mgmt port [8090]: open
		Creating: /Users/User/Documents/lab/splunk/splunkforwarder/var/run/splunk/appserver/i18n
		Creating: /Users/User/Documents/lab/splunk/splunkforwarder/var/run/splunk/appserver/modules/static/css
		Creating: /Users/User/Documents/lab/splunk/splunkforwarder/var/run/splunk/upload
		Creating: /Users/User/Documents/lab/splunk/splunkforwarder/var/run/splunk/search_telemetry
		Creating: /Users/User/Documents/lab/splunk/splunkforwarder/var/run/splunk/search_log
		Creating: /Users/User/Documents/lab/splunk/splunkforwarder/var/spool/splunk
		Creating: /Users/User/Documents/lab/splunk/splunkforwarder/var/spool/dirmoncache
		Creating: /Users/User/Documents/lab/splunk/splunkforwarder/var/lib/splunk/authDb
		Creating: /Users/User/Documents/lab/splunk/splunkforwarder/var/lib/splunk/hashDb
New certs have been generated in '/Users/User/Documents/lab/splunk/splunkforwarder/etc/auth'.
	Checking conf files for problems...
	Done
	Checking default conf files for edits...
	Validating installed files against hashes from '/Users/User/Documents/lab/splunk/splunkforwarder/splunkforwarder-9.1.1-64e843ea36b1-darwin-universal2-manifest'
	All installed files intact.
	Done
All preliminary checks passed.

Starting splunk server daemon (splunkd)...

Done

❯
```

## Add Receiver

## Add Receiver

a. Login to the Splunk Console.
b. Navigate to: **Settings** > **Forwarding and Receiving**.
c. Under "Receive data," click on "**+ Add New**."

   ![Configure Receiver](images/settings-configure-receiver.png)

   i. Add the value `9997` for "**Listen on this port**."
   ii. Click on "**Save**."
