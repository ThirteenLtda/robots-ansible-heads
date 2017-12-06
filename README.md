Install the HEADS software on the navbox computer

The create-user.yml playbook creates the production and dev users, and set them
up to be usable for Autoproj. Moreover, they set up their access using the same
SSH keys as the target user from Ansible.

The rock.yml playbook does the actual bootstrap.

**NOTE** because of the private repositories, you MUST ssh-add your SSH key to
the ssh agent so that ansible can authenticate with GitHub and GitLab. This
is verified by the playbook (there's going to be a "clean" error if it
is not).
