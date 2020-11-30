# github-actions-template-terraform

## これは何？  
- リポジトリにterraformファイルをcommitすると、terraform plan/applyしてSlack通知するWorkflowです。
	- push to develop branch  
	Pushすると`terraform plan` --> Slack通知  
	- merge to main branch  
	Mergeすると`terraform apply -auto-approve` --> Slack通知  

## GitHubのSettings-->Secretsで以下2つ設定が必要です。
- GOOGLE_CREDENTIALS
   - ServiceAccount用のキーファイルの中身を貼り付けてください。	
   - cf.
      - https://cloud.google.com/docs/authentication/production#create_service_account
- SLACK_WEBHOOK_URL
   - SlackのIncommingWebHookURLを貼り付けてください。	
