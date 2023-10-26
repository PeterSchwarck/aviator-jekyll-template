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
  - code_block: |-
      $.get("http://api.myapp.com/books/", { "token": "YOUR_APP_KEY"}, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
  - code_block: |-
      r = requests.get("http://api.myapp.com/books/", token="YOUR_APP_KEY")
      print r.text
    title: Python
    language: python
  - code_block: |-
      var request = require("request");
      request("http://api.myapp.com/books?token=YOUR_APP_KEY", function (error, response, body) {
      if (!error && response.statusCode == 200) {
        console.log(body);
      }
    title: Node.js
    language: javascript
  - code_block: |-
      curl http://sampleapi.readme.com/orders?key=YOUR_APP_KEY
    title: Curl
    language: bash

    title: Path parameters
    language: html
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
