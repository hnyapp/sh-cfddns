# bash-cfddns
Bash script to emulate DDNS client for Cloudflare-managed domain

# Difference from the original family
-The record name to be updated can be specified with the first argument. (I wanted to use it with cron.)

# config
Change the following variables in the script.

auth_email="john.appleseed@example.org"            # The email used to login 'https://dash.cloudflare.com'
auth_key="f1nd7h47fuck1n6k3y1ncl0udfl4r3c0n50l3"   # Top right corner, "My profile" > "Global API Key"
zone_identifier="f1nd7h3fuck1n6z0n31d3n71f13r4l50" # Can be found in the "Overview" tab of your domain

# Execution example
bash cfupdater-v4 ipv4.example.org
bash cfupdater-v6 ipv6.example.org
bash cfupdater-dualstack dualstack.example.org
