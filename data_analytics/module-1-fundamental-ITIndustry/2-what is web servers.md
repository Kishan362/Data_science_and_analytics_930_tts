# What is a Web Server?

A **web server** is a computer system or software that stores website files (HTML pages, images, CSS, JavaScript) and delivers them to users over the internet when requested through a web browser. When you visit a website, your browser sends a request to the web server, and the server responds by sending the requested webpage back to your browser.

## How Does a Web Server Work?

1. A user opens a web browser and types a URL.
2. The browser sends an HTTP/HTTPS request to the web server.
3. The web server receives the request and processes it.
4. The server finds the requested files (HTML, CSS, images).
5. The server sends the files back to the browser as an HTTP response.
6. The browser displays the webpage to the user.

## Types of Web Servers

### 1. Apache HTTP Server
- Developed by the Apache Software Foundation.
- Most widely used web server in the world.
- Open-source and free to use.
- Supports multiple platforms (Windows, Linux, Mac).
- Used by millions of websites including YouTube and Facebook.

### 2. Nginx (Engine X)
- Developed by Igor Sysoev.
- Known for high performance and low memory usage.
- Acts as both a web server and a reverse proxy server.
- Handles a large number of concurrent connections efficiently.
- Used by Netflix, WordPress.com, and many high-traffic sites.

### 3. Microsoft Internet Information Services (IIS)
- Developed by Microsoft.
- Built into Windows Server operating systems.
- Works well with Microsoft technologies like ASP.NET.
- Used by enterprise-level applications and intranets.

### 4. Apache Tomcat
- Developed by the Apache Software Foundation.
- Primarily serves Java-based web applications.
- Acts as a servlet container for Java Servlet and JSP pages.
- Used for running dynamic web applications written in Java.

### 5. LiteSpeed Web Server
- Developed by LiteSpeed Technologies.
- Known for speed and high performance.
- Compatible with Apache configurations.
- Uses less memory than Apache under high traffic.

### 6. Caddy
- A modern, open-source web server.
- Automatic HTTPS with free SSL certificates.
- Simple configuration with a single file.
- Growing in popularity for its ease of use.

## Types of Web Servers Based on Purpose

### 1. Static Web Server
- Serves only fixed/static content like HTML, CSS, and images.
- Does not generate dynamic content.
- Example: Serving a simple portfolio website.

### 2. Dynamic Web Server
- Generates content on the fly based on user requests.
- Uses server-side scripting languages like PHP, Python, or Java.
- Example: Social media sites, e-commerce platforms.

## Key Features of a Web Server

- Handles HTTP and HTTPS requests from clients (browsers).
- Stores and serves website files.
- Supports SSL/TLS encryption for secure connections.
- Manages user authentication and access control.
- Logs all requests for monitoring and troubleshooting.

## Difference Between Web Server and Application Server

| Feature | Web Server | Application Server |
|---------|-----------|-------------------|
| Serves | Static and dynamic web pages | Business logic and dynamic content |
| Protocol | HTTP/HTTPS | HTTP, RMI, JMS |
| Examples | Apache, Nginx | JBoss, WebLogic, Tomcat |
| Usage | Hosting websites | Running enterprise applications |

## Short Answer

A web server is a system that stores website files and delivers them to users over the internet when requested. The most popular web servers are Apache, Nginx, IIS, and Tomcat.
