
# My tmux Configuration

## Introduction

Welcome to my tmux configuration repository! This repository contains a tmux setup tailored for efficient terminal session management. Tmux is a powerful terminal multiplexer that allows for the management of multiple terminal sessions in a single window.
This config is meant to work well with nvim inside of WezTerm.

## Features

- **Session Management:** Facilitates easy management of multiple terminal sessions.
- **Window and Pane Layouts:** Offers custom layouts for various workflows.

## Getting Started

### Prerequisites

- tmux (version 3.2a or higher)

### Installation (Linux)

1. Copy the tmux configuration file to your home directory:
- ~/.tmux.conf

2. Install the Tmux Plugin Manager (https://github.com/tmux-plugins/tpm)
3. Run the install process using <prefix key>I

### Automatic Setup of Dev Environment
Customize ./tmux-setup.sh to your liking. This default script is set up to run the following:
* Python IDE Window
* SQL IDE Window
    - SQL credentials are read from .env file and added to the session through :DBUIAddConnection followed by :DBUIFindBuffer
        - Added connections are stored by default at ~/.local/share/db_ui/connections.json
* GIT Window

To attach to a running session with this configuration or start up a new session, run:
```
./tmux-setup.sh
```

To restart the session, run:
```
tmux kill-session -t dev-env && ./tmux-setup.sh
```

Please note that "dev-env" is the default session name.


## Customization

This configuration can be customized to fit your needs. Modify the `.tmux.conf` file to suit your preferences. For detailed instructions on tmux commands and configuration, visit the [tmux GitHub page](https://github.com/tmux/tmux) or the [tmux man page](https://man7.org/linux/man-pages/man1/tmux.1.html).

## Contributing

Contributions to this tmux configuration are welcome. For suggestions or improvements, please open an issue or a pull request.

## License

This tmux configuration is released under the [MIT License](LICENSE).
