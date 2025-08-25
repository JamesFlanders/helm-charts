<p align="center">
<img src="https://i.imgur.com/9xbQw9j.png" alt="Logo" width="250" height="250"/>
</p>
<h1 align="center">Helm Charts</h1>
<p align="center">
<a href="https://github.com/JamesFlanders/helm-charts/actions/workflows/release.yml"><img alt="GitHub Actions Workflow Status" src="https://img.shields.io/github/actions/workflow/status/JamesFlanders/helm-charts/release.yml"></a>
<a href="https://opensource.org/licenses/MIT"><img alt="GitHub License" src="https://img.shields.io/github/license/JamesFlanders/helm-charts"></a>
</p>

---

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
| host            | Name of the DNS record to link to the container           | <Domain name used by myself (In the homelab this is generally '<domain>.caenen.net')>       |
| include_volumes | Include the creation of the PersistentVolumeClaim         | `false` (When you want to create the PVCs for the first time, then set this value to 'true' |

# Usage

## Usage within Portainer

Chart URL: https://JamesFlanders.github.io/helm-charts

1. Find in the navigation the Administration section, and here navigate to `Settings > General`
2. Scroll down to the `Kubernetes` section
3. Fill in the URL of this chart into the `URL` field in the Helm Repository section
4. Click on `Save kubernetes settings`


# License

[MIT License](https://opensource.org/licenses/MIT)\
Copyright (c) 2024 [James Flanders](https://github.com/JamesFlanders)

