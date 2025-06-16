# splunk_adv

```bash
# Install Splunk
# This will install Splunk under /opt/splunk
sudo dpkg -i splunk-9.4.3_______linux-amd64.deb

sudo chown -R your-username:your-username /opt/splunk
sudo chmod -R 755 /opt/splunk

# Start Splunk for the first time
# After installation, start Splunk manually and accept the license agreement:
/opt/splunk/bin/splunk start
# /opt/splunk/bin/splunk start

# Enable Splunk to start at boot (optional but recommended):
# This creates a systemd service so Splunk starts automatically after reboot.
/opt/splunk/bin/splunk enable boot-start

# Access Splunk Web Interface
https://localhost:8000
```

```bash
######## Optional: Run Splunk as a dedicated user (for production) ########
# For production use, it's best practice to create a dedicated splunk user:
sudo useradd -r splunk
sudo chown -R splunk:splunk /opt/splunk
sudo su - splunk
/opt/splunk/bin/splunk start
```
