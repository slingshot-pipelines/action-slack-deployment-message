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

|      INPUT      |  TYPE  | REQUIRED | DEFAULT |                                                      DESCRIPTION                                                       |
|-----------------|--------|----------|---------|------------------------------------------------------------------------------------------------------------------------|
|    COMPONENT    | string |   true   |         |                                        The name of the component being deployed                                        |
|   ENVIRONMENT   | string |   true   |         |                                           The environment being deployed to                                            |
|   JOB_STATUS    | string |   true   |         | The result of the deployment. One of "success", "failure", or "cancelled". Should be passed as the `job.status` field. |
|                 |        |          |         |              See https://docs.github.com/en/actions/reference/workflows-and-actions/contexts#job-context               |
|     PROJECT     | string |   true   |         |                                         The name of the project being deployed                                         |
| SLACK_BOT_TOKEN | string |   true   |         |                               The Slack bot token used to authenticate the message post                                |
|  SLACK_CHANNEL  | string |   true   |         |                                 The Slack channel (name or ID) to post the message to                                  |
|     VERSION     | string |   true   |         |                                               The version being deployed                                               |

<!-- AUTO-DOC-INPUT:END -->

## Outputs

<!-- AUTO-DOC-OUTPUT:START - Do not remove or modify this section -->
No outputs.
<!-- AUTO-DOC-OUTPUT:END -->
