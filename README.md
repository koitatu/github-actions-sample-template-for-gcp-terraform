# github-actions-template-terraform

## リポジトリにあるものは？  
- リポジトリにterraformファイルをcommitすると、terraform plan/applyしてSlack通知するWorkflowです。
   - push to develop branch  
     developブランチへPushすると`terraform plan` --> Slack通知  
   - merge to main branch  
     MainブランチへMergeすると`terraform apply -auto-approve` --> Slack通知  

## GitHubのSettings-->Secretsで以下2つ設定が必要です。
- GOOGLE_CREDENTIALS
   - ServiceAccount用のキーファイルの中身を貼り付けてください。	
   - cf.
      - https://cloud.google.com/docs/authentication/production#create_service_account
- SLACK_WEBHOOK_URL
   - SlackのIncommingWebHookURLを貼り付けてください。	
- sample  
![image](https://user-images.githubusercontent.com/6356691/100606598-0556b900-334d-11eb-9dd6-3255c8e7acec.png)
