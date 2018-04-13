    $ borg init --encryption=repokey 12337@ch-s012.rsync.net:backup/x1/
    $ cp ik-borg-backup.{service,timer} /usr/lib/systemd/user/
    $ cp ik-borg-backup /usr/local/bin/

Create configuration and password

    $ echo "my_password" > "$HOME/.secrets/borg-passwd"
    $ chmod 400 "$HOME/.secrets/borg-passwd"
    $ echo "my@repo.net:backup/path" > "$HOME/.config/ik-borg-backup/repository"