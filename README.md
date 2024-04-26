# MolexAI Configurations
A guide on how to add configurations to your app with `.molexconfig`.

### Getting started


### App intergrations
To intergrate apps like **Micro, Loom, or Auro** type the following below in your yaml file located in your`.molexconfig` folder.

```yaml
integrations:
  auro: # Auro intergration
    commands: 
      email: # Entering the email command line
        - /send-email --address mom@gmail.com --subject "Hello mom" --body "How are you doing?"
      autonomous: true
```
You can also test, monitor, or deploy your app with the **Loom** intergration.

```yaml
integrations:
  loom: # Loom intergration
    commands:
      pipeline: # Entering the pipeline command line
        - /new-pipeline --name production
        - /new-workflow --name production --type "CI/CD"
        - /test --workflow production
        - /monitor --workflow production
        - /deploy --workflow production
      autonomous: true
```
More to come as our journey continues, enjoy.
