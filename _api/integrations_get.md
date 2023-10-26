---
title: Integrations
position_number: 1.5
type: get
description: Get event subscriptions
parameters:
  - name:
    content:
content_markdown: Lists all your integration’s webhook event subscriptions
left_code_blocks:
  - code_block: |+
      <table>
      <thead>
        <tr>
          <th>Path Parameter</th>
          <th>Type</th>
          <th>Description</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>your-account-name</td>
          <td>String</td>
          <td>Specifies the name of your primary non-messaging account.  </td>
        </tr>
      </tbody>
      </table>  

    title: Path parameters
    language: html
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
