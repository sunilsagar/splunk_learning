# Installing and Configuring Splunk

## 1. Install Splunk

### MacBook:

You can download Splunk from the official website: [Splunk Download](https://www.splunk.com/en_us/download/splunk-enterprise.html#)

```bash
# Download Splunk
wget -O splunk-9.1.1-64e843ea36b1-darwin-64.tgz "https://download.splunk.com/products/splunk/releases/9.1.1/osx/splunk-9.1.1-64e843ea36b1-darwin-64.tgz"

# Install Splunk
tar -xvzf splunk-9.1.1-64e843ea36b1-darwin-64.tgz

❯ ./splunk start --accept-license

This appears to be your first time running this version of Splunk.

Splunk software must create an administrator account during startup. Otherwise, you cannot log in.
Create credentials for the administrator account.
Characters do not appear on the screen when you type in credentials.

Please enter an administrator username: sunil
Password must contain at least:
   * 8 total printable ASCII character(s).
Please enter a new password:
Please confirm new password:
Copying '/Users/User/Documents/lab/splunk/splunk/etc/openldap/ldap.conf.default' to '/Users/User/Documents/lab/splunk/splunk/etc/openldap/ldap.conf'.
Generating RSA private key, 2048 bit long modulus
....................+++++
......................................................................................................................................+++++
e is 65537 (0x10001)
writing RSA key

Generating RSA private key, 2048 bit long modulus
.........................+++++
.......+++++
e is 65537 (0x10001)
writing RSA key

Moving '/Users/User/Documents/lab/splunk/splunk/share/splunk/search_mrsparkle/modules.new' to '/Users/User/Documents/lab/splunk/splunk/share/splunk/search_mrsparkle/modules'.

Splunk> Needle. Haystack. Found.

Checking prerequisites...
	Checking http port [8000]: open
	Checking mgmt port [8089]: open
	Checking appserver port [127.0.0.1:8065]: open
	Checking kvstore port [8191]: open
	Checking configuration... Done.
		Creating: /Users/User/Documents/lab/splunk/splunk/var/lib/splunk
		Creating: /Users/User/Documents/lab/splunk/splunk/var/run/splunk
		Creating: /Users/User/Documents/lab/splunk/splunk/var/run/splunk/appserver/i18n
		Creating: /Users/User/Documents/lab/splunk/splunk/var/run/splunk/appserver/modules/static/css
		Creating: /Users/User/Documents/lab/splunk/splunk/var/run/splunk/upload
		Creating: /Users/User/Documents/lab/splunk/splunk/var/run/splunk/search_telemetry
		Creating: /Users/User/Documents/lab/splunk/splunk/var/run/splunk/search_log
		Creating: /Users/User/Documents/lab/splunk/splunk/var/spool/splunk
		Creating: /Users/User/Documents/lab/splunk/splunk/var/spool/dirmoncache
		Creating: /Users/User/Documents/lab/splunk/splunk/var/lib/splunk/authDb
		Creating: /Users/User/Documents/lab/splunk/splunk/var/lib/splunk/hashDb
New certs have been generated in '/Users/User/Documents/lab/splunk/splunk/etc/auth'.
	Checking critical directories...	Done
	Checking indexes...
		Validated: _audit _configtracker _internal _introspection _metrics _metrics_rollup _telemetry _thefishbucket history main summary
	Done
	Checking filesystem compatibility...  Done
	Checking conf files for problems...
	Done
	Checking default conf files for edits...
	Validating installed files against hashes from '/Users/User/Documents/lab/splunk/splunk/splunk-9.1.1-64e843ea36b1-darwin-64-manifest'
	All installed files intact.
	Done
All preliminary checks passed.

Starting splunk server daemon (splunkd)...
Generating a RSA private key
.....................................+++++
....................................................................................................................+++++
writing new private key to 'privKeySecure.pem'
-----
Signature ok
subject=/CN=My-HostName/O=SplunkUser
Getting CA Private Key
writing RSA key
PYTHONHTTPSVERIFY is set to 0 in splunk-launch.conf disabling certificate validation for the httplib and urllib libraries shipped with the embedded Python interpreter; must be set to "1" for increased security
Done


Waiting for web server at http://127.0.0.1:8000 to be available................... Done


If you get stuck, we're here to help.
Look for answers here: http://docs.splunk.com

The Splunk web interface is at http://<hostname>:8000 
This is also accessible at : 

```
Splunk is also accessible at URL : 
```bash
http://localhost:8000
http://127.0.0.1:8000
```