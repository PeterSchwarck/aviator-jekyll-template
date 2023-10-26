---
title: Integrations
position_number: 1.5
type: get
description: Get event subscriptions
parameters:
  - name: Path parameter
    content: '{your-account-name}'
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
          {z
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
