# Go Clean Architecture Comparison

### [bxcodec/go-clean-arch](https://github.com/bxcodec/go-clean-arch/tree/v3) ![GitHub Repo stars](https://img.shields.io/github/stars/bxcodec/go-clean-arch?style=flat)

```
.
├── app                                 # Entry points, configurations and orchestration
│    └── main.go
├── [BOUNDED CONTEXT]
│    ├── delivery                       # Interface adapters with framework
│    │   └── http
│    │       └── [ENTITY]_handler.go    # REST handlers implementation
│    ├── repository                     # Infrastracture / Repository
│    │   └── mysql
│    │       └── [ENTITY]_mysql.go
│    └── usecase                        # Bussinse logic
│        └── [ENTITY]_usecase.go
└── domain                              # Entities and interfaces
     ├── [ENTITY].go
     └── errors.go
```

### [evrone/go-clean-template](https://github.com/evrone/go-clean-template) ![GitHub Repo stars](https://img.shields.io/github/stars/evrone/go-clean-template?style=flat)

```
.
├── cmd                                 # Entry points
│    └── app
│        └── main.go
├── config                              # Configurations
│    └── config.go
└── internal
     ├── app                            # Orchestration
     │   └── app.go
     ├── controller                     # Interface adapters with framework
     │   ├── amqp_rpc
     │   │   ├── router.go
     │   │   └── [ENTITY].go
     │   └── http
     │       ├── error.go
     │       ├── router.go
     │       └── [ENTITY].go            # REST handlers implementation
     ├── entity                         # Entities without interfaces
     │   └── [ENTITY].go
     └── usecase
         ├── repo                       # Infrastracture / Repository
         │   └── [ENTITY]_postgres.go
         ├── webapi                     # Infrastracture / External interface
         │   └── [ENTITY]_google.go
         ├── interfaces.go              # Repository and usecase interfaces
         └── [ENTITY].go                # Bussinse logic
```

### [ThreeDotsLabs/wild-workouts-go-ddd-example](https://github.com/ThreeDotsLabs/wild-workouts-go-ddd-example) ![GitHub Repo stars](https://img.shields.io/github/stars/ThreeDotsLabs/wild-workouts-go-ddd-example?style=flat)

```
.
└── internal
     └── [BOUNDED CONTEXT]
         ├── adapters                               # Infrastracture / Repository
         │   ├── [ENTITY]_firestore_repository.go
         │   ├── [ENTITY]_memory_repository.go
         │   └── [ENTITY]_mysql_repository.go
         ├── app                                    # Bussinse logic with CQS
         │   ├── command
         │   │   ├── [COMMAND]_[ENTITY].go
         │   ├── query
         │   │   ├── [QUERY]_[ENTITY].go
         │   │   └── types.go
         │   └── app.go
         ├── domain                                 # Entities and interfaces
         │   ├── [ENTITY].go
         │   └── repository.go                      # Repository interfaces
         ├── ports                                  # Interface adapters with framework
         │   ├── grpc.go
         │   └── http.go                            # REST handlers implementation
         ├── service                                # Orchestration and configurations
         │   └── application.go
         └── main.go                                # Entry point
```

### [amitshekhariitbhu/go-backend-clean-architecture](https://github.com/amitshekhariitbhu/go-backend-clean-architecture) ![GitHub Repo stars](https://img.shields.io/github/stars/amitshekhariitbhu/go-backend-clean-architecture?style=flat)

```
.
├── api                             # Interface adapter with framework
│    ├── controller
│    │   └── [ENTITY]_controller.go
│    │   └── [ACTION]_controller.go
│    └── route
│        └── [ENTITY]_route.go
│        └── [ACTION]_route.go
├── bootstrap                       # Orchestration and configurations
│    └── app.go
├── cmd                             # Entry points
│    └── main.go
├── domain                          # Entities and interfaces
│    ├── [ENTITY].go
│    └── [ACTION].go
├── repository                      # Infrastracture / Repository
│    └── [ENTITY]_repository.go
└── usecase                         # Bussinse logic
     ├── [ENTITY]_usecase.go
     └── [ACTION]_usecase.go
```

### [8treenet/freedom](https://github.com/8treenet/freedom) ![GitHub Repo stars](https://img.shields.io/github/stars/8treenet/freedom?style=flat)

```
.
└── [BOUNDED CONTEXT]
     ├── adapter
     │   ├── consumer
     │   │   └── consumer.go
     │   ├── controller                         
     │   │   └── [ENTITY].go
     │   └── repository                         # Infrastracture / Repository
     │       └── [ENTITY].go
     ├── domain                                 # Entities with more DDD concepts and interfaces
     │   ├── aggregate
     │   │   ├── [ENTITY]_[AGGREGATE].go
     │   ├── dependency
     │   │   └── dependency.go
     │   ├── entity
     │   │   └── [ENTITY].go
     │   ├── event
     │   │   └── [ENTITY]_[EVENT].go
     │   └── [SERVICE].go
     └── server
         ├── conf                               # Configurations
         │   └── config.go
         └── main.go                            # Entry point and orchestration
```

### [eminetto/clean-architecture-go-v2](https://github.com/eminetto/clean-architecture-go-v2) ![GitHub Repo stars](https://img.shields.io/github/stars/eminetto/clean-architecture-go-v2?style=flat)

```
.
├── api
│    ├── handler
│    │   └── [ENTITY].go
│    ├── presenter
│    │   └── [ENTITY].go
│    └── main.go
├── cmd                             # Entry point
│    └── main.go
├── config                          # Configurations
│    └── config.go
├── entity                          # Entities
│    └── [ENTITY].go
├── infrastructure
│    └── repository
│        └── [ENTITY]_mysql.go
└── usecase                         # Bussinse logic
     └── [ENTITY]
         ├── inmem.go
         ├── interface.go
         └── service.go
```


### [AleksK1NG/Go-Clean-Architecture-REST-API](https://github.com/AleksK1NG/Go-Clean-Architecture-REST-API) ![GitHub Repo stars](https://img.shields.io/github/stars/AleksK1NG/Go-Clean-Architecture-REST-API?style=flat)

```
.
├── cmd
│    └── api
│        └── main.go
├── config
│    └── config.go
└── internal
     ├── [BOUNDED CONTEXT]
     │   ├── delivery
     │   │   └── http
     │   │       ├── hanldlers.go
     │   │       └── routes.go
     │   ├── repository
     │   │   ├── pg_repository.go
     │   │   └── sql_queries.go
     │   ├── usecase
     │   │   ├── usecase.go
     │   ├── delivery.go
     │   ├── pg_repository.go
     │   └── usecase.go
     ├── models
     │   ├── [ENTITY].go
     └── server
         ├── handlers.go
         └── server.go
```
