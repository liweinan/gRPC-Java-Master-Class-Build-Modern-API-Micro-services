- [https://github.com/grpc/grpc-java/blob/master/documentation/server-reflection-tutorial.md](https://github.com/grpc/grpc-java/blob/master/documentation/server-reflection-tutorial.md)

```bash
➤ grpc_cli ls localhost:50051
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