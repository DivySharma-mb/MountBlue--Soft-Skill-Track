# <center>REST Architecture<center>

What does an *interactive* software or sevice mean?

In computer science, interactive refers to a software which accepts and responds to input from people—for example, data or commands, and, creation of such softwares is what software architectures, like the REST architecture, are used for.

## **REST**

According to Wikipedia, **REST**, or, **Representational state transfer** is a software architectural style that is commonly used to create interactive applications that uses [Web Services](https://en.wikipedia.org/wiki/Web_service).

REST provides standards between computer systems on the web, making it easier for systems to communicate with each other. REST-compliant systems, often called *RESTful* systems, are characterized by how they are stateless and separate the concerns of client and server.

In a RESTful Web service, requests made to a resource's URI elicit a response with a payload formatted in HTML, XML, JSON, or some other format. For example, the response can confirm that the resource state has been changed. The response can also include hypertext links to related resources.

By using a stateless protocol and standard operations, RESTful systems aim for fast performance, reliability, and the ability to grow by reusing components that can be managed and updated without affecting the system as a whole, even while it is running.

## **Architectural constraints**

The goal of REST is to increase performance, scalability, simplicity, modifiability, visibility, portability, and reliability. This is achieved through following REST principles such as a client–server architecture, statelessness, cacheability, use of a layered system, support for code on demand, and using a uniform interface. These principles must be followed for the system to be classified as REST.

### **Uniform Interface**

A resource in the system should have only one logical URI, and that should provide a way to fetch related or additional data. It’s always better to synonymize a resource with a web page.

Any single resource should not be too large and contain each and everything in its representation. Whenever relevant, a resource should contain links (HATEOAS) pointing to relative URIs to fetch related information.

Also, the resource representations across the system should follow specific guidelines such as naming conventions, link formats, or data format (XML or/and JSON).

All resources should be accessible through a common approach such as HTTP GET and similarly modified using a consistent approach.

#### **Client-server**

This constraint essentially means that client application and server application MUST be able to evolve separately without any dependency on each other. A client should know only resource URIs, and that’s all.

#### **Stateless**

Make all client-server interactions stateless. The server will not store anything about the latest HTTP request the client made. It will treat every request as new.

If the client application needs to be a stateful application for the end-user, where user logs in once and do other authorized operations after that, then each request from the client should contain all the information necessary to service the request – including authentication and authorization details.

#### **Cacheable**

In REST, caching shall be applied to resources when applicable, and then these resources MUST declare themselves cacheable. Caching can be implemented on the server or client-side.

#### **Layered system**

REST allows you to use a layered system architecture where you deploy the APIs on server A, and store data on server B and authenticate requests in Server C, for example. A client cannot ordinarily tell whether it is connected directly to the end server or an intermediary along the way.

#### **Code on demand**

This constraint is optional. Most of the time, you will be sending the static representations of resources in the form of XML or JSON. But when you need to, you are free to return executable code to support a part of your application, e.g., clients may call your API to get a UI widget rendering code.

## **Architectural Properties**

The constraints of the REST architectural style affect the following architectural properties:

**a)** Performance in component interactions, which can be the dominant factor in user-perceived performance and network efficiency.

**b)** Scalability allowing the support of large numbers of components and interactions among components.

**c)** Simplicity of a uniform interface.

**d)** Modifiability of components to meet changing needs (even while the application is running).

**e)** Visibility of communication between components by service agents.

**f)** Portability of components by moving program code with the data.

**g)** Reliability in the resistance to failure at the system level in the presence of failures within components, connectors, or data.

#### Citations:

https://en.wikipedia.org/wiki/Representational_state_transfer

https://www.codecademy.com/articles/what-is-rest

https://restfulapi.net/rest-architectural-constraints/#:~:text=REST%20stands%20for%20Representational%20State,the%20development%20of%20web%20services
