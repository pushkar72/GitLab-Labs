# Microsoft Teams Integration

## Task 1 : Create Outlook WebHook

- Open MS Teams and Create New Team **Sanofi**
- In Sanofi > General > Connectors

    ![sc](images/L15-1.jpg)

- Search WebHook adn Configure InComing Webhook
  
    ![sc](images/L15-2.jpg)

- Enter Webhook Name and Click Create
- Note WebHook Url
  
  ![sc](images/L15-3.jpg)

---
## Task 2 : Register Webhook with Gitlab

- Goto GitLab Project > Settings > Webhooks
- Enter Webhook Url Copied from MS Teams. Leave Secret Token Empty
  
  ![sc](images/L15-4.jpg)

- Select _Push Events_, _Pipeline Events_ and click **Add WebHook**