Dotfiles
=========

Clones a bare repository and checks it out into the home folder.

It stashes any conflicts or changes to maintain idempotency.
However, it may overwrite unpushed commits (the changes would still be stashed).

Requirements
------------

Git installed on the target

Role Variables
--------------

```dotfiles_repo``` The repo to clone. Defaults to my dotfiles.

```dotfiles_repo_version``` git ref to checkout. Defaults to master.

```dotfiles_repo_accept_hostkey``` Defaults to true.

```dotfiles_home``` Defaults to ~.

```dotfiles_repo_local_destination``` Defaults to $HOME/.dotfiles

Dependencies
------------

None

Example Playbook
----------------

    - hosts: localhost
      roles:
         - { role: lsevcik.dotfiles }

License
-------

MIT

Author Information
------------------

Created in 2021 by Logan Sevcik.
Inspired by Jeff Geerling's role of the same name.
