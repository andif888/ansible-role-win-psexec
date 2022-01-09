ansible-role-win-psexec
=========

Downloads and installs PsExec.exe and PsExec64.exe

Role Variables
--------------

The default values for the variables are set in defaults/main.yml:

```yaml
ps_tools_extract_path: '%windir%\Temp\pstools'
ps_tools_install_path: '%windir%\system32'
ps_tools_download_url: 'https://download.sysinternals.com/files/PSTools.zip'
ps_tools_filename_zip: 'PSTools.zip'
pstools_delete_extract_dir: true
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
---
- hosts: windows
  become: true
  gather_facts: yes
  vars:
    pstools_delete_extract_dir: false

  roles:
    - ansible-role-win-psexec
```
