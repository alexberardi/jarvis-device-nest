# jarvis-device-nest

Google Nest thermostat and camera control via the Smart Device Management API for [Jarvis](https://github.com/alexberardi/jarvis-node-setup).

## Install

```bash
python scripts/command_store.py install --url https://github.com/alexberardi/jarvis-device-nest
```

## Setup

1. Create a Google Cloud project and enable the Smart Device Management API
2. Register for [Device Access](https://console.nest.google.com/device-access) ($5 one-time fee)
3. Create a Device Access project to get your project ID
4. Complete OAuth setup through Jarvis to link your Google account

## Supported Devices

- Nest Thermostat (all generations)
- Nest Cam (indoor/outdoor)
- Nest Doorbell

## Secrets

| Key | Required | Description |
|-----|----------|-------------|
| `NEST_PROJECT_ID` | Yes | SDM Device Access project ID |
| `NEST_ACCESS_TOKEN` | Auto | OAuth access token (auto-populated after auth) |
| `NEST_REFRESH_TOKEN` | Auto | OAuth refresh token (auto-populated after auth) |
| `NEST_CLIENT_ID` | No | Override default Google OAuth client ID |
| `NEST_TEMP_UNIT` | No | Temperature unit: `F` (default) or `C` |

## Structure

```
device_families/nest/protocol.py   # Device protocol adapter
```
