
# Reload
**Command:** `vagrant reload`

The equivalent of running a [halt][halt] followed by an [up][up].

This command is usually required for changes made in the Vagrantfile to take effect. After making any modifications to the Vagrantfile, a `reload` should be called.

The configured provisioners will not run again, by default. You can force the provisioners to re-run by specifying the `--provision` flag.

## Options
* `--provision` - Force the provisioners to run.

* `--provision-with x,y,z` - This will only run the given provisioners. For example, if you have a `:shell` and `:chef_solo` provisioner and run `vagrant provision --provision-with shell`, only the shell provisioner will be run.

[halt]: https://docs.vagrantup.com/v2/cli/halt.html
[up]: https://docs.vagrantup.com/v2/cli/up.html