# quarantine

A linux vagrant environment with some things dev-friendly things installed, most notably:

- Go v1.14
- Docker 19.03.8
- Kind v0.8.0-alpha
- Kubectl v1.17.0

## Host requirements

1. Vagrant
1. Virtualbox
1. Ansible

## Usage

1. Clone this.
1. Set LINUX_PLAYGROUND_CPUS (default: number of cores on your host),
   LINUX_PLAYGROUND_MEMORY (in MB. Default: 2048), and
1. `./vmup.sh`.
1. The first time you launch tmux, press prefix+I to install TPM plugins. The
   default prefix is ctrl+space.
