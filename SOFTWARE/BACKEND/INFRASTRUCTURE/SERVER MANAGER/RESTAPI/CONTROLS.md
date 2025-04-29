# Route: https://api.host.nelmin.dev/v1/controls/{server_id}

Authorization Header: NDH {USER_API_KEY}

## Power

### /power/status

Request Type: GET <br/>
Description: Returns the current status (Online, Offline, Restarting) <br/>

### /power/start

Request Type: POST <br/>
Description: Starts the server <br/>

### /power/restart

Request Type: POST <br/>
Description: Restarts the server <br/>

### /power/stop

Request Type: POST <br/>
Description: Stops the server <br/>

### /power/kill

Request Type: POST <br/>
Description: Stops the server immediately <br/>

## Sever Version & Software

### /version

Request Type: GET <br/>
Description: Returns the current server version and software (e.g.: Fabric 1.12.2) <br/>

### /version/change

Request Type: POST <br/>
Description: Changes server version and software (e.g.: Fabric 1.12.2) <br/>
Body: <br/>

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

Request Type: POST <br/>
Description: Deletes all plugins, worlds, etc. resets the server to the default of the provided software and version, if
provided <br/>
Body: <br/>

```json5
{
  "software": "",
  // fabric, sponge, pufferfish, papermc, folia, etc.
  "version": ""
  // 1.12.2, 1.21.4, etc.
}
```

### /delete/container

Request Type: POST <br/>
Description: Deletes the docker container of the Server <br/>