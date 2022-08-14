# duplicacy-gui-systemd
.service file for starting duplicacy-GUI

Allows systemd to start the duplicacy Web UI automatically.

Edit ExecStart= to point to the executable you've downloaded from the duplicacy website. It can be an absolute path or a location that exists in PATH. On my system this executes /usr/local/bin/dwe_main.

Suggest installing as your user, /home/${USER}/.config/systemd/user/duplicacy.service. After this you can enable and start the service, systemctl --user enable --now duplicacy.service.
