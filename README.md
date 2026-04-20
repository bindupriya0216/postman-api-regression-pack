# User Service API — Regression Pack

Automated API test suite built in Postman to validate core CRUD operations, auth, and error handling.

**Tech:** Postman, JavaScript, REST API, Environment Variables  
**Run Stats:** 4 requests | 6 assertions | 0 failures | 446ms avg response

### Coverage
| Request | Method | Validation |
| --- | --- | --- |
| Get User By ID | GET | 200 status, auth header, response time < 1s |
| Create User | POST | 201 status, saves dynamic `userId` to environment |
| Get Created User | GET | Request chaining using `{{userId}}`, handles mock API 404 |
| Get Invalid User | GET | Negative test: 404 status, error response < 2s |

### Key Skills Demonstrated
1. **Environment-based config**: `{{baseUrl}}` and `{{xApiKey}}` for multi-env testing
2. **Request chaining**: Extract `id` from POST response, auto-inject into next GET
3. **Auth handling**: Global `x-api-key` header at collection level
4. **Positive/Negative testing**: Validates 200/201 success and 404 error paths
5. **Mock API awareness**: Tests accept 200/404 to handle stateless mocks

### How to Run
1. Import both `.json` files into Postman
2. Select `reqres test environment`
3. Collection Runner > Run User Service API
