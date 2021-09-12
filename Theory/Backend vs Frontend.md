Like an Iceberg, Frontend is the visible part of the Iceberg, Backend is the part below waterlevel, and no user can see it.

Frontend -> Client Side
Backend -> Server side

Backend usually is HUGE, it cointains data and can consist of thousands of different pieces called microservices.

Full stack = Frontend + Backend

No need to create separate backends for multiple frontends. Multiple frondends are usually used for different devices. 

## Building blocks

### Frontend

1. HTML -> Hypertext Markup Languaje
   1. Defines the form of the page, buttons, 
2. CSS -> Cascade Styling Sheet
   1. Define styles for different parts, nice looking WebApps
3. JavaScript -> Most popular programming language
   1. Dynamic and response to user actions, like an engine in your car
   2. Responsible for communnication with Backend

### Backend

LOTS of technologies divided in three groups:

1. Programming Languages: Used to build API's and backend logic
   * Python
   * Java
   * NodeJS
   * PHP
   * C#

2. Infrastructure services:
   1. Subgroup 1: Used to buildand run actual backend applications written using different programming languages and also databeses
         * Docker
         * Kubernetes
   * Docker
   * AWS: Run any service, hosting service
   * ELK
   * Apache/Kafka: High speed messages exchange, for different services  to talk efficiently between them.

3. Databases:
   1. SQL or Relational
        * MySQL: Long-term storage with tables with stable relations between them
   2. Non-Relational
        * MongoDB: Most popular, different documents with different set of fields.
        * Redis: Very fast, stores data in RAM, real-time data processing

Usually build for screens, to show content.Those files have to be hosted on the server. It has static HTML or dynamic, created upon each client request. It can send additional requests to the server. 

Clients and servers communicate with requests and requests. Send multiple requests to different servers. Server can immediatly send response or send additional requests to other servers, read databeses, etc. It can read, save or modify data.

Usually services are set as different servers.

Most common protocol is HTTPS. It can send Text, images, data, etc.

- Language for communication... REST API. Server exposes multiple endpoints with diffetent methods to the API, and client send requests to those different end points.

- Another popular language is GraphQL (Query Language). There is just one endpoint.

## Frontend

**Responsive layout:** 

Layout smoothly adjust depending on screen size. When devices go from portrait to landscape, it is expected to see more data.

Tools: 
- Mobile First Design: Start design with mobile user in mind. It is more difficult to adapt the other way around
- CSS Media Queries: Target web browser by some caracteristics, features, device settings, user settings, etc. Example of use: Make background dark when oppening in the evening.
- Elements sizing with relative units: Sizes defined in percentages of the width, viewport, or boxes.
- CSS Flexbox: Simplify positioning, dependant on the screen size. Control dimensions relative to position and spacing.
- Separate CSS files for mobile and desktop: Easy to detect which device asks for the pase, and server sends specific page for a device kind.
- Use a domain for mobile application: (Subdomain) Like using `m.twitter.com` for mobile twitter, after detecting mobile device. Drawbacks, sharing URL's between users is a little bit messy.

## Traditional WebApp

When user opensa a URL, the device loads HTML/CSS/JS files for this URL. As you click on a link, the web browser requests the files for the other webpage and the page completely reloads. If you see white page for a couple seconds, webpages are rendered on the server side.

## Single Page App

The initial request is the same. CSS/JS contain all the logic for the site, but HTML is loades only once. Split apps into different subfiles, client can render other pages, without server help, without page reload. Client could send requests for data.

**Frameworks for SPA**
This works to small and huge enterprise apps

1. REACT: Flexible, shorter learning curve
2. ANGULAR: Large enterprises
3. VUE: Flexible, shorter learning curve
4. SVALTE
5. EMBER
6. METEOR

Pros
- Webpages aren't reload on user activity
- App fells more responsive
- Easier to deploy for fewer files
- Effectife bandwidth usage

Cons:
- Additional server configuration for proper SEO
- Large JS bundle size impacts initial page loading

## SAMPLE WEBAPP ARQUITECTURE


Frontend made with REACT.

API uses MongoDB Client.

![alt text](WebAPP_Arquitecture.jpeg)
