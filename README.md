# poppygo docker compose traefik setup

This is a minimal traefik setup for docker-compose. All configuration is done in the .env.

## Quickstart

Clone the project.

```
git clone https://github.com/poppygo/traefik-docker-compose-setup.git traefik
touch acme.json
chmod 600 acme.json
cp .env.sample .env
```

Create credentials for new admin user with password.

```
echo $(htpasswd -nb <user> <password>) | sed -e s/\\$/\\$\\$/g
```

Edit .env, paste the user credentials and replace the other values.

```
CREDENTIALS=admin:$xxxxxxxxxxxx/
DASHBOARD_HOSTNAME=traefik.example.com
ACME_EMAIL=postmaster@example.com
```

