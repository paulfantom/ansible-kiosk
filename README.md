# Ansible Role: kiosk

[![Build Status](https://travis-ci.com/paulfantom/ansible-kiosk.svg?branch=master)](https://travis-ci.com/paulfantom/ansible-kiosk)
[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)
[![Ansible Role](https://img.shields.io/badge/ansible%20role-paulfantom.kiosk-blue.svg)](https://galaxy.ansible.com/paulfantom/kiosk/)
[![GitHub tag](https://img.shields.io/github/tag/paulfantom/ansible-kiosk.svg)](https://github.com/paulfantom/ansible-kiosk/tags)

## Description

Create secure kiosk from raspberry using Xorg, openbox, and chromium browser.
Role based on blog post available at https://die-antwort.eu/techblog/2017-12-setup-raspberry-pi-for-kiosk-mode/

## Requirements

- Ansible >= 2.7 (It might work on previous versions, but we cannot guarantee it)

## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `kiosk_url` | "https://duckduckgo.com" | default URL to open in kiosk browser |
| `kiosk_delay` | 1 | delay (in seconds) before starting a browser |
| `kiosk_startx_params` | ["-nocursor"] | parameters to run `startx` with |
| `kiosk_browser_params` | ["--disable-infobars", "--kiosk"] | parameters to start browser with |
| `kiosk_user` | ["pi"] | autologin with this user |

## Example

### Playbook

Use it in a playbook as follows:
```yaml
- hosts: all
  roles:
    - paulfantom.kiosk
```

## Contributing

See [contributor guideline](CONTRIBUTING.md).

## License

This project is licensed under MIT License. See [LICENSE](/LICENSE) for more details.
