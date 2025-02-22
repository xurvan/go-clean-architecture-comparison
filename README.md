# Go Clean Architecture Comparison

### [bxcodec/go-clean-arch](https://github.com/bxcodec/go-clean-arch/tree/v3) ![GitHub Repo stars](https://img.shields.io/github/stars/bxcodec/go-clean-arch?style=flat)

```
.
├── app                                 # Entry points and orchestration
│    └── main.go
├── [BOUNDED CONTEXT]
│    ├── delivery                       # Interface adapters
│    │   └── http
│    │       └── [ENTITY]_handler.go    # REST handlers implementation
│    ├── repository                     # Persistence Layer
│    │   └── mysql
│    │       └── [ENTITY]_mysql.go
│    └── usecase                        # Bussinse logic
│        └── [ENTITY]_usecase.go
└── domain                              # Enteties with repository and usecase interfaces
     ├── [ENTITY].go
     └── errors.go
```

### [evrone/go-clean-template](https://github.com/evrone/go-clean-template) ![GitHub Repo stars](https://img.shields.io/github/stars/evrone/go-clean-template?style=flat)

```
.
├── cmd                                 # Entry points
│    └── app
│        └── main.go
├── config                              # Represents external input into the system
│    └── config.go
└── internal
     ├── app                            # Orchestration
     │   └── app.go
     ├── controller                     # Interface adapters
     │   ├── amqp_rpc
     │   │   ├── router.go
     │   │   └── [ENTITY].go
     │   └── http
     │       ├── error.go
     │       ├── router.go
     │       └── [ENTITY].go            # REST handlers implementation
     ├── entity
     │   └── [ENTITY].go
     └── usecase
         ├── repo                       # Persistence Layer
         │   └── [ENTITY]_postgres.go
         ├── webapi                     # Persistence Layer
         │   └── [ENTITY]_google.go
         ├── interfaces.go              # Repository and usecase interfaces
         └── [ENTITY].go                # Bussinse logic
```

### [ThreeDotsLabs/wild-workouts-go-ddd-example](https://github.com/ThreeDotsLabs/wild-workouts-go-ddd-example) ![GitHub Repo stars](https://img.shields.io/github/stars/ThreeDotsLabs/wild-workouts-go-ddd-example?style=flat)

```
.
└── internal
     └── [BOUNDED CONTEXT]
         ├── adapters                               # Persistence Layer
         │   ├── [ENTITY]_firestore_repository.go
         │   ├── [ENTITY]_memory_repository.go
         │   ├── [ENTITY]_mysql_repository.go
         ├── app                                    # Bussinse logic
         │   ├── command
         │   │   ├── do_[ENTITY].go
         │   │   ├── action_on_[ENTITY].go
         │   ├── query
         │   │   ├── select_[ENTITY].go
         │   │   ├── search_[ENTITY].go
         │   │   └── types.go
         │   └── app.go
         ├── domain
         │   ├── [ENTITY].go
         │   └── repository.go                      # Repository interfaces
         ├── ports                                  # Interface adapters
         │   ├── grpc.go
         │   └── http.go                            # REST handlers implementation
         ├── service                                # Orchestration
         │   └── application.go
         └── main.go                                # Entry points
```
