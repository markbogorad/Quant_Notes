up:: [[Computer Science MOC]]
tags:: #Programming  
# APIs
- A set of rules that allow different software applications to communicate with each other
## Types of APIs
- **Web APIs:** These are used for web-based applications and services. They allow interaction over the internet using protocols such as HTTP/HTTPS. Examples include REST (Representational State Transfer) and SOAP (Simple Object Access Protocol).
- **Library/Framework APIs:** These are used within a particular programming language or framework. They provide specific functionality that developers can incorporate into their applications.
- **Operating System APIs:** These allow software applications to interact with the underlying operating system. Examples include Windows API and POSIX for Unix-based systems.
- **Database APIs:** These provide methods for querying and manipulating databases. Examples include JDBC for Java and ADO.NET for .NET.
## Components of an API
- **Endpoint:** The specific URL where an API can be accessed. Each endpoint corresponds to a particular function or data resource.
- **Request:** The call made to an API endpoint. This usually includes a method (such as GET, POST, PUT, DELETE), headers, and sometimes a body (for data).
- **Response:** The data returned by the API after processing a request. This usually includes a status code (indicating success or failure) and the requested data in a structured format like JSON or XML.
- **Authentication:** Many APIs require authentication to ensure that only authorized users can access certain resources. This can be done using API keys, tokens, or OAuth.
### Example (Quandl):
1) Request a key and use `requests` library
```
import requests

api_key = 'YOUR_API_KEY'
dataset = 'WIKI/AAPL` # sample dataset (there are others)
url = f'https://www.quandl.com/api/v3/datasets/{dataset}.json?api_key={api_key}'

response = requests.get(url)
data = response.json()

print(data)
```
 Or do it with an integration:
 ```
import quandl

# Replace with your actual API key
quandl.ApiConfig.api_key = 'YOUR_API_KEY'

# Fetch data for Apple Inc. from the WIKI dataset
data = quandl.get('WIKI/AAPL')

# Display the first few rows of the data
print(data.head())

```

