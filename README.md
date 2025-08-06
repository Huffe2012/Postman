**📬 Postman API Exploration Lab**
This lab focused on using Postman to interact with and analyze APIs. The goal was to get hands-on experience with how API requests work, how to interpret status codes, and how to read response headers and bodies.

🛠️ Setup
✅ Downloaded Postman from postman.com

✅ Installed on a Ubuntu Linux virtual machine

🔍 What I Did
1. ✅ Tested a Successful GET Request
Endpoint Used: https://api.github.com/

Method: GET

Expected Result: 200 OK

Observation:

The response confirmed the endpoint was live and working

I analyzed the response headers, which included important metadata such as content type, rate limits, and server info.

<img width="1621" height="809" alt="Screenshot 2025-08-05 224316" src="https://github.com/user-attachments/assets/a6b0c1b6-835e-4951-b93f-82ffeb40a78e" />

<img width="1614" height="840" alt="Screenshot 2025-08-05 224334" src="https://github.com/user-attachments/assets/c21ed032-423f-4024-9c89-4305b670e333" />


While looking at the body of this API, I discovered links to other REST API endpoints, such as:

/user

/gists

/events

/repos/{owner}/{repo}

This gave me a better understanding of how APIs are structured and how different endpoints can be explored from a single root request.

<img width="1577" height="812" alt="Screenshot 2025-08-05 224352" src="https://github.com/user-attachments/assets/572dd244-1184-4361-948f-9bd52529770a" />


2. ❌ Tested a GET Request That Requires Authentication
Endpoint Used: https://api.github.com/user

Method: GET

Expected Result: 401 Unauthorized

<img width="1623" height="823" alt="Screenshot 2025-08-05 222856" src="https://github.com/user-attachments/assets/8f1b079d-f8c5-453d-98a3-978cb1ee80b4" />

<img width="1371" height="447" alt="Screenshot 2025-08-05 222923" src="https://github.com/user-attachments/assets/796fc59f-b978-47c5-a53c-abd883a36a54" />


What Happened:

GitHub returned a 401 status code, indicating authentication is required

I inspected the response body, which returned:

json
Copy
Edit
{
  "message": "Requires authentication",
  "documentation_url": "https://docs.github.com/rest/users/users#get-the-authenticated-user",
  "status": "401"
}

<img width="1604" height="653" alt="Screenshot 2025-08-05 223003" src="https://github.com/user-attachments/assets/f9d3ab1b-8588-499b-89d8-65817a9a0db9" />


This taught me that certain endpoints require either:

Basic Auth (username/password)

OAuth Token

Personal Access Token

🧠 What I Learned

Postman makes it easy to test and analyze API requests

Status codes like 200 OK and 401 Unauthorized quickly inform you of request success or failure

Headers provide valuable info like content type, server settings, and rate limits

401 errors signal that credentials are missing or invalid — useful for learning about API authentication

🛠️ Key Features of REST APIs

Feature	Description

Stateless	Each request stands alone; no memory of previous requests.

Resource-based	You access resources (like users, posts, comments) using URLs.

Uses HTTP methods	GET, POST, PUT, DELETE, etc.

Standard format	Most responses are returned in JSON or sometimes XML.

Scalable	REST works well for web and mobile apps due to its simplicity and structure.

📚 Next Steps
In future labs, I plan to:

Use POST, PUT, and DELETE methods

Test APIs that require authentication
