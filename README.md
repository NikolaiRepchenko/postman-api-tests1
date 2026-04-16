# Postman API Testing

This repository contains API testing examples using Postman.

## 🔧 What is covered
- REST API testing
- Positive and negative scenarios
- Status code validation
- Response body validation
- Environment variables
- Pre-request scripts
- Tests (JavaScript)

## 📂 Structure
- collection.json
- environment.json

## 🚀 Example tests

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Response has token", function () {
    const jsonData = pm.response.json();
    pm.expect(jsonData.token).to.exist;
});
