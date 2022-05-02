## HTTP Status Codes
There are a lot of different status codes in total, in which there are 5 types.

The first one is 4xx, which you probably know, such as 404. You will find an complete definition of these below.


### 4xx Codes
400 - Bad Request. The server cannot or will not process the request due to an apparent client error (e.g., malformed request syntax, size too large, invalid request message framing, or deceptive request routing).

401 - Unauthorized. The server cannot let the visitor through, because he is not allowed to perform the request.

402 - Payment Required. Reserved for future use. The original intention was that this code might be used as part of some form of digital cash or micropayment scheme, as proposed, for example, by GNU Taler, but that has not yet happened, and this code is not widely used. Google Developers API uses this status if a particular developer has exceeded the daily limit on requests. Sipgate uses this code if an account does not have sufficient funds to start a call. Shopify uses this code when the store has not paid their fees and is temporarily disabled. Stripe uses this code for failed payments where parameters were correct, for example blocked fraudulent payments.

403 - Forbidden. The request contained valid data and was understood by the server, but the server is refusing action. This may be due to the user not having the necessary permissions for a resource or needing an account of some sort, or attempting a prohibited action (e.g. creating a duplicate record where only one is allowed). This code is also typically used if the request provided authentication by answering the WWW-Authenticate header field challenge, but the server did not accept that authentication. The request should not be repeated.

404 - Not Found. The requested resource could not be found but may be available in the future. Subsequent requests by the client are permissible.

405 - Method Not Allowed. A request method is not supported for the requested resource; for example, a GET request on a form that requires data to be presented via POST, or a PUT request on a read-only resource.

406 - The requested resource is capable of generating only content not acceptable according to the Accept headers sent in the request.

407 - Proxy Authentication Required. The client must first authenticate itself with the proxy.

408 - Request timeout. The server timed out waiting for the request. According to HTTP specifications: "The client did not produce a request within the time that the server was prepared to wait. The client MAY repeat the request without modifications at any later time."

409 - Conflict. Indicates that the request could not be processed because of conflict in the current state of the resource, such as an edit conflict between multiple simultaneous updates.

410 - Gone. Indicates that the resource requested is no longer available and will not be available again. This should be used when a resource has been intentionally removed and the resource should be purged. Upon receiving a 410 status code, the client should not request the resource in the future. Clients such as search engines should remove the resource from their indices. Most use cases do not require clients and search engines to purge the resource, and a "404 Not Found" may be used instead.

411 - Length Required. The request did not specify the length of its content, which is required by the requested resource.

412 - Precondition failed. The server does not meet one of the preconditions that the requester put on the request header fields.

413 - Payload too large. The request is larger than the server is willing or able to process. Previously called "Request Entity Too Large".

414 - URI Too long. The URI provided was too long for the server to process. Often the result of too much data being encoded as a query-string of a GET request, in which case it should be converted to a POST request. Called "Request-URI Too Long" previously.

415 - Unsupported Media Type. The request entity has a media type which the server or resource does not support. For example, the client uploads an image as image/svg+xml, but the server requires that images use a different format.

416 - Range Not Satisfiable. The client has asked for a portion of the file (byte serving), but the server cannot supply that portion. For example, if the client asked for a part of the file that lies beyond the end of the file. Called "Requested Range Not Satisfiable" previously.

417 - Expectation Failed. The server cannot meet the requirements of the Expect request-header field.

418 - I'm a teapot. This code was defined in 1998 as one of the traditional IETF April Fools' jokes, in RFC 2324, Hyper Text Coffee Pot Control Protocol, and is not expected to be implemented by actual HTTP servers. The RFC specifies this code should be returned by teapots requested to brew coffee. This HTTP status is used as an Easter egg in some websites, such as Google.com's I'm a teapot easter egg.
421 - Misdirected Request. The request was directed at a server that is not able to produce a response (for example because of connection reuse).

422 - Unprocessable Entity. The request was well-formed but was unable to be followed due to semantic errors.

423 - Locked. The resource that is being accessed is locked.

424 - Failed Dependency. The request failed because it depended on another request and that request failed (e.g., a PROPPATCH).

425 - Too Early. Indicates that the server is unwilling to risk processing a request that might be replayed.

426 - Upgrade Required. The origin server requires the request to be conditional. Intended to prevent the 'lost update' problem, where a client GETs a resource's state, modifies it, and PUTs it back to the server, when meanwhile a third party has modified the state on the server, leading to a conflict.

429 - Too many requests. The user has sent too many requests to the server in a given amount of time. Intended for use with rate-limiting schemes.

431 - Request Header Fields Too Large. The server is unwilling to process the request because either an individual header field, or all the header fields collectively, are too large.

451 - Unavailable for legal reasons. A server operator has received a legal demand to deny access to a resource or to a set of resources that includes the requested resource. The code 451 was chosen as a reference to the novel Fahrenheit 451.


### 5xx Codes
The server failed to fulfil a request. Response status codes beginning with the digit "5" indicate cases in which the server is aware that it has encountered an error or is otherwise incapable of performing the request. Except when responding to a HEAD request, the server should include an entity containing an explanation of the error situation, and indicate whether it is a temporary or permanent condition. Likewise, user agents should display any included entity to the user. These response codes are applicable to any request method.
