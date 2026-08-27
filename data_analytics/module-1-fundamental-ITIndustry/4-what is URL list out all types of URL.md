# What is a URL?

A **URL** stands for **Uniform Resource Locator**. It is the address used to access resources on the internet. Every website, image, video, or file on the internet has a unique URL that tells the browser where to find it. A URL is the same as a web address that you type in the browser's address bar.

## Parts of a URL

A typical URL has the following parts:

```
https://www.example.com/products/shoes?id=101&color=red
|____|  |____________|  |______________|  |______________|
  |          |                |                  |
Protocol   Domain          Path              Query String
```

### 1. Protocol (Scheme)
- Tells the browser how to communicate with the server.
- Examples: `https://`, `http://`, `ftp://`, `mailto:`

### 2. Domain Name (Host)
- The name of the website or server.
- Example: `www.example.com`

### 3. Path
- The specific location of the page or file on the server.
- Example: `/products/shoes`

### 4. Query String
- Parameters passed to the server for dynamic content.
- Example: `?id=101&color=red`

### 5. Port Number (Optional)
- Specifies the port on the server to connect to.
- Example: `https://www.example.com:443`

### 6. Fragment (Anchor)
- Points to a specific section within a webpage.
- Example: `#section2`

---

## Types of URLs

### 1. Static URL
- The URL does not change and always points to the same content.
- The file is stored as a fixed HTML file on the server.
- Example: `https://www.example.com/about.html`
- Easy to index by search engines.

### 2. Dynamic URL
- The URL changes based on user input or database queries.
- Content is generated in real-time by the server.
- Example: `https://www.example.com/products.php?id=101`
- Common in e-commerce and social media sites.

### 3. Absolute URL
- Contains the complete address of a resource including protocol, domain, and path.
- Can be used from any location on the internet.
- Example: `https://www.example.com/images/photo.jpg`

### 4. Relative URL
- Contains only the partial path of a resource.
- Works only relative to the current page's URL.
- Example: `/images/photo.jpg` or `../images/photo.jpg`

### 5. Base URL
- The root address from which all relative URLs are built.
- Example: `https://www.example.com/`

### 6. Short URL (URL Shortener)
- A condensed version of a long URL using a URL shortening service.
- Redirects the user to the original long URL.
- Example: `https://bit.ly/3xY7z` redirects to `https://www.example.com/very/long/path/to/page`

### 7. Canonical URL
- The preferred version of a URL when multiple URLs lead to the same content.
- Used for SEO to avoid duplicate content issues.
- Example: `https://www.example.com/` is preferred over `https://example.com/`

### 8. Custom URL
- A URL that is personalized or branded for a specific purpose.
- Example: `https://youtube.com/@channelname`

---

## Types of URL Protocols

| Protocol | Full Form | Usage |
|----------|-----------|-------|
| `http://` | HyperText Transfer Protocol | Standard web pages (not secure) |
| `https://` | HyperText Transfer Protocol Secure | Secure web pages with SSL encryption |
| `ftp://` | File Transfer Protocol | Transferring files between client and server |
| `sftp://` | SSH File Transfer Protocol | Secure file transfer over SSH |
| `mailto:` | Mail Transfer Protocol | Opening email client to send mail |
| `file://` | Local File Protocol | Accessing local files on the computer |
| `telnet://` | Telnet Protocol | Remote access to servers and devices |

## URL vs URI vs URN

| Feature | URL | URI | URN |
|---------|-----|-----|-----|
| Full Form | Uniform Resource Locator | Uniform Resource Identifier | Uniform Resource Name |
| Purpose | Locates a resource with address | Identifies a resource by name | Names a resource permanently |
| Contains Location? | Yes | No | No |
| Example | `https://www.google.com` | `urn:isbn:0451450523` | `urn:isbn:0451450523` |

## Short Answer

A URL (Uniform Resource Locator) is the address of a resource on the internet. The main types of URLs are Static, Dynamic, Absolute, Relative, Short, and Canonical URLs. URLs use protocols like HTTP, HTTPS, and FTP to communicate with servers.
