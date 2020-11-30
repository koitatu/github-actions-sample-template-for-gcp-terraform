# github-actions-sample-template-for-gcp-terraform
## このリポジトリは？  
- リポジトリにTerraformファイルをcommitすると、GCPに対してterraform plan/apply後、Slack通知するGithub ActionsのサンプルWorkflowを置いてます。
   - push to develop branch  
     Pushすると`terraform plan` --> Slack通知  
   - merge to main branch  
     Mergeすると`terraform apply -auto-approve` --> Slack通知  

## 利用前に必要なこと
### ..githubディレクトリのリネームと配置
```
cp -a ..github /path_to_your_repo/.github
```

### GitHubのSettings-->Secretsで以下2つ設定が必要です。
- GOOGLE_CREDENTIALS
   - ServiceAccount用のキーファイルの中身を貼り付けてください。	
   - cf.
      - https://cloud.google.com/docs/authentication/production#create_service_account
- SLACK_WEBHOOK_URL
   - SlackのIncommingWebHookURLを貼り付けてください。	
- sample  
![image](https://user-images.githubusercontent.com/6356691/100606598-0556b900-334d-11eb-9dd6-3255c8e7acec.png)
