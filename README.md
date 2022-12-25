### Services vm

Kang Web Serices (LOL) ansible bootstrap.

- Caddy to serve as a reverse proxy.
- Sempahore (to execute ansible playbooks)
- Harbor (to serve as a pull-through registry)

Replace semaphore-postgres.env and semaphore-config.json with your own

```
ansible-playbook bootstrap.yml -K --ask-vault-pass
```

Due to the nature of our infrastructure setup, requests will be routed from core switch -> HAProxy -> Istio External -> Caddy

Certificates will be issued by caddy using LE.

Istio will proxy in tls mode.
