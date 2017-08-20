About
-----

Ansible role for installing nano with syntax highlighting and custom options.

Requirements
------------

nano should be available in your package management system.

Role Variables
--------------

Variables with examples:

```yml
# git url for repository containing syntax highlighting files
nano_syntax_repo: 'https://github.com/scopatz/nanorc.git'

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
