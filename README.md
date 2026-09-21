# action-slack-deployment-message

A GitHub action for sending a Slack message announcing the result of a deployment

## Example

```yml
-
  name: Notify Slack
  if: always()
  uses: slingshot-pipelines/action-slack-deployment-message@v0
  with:
    SLACK_BOT_TOKEN: ${{ secrets.SLACK_BOT_TOKEN }}
    SLACK_CHANNEL: deployments
    PROJECT: slingshot-pipelines
    COMPONENT: api
    VERSION: v1.2.3
    ENVIRONMENT: production
    JOB_STATUS: ${{ job.status }}
```

## Inputs

<!-- AUTO-DOC-INPUT:START - Do not remove or modify this section -->
<!-- AUTO-DOC-INPUT:END -->

## Outputs

<!-- AUTO-DOC-OUTPUT:START - Do not remove or modify this section -->
No outputs.
<!-- AUTO-DOC-OUTPUT:END -->
