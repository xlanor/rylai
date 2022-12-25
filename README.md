### Services vm

Since our services will provide services to our kubernetes cluster.

- Sempahore (to execute ansible playbooks)
- Harbor (to serve as a pull-through registry)

Replace semaphore-postgres.env and semaphore-config.json with your own

ansible-playbook bootstrap.yml -K --ask-vault-pass

