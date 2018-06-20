## My Note

<script type='text/javascript' src="//ajax.googleapis.com/ajax/libs/jquery/2.0.2/jquery.min.js"></script>

<script>

var xmlHttp = new XMLHttpRequest();

xmlHttp.onreadystatechange = function() {
    if (xmlHttp.readyState == XMLHttpRequest.DONE) {
        var res_str = xmlHttp.responseText;
        var obj = JSON.parse(res_str);
        var short_url = obj.id;
        console.log(short_url);
    }
}

xmlHttp.open("POST", "https://www.googleapis.com/urlshortener/v1/url?key=AIzaSyCOVTzj6a7qQ-Z9TaisU-fWTdnOiNdYMQc", true);
xmlHttp.setRequestHeader("Content-Type", "application/json; charset=utf-8");

var req = new Object();

req.longUrl = "http://www.google.com/";


var jsonStr = JSON.stringify(req);

xmlHttp.send(jsonStr);

</script>
