---
title: Integrations
position_number: 1.5
type: put
description: Updates your integration’s webhook event subscriptions
request:
  -path-parameters:
    - name: '{your-account-name}'
      content: 'Specifies the name of your primary non-messaging account.'
  -request_body:
    - name:
      content:
content_markdown: Lists all your integration’s webhook event subscriptions
left_code_blocks:
  - code_block: curl https://next.textus.com/{your-account-name}/integrations
    title: CURL
    language: json
right_code_blocks:
  - code_block: |-
      {
        "@type": "hydra:Collection",
        "@context": "/contexts/hydra:Collection.jsonld",
        "id": "http://www.example.com/my_account/integrations",
        "members": [
          {
            "@type": "Integration",
            "@context": "/contexts/Integration.jsonld",
            "id": "/integrations/0yX2VrJ",
            "active": true,
            "provider": "webhook",
            "config": {
              "baseUrl": "https://foo.bar.com/zest",
              "webhookSecret": "textus-abcdefgh12345678",
              "clientSecret": "[FILTERED]"
            },
            "settings": {}
          }
        ],
        "totalItems": 1
      }
    title: Response
    language: json
  - code_block: |-
      {
        "error": true,
        "message": "Book doesn't exist"
      }
    title: Error
    language: json
---
