# GitHub Action Notifier - Slack

Customized GitHub Action integration with Slack inspired by [rtCamp/action-slack-notify](https://github.com/rtCamp/action-slack-notify)

## How it looks

<img width="485" alt="action-slack-notify-rtcamp" src="https://user-images.githubusercontent.com/44806418/98253636-953a5a80-1f7b-11eb-88be-ab73a039bc70.png">

<img width="485" alt="action-slack-notify-rtcamp" src="https://user-images.githubusercontent.com/44806418/98254171-404b1400-1f7c-11eb-9ad7-260ae0f0b656.png">

## Usage

```yaml
 - name: slack-notification-for-failure
   uses: codigube/github-action-notify-slack@v1.0.0
   if: failure() || cancelled()
   env:
    SLACK_COLOR: '#DF5A49'
    SLACK_MESSAGE: 'Job ${{ github.job }} failed'

- name: slack-notification-for-success
  uses: codigube/github-action-notify-slack@v1.0.0
  if: success()
  env:
    SLACK_MESSAGE: 'Job ${{ github.job }} succeeded'
```

For more detailed configuration, please refer to [rtCamp/action-slack-notify](https://github.com/rtCamp/action-slack-notify)