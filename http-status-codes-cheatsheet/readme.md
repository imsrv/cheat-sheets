# HTTP Status Codes Cheat Sheet


HTTP status codes are three-digit numbers that indicate the outcome of an HTTP request. They fall into five classes:


### 1xx : HTTP Info. Codes
| Class | Code | Status | Description |
|-------|------|--------|-------------|
| 1xx   | 100  | Continue | The server has received the request headers and the client should proceed with the request. |
| 1xx   | 101  | Switching Protocols | The server is willing to change the application protocol being used on this connection. |
| 1xx   | 102  | Processing | The server has received and is processing the request but hasn't completed it yet. |
| 1xx   | 103  | Checkpoint | Used in the draft-ietf-httpbis-checkout-16 HTTP spec to resume aborted PUT or POST requests. |
| 1xx   | 122  | Request-URI Too Long | A Microsoft extension, indicating that a URI is longer than a server is willing to interpret. |


### 2xx : HTTP Success Codes
| Class | Code | Status | Description |
|-------|------|--------|-------------|
| 2xx   | 200  | OK | The request was successful. |
| 2xx   | 201  | Created | The request resulted in a new resource being created. |
| 2xx   | 202  | Accepted | The request has been accepted but not yet processed. |
| 2xx   | 203  | Non-Authoritative Information | The server successfully processed the request but is returning information from another source. |
| 2xx   | 204  | No Content | The server successfully processed the request but there is no additional content to send. |
| 2xx   | 205  | Reset Content | The server successfully processed the request, and the user agent should reset the document view. |
| 2xx   | 206  | Partial Content | The server is delivering only part of the resource due to a range header sent by the client. |
| 2xx   | 207  | Multi-Status | The message body that follows is an XML message and can contain a number of separate response codes. |
| 2xx   | 208  | Already Reported | The members of a DAV binding have already been enumerated in a previous reply to this request, and are not being included again. |
| 2xx   | 226  | IM Used | The server has fulfilled a request for the resource and the response is a representation of the result. |

### 3xx : HTTP Redirection Codes
| Class | Code | Status | Description |
|-------|------|--------|-------------|
| 3xx   | 300  | Multiple Choices | The requested resource has multiple choices, each with different locations. |
| 3xx   | 301  | Moved Permanently | The requested resource has been permanently moved to a new location. |
| 3xx   | 302  | Found | The requested resource resides temporarily under a different URL. |
| 3xx   | 303  | See Other | The response to the request can be found under a different URI. |
| 3xx   | 304  | Not Modified | Indicates that the resource has not been modified since the version specified by the request headers. |
| 3xx   | 305  | Use Proxy | The requested resource must be accessed through the proxy mentioned in the location header. |
| 3xx   | 306  | Switch Proxy | No longer used. Originally meant "Subsequent requests should use the specified proxy." |
| 3xx   | 307  | Temporary Redirect | The requested resource resides temporarily under a different URI, and the user agent must not change the request method if it performs an automatic redirection to that URI. |
| 3xx   | 308  | Permanent Redirect | The requested resource has been permanently moved to another location, and the client should update its URLs to the new location. |

### 4xx : HTTP Client Error Codes
| Class | Code | Status | Description |
|-------|------|--------|-------------|
| 4xx   | 400  | Bad Request | The server cannot or will not process the request due to a client error. |
| 4xx   | 401  | Unauthorized | Similar to 403 Forbidden but specifically for authentication purposes. |
| 4xx   | 402  | Payment Required | Reserved for future use. |
| 4xx   | 403  | Forbidden | The client does not have the necessary permission. |
| 4xx   | 404  | Not Found | The server cannot find the requested resource. |
| 4xx   | 405  | Method Not Allowed | The method specified in the request is not allowed for the resource identified by the request URI. |
| 4xx   | 406  | Not Acceptable | The server cannot produce a response matching the list of acceptable values defined in the request's headers. |
| 4xx   | 407  | Proxy Authentication Required | The client must first authenticate itself with the proxy. |
| 4xx   | 408  | Request Timeout | The server timed out waiting for the request. |
| 4xx   | 409  | Conflict | The request could not be completed due to a conflict with the current state of the target resource. |
| 4xx   | 410  | Gone | Indicates that the resource requested is no longer available and will not be available again. |
| 4xx   | 411  | Length Required | The server refuses to accept the request without a defined Content-Length. |
| 4xx   | 412  | Precondition Failed | The server does not meet one of the preconditions specified in the request headers. |
| 4xx   | 413  | Payload Too Large | The request is larger than the server is willing or able to process. |
| 4xx   | 414  | URI Too Long | The URI provided was too long for the server to process. |
| 4xx   | 415  | Unsupported Media Type | The server does not support the request's media type. |
| 4xx   | 416  | Range Not Satisfiable | The client has asked for a portion of the file but the server cannot supply that portion. |
| 4xx   | 417  | Expectation Failed | The server cannot meet the requirements of the Expect request-header field. |
| 4xx   | 418  | I'm a teapot | This code was defined in 1998 as one of the traditional IETF April Fools' jokes. |
| 4xx   | 421  | Misdirected Request | The request was directed at a server that is not able to produce a response. |
| 4xx   | 422  | Unprocessable Entity | The request was well-formed but was unable to be followed due to semantic errors. |
| 4xx   | 423  | Locked | The resource that is being accessed is locked. |
| 4xx   | 424  | Failed Dependency | The request failed due to the failure of a previous request. |
| 4xx   | 425  | Too Early | Indicates that the server is unwilling to risk processing a request that might be replayed. |
| 4xx   | 426  | Upgrade Required | The client should switch to a different protocol. |
| 4xx   | 428  | Precondition Required | The origin server requires the request to be conditional. |
| 4xx   | 429  | Too Many Requests | The user has sent too many requests in a given amount of time. |
| 4xx   | 431  | Request Header Fields Too Large | The server is unwilling to process the request because either an individual header field or all the header fields collectively are too large. |
| 4xx   | 451  | Unavailable For Legal Reasons | The server is denying access to the resource as a consequence of legal demand. |

### 5xx : HTTP Server Error Codes
| Class | Code | Status | Description |
|-------|------|--------|-------------|
| 5xx   | 500  | Internal Server Error | A generic error message returned when an unexpected condition was encountered by the server. |
| 5xx   | 501  | Not Implemented | The server does not support the functionality required to fulfill the request. |
| 5xx   | 502  | Bad Gateway | The server, while acting as a gateway or proxy, received an invalid response from an inbound server it accessed while attempting to fulfill the request. |
| 5xx   | 503  | Service Unavailable | The server is not ready to handle the request. Common causes are a server that is down for maintenance or that is overloaded. |
| 5xx   | 504  | Gateway Timeout | The server, while acting as a gateway or proxy, did not receive a timely response from an upstream server or some other auxiliary server it needed to access to complete the request. |
| 5xx   | 505  | HTTP Version Not Supported | The server does not support the HTTP protocol version that was used in the request. |
| 5xx   | 506  | Variant Also Negotiates | Transparent content negotiation for the request results in a circular reference. |
| 5xx   | 507  | Insufficient Storage | The server is unable to store the representation needed to complete the request. |
| 5xx   | 508  | Loop Detected | The server detected an infinite loop while processing the request. |
| 5xx   | 510  | Not Extended | Further extensions to the request are required for the server to fulfill it. |
| 5xx   | 511  | Network Authentication Required | The client needs to authenticate to gain network access. |
