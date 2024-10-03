## Openconnect VPN
1. Initial installation: `ansible-playbook -i hosts/openconnect-server openconnect.yaml --tags="install"`

2. Add users to default/main.yaml and run `ansible-playbook -i hosts/openconnect-server openconnect.yaml --tags="add_clients"`

3. Remove users: update `clients_to_remove` in default/main.yaml and run `ansible-playbook -i hosts/openconnect-server openconnect.yaml --tags="remove_clients"`

4. Get all users certifacate: `ansible-playbook -i hosts/openconnect-server openconnect.yaml --tags="add_clients" --extra-vars "get_all_users_certs=True"`