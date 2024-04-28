# MolexAI Configurations
A guide on how to add configurations to your app with `.molexconfig`.

## Getting started
To begin type the following in your yaml file located in your `.molexconfig` folder.
```yaml
integrations:
  auro: # In this example we'll use the Auro intergration
    commands: 
      email: # Entering the email workspace
        - /send-email --address mom@gmail.com --subject "Hello mom" --body "How are you doing?"
      autonomous: true 
```

## Intergrations guide
To intergrate apps like **Micro, Loom, or Auro** type the following below in your yaml file located in your`.molexconfig` folder.

### Auro
```yaml
integrations:
  auro: # Auro intergration
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
