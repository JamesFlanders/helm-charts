# Introduction

This is repository is a collection of Helm Charts built for my own homelab. Which means that the Helm Charts provided
here a tailored to the specific setup of my homelab. This means that certain requirements have been fullfilled to make
these charts work. So when attempting to use these charts without those requirements might result in undesirable results
or might not even work. These requirements are listed below, but use at your own risk.

## Requirements

- An NFS-share as storage class should be provided with the name 'nfs'

# Common Values

All these charts make use of a YAML file called `values.yaml`. This file can be used to configure the charts to be able
to reuse them in different ways. Some of the variables defined in here are unique to the application that is being
deployed.
But a lot of them are common between all charts. These common values and their purpose are listed below:

| Name            | Description/Purpose                                       | Default Value                                                                               |
|-----------------|-----------------------------------------------------------|---------------------------------------------------------------------------------------------|
| app             | Name of the application (e.g. AdGuard, Minecraft, etc...) | <Depends on application>                                                                    |
| instance        | Name of the instance of the application                   | <Depends on instance (Generally named after a Jupiter moon in the context of my homelab)>   |
| host            | Name of the DNS record to link to the container           | <Domain name used by myself (In the homelab this is generally '<domain>.caenen.net')>       |
| include_volumes | Include the creation of the PersistentVolumeClaim         | `false` (When you want to create the PVCs for the first time, then set this value to 'true' |

# Usage

## Usage within Portainer
_To be documented_