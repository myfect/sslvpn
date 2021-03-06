# Fortinet SSL VPN Small client

=======================

## Description

FortiClient extends the power of FortiGate's Unified threat management to endpoints on your network. Desktops, laptops, tablets and smartphones, FortiClient enables every device - local or remote, stationary or mobile - to integrate with your FortiGate. With no per-seat license fees, FortiClient takes the headaches out of managing multiple endpoints so your users and guests can work efficiently anywhere, without compromising your security. It's the end-point solution for your FortiGate network.

## Features

* Install and uninstall via Chocolatey
* [NEW] Tests local source (if exists) to prevent dowloading package from Internet
* Requires source path to MyGet


### 2016-10-01 Build 4.0.2329

* package rebuild for myget
* removed double source link
* added Virus Total check link - [https://www.virustotal.com/en/file/7cde4467503e8cd670c37a4137e836e479ee5da0b8ee023d74fe5a0f212e60aa/analysis/1475337595/](https://www.virustotal.com/en/file/7cde4467503e8cd670c37a4137e836e479ee5da0b8ee023d74fe5a0f212e60aa/analysis/1475337595/)

### 2016-06-20 Build 4.0.2329

* initial package

## Usage

### Direct

```cmd
choco install sslvpn -source https://www.myget.org/F/public-choco

```

or with added source

```cmd
choco source add -n=public-choco -s"https://www.myget.org/F/public-choco" --priority=10
choco install sslvpn

```

## YAML

```yaml

sslvpn:
  ensure: latest
  uninstall_options: "--force --all-versions"
  provider: chocolatey
  source: https://www.myget.org/F/public-choco
```