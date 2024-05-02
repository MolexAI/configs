# MolexAI Configurations
A guide on how to add configurations to your app with `.molexconfig`.

# Getting started
Here is the basic format for your yaml file located in your`.molexconfig` folder.
<br>Don't forget, the name of the yaml file should be `config.yaml`.</br>

```yaml
name: MolexAI Example App
version: 0.0.1 # (DISCLAIMER) Version must be formatted in this order!
description: This is an example app!
```

## Integrations guide
To integrate apps like **Micro, Loom, or Auro** type the following below in your yaml file located in your`.molexconfig` folder.

### Auro
```yaml
integrations:
  auro: # Auro integration
    commands: 
      email: # Entering the email workspace
        - /send-email --address mom@gmail.com --subject "Hello mom" --body "How are you doing?"
      autonomous: true
```
### Loom

```yaml
integrations:
  loom: # Loom intergration
    commands:
      pipeline: # Entering the pipeline workspace
        - /new-pipeline --name production
        - /new-workflow --name production --type "CI/CD"
        - /test --workflow production
        - /monitor --workflow production
        - /deploy --workflow production
      autonomous: true
```
### Micro

```yaml
integrations:
  micro: # Micro intergration
    commands:
      secure: # Entering the encryption workspace
        - /encrypt --file secret.txt
        - /decrypt --file secret.txt
      test: # Entering the testing workspace
        - /penetration-test --target https://molex.com
        - /vulnerability-scan --target https://molex.com
        - /security-audit --target https://molex.com
      autonomous: true
```

## Jobs guide
To add jobs like `update`, `restart`, `compile`, or `retrieve` follow the instructions below in your yaml file located in your`.molexconfig` folder.

### Update
```yaml
jobs:
  update:
    commands: # The list of commands to enter and run your update script.
      - cd scripts # Enter the directory of your scripts.
      - ./update.sh # Run your update script (python or shell).
```

### Retrieve
```yaml
jobs:
  retrieve:
    commands:
      - cd scripts
      - python backup.py
```

### Restart
```yaml
jobs:
  restart:
    commands:
      - cd scripts
      - ./restart.sh
```

### Compile (Required to run the config)
```yaml
jobs:
  compile:
    commands:
      - cd scripts
      - python compile.py
```
