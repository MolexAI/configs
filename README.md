# MolexAI Configurations :gear:
A guide on how to add configurations to your app with `.molexconfig`.

## Getting started :rocket:
Here is the basic format for your JSON file located in your `.molexconfig` folder.
> **Note:** The name of the JSON file should be `molexconfig.json`.

```json
{
  "name": "MolexAI Example App",
  "version": "0.0.1",
  "description": "This is an example app!",
  "url": "https://github.com/example/example_app",
  "token": "molex_id_example"
}
```

## Integrations guide :link:
To integrate apps like **Micro, Loom, or Auro** type the following below in your JSON file located in your `.molexconfig` folder.

<details>
<summary>Auro</summary>

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
</details>

<details>
<summary>Loom</summary>

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
</details>

<details>
<summary>Micro</summary>

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
</details>

## Jobs guide :hammer_and_wrench:
To add jobs like `update`, `restart`, `compile`, or `retrieve` follow the instructions below in your JSON file located in your `.molexconfig` folder.

<details>
<summary>Update</summary>

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
</details>

<details>
<summary>Retrieve</summary>

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
</details>

<details>
<summary>Restart</summary>

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
</details>

<details>
<summary>Compile (Required to run the config)</summary>

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
</details>

---

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)
