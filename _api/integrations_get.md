---
title: /{your-account-name}/integrations
position_number: 1.5
type: get
description: Lists all your integration’s webhook event subscriptions  
parameters:
  - name:
    content:
content_markdown: |-
  Deletes a book in your collection.
left_code_blocks:
  - code_block: |-
      $.ajax({
        "url": "https://next.textus.com/{your-account-name}/integrations",
        "type": "GET",
        "data": {
          "token": "YOUR_APP_KEY"
        },
        "success": function(data) {
          alert(data);
        }
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |2-
      {
        "id": 3,
        "status": "deleted"
      }
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Book doesn't exist"
      }
    title: Error
    language: json
---

