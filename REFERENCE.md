# Reference
<!-- DO NOT EDIT: This document was generated by Puppet Strings -->

## Table of Contents

**Resource types**

* [`windows_firewall_global`](#windows_firewall_global): Manage windows global firewall settings
* [`windows_firewall_group`](#windows_firewall_group): Enable/Disable windows firewall group
* [`windows_firewall_profile`](#windows_firewall_profile): Enable/Disable windows firewall profile
* [`windows_firewall_rule`](#windows_firewall_rule): Manage Windows Firewall with Puppet

## Resource types

### windows_firewall_global

Manage windows global firewall settings

#### Properties

The following properties are available in the `windows_firewall_global` type.

##### `strongcrlcheck`

Configures how CRL checking is enforced

##### `saidletimemin`

Configures the security association idle time in minutes.

##### `defaultexemptions`

Valid values: none, neighbordiscovery, icmp, dhcp, notconfigured

Configures the default IPsec exemptions. Default is to exempt IPv6 neighbordiscovery protocol and DHCP from IPsec.

##### `ipsecthroughnat`

Valid values: never, serverbehindnat, serverandclientbehindnat, notconfigured

Configures when security associations can be established with a computer behind a network address translator

##### `authzusergrp`

Configures the users that are authorized to establish tunnel mode connections.

##### `authzcomputergrp`

Configures the computers that are authorized to establish tunnel mode connections

##### `authzusergrptransport`

Authz user group transport

##### `authzcomputergrptransport`

Authz computer transport

##### `statefulftp`

Valid values: enable, disable, notconfigured

Stateful FTP

##### `statefulpptp`

Valid values: enable, disable, notconfigured

Stateful PPTP

##### `keylifetime`

Sets main mode key lifetime in minutes and sessions

##### `secmethods`

configures the main mode list of proposals

##### `forcedh`

Valid values: yes, no

configures the option to use DH to secure key exchange

##### `boottimerulecategory`

Boot time rule category

##### `firewallrulecategory`

Firewall rule category

##### `stealthrulecategory`

Stealth rule category

##### `consecrulecategory`

con sec rule category

#### Parameters

The following parameters are available in the `windows_firewall_global` type.

##### `name`

namevar

Not used (reference only)

### windows_firewall_group

Enable/Disable windows firewall group

#### Properties

The following properties are available in the `windows_firewall_group` type.

##### `enabled`

Valid values: yes, no

Whether the rule group is enabled (Yes or No)

#### Parameters

The following parameters are available in the `windows_firewall_group` type.

##### `name`

namevar

Name of the rule group to enable/disable

### windows_firewall_profile

Enable/Disable windows firewall profile

#### Properties

The following properties are available in the `windows_firewall_profile` type.

##### `state`

Valid values: on, off

State of this firewall profile

##### `firewallpolicy`

Configures default inbound and outbound behavior

##### `localfirewallrules`

Valid values: enable, disable, notconfigured

Merge local firewall rules with Group Policy rules. Valid when configuring a Group Policy store

##### `localconsecrules`

Valid values: enable, disable, notconfigured

Merge local connection security rules with Group Policy rules. Valid when configuring a Group Policy store

##### `inboundusernotification`

Valid values: enable, disable, notconfigured

Notify user when a program listens for inbound connections.

##### `remotemanagement`

Valid values: enable, disable, notconfigured

Allow remote management of Windows Firewall

##### `unicastresponsetomulticast`

Valid values: enable, disable, notconfigured

Control stateful unicast response to multicast.

##### `logallowedconnections`

Valid values: enable, disable, notconfigured

log allowed connections

##### `logdroppedconnections`

Valid values: enable, disable, notconfigured

log dropped connections

##### `maxfilesize`

maximum size of log file in KB

##### `filename`

Name and location of the firewall log

#### Parameters

The following parameters are available in the `windows_firewall_profile` type.

##### `name`

namevar

Name of the profile to work on

### windows_firewall_rule

Manage Windows Firewall with Puppet

#### Properties

The following properties are available in the `windows_firewall_rule` type.

##### `ensure`

Valid values: present, absent

The basic property that the resource should be in.

Default value: present

##### `enabled`

Valid values: yes, no

Whether the rule is enabled (Yes or No)

##### `description`

Description of this rule

##### `direction`

Valid values: in, out

Direction the rule applies to (In/Out)

##### `profiles`

Valid values: domain, private, public, any

Which profile(s) this rule belongs to, use an array to pass more then one

##### `grouping`

group that the rule belongs to (read-only)

##### `localip`

the local IP the rule targets

##### `remoteip`

the remote IP the rule targets

##### `protocol`

the protocol the rule targets

##### `protocol_type`

protocol type to use (with ICMPv4/ICMPv6)

##### `protocol_code`

protocol code to use (with ICMPv4/ICMPv6)

##### `localport`

the local port the rule targets

##### `remoteport`

the remote port the rule targets

##### `edge_traversal`

Valid values: yes, deferapp, deferuser, no

Apply rule to encapsulated traffic (?) - see: https://serverfault.com/questions/89824/windows-advanced-firewall-what-does-edge-traversal-mean#89846

##### `action`

Valid values: block, allow

What to do when this rule matches (Accept/Reject)

##### `program`

Path to program this rule applies to

##### `interfacetypes`

Valid values: wireless, lan, ras, any

Interface types this rule applies to

##### `security`

Valid values: authenticate, authenc, authdynenc, authnoencap, notrequired

Security that applies to this rule

##### `rule_source`

Where this rule originated

#### Parameters

The following parameters are available in the `windows_firewall_rule` type.

##### `name`

namevar

Name of this rule
