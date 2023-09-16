# Operation - Start Stop Staus

## 1. Status
```bash
splunk status
```
```
❯ ./splunk status
splunkd is running (PID: 27450).
splunk helpers are running (PIDs: 27451 27689 27731 27739).
```

## 2. Stop Splunk
```bash
splunk stop
```
```
❯ ./splunk stop
Stopping splunkd...
Shutting down.  Please wait, as this may take a few minutes.
...
Stopping splunk helpers...

Done.
❯
❯ ./splunk status
splunkd is not running.
❯
```

## 3. Start Splunk
```bash
splunk start
```
```
❯ ./splunk start

Splunk> Needle. Haystack. Found.

Checking prerequisites...
	Checking http port [8000]: open
	Checking mgmt port [8089]: open
	Checking appserver port [127.0.0.1:8065]: open
	Checking kvstore port [8191]: open
	Checking configuration... Done.
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
PYTHONHTTPSVERIFY is set to 0 in splunk-launch.conf disabling certificate validation for the httplib and urllib libraries shipped with the embedded Python interpreter; must be set to "1" for increased security
Done


Waiting for web server at http://127.0.0.1:8000 to be available............ Done


If you get stuck, we're here to help.
Look for answers here: http://docs.splunk.com

The Splunk web interface is at http://<HOSTNAME>:8000
```
