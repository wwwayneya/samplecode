## My Note

1. helloworld

xmlHttp.onreadystatechange = function() {
    if (xmlHttp.readyState == XMLHttpRequest.DONE) {
        var res_str = xmlHttp.responseText;
        var obj = JSON.parse(res_str);
        var short_url = obj.id;
        console.log(short_url);
    }
}

