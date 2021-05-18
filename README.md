# Ansible role - KYPO Sandbox Logging Msfconsole Commands

This role provides local Metasploit command logging. 

By default, the Metasploit commands history contains only correct/known commands. Logging incorrect/unknown commands require the modification of the Metasploit source code file. The patch tool with the specific patch file is used to achieve that. The current modification is compatible with Metasploit version `v6.0.44`. If you are using a different version, check if the patch file is still applicable; otherwise, consider using your own patch file, by setting up the optional parameters.

## Requirements

* Metasploit 

* This role requires root access, so you either need to specify `become` directive as a global or while invoking the role.

    ```yml
    become: yes
    ```
    
* Also requires Ansible variables, therefore do not disable directive `gather_facts`.

## Role parameters

Optional parameters
* `slm_patch_file` - Path of the patch file as accepted by the GNU patch tool. (default: `shell.rb.patch`).
* `slm_file_to_be_patched` - Path of the file on the remote machine to be patched. (default: `/opt/metasploit-framework/embedded/framework/lib/rex/ui/text/shell.rb`).


## Example

The simplest example of logging msf commands configuration.

```
  roles:
    - role: sandbox-logging-msf
      become: yes
```
