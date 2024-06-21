.PHONY: deploy-rke check-syntax

# Variables
INVENTORY = inventory
PLAYBOOK = rke.yml
LIMIT = rke-cluster-01
VAULT_PASS_FILE = ~/.vlt/.vlt_pass

deploy-rke:
	ansible-playbook -i $(INVENTORY) $(PLAYBOOK) --limit $(LIMIT) --vault-password-file $(VAULT_PASS_FILE)

check-syntax:
	ansible-playbook -i $(INVENTORY) $(PLAYBOOK) --syntax-check --vault-password-file $(VAULT_PASS_FILE)
