# EX-L2-Config-Builder
An Ansible playbook to automatically generate and/or deploy Juniper EX distribution and access switch configurations. This playbook uses the ELS (Enhanced Layer 2 Software) 
syntax to configure uplink interfaces, management interface, vlans, IRB interfaces, MSTP, Ethernet OAM LFM, and LLDP.

# Diagram
![](ex-l2-config-builder.png)

# Running Playbook
1. Update master-vars.yml file with specifics for your network. See in file instructions.
2. Update files under group_vars/all with specifics for your network. See in file instructions.
3. a. Build configs: ansible-playbook build.yml
3. b. Build configs & deploy: ansible-playbook -i inventory build_deploy.yml
4. Generated configs are in the ./Configs directory

# TODO
- Provide a way to add access switch specific user interface VLAN configurations
