# TFL API

Using the TFL API to get information on line status' and journey information.

## Getting Started
* [TFL API set up](https://api-portal.tfl.gov.uk/login)
* [Line API found here](https://api.tfl.gov.uk/#Line)
* [Postman Chrome API dev tool](https://www.getpostman.com/)
* [Handlebars JS Tempate tool](http://handlebarsjs.com/)
* [National Public Transport Access Nodes (NaPTAN) ](https://data.gov.uk/dataset/naptan)
* [Stop Point Search](https://api.tfl.gov.uk/Stoppoint/Search/Chesham)
* [open stack](http://opendata.stackexchange.com/questions/4027/london-rail-and-tube-station-locations)
 * [location of things blog](https://blog.tfl.gov.uk/2015/10/08/unified-api-part-2-lot-location-of-things/)

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

* /StopPoint/{id}/Arrivals
* chesham 940GZZLUCSM
* https://api.tfl.gov.uk/StopPoint/940GZZLUCSM/Arrivals?app_id=yyy&app_key=XXX
* _
