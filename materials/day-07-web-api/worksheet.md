# Day 7 Worksheet: Web API

Verify endpoints (adapt resource name as in tutorial):
- GET /api/items → 200 OK with array of items
- POST /api/items → 201 Created with Location header
- GET /api/items/{id} → 200 OK or 404 Not Found

 Additional checks:
- Swagger UI available at /swagger
- Authentication required for POST when enabled
- JSON validation errors return 400 with problem details
