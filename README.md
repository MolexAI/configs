# MolexAI Configurations
A guide on how to add configurations to your app with `.molexconfig`.

# Getting started
Here is the basic format for your JSON file located in your`.molexconfig` folder.
<br>Don't forget, the name of the JSON file should be `config.json`.</br>

```json
{
  "name": "MolexAI Example App",
  "version": "0.0.1",
  "description": "This is an example app!"
}
```

## Integrations guide
To integrate apps like **Micro, Loom, or Auro** type the following below in your JSON file located in your`.molexconfig` folder.

### Auro
```json
{
  "integrations": {
    "auro": {
      "commands": {
        "email": [
          "/send-email --address mom@gmail.com --subject \"Hello mom\" --body \"How are you doing?\""
        ]
      },
      "autonomous": true
    }
  }
}
```
### Loom

```json
{
  "integrations": {
    "loom": {
      "commands": {
        "pipeline": [
          "/new-pipeline --name production",
          "/new-workflow --name production --type \"CI/CD\"",
          "/test --workflow production",
          "/monitor --workflow production",
          "/deploy --workflow production"
        ]
      },
      "autonomous": true
    }
  }
}
```
### Micro

```json
{
  "integrations": {
    "micro": {
      "commands": {
        "secure": [
          "/encrypt --file secret.txt",
          "/decrypt --file secret.txt"
        ],
        "test": [
          "/penetration-test --target https://molex.com",
          "/vulnerability-scan --target https://molex.com",
          "/security-audit --target https://molex.com"
        ]
      },
      "autonomous": true
    }
  }
}
```

## Jobs guide
To add jobs like `update`, `restart`, `compile`, or `retrieve` follow the instructions below in your JSON file located in your`.molexconfig` folder.

### Update
```json
{
  "jobs": {
    "update": {
      "commands": [
        "cd scripts",
        "./update.sh"
      ]
    }
  }
}
```

### Retrieve
```json
{
  "jobs": {
    "retrieve": {
      "commands": [
        "cd scripts",
        "python backup.py"
      ]
    }
  }
}
```

### Restart
```json
{
  "jobs": {
    "restart": {
      "commands": [
        "cd scripts",
        "./restart.sh"
      ]
    }
  }
}
```

### Compile (Required to run the config)
```json
{
  "jobs": {
    "compile": {
      "commands": [
        "cd scripts",
        "python compile.py"
      ]
    }
  }
}
```
