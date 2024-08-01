# .NET API Service Starter

This is a minimal .NET API service starter based on [Google Cloud Run Quickstart](https://cloud.google.com/run/docs/quickstarts/build-and-deploy/deploy-dotnet-service).

## Getting Started

Server should run automatically when starting a workspace. To run manually, run:
```sh
dotnet watch --urls=http://localhost:3000
```

## Testing With cURL

To test the server, you can run these codes after running the server:

Get Users;
```sh
curl http://localhost:3000/users
```

Add User;
```sh
curl -X POST http://localhost:3000/users \
     -H "Content-Type: application/json" \
     -d '{"Name": "Alice", "Email": "alice@example.com"}'
```

Update User;
```sh
curl -X PUT http://localhost:3000/users/1 \
     -H "Content-Type: application/json" \
     -d '{"Name": "Alice Updated", "Email": "aliceupdated@example.com"}'
```

Delete User; 
```sh
curl -X DELETE http://localhost:3000/users/1
```
