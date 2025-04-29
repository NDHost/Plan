# Route: https://api.host.nelmin.dev/v1/controls/{server_id}

Authorization Header: NDH {USER_API_KEY}

## Power

### /power/status

Request Type: GET
Description: Returns the current status (Online, Offline, Restarting)

### /power/start

Request Type: POST
Description: Starts the server

### /power/restart

Request Type: POST
Description: Restarts the server

### /power/stop

Request Type: POST
Description: Stops the server

### /power/kill

Request Type: POST
Description: Stops the server immediately

## Sever Version & Software

### /version

Request Type: GET
Description: Returns the current server version and software (e.g.: Fabric 1.12.2)

### /version/change

Request Type: POST
Description: Changes server version and software (e.g.: Fabric 1.12.2)
Body:

```json5
{
  "software": "",
  // fabric, sponge, pufferfish, papermc, folia, etc.
  "version": ""
  // 1.12.2, 1.21.4, etc.
}
```

# Danger Controls

### /delete/server

Request Type: POST
Description: Deletes all plugins, worlds, etc. resets the server to the default of the provided software and version, if
provided
Body:

```json5
{
  "software": "",
  // fabric, sponge, pufferfish, papermc, folia, etc.
  "version": ""
  // 1.12.2, 1.21.4, etc.
}
```

### /delete/container

Request Type: POST
Description: Deletes the docker container of the Server