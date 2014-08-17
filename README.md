#Requirements
1. You'll need ansible installed (minimum version=1.7)
2. Public-key auth access to any sudo account on our server
3. gkeyring python package installed
4. The ansible vault password stored in your gnome-keyring vault as "clipx-vault"

#How to run ansible

    ansible-playbook -i hosts site.yml  --vault-password-file vault_pass.sh

#Updating the secret environment variables

    ansible-vault edit clipx-secrets.yml  --vault-password-file vault_pass.sh

Make sure that the vault_pass.sh file is executable, and that your version of ansible is atleast 1.7