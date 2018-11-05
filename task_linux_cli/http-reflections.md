###What i learned about http
1) To make communication between a variety of hosts and clients possible and support mixtures of network configurations http is __stateless__ i.e. __it keeps very little information about a particular system and doesn't keep state between message exchanges__.
2) Communication between client and host occurs in __request-response__ pair.
3) `U`niform `R`esource `L`ocation - an address, where request is sent -  consist of these main parts:
    |protocol://|host|(:port,default is 80 )|/resource path|?query&query|
    |---|---|----|-----|-----|
    |http://|www.domain.com|(:1234)|/path/to/resource|?a=b&x=y|
4) URLs reveal the identity of the particular host with which we want to communicate, but the action that should be performed on the host is specified via HTTP __verbs__. Of course, there are several actions that a client would like the host to perform. HTTP has formalized on a few that capture the essentials that are universally applicable for all kinds of applications.
Main verbs are:
    - __GET__ - fetch, take data from the resource. The URL of this request contains all neccessary data _host to locate and return needed resource_;
    - __POST__ - create a new resource. Usually carries a _payload that specifies the data for the new resource_;
    - __PUT__ - update existing resource with new data;
    - __DELETE_ - delete an existing resource.
5) Status codes - code of the server's response to client's request. __Status codes tell client how to treat the response from the host__.
    - `1xx` family - informational messages.
    - `2xx` family - success (if request-response went without any errors)
    - `3xx` family - requires client to take additional action (needs)
    - `4xx` family - errors in request from client (client causes an error)
    - `5xx` family - errors in response from server (server causes an error)
6) Lifecycle of an http request :
    - resolve IP address from host name via DNS
    - establish a connection with the server
    - send a request
    - wait for a response
    - close connection
7) To provide a client with unique experience it's neccessary to identify it. Host can identify client with the help of:
    - Request headers: `From`, `Referer`, `User-Agent`;
    - Client IP;
    - Fat URLs;
    - Cookies. Cookies allow the server to attach arbitrary information for outgoing responses via the `Set-Cookie` response header. 
8) Authentication:
    - __Basic__: the server initially denies the client's request with a WWW-Authenticate response header and a 401 Unauthorized status code. On seeing this header, the browser displays a login dialog, prompting for a username and password. This information is sent in a base-64 encoded format in the Authentication request header. The server can now validate the request and allow access if the credentials are valid. Some servers might also send an Authentication-Info header containing additional authentication details.
    - __Digest__: A corollary to Basic-Authentication is Proxy Authentication. Instead of a web server, the authetication challenge is requested by an intermediate proxy. The proxy sends a Proxy-Authenticate header with a 407 Unauthorized status code. In return, the client is supposed to send the credentials via the Proxy-Authorization request header.