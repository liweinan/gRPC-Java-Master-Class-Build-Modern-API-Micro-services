- [https://github.com/grpc/grpc-java/blob/master/documentation/server-reflection-tutorial.md](https://github.com/grpc/grpc-java/blob/master/documentation/server-reflection-tutorial.md)

---

```bash
➤ mvn exec:java -Dexec.mainClass="greeting.server.GreetingServer"
Server started
Listing on port : 50052
```

---

```bash
➤ grpc_cli ls localhost:50052
greeting.GreetingService
grpc.reflection.v1alpha.ServerReflection
```

---

```bash
➤ grpcurl --plaintext -d '{"first_name": "foo"}' localhost:50051 greeting.GreetingService/greet
{
  "result": "Hello : foo"
}
```