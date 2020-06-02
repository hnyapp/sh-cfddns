# sh-cfddns
Shell script to emulate DDNS client for Cloudflare-managed domain.
I wanted to use it on busybox.

# Difference from the original family
- Made it work with the sh command.
- The record name to be updated can be specified with the first argument. (I wanted to use it with cron.)
- Supports changes to cloudflare api. (As of 2020/06/02)

# Configuration
You need grep and curl installed.

Change the following variables in the script.

auth_email="john.appleseed@example.org"            # The email used to login 'https://dash.cloudflare.com'
auth_key="f1nd7h47fuck1n6k3y1ncl0udfl4r3c0n50l3"   # Top right corner, "My profile" > "Global API Key"
zone_identifier="f1nd7h3fuck1n6z0n31d3n71f13r4l50" # Can be found in the "Overview" tab of your domain

# Execution example
sh cfupdater-v4 ipv4.example.org

sh cfupdater-v6 ipv6.example.org

sh cfupdater-dualstack dualstack.example.org
