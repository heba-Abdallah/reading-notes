APIs
API Design Best Practices

What does REST stand for?
REST stands for Representational State Transfer. (It is sometimes spelled "ReST".) It relies on a stateless, client-server, cacheable communications protocol -- and in virtually all cases, the HTTP protocol is used.
REST APIs are designed around a resources.

What is an identifer of a resource? Give an example.

genes, organisms, tools, and reagents (such as antibodies).
What are the most common HTTP verbs?
Are POST, GET, PUT, PATCH, and DELETE.
What should the URIs be based on?
Resource Description Framework.
Give an example of a good URI:
example.com/articles/good-uri-design.
What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
is one that requires consumer to make tremendous (subjective matter) amount of distinct API calls to get needed information about a resource. George Reese has defined chatty API as any API that requires consumer to do more than a single call to perform a single, common operation. its poor quality.
What status code does a successful GET request return?
2xx Successful: This means the server successfully processed the request, but is not returning any content.
What status code does an unsuccessful GET request return?
412:“Precondition Failed.” Your browser included certain conditions in its request headers, and the server did not meet those specifications.
What status code does a successful POST request return?
The origin server MUST create the resource before returning the 201 status code.
What status code does a successful DELETE request return?
A 202 ( Accepted ) status code if the action will likely succeed but has not yet been enacted.