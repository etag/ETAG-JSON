ETAG-JSON
=========

ETAG-JSON is a format for capturing data and metadata associated with ETAG RFID readers and associated accessories.  It builds upon existing standards, such as  A full ETAG-JSON object contains information to uniquely identify the ETAG reader, connected accessories, RFID reads and associated accessory reads. JSON objects consist of key/value pairs where member values can be strings, numbers, objects, arrays or the literal values 'true','false','null.  

ETAG reader metadata is extensible (tags can be added as needed) but should contain at a minimum: id, location, name, firmwareversion, 

* `id` should be an [RFC4122](http://www.ietf.org/rfc/rfc4122.txt) compliant Version 1 timestamp/nodeid UUID.
* `location` is represented as a [GeoJSON](http://geojson.org/geojson-spec.html) fragment describing the location, most typically `location: { type: Point, coordinates: [ 0 , 0 ] }`


   { type: "ETAGMetadata",
    id: "2fb767b0-06ba-11e4-9191-0800200c9a66",
    location: { type: Point, coordinates: [ 0 , 0 ] }
    
    
   [
           { timestamp: "2015-01-02T110000Z", reader_url: "http://<something>/reader/2fb767b0-06ba-11e4-9191-0800200c9a66", tag_id: "someid", FIXME} 
      
      ]
      
   }
      
