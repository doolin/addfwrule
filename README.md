#Add a New Rule to all Firewall Policies

Version: *1.0*
<br />
Author: *Tim Spencer* - *tspencer@cloudpassage.com*


This Ruby script creates a firewall rule and adds it to all defined firewall policies.

##Requirements and Dependencies

To run, this script requires:

* Ruby installed on the host that runs the script
* Ruby gems: oauth2, rest-client, json (see Gemfile, below)
* Full-access Halo API key (for write access to the API)

*Note:*  Currently, this script works only on Linux firewalls.


##List of Files

* **addruletoallpolicies.rb**:  -  The script file
* **Gemfile**:  -  Ruby file you can use for bundler installation of the required gems; included for your convenience
* **Gemfile.lock**  -  .lock file from a bundler install; included for your reference
* **README.md**  -  This ReadMe file
* **LICENSE.txt**  -  License from CloudPassage


##Usage

There comes a time when you need to add a rule to all your firewall policies. If you have many 
firewall policies, this is very tedious to do! I wrote this script to do this automatically using the 
CloudPassage API.  It's a bit simple, but it suited my needs.  You can probably adapt it to whatever 
your particular needs are pretty easily by editing the json.

1. Create environment variables HALO_ID and HALO_SECRET_KEY to hold your full-access Halo API key (copied from the Halo Portal).
1. In the script, give the "zonename" variable the name of the IP zone (must already be defined in the Portal) that you want the rule to use.
1. In the "rule=" definition in the script, configure the firewall rule as you wish.
1. Execute the script.


