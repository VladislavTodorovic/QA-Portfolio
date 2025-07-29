**REST API Testing with Postman – Swagger Petstore Example**

I created eight requests (four with positive and four with negative scenarios) using the REST API in Postman for the Swagger Petstore ([https://petstore.swagger.io/](https://petstore.swagger.io/)). Additionally, I defined two environment variables, used a randomly generated value for the “name” field in one of the request bodies, and implemented two test script snippets for each request.

[https://www.postman.com/vladislavtodorovic/workspace/next-level-qa-5-nedelja-domaci-osnovni/collection/36218870-01a6c9ca-6a9e-4a5a-a709-12cc86c1a962?action=share\&creator=36218870](https://www.postman.com/vladislavtodorovic/workspace/next-level-qa-5-nedelja-domaci-osnovni/collection/36218870-01a6c9ca-6a9e-4a5a-a709-12cc86c1a962?action=share&creator=36218870)

|  | Test Case Name | Type of Request | Scripts |
| ----- | ----- | :---: | ----- |
| 1\. | Place An Order For A Pet | POST | Status code is 200 Response time is less than 200ms |
| 2\. | Update an Existing Pet | PUT | Status code is 200 Response time is less than 200ms |
| 3\. | Find Pet | GET | Status code is 200 Response time is less than 200ms |
| 4\. | Delete Pet | DELETE | Status code is 200 Response time is less than 200ms |
| 5\. | Place an Order for a Pet Wrong | POST | Status code is 500 Response time is less than 200ms |
| 6\. | Update an Existing Pet Wrong | PUT | Status code is 500 Response time is less than 200ms |
| 7\. | Find Pet Wrong | GET | Status code is 500 Response time is less than 200ms |
| 8\. | Delete Pet Wrong | DELETE | Status code is 500 Response time is less than 200ms |

