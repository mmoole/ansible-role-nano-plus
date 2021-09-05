About
-----

Ansible role for installing nano with syntax highlighting and custom options.

Requirements
------------

nano should be available in your package management system. Some version of git must be available in path in order to clone the repository containing the files for syntax-highlighting.
You can use a version specific tag of the source repository to adapt if an older version of nano is installed on the host.

Role Variables
--------------

Variables with examples:

```yml
# git url for repository containing syntax highlighting files
nano_syntax_repo: 'https://github.com/scopatz/nanorc.git'

# version of repository: can be a tree, tag or specific commit
nano_syntax_repo_ver: 'HEAD'
# nano_syntax_repo_ver: 'v2.9'

# set options for nanorc file, a default set is the following
nano_rcoptions:
  - set autoindent
  - set mouse
  #- set linenumbers
  - set quickblank
  - set smarthome
  - set smooth
  - set tabsize 2
  - set tabstospaces

# or leave them blank:
#nano_rcoptions: []

# set your complete path for nanorc on remote machine file if needed:
#nano_rcfile_custom: '~/.nanorc'

# set whether system-wide nanorc file or user profile located file should be used
nano_rc_systemwide: false
```

Example Usage
-------------

```yml
roles:
  - ansible-role-nano-plus
```

You may need to re-login on your shell if a newer version of nano was installed at a different location than the default one included with your system.

Acknowledgements
----------------

Thanks to
* https://github.com/scopatz/nanorc
* https://github.com/serialhex/nano-highlight.git
* https://monkeyswithbuttons.wordpress.com/2014/04/03/multi-os-support-in-ansible/

See also
--------

http://nano-editor.org/

License
-------

MIT
