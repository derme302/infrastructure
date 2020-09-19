# ansible-playbooks
Playbooks for automating server procedures


## Getting Started Ansible
### SSH

You must use the SSH protocol with Ansible to securely log into managed nodes. Don't fear! It's not as hard as it sounds :) You can then use your keys to apply your Playbook configurations. Create an SSH key-pair on the control node to use for authentication. This guide assumes your public and private SSH key-pair is stored in `~/.ssh/id_rsa.pub` and `~/.ssh/id_rsa`.

```ssh-keygen -t rsa -b 4096```

Copy the key to the node you want to use with Ansible. Replace 192.168.0.100 with your nodes ip address.

```ssh-copy-id root@192.168.0.100```

Repeat this procedure for each other node you want to target.

### Running your Playbook

Finally actually running the playbook is as simple as naviagting to the directory and pointing ansible at your node.

```ansible-playbook -i hostname/ip, playbook.yml```

Note: The `,` is important here.
