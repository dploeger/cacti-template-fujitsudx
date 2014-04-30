# Cacti Template for Fujitsu DX

## Introduction

This is a collection of snmp-query-scripts and a host template to graph values 
coming from a Fujitsu DX-storage.

## Installation

- Copy the contents of the snmp\_queries-Subdirectory into <cacti-home>
  /resource/snmp_queries
- Import the included host template using the Cacti web gui

## Usage

Before using the template, be sure to configure the DX SNMP-settings under 
System/Network - Action "Setup SNMP Interface", "Setup SNMP Community", etc. 
Also check, that you have started Perfmon under System/Utility 
Action "Start/Stop Perfmon" or you will not see any values.

- Create a new cacti device and input host name, snmp community, etc.
- Select "Fujitsu DX" for "Host Template"
- Click "Create Graphs for this host"
- Select the specific ids of the items you want to graph

## IDs

This can be a bit cumbersome, as the DX will report all possible item ids, not 
just the ones you actually use.

The ids for volume statistics and disk statistics can be read in the 
DX web ui, but the CA port indexes may be a bit problematic. You'll have to
experiment a bit for this.
