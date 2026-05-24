# information

the open claw config file :
{
  "gateway": {
    "mode": "local",
    "auth": {
      "mode": "token",
      "token": "xxxxx"
    },
    "port": 18789,
    "bind": "loopback",
    "tailscale": {
      "mode": "off",
      "resetOnExit": false
    },
    "controlUi": {
      "allowInsecureAuth": true
    },
    "nodes": {
      "denyCommands": [
        "camera.snap",
        "camera.clip",
        "screen.record",
        "contacts.add",
        "calendar.add",
        "reminders.add",
        "sms.send",
        "sms.search"
      ]
    }
  },
  "agents": {
    "defaults": {
      "workspace": "/home/shit/.openclaw/workspace",
      "model": {
        "primary": "custom-localhost-3001/auto"
      },
      "models": {
        "custom-localhost-3001/auto": {
          "alias": "frellm"
        }
      }
    }
  },
  "session": {
    "dmScope": "per-channel-peer"
  },
  "tools": {
    "profile": "coding",
    "web": {
      "search": {
        "provider": "duckduckgo",
        "enabled": true
      }
    }
  },
  "models": {
    "mode": "merge",
    "providers": {
      "custom-localhost-3001": {
        "baseUrl": "http://localhost:3001/v1",
        "api": "openai-completions",
        "apiKey": "freellmapi-xxx",
        "models": [
          {
            "id": "auto",
            "name": "auto (Custom Provider)",
            "contextWindow": 128000,
            "maxTokens": 4096,
            "input": [
              "text",
              "image"
            ],
            "cost": {
              "input": 0,
              "output": 0,
              "cacheRead": 0,
              "cacheWrite": 0
            },
            "reasoning": false
          }
        ]
      }
    }
  },
  "plugins": {
    "entries": {
      "clickclack": {
        "enabled": true
      },
      "duckduckgo": {
        "enabled": true
      }
    }
  },
  "channels": {
    "clickclack": {
      "enabled": true
    }
  },
  "hooks": {
    "internal": {
      "enabled": true,
      "entries": {
        "boot-md": {
          "enabled": true
        },
        "bootstrap-extra-files": {
          "enabled": true
        },
        "command-logger": {
          "enabled": true
        },
        "compaction-notifier": {
          "enabled": true
        },
        "session-memory": {
          "enabled": true
        }
      }
    }
  },
  "wizard": {
    "lastRunAt": "2026-05-23T15:46:49.357Z",
    "lastRunVersion": "2026.5.20",
    "lastRunCommand": "onboard",
    "lastRunMode": "local"
  },
  "meta": {
    "lastTouchedVersion": "2026.5.20",
    "lastTouchedAt": "2026-05-23T15:46:49.521Z"
  },
  "skills": {
    "install": {
      "nodeManager": "npm"
    }
  }
}
