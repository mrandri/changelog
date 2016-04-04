The [securityrouter.org](http://securityrouter.org) project is a network operating system and software distribution based on OpenBSD which is developed and maintained by <a href="http://halon.io">Halon Security</a>. New systems are deployed by [downloading](http://dl2.halon.se/vsr/) a software image. The easiest way to update existing systems is to perform an [automatic update](http://securityrouter.org/wiki/Update) from within the product's administration.

New major versions (for example 3.5 which is based on OpenBSD 5.7) often contains numerous configuration syntax changes, which might render a previously working configuration invalid, and thus affect the operation of the system after an update. We therefore urge all users to perform such updates with caution; **take a snapshot** if running it as a virtual machine, or at least **backup the plain-text configuration** and **monitor the update** on the screen/[console](http://securityrouter.org/wiki/Serial_console), so that you can perform recovery or roll back to an older software version (using our help), if necessary.

There is an [RSS feed](https://github.com/halonsecurity/securityrouter.org/releases.atom) available.

## 3.0-p29
Released on 2013-03-11
- **`New`** New model VSR-Lite available for purchase
- **`New`** Support for PC Engine's ALIX system boards
- **`Imp`** VPN servers support search domain and routes for Apple OSX and iOS clients
- **`Imp`** Other minor improvements
- **`Bug`** dhsyncd would fail to start if any carp interface was down

## 3.0-p28
Released on 2013-02-25
- **`New`** New CLI command `replace-swap` in `configure`
- **`Imp`** Support for Dell R320
- **`Imp`** Edit buttons in tables
- **`Imp`** Support `rdomain` and `proxy-arp` in cluster activation
- **`Imp`** Other minor improvements

## 3.0-p27
Released on 2013-02-20
- **`Imp`** Support for more Broadcom NICs
- **`Imp`** Other minor improvements
- **`Bug`** Could not enable free mode (VSR-Free) without serial

## 3.0-p26
Released on 2013-02-05
- **`Imp`** VLAN on trunk interfaces
- **`Imp`** Suppress repeated cluster errors
- **`Imp`** Other minor improvements
- **`Bug`** When configuring partial date and time

## 3.0-p25
Released on 2012-12-14
- **`New`** Microsoft Hyper-V support
- **`New`** Ability to use additional disk as storage for logs, etc
- **`New`** Ability to update with verification using storage disk
- **`Imp`** Improved performance during commit/test
- **`Imp`** Question on drain/flush load balancer node pausing
- **`Imp`** Changed Subversion format to FSFS
- **`Imp`** Improved loading time on firewall page with many rules
- **`Imp`** Overall improvements
- **`Bug`** IP ranges in macros on firewall page
- **`Bug`** Load balancer wizard didn't work with missing statement
- **`Note`** Reserved routing domain 239-255

## 3.0-p24
Released on 2012-11-21
- **`New`** The `proxy-arp` makes it possible to use [LAN network in VPN server](http://sr.wiki.halon.se/wiki/VPN_server#Proxy_ARP)
- **`Imp`** Cluster (`hdpd`) keeps information about dead hosts
- **`Imp`** Improved macro/table presentation on Network > Firewall
- **`Imp`** Many load balancer improvements
 - Proper source-tracking per redirect
 - Summarise statistics for multiple "listen on"
 - Ability to enable/disable hosts in all relays/redirects
 - Creates automatic rules for relays (tagged relayd)
 - Wizard for adding relays and redirects
 - User interface for global settings
 - [MIB](http://sr.wiki.halon.se/wiki/Load_balancing#SNMP_traps) for traps
- **`Imp`** User interface for SNMP settings on System > SNMP
- **`Bug`** Fixed problem when renaming duplicate macros/tables
- **`Bug`** Exports on Configuration > Revision management named properly
- **`Bug`** Fixed issue with `statd` removing graphs when redirects is down

## 3.0-p23
Released on 2012-10-25
- **`Imp`** Allow more than 4 VPN server groups by creating /dev/tunX dynamically
- **`Imp`** Visual noise when displaying all rulesets on firewall page removed
- **`Imp`** Permit hyphens in the host part in FQDNs (search-domain and host-name)
- **`Imp`** Other minor improvements

## 3.0-p22
Released on 2012-10-22
- **`New`** Real-time graphs
- **`New`** Graphs for firewall states
- **`New`** Login banner in web administration
- **`New`** Highlight text in CLI output with | mark
- **`Imp`** Forwarding (firewall/routing) performance improved
- **`Imp`** Ability to configure DNS, routes, etc per VPN group
- **`Imp`** Always allow DHCP on VPN interfaces for dhinfod to work
- **`Imp`** Shortcuts to rule and state statistics on Firewall page
- **`Imp`** Better logging when using SOAP's commandRun
- **`Imp`** Go directly to deploy/diff when saving on clear-text page
- **`Imp`** Ability to restore the terminal using CLI's "reset"
- **`Imp`** Display line numbers of configuration error page
- **`Imp`** Firewall page now visually renders more protocols
- **`Imp`** Less obstructive reloading of VPN server
- **`Imp`** Other minor improvements
- **`Bug`** Bug in PHP/CURL's DNS reloading remedied
- **`Bug`** Memory leak in UUID generation
- **`Bug`** Invalid netmask displayed as 0.0.0.0 on basic setup page

## 3.0-p21
Released on 2012-09-25
- **`Imp`** Web admin settings for VPN-server client routes
- **`Imp`** Usability improvements
- **`Bug`** Real-time firewall log issue resolved

## 3.0-p20
Released on 2012-09-24
 - New: VPN-server (L2TP/PPTP) supports client routes
 - Bug: Issue with IPsec 3DES key generation button resolved

## 3.0-p19
Released on 2012-09-10
- **`New`** VPN-server (L2TP) NAT-T support
- **`New`** VPN-server (L2TP/PPTP) DNS suffix support
- **`New`** Replaced [`configure`](http://wiki.halon.se/SR/Configure) "diff" with new "compare" command
- **`Imp`** Various graphical usability improvements
- **`Bug`** Saving a firewall macro with multiple items resulted in duplicate brackets
- **`Bug`** L2TP passphrase not saved when editing existing server

## 3.0-p18
Released on 2012-09-02
- **`New`** VSR-Free, a free license
- **`New`** License subscription, option to automatically downloads license keys
- **`Imp`** [CLI](http://wiki.halon.se/SR/CLI) can install and remove license keys
- **`Imp`** Log failed password attempts via HTTPS
- **`Imp`** Added support for option 82 in the dhcp-relay
- **`Bug`** Multiple negations on firewall page didn't render properly

## 3.0-p17
Released on 2012-08-22
- **`New`** [DHCPv6](http://wiki.halon.se/SR/IPv6#DHCPv6) server, client and prefix delegation
- **`New`** IPv6 router solicitation client
- **`New`** [User classes](http://wiki.halon.se/SR/Users), including read-only users (login.conf)
- **`New`** Web graph layout is customisable and auto saved
- **`Imp`** Ability to renew DHCP leases
- **`Imp`** Web improvements for Apple iOS and Microsoft IE 9
- **`Imp`** Web terminal has better scroll-back
- **`Imp`** Web shows disk usage on System > Hardware
- **`Imp`** Changed system paths according to BSD defaults
- **`Imp`** [CLI](http://wiki.halon.se/SR/CLI) parsing improved with quoted strings
- **`Imp`** Web settings stored in HTML5 local storage
- **`Imp`** Updated jQuery
- **`Bug`** Resolved cluster memory leak in backend
- **`Bug`** Resolved issue with /tmp getting full
- **`Bug`** Resolved web cluster page script error
- **`Bug`** Suppressed warning when confirming deployment
- **`Bug`** Spelling corrections

## 3.0-p16
Released on 2012-07-10
- **`New`** Diagnostics > Terminal with full ANSI support
- **`New`** Working copy allows for atomic apply of multiple changes
- **`Imp`** Ability to tag configuration revisions with a message
- **`Imp`** Ability to cancel a pending configuration test
- **`Imp`** Network > Interface got statistics
- **`Imp`** Network > Interface got PPPoE support
- **`Imp`** Network > Firewall supports negation of addresses
- **`Imp`** Network > Basic setup got PPPoE support
- **`Imp`** Network > DHCP server lists connected clients (leases)
- **`Imp`** PPPoE interface automatically adds routes and rules
- **`Imp`** Welcome texts on first boot
- **`Imp`** New layout on login screen
- **`Imp`** Highlights save or warns about unsaved changes
- **`Imp`** Validating function configCheck() in SOAP API
- **`Imp`** Default arguments in SOAP API
- **`Imp`** Command for showing licenses in CLI
- **`Bug`** Now validates reserved DHCP host's name more strictly
- **`Bug`** No longer kicked out of console when setting root password
- **`Bug`** Resolved issue with dhsyncd causing sawtooth CPU usage

## 3.0-p15
Released on 2012-06-11
- **`Imp`** Support for ne (NE1000) interfaces (used by Parallels Desktop)
- **`Imp`** Changed the fail-path when activating clustering
- **`Bug`** Error on first page for un-configured interfaces resolved
- **`Bug`** Issue when duplicating rules on the firewall page resolved

## 3.0-p14
Released on 2012-06-08
- **`New`** Introduced cluster support using SSL certificates
- **`New`** Introduced PPPoE support
- **`New`** Introduced RADIUS support for PPTP and L2TP server with groups
- **`New`** Last ethernet interface automatically becomes cluster sync on installation
- **`New`** Possibility to update a cluster node through other node via sync interface
- **`New`** New replace command in CLI configure
- **`New`** Load balancer shows statistics for layer 3 (redirects)
- **`New`** Keyboard layout support for video consoles
- **`Imp`** Internal IPC moved from TCP to Unix sockets for increased local security
- **`Imp`** Firewall page supports "received-on" routing domains
- **`Imp`** Friendly warning on password change in web administration
- **`Imp`** DHCP server supports clustering
- **`Imp`** DHCP server supports DHCP option 43
- **`Imp`** Make DHCP server leases persistent across reboots
- **`Imp`** Possibility to only change one of the DHCP range values
- **`Imp`** Router advertisements supports clustering
- **`Imp`** Basic setup displays unplugged cable correctly
- **`Imp`** Support Intel 10/100 network cards (fxp)
- **`Imp`** HTTPS server supports certificates and keys in configuration
- **`Imp`** Renamed "cd" to "edit" in CLI configure
- **`Imp`** License page more detailed explains license keys
- **`Imp`** Overview page consumes less CPU
- **`Imp`** Load balancer inherits default SSL certificate unless overridden
- **`Imp`** Load balancer page layout improved
- **`Imp`** Web browser cache is automatically flushed after software updates
- **`Imp`** Users "admin" and "root" can force reboots from CLI
- **`Imp`** Users "admin" and "root" can perform a factory reset from CLI
- **`Imp`** Allowed all users to view packets in tcpdump from CLI
- **`Imp`** License, copyright and credit page added under Help page
- **`Imp`** Prevents users from removing themselves by mistake
- **`Imp`** IPsec tunnel ping test works on /0 networks
- **`Imp`** Hide shutdown button on hardware page by default
- **`Bug`** Bug in tcpbench resolved (patch sent upstream)
- **`Bug`** Display error on DHCP page resolved
- **`Bug`** The PPTP proxy has issues with clients sending GRE too early
- **`Bug`** Monotonic time were not always used for wake ups
- **`Bug`** Change of order of some keys in configuration didn't triggering a commit
- **`Bug`** Parsing error on load balancer page resolved
- **`Bug`** Syslog didn't log with host name
- **`Bug`** DHCP settings link on interface page didn't work for all interface types

## 3.0-p13
Released on 2012-03-22
- **`Bug`** DHCP relay regression issue resolved

## 3.0-p12
Released on 2012-03-20
- **`New`** Hardware detection for Halon HSR-1000

## 3.0-p11
Released on 2012-03-16
- **`New`** [Load balancer](http://wiki.halon.se/SR/Load_balancing) user interface
- **`New`** [FTP proxy](http://wiki.halon.se/SR/Proxies) for NAT called `interface X { ftp-proxy`
- **`New`** [PPTP proxy](http://wiki.halon.se/SR/Proxies) for NAT called `interface X { pptp-proxy`
- **`Imp`** Firewall user interface supports `divert`
- **`Bug`** Load balancer stability issue patched
- **`Bug`** Suppressed unnecessary `interface-group` events
