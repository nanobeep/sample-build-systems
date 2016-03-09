# App-Build and Service-Polling Example

## System Setup

CentOS 7.2 x64, 512MB, DigitalOcean

## App Code and Build

See: https://github.com/nanobeep/sample-build

## Usage

Examples show using `staging` inventory. The `production` inventory has 2 servers for showing serialized (1 at a time) deploys.

### Initial Setup

`ansible-playbook -i inventory/staging setup.yml`

### Deploy Default Branch

`ansible-playbook -i inventory/staging deploy.yml`

The default `branch` is set as a variable in `inventory/group_vars/all`.

### Deploy Specific Branch

`ansible-playbook -i inventory/staging deploy.yml --extra-vars "branch=spanish"`

You can create default branches per inventory by overriding the `branch` variable in `inventory/group_vars/[environment name]`. Setting the `branch` via the CLI will override whatever defaults are in the code.

