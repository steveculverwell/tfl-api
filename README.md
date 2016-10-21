# TFL API

Using the TFL API to get information on line status' and journey information.

## Getting Started
* [TFL API set up](https://api-portal.tfl.gov.uk/login)
* [Line API found here](https://api.tfl.gov.uk/#Line)
* [Postman Chrome API dev tool](https://www.getpostman.com/)
* [Handlebars JS Tempate tool](http://handlebarsjs.com/)

```javascript
      $(document).ready(function() {
      $.ajax({
          url: 'https://api.tfl.gov.uk/Line/Mode/tube/Status?detail=False&app_id=&app_key=',
          type: 'GET',
          dataType: 'json',
      }).done(function(response) {
          var template = Handlebars.compile($('#template').html());
          $('.derp').append(template(response));
      }).fail(function() {

      })
      });
```


