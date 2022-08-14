# duplicacy-gui-systemd
.service file for starting duplicacy Web GUI automatically.

Edit `ExecStart=` to point to the executable you've downloaded from the duplicacy website. It can be an absolute path or a location that exists in $PATH. On my system this executes /usr/local/bin/dwe_main. Do not remove the -background flag, this keeps it from trying to open the web browser.

Suggest installing as your user, /home/${USER}/.config/systemd/user/duplicacy.service. After this you can enable and start the service, `systemctl --user enable --now duplicacy.service`. Manage with normal systemctl commands, but include --user each time.
