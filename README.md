# Kore.io Project Test
![](https://kore.io/images/logos/logo-front.png)

Kore is an easy to use web application framework for writing scalable web APIs in C.
Its main goals are security, scalability and allowing rapid development and deployment of such APIs.

Because of this Kore is an ideal candidate for building robust, scalable and secure web things.

# Getting started

Kore makes it easy to get started without having to fiddle with build frameworks such as make. Using the builtin commands you can create, compile and run Kore applications. However if you prefer building Makefiles and linking the libraries together yourself, go for it.

```
$ kore create myapp
$ cd myapp
$ kore run
compiling myapp.c
myapp built succesfully!
[parent]: running on https://127.0.0.1:8888
[parent]: kore is starting up
[wrk 0]: worker 0 started (cpu#0)

```

# Hello world

Kore exposes an easy to use API to build your applications. Below is an example of how simple it is to get going with writing web applications in C. The code will respond to all requests with an "Hello world" response.

```
#include <kore/kore.h>
#include <kore/http.h>

int	page(struct http_request *);

int
page(struct http_request *req)
{
    http_response(req, 200, "Hello world", 11);
    return (KORE_RESULT_OK);
}
```

# Kore web framework

Kore is a web application framework written in C that allows you to create blazing fast web applications. It focuses on security, stability and rapid development.
The latest version is 2.0.0 and was released 1st of August 2016.
This gitbook serves as the main documentation for the project.
The documentation is correct for the latest 2.0.0 release but may not be correct for the latest master branch on github.
