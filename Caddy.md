# Caddy jako reverse proxy na hoście

```Caddyfile

# Ansible managed

gitea.alx.net.pl {
    reverse_proxy localhost:3000
}
```

