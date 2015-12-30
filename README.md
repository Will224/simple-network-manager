# simple-site-monitor

A simple site monitor for checking whether a host is online/available and tracking any downtime.  

(Written in BASH)

# ------------------------------------------------------------------------------------- #
#                                                                                       #
# This program is free software: you can redistribute it and/or modify it under the     #
# terms of the GNU General Public License as published by the Free Software             #
# Foundation, either version 3 of the License, or (at your option) any later version.   #
#                                                                                       #
# This program is distributed in the hope that it will be useful, but WITHOUT ANY       #
# WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A       #
# PARTICULAR PURPOSE. See the GNU General Public License for more details.              #
#                                                                                       #
# You should have received a copy of the GNU General Public License along with this     #
# program. If not, see http://www.gnu.org/licenses/.                                    #
#                                                                                       #
# ------------------------------------------------------------------------------------- #


# The site-status.sh script will monitor a user-generated list of sites and
# update status to a very simple web page(status.html), as well as generate an availability
# log for tracking length of any outages.
#
# This script is meant to be implemented via a Cron task using whatever interval
# of time deemed necessary. The script uses the fping package to do a quick test evaluate
# the availability of a site and reports results to a simple webpage and availability log.
#
# Upon launch the script checks to see if the fping package is installed, verifies
# that all of the necessary files exist, and verifies the site_list text file is not empty.


