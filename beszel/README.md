# Beszel

Lightweight monitoring hub and local agent.

## Run

```bash
docker compose up -d
```

The hub is exposed through Caddy at:

```text
https://beszel.perpixai.com
```

## First local system

1. Open the hub and create the admin user.
2. Create a universal token in `/settings/tokens`, or use the token/key from the Add System dialog.
3. Add these values to `/opt/perpix/.env`:

```env
BESZEL_APP_URL=https://beszel.perpixai.com
BESZEL_AGENT_TOKEN=
BESZEL_AGENT_KEY=
```

4. Restart the stack:

```bash
docker compose up -d
```

5. In the Beszel UI, use this Host / IP for the local agent:

```text
/beszel_socket/beszel.sock
```
