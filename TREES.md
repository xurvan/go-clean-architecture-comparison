## Clean architecture sample repositories trees

### [bxcodec/go-clean-arch](https://github.com/bxcodec/go-clean-arch) ![GitHub Repo stars](https://img.shields.io/github/stars/bxcodec/go-clean-arch?style=flat)

```
.
├── app
│   └── main.go
├── article
│   ├── mocks
│   │   ├── ArticleRepository.go
│   │   └── AuthorRepository.go
│   ├── service.go
│   └── service_test.go
├── domain
│   ├── article.go
│   ├── author.go
│   └── errors.go
├── internal
│   ├── repository
│   │   ├── mysql
│   │   │   ├── article.go
│   │   │   ├── article_test.go
│   │   │   ├── author.go
│   │   │   └── author_test.go
│   │   └── helper.go
│   ├── rest
│   │   ├── middleware
│   │   │   ├── cors.go
│   │   │   ├── cors_test.go
│   │   │   └── timeout.go
│   │   ├── mocks
│   │   │   └── ArticleService.go
│   │   ├── article.go
│   │   └── article_test.go
│   ├── workers
│   │   └── README.md
│   └── README.md
├── misc
│   └── make
│       ├── help.Makefile
│       └── tools.Makefile
├── article.sql
├── clean-arch.png
├── compose.yaml
├── Dockerfile
├── example.env
├── go.mod
├── go.sum
├── LICENSE
├── Makefile
└── README.md
```

### [evrone/go-clean-template](https://github.com/evrone/go-clean-template) ![GitHub Repo stars](https://img.shields.io/github/stars/evrone/go-clean-template?style=flat)

```
.
├── cmd
│   └── app
│       └── main.go
├── config
│   ├── config.go
│   └── config.yml
├── docs
│   ├── img
│   │   ├── example-http-db.png
│   │   ├── layers-1.png
│   │   ├── layers-2.png
│   │   └── logo.svg
│   ├── docs.go
│   ├── swagger.json
│   └── swagger.yaml
├── integration-test
│   ├── Dockerfile
│   └── integration_test.go
├── internal
│   ├── app
│   │   ├── app.go
│   │   └── migrate.go
│   ├── controller
│   │   ├── amqp_rpc
│   │   │   ├── router.go
│   │   │   └── translation.go
│   │   └── http
│   │       └── v1
│   │           ├── error.go
│   │           ├── router.go
│   │           └── translation.go
│   ├── entity
│   │   └── translation.go
│   └── usecase
│       ├── repo
│       │   └── translation_postgres.go
│       ├── webapi
│       │   └── translation_google.go
│       ├── interfaces.go
│       ├── mocks_test.go
│       ├── translation.go
│       └── translation_test.go
├── migrations
│   ├── 20210221023242_migrate_name.down.sql
│   └── 20210221023242_migrate_name.up.sql
├── pkg
│   ├── httpserver
│   │   ├── options.go
│   │   └── server.go
│   ├── logger
│   │   └── logger.go
│   ├── postgres
│   │   ├── options.go
│   │   └── postgres.go
│   └── rabbitmq
│       └── rmq_rpc
│           ├── client
│           │   ├── client.go
│           │   └── options.go
│           ├── server
│           │   ├── options.go
│           │   └── server.go
│           ├── connection.go
│           └── errors.go
├── docker-compose.yml
├── Dockerfile
├── go.mod
├── go.sum
├── LICENSE
├── Makefile
├── README_CN.md
└── README.md
```

### [ThreeDotsLabs/wild-workouts-go-ddd-example](https://github.com/ThreeDotsLabs/wild-workouts-go-ddd-example) ![GitHub Repo stars](https://img.shields.io/github/stars/ThreeDotsLabs/wild-workouts-go-ddd-example?style=flat)

```
.
├── api
│   ├── openapi
│   │   ├── trainer.yml
│   │   ├── trainings.yml
│   │   └── users.yml
│   └── protobuf
│       ├── trainer.proto
│       └── users.proto
├── docker
│   ├── app
│   │   ├── Dockerfile
│   │   ├── reflex.conf
│   │   └── start.sh
│   ├── app-prod
│   │   └── Dockerfile
│   ├── firestore-emulator
│   │   ├── Dockerfile
│   │   ├── firebase.json
│   │   └── start.sh
│   └── web
│       ├── Dockerfile
│       └── start.sh
├── internal
│   ├── common
│   │   ├── auth
│   │   │   ├── http.go
│   │   │   └── http_mock.go
│   │   ├── client
│   │   │   ├── trainer
│   │   │   │   ├── openapi_client_gen.go
│   │   │   │   └── openapi_types.gen.go
│   │   │   ├── trainings
│   │   │   │   ├── openapi_client_gen.go
│   │   │   │   └── openapi_types.gen.go
│   │   │   ├── users
│   │   │   │   ├── openapi_client_gen.go
│   │   │   │   └── openapi_types.gen.go
│   │   │   ├── auth.go
│   │   │   ├── grpc.go
│   │   │   └── net.go
│   │   ├── decorator
│   │   │   ├── command.go
│   │   │   ├── logging.go
│   │   │   ├── metrics.go
│   │   │   └── query.go
│   │   ├── errors
│   │   │   └── errors.go
│   │   ├── genproto
│   │   │   ├── trainer
│   │   │   │   ├── trainer_grpc.pb.go
│   │   │   │   └── trainer.pb.go
│   │   │   └── users
│   │   │       ├── users_grpc.pb.go
│   │   │       └── users.pb.go
│   │   ├── logs
│   │   │   ├── cqrs.go
│   │   │   ├── http.go
│   │   │   └── logrus.go
│   │   ├── metrics
│   │   │   └── dummy.go
│   │   ├── server
│   │   │   ├── httperr
│   │   │   │   └── http_error.go
│   │   │   ├── grpc.go
│   │   │   └── http.go
│   │   ├── tests
│   │   │   ├── clients.go
│   │   │   ├── e2e_test.go
│   │   │   ├── hours.go
│   │   │   ├── jwt.go
│   │   │   └── wait.go
│   │   ├── go.mod
│   │   └── go.sum
│   ├── trainer
│   │   ├── adapters
│   │   │   ├── dates_firestore_repository.go
│   │   │   ├── hour_firestore_repository.go
│   │   │   ├── hour_memory_repository.go
│   │   │   ├── hour_mysql_repository.go
│   │   │   └── hour_repository_test.go
│   │   ├── app
│   │   │   ├── command
│   │   │   │   ├── cancel_training.go
│   │   │   │   ├── make_hours_available.go
│   │   │   │   ├── make_hours_unavailable.go
│   │   │   │   └── schedule_training.go
│   │   │   ├── query
│   │   │   │   ├── available_hours.go
│   │   │   │   ├── hour_availability.go
│   │   │   │   └── types.go
│   │   │   └── app.go
│   │   ├── domain
│   │   │   └── hour
│   │   │       ├── availability.go
│   │   │       ├── availability_test.go
│   │   │       ├── hour.go
│   │   │       ├── hour_test.go
│   │   │       └── repository.go
│   │   ├── ports
│   │   │   ├── grpc.go
│   │   │   ├── http.go
│   │   │   ├── openapi_api.gen.go
│   │   │   └── openapi_types.gen.go
│   │   ├── service
│   │   │   ├── application.go
│   │   │   └── component_test.go
│   │   ├── fixtures.go
│   │   ├── go.mod
│   │   ├── go.sum
│   │   └── main.go
│   ├── trainings
│   │   ├── adapters
│   │   │   ├── trainer_grpc.go
│   │   │   ├── trainings_firestore_repository.go
│   │   │   ├── trainings_firestore_repository_test.go
│   │   │   └── users_grpc.go
│   │   ├── app
│   │   │   ├── command
│   │   │   │   ├── approve_training_reschedule.go
│   │   │   │   ├── cancel_training.go
│   │   │   │   ├── cancel_training_test.go
│   │   │   │   ├── reject_training_reschedule.go
│   │   │   │   ├── request_training_reschedule.go
│   │   │   │   ├── reschedule_training.go
│   │   │   │   ├── schedule_training.go
│   │   │   │   └── services.go
│   │   │   ├── query
│   │   │   │   ├── all_trainings.go
│   │   │   │   ├── trainings_for_user.go
│   │   │   │   └── types.go
│   │   │   └── app.go
│   │   ├── domain
│   │   │   └── training
│   │   │       ├── cancel_balance.go
│   │   │       ├── cancel.go
│   │   │       ├── cancel_test.go
│   │   │       ├── repository.go
│   │   │       ├── reschedule.go
│   │   │       ├── reschedule_test.go
│   │   │       ├── training.go
│   │   │       ├── training_test.go
│   │   │       ├── user.go
│   │   │       └── user_test.go
│   │   ├── ports
│   │   │   ├── http.go
│   │   │   ├── openapi_api.gen.go
│   │   │   └── openapi_types.gen.go
│   │   ├── service
│   │   │   ├── component_test.go
│   │   │   ├── mocks.go
│   │   │   └── service.go
│   │   ├── go.mod
│   │   ├── go.sum
│   │   └── main.go
│   └── users
│       ├── firestore.go
│       ├── fixtures.go
│       ├── go.mod
│       ├── go.sum
│       ├── grpc.go
│       ├── http.go
│       ├── main.go
│       ├── openapi_api.gen.go
│       └── openapi_types.gen.go
├── scripts
│   ├── build-docker.sh
│   ├── deploy.sh
│   ├── lint.sh
│   ├── openapi-http.sh
│   ├── openapi-js.sh
│   ├── proto.sh
│   └── test.sh
├── sql
│   └── schema.sql
├── terraform
│   ├── service
│   │   ├── outputs.tf
│   │   ├── service.tf
│   │   └── vars.tf
│   ├── cloud-run.tf
│   ├── docker-images.tf
│   ├── firebase.tf
│   ├── firestore.tf
│   ├── iam.tf
│   ├── Makefile
│   ├── outputs.tf
│   ├── project.tf
│   ├── README.md
│   ├── repo.tf
│   ├── set-envs.sh
│   └── vars.tf
├── tools
│   └── c4
│       ├── out
│       │   ├── view-trainer.plantuml
│       │   ├── view-trainer.png
│       │   ├── view-trainings.plantuml
│       │   └── view-trainings.png
│       ├── generate.sh
│       ├── go.mod
│       ├── go.sum
│       ├── main.go
│       ├── scraper.yml
│       └── view.yml
├── web
│   ├── public
│   │   ├── __
│   │   │   └── firebase
│   │   │       └── init.json
│   │   ├── favicon.ico
│   │   └── index.html
│   ├── src
│   │   ├── assets
│   │   │   └── main.css
│   │   ├── components
│   │   │   ├── WebFooter.vue
│   │   │   └── WebMenu.vue
│   │   ├── layouts
│   │   │   ├── App.vue
│   │   │   └── Login.vue
│   │   ├── pages
│   │   │   ├── Calendar.vue
│   │   │   ├── Login.vue
│   │   │   ├── ScheduleTraining.vue
│   │   │   ├── SetSchedule.vue
│   │   │   └── TrainingsList.vue
│   │   ├── repositories
│   │   │   ├── clients
│   │   │   │   ├── trainer
│   │   │   │   │   └── src
│   │   │   │   │       ├── api
│   │   │   │   │       │   └── DefaultApi.js
│   │   │   │   │       ├── model
│   │   │   │   │       │   ├── DateHours.js
│   │   │   │   │       │   ├── Error.js
│   │   │   │   │       │   ├── Hour.js
│   │   │   │   │       │   ├── HourUpdate.js
│   │   │   │   │       │   └── ModelDate.js
│   │   │   │   │       ├── ApiClient.js
│   │   │   │   │       └── index.js
│   │   │   │   ├── trainings
│   │   │   │   │   └── src
│   │   │   │   │       ├── api
│   │   │   │   │       │   └── DefaultApi.js
│   │   │   │   │       ├── model
│   │   │   │   │       │   ├── Error.js
│   │   │   │   │       │   ├── PostTraining.js
│   │   │   │   │       │   ├── Training.js
│   │   │   │   │       │   ├── Trainings.js
│   │   │   │   │       │   └── TrainingTime.js
│   │   │   │   │       ├── ApiClient.js
│   │   │   │   │       └── index.js
│   │   │   │   └── users
│   │   │   │       └── src
│   │   │   │           ├── api
│   │   │   │           │   └── DefaultApi.js
│   │   │   │           ├── model
│   │   │   │           │   ├── Error.js
│   │   │   │           │   ├── User.js
│   │   │   │           │   └── UserSignIn.js
│   │   │   │           ├── ApiClient.js
│   │   │   │           └── index.js
│   │   │   ├── auth.js
│   │   │   ├── trainings.js
│   │   │   └── user.js
│   │   ├── date.js
│   │   ├── firebase.js
│   │   └── main.js
│   ├── babel.config.js
│   ├── firebase.json
│   ├── package.json
│   ├── package-lock.json
│   ├── vue.config.js
│   ├── webpack.config.js
│   └── yarn.lock
├── cloudbuild.yaml
├── docker-compose.ci.yml
├── docker-compose.yml
├── LICENSE
├── Makefile
└── README.md
```

### [amitshekhariitbhu/go-backend-clean-architecture](https://github.com/amitshekhariitbhu/go-backend-clean-architecture) ![GitHub Repo stars](https://img.shields.io/github/stars/amitshekhariitbhu/go-backend-clean-architecture?style=flat)

```
.
├── api
│   ├── controller
│   │   ├── login_controller.go
│   │   ├── profile_controller.go
│   │   ├── profile_controller_test.go
│   │   ├── refresh_token_controller.go
│   │   ├── signup_controller.go
│   │   └── task_controller.go
│   ├── middleware
│   │   └── jwt_auth_middleware.go
│   └── route
│       ├── login_route.go
│       ├── profile_route.go
│       ├── refresh_token_route.go
│       ├── route.go
│       ├── signup_route.go
│       └── task_route.go
├── assets
│   ├── button-view-api-docs.png
│   ├── go-arch-private-api-request-flow.png
│   ├── go-arch-public-api-request-flow.png
│   ├── go-backend-arch-diagram.png
│   └── go-backend-clean-architecture.png
├── bootstrap
│   ├── app.go
│   ├── database.go
│   └── env.go
├── cmd
│   └── main.go
├── domain
│   ├── mocks
│   │   ├── LoginUsecase.go
│   │   ├── ProfileUsecase.go
│   │   ├── RefreshTokenUsecase.go
│   │   ├── SignupUsecase.go
│   │   ├── TaskRepository.go
│   │   ├── TaskUsecase.go
│   │   └── UserRepository.go
│   ├── error_response.go
│   ├── jwt_custom.go
│   ├── login.go
│   ├── profile.go
│   ├── refresh_token.go
│   ├── signup.go
│   ├── success_response.go
│   ├── task.go
│   └── user.go
├── internal
│   ├── fakeutil
│   │   └── fakeutil.go
│   └── tokenutil
│       └── tokenutil.go
├── mongo
│   ├── mocks
│   │   ├── Client.go
│   │   ├── Collection.go
│   │   ├── Cursor.go
│   │   ├── Database.go
│   │   └── SingleResult.go
│   └── mongo.go
├── repository
│   ├── task_repository.go
│   ├── user_repository.go
│   └── user_repository_test.go
├── usecase
│   ├── login_usecase.go
│   ├── profile_usecase.go
│   ├── refresh_token_usecase.go
│   ├── signup_usecase.go
│   ├── task_usecase.go
│   └── task_usecase_test.go
├── docker-compose.yaml
├── Dockerfile
├── go.mod
├── go.sum
├── LICENSE
└── README.md
```

### [8treenet/freedom](https://github.com/8treenet/freedom) ![GitHub Repo stars](https://img.shields.io/github/stars/8treenet/freedom?style=flat)

```
.
├── doc
│   ├── ddd-guide.md
│   ├── http-client-guide.md
│   ├── po-guide.md
│   ├── route-guide.md
│   ├── service-guide.md
│   └── worker-guide.md
├── example
│   ├── base
│   │   ├── adapter
│   │   │   ├── controller
│   │   │   │   ├── default.go
│   │   │   │   └── defaultV2.go
│   │   │   └── repository
│   │   │       ├── default.go
│   │   │       └── interface.go
│   │   ├── domain
│   │   │   ├── po
│   │   │   │   └── po.go
│   │   │   ├── vo
│   │   │   │   └── vo.go
│   │   │   ├── default.go
│   │   │   └── defaultV2.go
│   │   ├── infra
│   │   │   ├── request.go
│   │   │   └── response.go
│   │   ├── server
│   │   │   ├── conf
│   │   │   │   ├── config.go
│   │   │   │   ├── config.toml
│   │   │   │   └── config.yaml
│   │   │   └── main.go
│   │   └── README.md
│   ├── fshop
│   │   ├── adapter
│   │   │   ├── consumer
│   │   │   │   └── consumer.go
│   │   │   ├── controller
│   │   │   │   ├── cart.go
│   │   │   │   ├── delivery.go
│   │   │   │   ├── goods.go
│   │   │   │   ├── order.go
│   │   │   │   └── user.go
│   │   │   └── repository
│   │   │       ├── admin.go
│   │   │       ├── cart.go
│   │   │       ├── delivery.go
│   │   │       ├── generate.go
│   │   │       ├── goods.go
│   │   │       ├── goods_test.go
│   │   │       ├── order.go
│   │   │       └── user.go
│   │   ├── api_test
│   │   │   ├── cart_test.go
│   │   │   ├── delivery_test.go
│   │   │   ├── goods_test.go
│   │   │   ├── order_test.go
│   │   │   └── user_test.go
│   │   ├── domain
│   │   │   ├── aggregate
│   │   │   │   ├── cart_add_cmd.go
│   │   │   │   ├── cart_factory.go
│   │   │   │   ├── cart_item_query.go
│   │   │   │   ├── cart_shop_cmd.go
│   │   │   │   ├── factory_test.go
│   │   │   │   ├── goods_shop_cmd.go
│   │   │   │   ├── interface.go
│   │   │   │   ├── order_delivery_cmd.go
│   │   │   │   ├── order_factory.go
│   │   │   │   ├── order_pay_cmd.go
│   │   │   │   └── shop_factory.go
│   │   │   ├── dependency
│   │   │   │   └── dependency.go
│   │   │   ├── entity
│   │   │   │   ├── admin.go
│   │   │   │   ├── cart.go
│   │   │   │   ├── delivery.go
│   │   │   │   ├── goods.go
│   │   │   │   ├── order.go
│   │   │   │   └── user.go
│   │   │   ├── event
│   │   │   │   ├── change_password.go
│   │   │   │   └── shop_goods.go
│   │   │   ├── po
│   │   │   │   ├── admin.go
│   │   │   │   ├── cart.go
│   │   │   │   ├── delivery.go
│   │   │   │   ├── goods.go
│   │   │   │   ├── order_detail.go
│   │   │   │   ├── order.go
│   │   │   │   ├── po.go
│   │   │   │   └── user.go
│   │   │   ├── vo
│   │   │   │   ├── req.go
│   │   │   │   └── vo.go
│   │   │   ├── cart.go
│   │   │   ├── goods.go
│   │   │   ├── goods_test.go
│   │   │   ├── order.go
│   │   │   └── user.go
│   │   ├── infra
│   │   │   ├── domainevent
│   │   │   │   ├── event_manager.go
│   │   │   │   ├── event_pub.go
│   │   │   │   ├── event_retry.go
│   │   │   │   ├── event_sub.go
│   │   │   │   └── event_transaction.go
│   │   │   ├── request.go
│   │   │   └── response.go
│   │   ├── server
│   │   │   ├── conf
│   │   │   │   ├── config.go
│   │   │   │   ├── config.toml
│   │   │   │   └── config.yaml
│   │   │   └── main.go
│   │   ├── Dockerfile
│   │   ├── fshop.sql
│   │   ├── go.mod.example
│   │   └── README.md
│   ├── http2
│   │   ├── adapter
│   │   │   ├── controller
│   │   │   │   ├── goods.go
│   │   │   │   └── shop.go
│   │   │   └── repository
│   │   │       ├── goods.go
│   │   │       └── interface.go
│   │   ├── domain
│   │   │   ├── po
│   │   │   │   └── po.go
│   │   │   ├── vo
│   │   │   │   └── goods.go
│   │   │   └── shop.go
│   │   ├── server
│   │   │   ├── conf
│   │   │   │   ├── config.go
│   │   │   │   ├── config.toml
│   │   │   │   └── config.yaml
│   │   │   └── main.go
│   │   └── README.md
│   └── infra-example
│       ├── adapter
│       │   ├── controller
│       │   │   ├── goods.go
│       │   │   ├── order.go
│       │   │   └── shop.go
│       │   └── repository
│       │       ├── generate.go
│       │       ├── goods.go
│       │       ├── goods_test.go
│       │       └── order.go
│       ├── api_test
│       │   └── api_test.go
│       ├── common
│       │   └── errors.go
│       ├── domain
│       │   ├── entity
│       │   │   ├── goods.go
│       │   │   └── order.go
│       │   ├── event
│       │   │   └── shop_goods.go
│       │   ├── po
│       │   │   ├── goods.go
│       │   │   └── order.go
│       │   ├── vo
│       │   │   └── dto.go
│       │   ├── goods.go
│       │   └── order.go
│       ├── infra
│       │   ├── demo
│       │   │   └── single.go
│       │   ├── domainevent
│       │   │   ├── event_manager.go
│       │   │   ├── event_pub.go
│       │   │   ├── event_retry.go
│       │   │   ├── event_sub.go
│       │   │   ├── event_test.go
│       │   │   └── event_transaction.go
│       │   ├── request.go
│       │   └── response.go
│       ├── server
│       │   ├── conf
│       │   │   ├── config.go
│       │   │   ├── config.toml
│       │   │   └── config.yaml
│       │   └── main.go
│       ├── freedom.sql
│       └── README.md
├── freedom
│   ├── cmd
│   │   ├── new_po.go
│   │   ├── new_project.go
│   │   ├── root.go
│   │   └── version.go
│   ├── template
│   │   ├── crud
│   │   │   ├── generate.go
│   │   │   ├── generate_test.go
│   │   │   └── template.go
│   │   └── project
│   │       ├── config.go
│   │       ├── controllers.go
│   │       ├── gomod.go
│   │       ├── infra.go
│   │       ├── object.go
│   │       ├── project.go
│   │       ├── repositorys.go
│   │       ├── server.go
│   │       ├── services.go
│   │       └── vo.go
│   └── main.go
├── infra
│   ├── kafka
│   │   ├── consumer.go
│   │   ├── middleware.go
│   │   ├── middleware_test.go
│   │   ├── msg.go
│   │   └── producer.go
│   ├── requests
│   │   ├── client.go
│   │   ├── http_request.go
│   │   ├── http_response.go
│   │   ├── http_trace.go
│   │   ├── middlewares.go
│   │   ├── request.go
│   │   └── request_test.go
│   ├── store
│   │   └── entity_cache.go
│   └── transaction
│       ├── transaction.go
│       └── xa.go
├── internal
│   ├── app.go
│   ├── bus.go
│   ├── core.go
│   ├── custom.go
│   ├── entity.go
│   ├── event_path_manager.go
│   ├── factory_pool.go
│   ├── freedom_test.go
│   ├── infra.go
│   ├── infra_pool.go
│   ├── init.go
│   ├── iris.go
│   ├── logger.go
│   ├── prometheus.go
│   ├── repo_pool.go
│   ├── repository.go
│   ├── service_locator.go
│   ├── service_pool.go
│   ├── store.go
│   ├── unit.go
│   ├── util.go
│   └── worker.go
├── middleware
│   ├── bus.go
│   ├── client_prometheus.go
│   ├── logger_config.go
│   ├── logger.go
│   ├── logger_handle.go
│   ├── recover.go
│   ├── request_logger.go
│   └── trace.go
├── app.go
├── freedom.go
├── go.mod
├── go.sum
├── LICENSE
├── profile.go
└── README.md
```

### [eminetto/clean-architecture-go-v2](https://github.com/eminetto/clean-architecture-go-v2) ![GitHub Repo stars](https://img.shields.io/github/stars/eminetto/clean-architecture-go-v2?style=flat)

```
.
├── api
│   ├── handler
│   │   ├── book.go
│   │   ├── book_test.go
│   │   ├── loan.go
│   │   ├── loan_test.go
│   │   ├── user.go
│   │   └── user_test.go
│   ├── middleware
│   │   ├── cors.go
│   │   └── metrics.go
│   ├── presenter
│   │   ├── book.go
│   │   └── user.go
│   └── main.go
├── cmd
│   ├── main.go
│   └── main_test.go
├── config
│   ├── config_dev.go
│   ├── config_prod.go
│   ├── config_staging.go
│   └── config_testing.go
├── entity
│   ├── book.go
│   ├── book_test.go
│   ├── entity.go
│   ├── error.go
│   ├── user.go
│   └── user_test.go
├── infrastructure
│   └── repository
│       ├── book_mysql.go
│       └── user_mysql.go
├── ops
│   ├── db
│   │   └── init.sql
│   └── prometheus
│       └── prometheus.yml
├── pkg
│   ├── metric
│   │   ├── interface.go
│   │   └── prometheus.go
│   └── password
│       ├── fake.go
│       ├── interface.go
│       └── password.go
├── usecase
│   ├── book
│   │   ├── mock
│   │   │   └── book.go
│   │   ├── inmem.go
│   │   ├── interface.go
│   │   ├── service.go
│   │   └── service_test.go
│   ├── loan
│   │   ├── mock
│   │   │   └── loan.go
│   │   ├── interface.go
│   │   ├── service.go
│   │   └── service_test.go
│   └── user
│       ├── mock
│       │   └── user.go
│       ├── inmem.go
│       ├── interface.go
│       ├── service.go
│       └── service_test.go
├── docker-compose.yml
├── go.mod
├── go.sum
├── Makefile
└── README.md
```

### [AleksK1NG/Go-Clean-Architecture-REST-API](https://github.com/AleksK1NG/Go-Clean-Architecture-REST-API) ![GitHub Repo stars](https://img.shields.io/github/stars/AleksK1NG/Go-Clean-Architecture-REST-API?style=flat)

```
.
├── cmd
│   └── api
│       └── main.go
├── config
│   ├── config-docker.yml
│   ├── config.go
│   └── config-local.yml
├── docker
│   ├── monitoring
│   │   ├── alerts.yml
│   │   ├── prometheus-local.yml
│   │   └── prometheus.yml
│   ├── Dockerfile
│   ├── Dockerfile.DelveHotReload
│   └── Dockerfile.HotReload
├── docs
│   ├── docs.go
│   ├── swagger.json
│   └── swagger.yaml
├── internal
│   ├── auth
│   │   ├── delivery
│   │   │   └── http
│   │   │       ├── handlers.go
│   │   │       ├── handlers_test.go
│   │   │       └── routes.go
│   │   ├── mock
│   │   │   ├── aws_repository_mock.go
│   │   │   ├── pg_repository_mock.go
│   │   │   ├── redis_repository_mock.go
│   │   │   └── usecase_mock.go
│   │   ├── repository
│   │   │   ├── aws_repository.go
│   │   │   ├── pg_repository.go
│   │   │   ├── pg_repository_test.go
│   │   │   ├── redis_repository.go
│   │   │   ├── redis_repository_test.go
│   │   │   └── sql_queries.go
│   │   ├── usecase
│   │   │   ├── usecase.go
│   │   │   └── usecase_test.go
│   │   ├── aws_repository.go
│   │   ├── delivery.go
│   │   ├── pg_repository.go
│   │   ├── redis_repository.go
│   │   └── usecase.go
│   ├── comments
│   │   ├── delivery
│   │   │   └── http
│   │   │       ├── handlers_test.go
│   │   │       ├── hanldlers.go
│   │   │       └── routes.go
│   │   ├── mock
│   │   │   ├── pg_repository_mock.go
│   │   │   └── usecase_mock.go
│   │   ├── repository
│   │   │   ├── pg_repository.go
│   │   │   ├── pg_repository_test.go
│   │   │   └── sql_queries.go
│   │   ├── usecase
│   │   │   ├── usecase.go
│   │   │   └── usecase_test.go
│   │   ├── delivery.go
│   │   ├── pg_repository.go
│   │   └── usecase.go
│   ├── middleware
│   │   ├── auth.go
│   │   ├── csrf.go
│   │   ├── debug.go
│   │   ├── metrics.go
│   │   ├── middlewares.go
│   │   ├── request_logger.go
│   │   └── sanitize.go
│   ├── models
│   │   ├── aws.go
│   │   ├── comment.go
│   │   ├── news.go
│   │   ├── session.go
│   │   └── user.go
│   ├── news
│   │   ├── delivery
│   │   │   └── http
│   │   │       ├── handlers.go
│   │   │       ├── handlers_test.go
│   │   │       └── routes.go
│   │   ├── mock
│   │   │   ├── pg_repository_mock.go
│   │   │   ├── redis_repository_mock.go
│   │   │   └── usecase_mock.go
│   │   ├── repository
│   │   │   ├── pg_repository.go
│   │   │   ├── pg_repository_test.go
│   │   │   ├── redis_repository.go
│   │   │   ├── redis_repository_test.go
│   │   │   └── sql_queries.go
│   │   ├── usecase
│   │   │   ├── usecase.go
│   │   │   └── usecase_test.go
│   │   ├── delivery.go
│   │   ├── pg_repository.go
│   │   ├── redis_repository.go
│   │   └── usecase.go
│   ├── server
│   │   ├── handlers.go
│   │   └── server.go
│   └── session
│       ├── mock
│       │   ├── redis_repository_mock.go
│       │   └── usecase_mock.go
│       ├── repository
│       │   ├── redis_repository.go
│       │   └── redis_repository_test.go
│       ├── usecase
│       │   ├── usecase.go
│       │   └── usecase_test.go
│       ├── redis_repository.go
│       └── usecase.go
├── migrations
│   ├── 01_create_initial_tables.down.sql
│   └── 01_create_initial_tables.up.sql
├── pkg
│   ├── converter
│   │   └── converter.go
│   ├── csrf
│   │   └── csrf.go
│   ├── db
│   │   ├── aws
│   │   │   └── aws.go
│   │   ├── postgres
│   │   │   └── db_conn.go
│   │   └── redis
│   │       └── conn.go
│   ├── httpErrors
│   │   └── http_errors.go
│   ├── logger
│   │   └── zap_logger.go
│   ├── metric
│   │   └── metric.go
│   ├── sanitize
│   │   └── sanitize.go
│   └── utils
│       ├── auth.go
│       ├── http.go
│       ├── images.go
│       ├── jwt.go
│       ├── pagination.go
│       └── validator.go
├── ssl
│   ├── ca.crt
│   ├── ca.key
│   ├── instructions.sh
│   ├── server.crt
│   ├── server.csr
│   ├── server.key
│   └── server.pem
├── docker-compose.delve.yml
├── docker-compose.dev.yml
├── docker-compose.local.yml
├── go.mod
├── go.sum
├── Makefile
└── README.md
```

### [percybolmer/ddd-go](https://github.com/percybolmer/ddd-go/tree/clean-architecture) ![GitHub Repo stars](https://img.shields.io/github/stars/percybolmer/ddd-go?style=flat)

```
.
├── cmd
│   └── main.go
├── domain
│   ├── banking
│   │   └── readme.MD
│   ├── customer
│   │   ├── memory
│   │   │   ├── memory.go
│   │   │   └── memory_test.go
│   │   ├── mongo
│   │   │   └── mongo.go
│   │   ├── customer.go
│   │   ├── customer_test.go
│   │   └── repository.go
│   └── product
│       ├── memory
│       │   ├── memory.go
│       │   └── memory_test.go
│       ├── product.go
│       ├── product_test.go
│       └── repository.go
├── services
│   ├── order
│   │   ├── order.go
│   │   └── order_test.go
│   └── tavern
│       ├── tavern.go
│       └── tavern_test.go
├── go.mod
├── go.sum
├── item.go
├── person.go
├── readme.MD
└── transaction.go
```

### [jfeng45/servicetmpl](https://github.com/jfeng45/servicetmpl) ![GitHub Repo stars](https://img.shields.io/github/stars/jfeng45/servicetmpl?style=flat)

```
.
├── adapter
│   ├── cacheclient
│   │   ├── generatedclient
│   │   │   ├── cacheJin.pb.go
│   │   │   └── doc.go
│   │   └── cacheClient.go
│   ├── paymentclient
│   │   └── paymentClient.go
│   ├── userclient
│   │   ├── generatedclient
│   │   │   ├── usergrpc.pb.go
│   │   │   └── usergrpc.proto
│   │   └── userGrpc.go
│   └── doc.go
├── cmd
│   ├── grpcclient
│   │   └── grpcClientMain.go
│   ├── grpcserver
│   │   └── grpcServerMain.go
│   └── main.go
├── config
│   ├── appConfigDev.yaml
│   ├── appConfig.go
│   ├── appConfigProd.yaml
│   └── configValidator.go
├── container
│   ├── dataservicefactory
│   │   ├── userdataservicefactory
│   │   │   ├── couchdbUserDataServiceFactory.go
│   │   │   ├── sqlUserDataServiceFactory.go
│   │   │   └── userDataServiceFactory.go
│   │   ├── cacheDataServiceFacory.go
│   │   ├── courseDataServiceFactory.go
│   │   ├── dataServiceFactory.go
│   │   ├── txDataServiceFactory.go
│   │   └── userDataServiceFactoryWrapper.go
│   ├── datastorefactory
│   │   ├── cacheGrpcFactory.go
│   │   ├── couchdbFactory.go
│   │   ├── datastoreFactory.go
│   │   └── sqlFactory.go
│   ├── logger
│   │   └── logger.go
│   ├── loggerfactory
│   │   ├── logrus
│   │   │   └── logrus.go
│   │   ├── zap
│   │   │   └── zap.go
│   │   ├── logFactory.go
│   │   ├── logrusFactory.go
│   │   └── zapFactory.go
│   ├── servicecontainer
│   │   └── serviceContainer.go
│   ├── usecasefactory
│   │   ├── listCourseFactory.go
│   │   ├── listUserFactory.go
│   │   ├── registrationFactory.go
│   │   ├── useCaseFactory.go
│   │   └── useCaseHelper.go
│   └── container.go
├── dataservice
│   ├── coursedata
│   │   ├── couchdb
│   │   │   └── courseDataCouchdb.go
│   │   └── sqldb
│   │       └── courseDataSql.go
│   ├── txdataservice
│   │   └── txDataServie.go
│   ├── userdata
│   │   ├── couchdb
│   │   │   └── userDataCouchdb.go
│   │   └── sqldb
│   │       └── userDataSql.go
│   └── dataService.go
├── model
│   ├── cache.go
│   ├── course.go
│   └── user.go
├── script
│   └── user.sql
├── tool
│   ├── gdbc
│   │   ├── databasehandler
│   │   │   ├── noSqlGdbc.go
│   │   │   ├── sqlGdbc.go
│   │   │   └── transaction.go
│   │   └── gdbc.go
│   ├── doc.go
│   └── timea.go
├── usecase
│   ├── listcourse
│   │   └── listCourse.go
│   ├── listuser
│   │   └── listUser.go
│   ├── registration
│   │   ├── registrationHelper.go
│   │   └── registraton.go
│   └── useCase.go
├── go.mod
├── go.sum
├── LICENSE.txt
├── README.md
└── README.zh.md
```

### [dipeshdulal/clean-gin](https://github.com/dipeshdulal/clean-gin) ![GitHub Repo stars](https://img.shields.io/github/stars/dipeshdulal/clean-gin?style=flat)

```
.
├── api
│   ├── controllers
│   │   ├── controllers.go
│   │   ├── jwt_auth_controller.go
│   │   └── user_controller.go
│   ├── middlewares
│   │   ├── cors.go
│   │   ├── db_trx.go
│   │   ├── jwt_auth.go
│   │   └── middlewares.go
│   └── routes
│       ├── auth.go
│       ├── routes.go
│       └── user.go
├── bootstrap
│   ├── app.go
│   └── modules.go
├── commands
│   ├── commands.go
│   └── serve.go
├── constants
│   └── context.go
├── docker
│   ├── custom.cnf
│   ├── db.Dockerfile
│   ├── run.sh
│   └── web.Dockerfile
├── domains
│   ├── auth.go
│   └── user.go
├── lib
│   ├── command.go
│   ├── db.go
│   ├── env.go
│   ├── lib.go
│   ├── logger.go
│   └── request_handler.go
├── migration
│   └── 20220410063647-create_users_table.sql
├── models
│   └── user.go
├── repository
│   ├── repository.go
│   └── user_repository.go
├── services
│   ├── jwt_auth_service.go
│   ├── services.go
│   └── user_service.go
├── dbconfig.yml
├── docker-compose.yml
├── go.mod
├── go.sum
├── LICENSE
├── logo.svg
├── Makefile
├── README.md
└── server.go
```

### [eyazici90/go-ddd](https://github.com/eyazici90/go-ddd) ![GitHub Repo stars](https://img.shields.io/github/stars/eyazici90/go-ddd?style=flat)

```
.
├── cmd
│   └── go-ddd
│       ├── config.json
│       └── main.go
├── docker
│   ├── docker-compose.yaml
│   └── Dockerfile
├── docs
│   ├── docs.go
│   ├── swagger.json
│   └── swagger.yaml
├── helm
│   └── go-ddd
│       ├── templates
│       │   ├── deployment.yaml
│       │   ├── pdb.yaml
│       │   ├── serviceaccount.yaml
│       │   └── service.yaml
│       ├── Chart.yaml
│       └── values.yaml
├── internal
│   ├── app
│   │   ├── behavior
│   │   │   ├── cancel.go
│   │   │   ├── log.go
│   │   │   ├── retry.go
│   │   │   ├── retry_test.go
│   │   │   ├── trace.go
│   │   │   ├── validate.go
│   │   │   └── validate_test.go
│   │   ├── command
│   │   │   ├── cancel_order.go
│   │   │   ├── command.go
│   │   │   ├── command_test.go
│   │   │   ├── create_order.go
│   │   │   ├── errors.go
│   │   │   ├── pay_order.go
│   │   │   └── ship_order.go
│   │   ├── event
│   │   │   └── event.go
│   │   ├── query
│   │   │   ├── dto.go
│   │   │   ├── map.go
│   │   │   └── service.go
│   │   └── mediator.go
│   ├── domain
│   │   ├── customer.go
│   │   ├── errors.go
│   │   ├── events.go
│   │   ├── order.go
│   │   ├── order_test.go
│   │   └── product.go
│   ├── http
│   │   ├── commands.go
│   │   ├── middlewares.go
│   │   ├── queries.go
│   │   ├── routes.go
│   │   ├── server.go
│   │   └── util.go
│   └── infra
│       ├── inmem
│       │   └── order_store.go
│       ├── mongo
│       │   ├── order_store.go
│       │   └── store.go
│       └── event_bus.go
├── pkg
│   ├── aggregate
│   │   ├── error.go
│   │   └── root.go
│   ├── httperr
│   │   └── http_error.go
│   ├── must
│   │   └── not_fail.go
│   ├── otel
│   │   └── trace.go
│   └── shutdown
│       └── graceful.go
├── go.mod
├── go.sum
├── LICENSE
├── Makefile
└── README.md
```

### [ThreeDotsLabs/monolith-microservice-shop](https://github.com/ThreeDotsLabs/monolith-microservice-shop) ![GitHub Repo stars](https://img.shields.io/github/stars/ThreeDotsLabs/monolith-microservice-shop?style=flat)

```
.
├── cmd
│   ├── microservices
│   │   ├── orders
│   │   │   └── main.go
│   │   ├── payments
│   │   │   └── main.go
│   │   └── shop
│   │       └── main.go
│   └── monolith
│       └── main.go
├── docker
│   └── entrypoint.sh
├── pkg
│   ├── common
│   │   ├── cmd
│   │   │   ├── router.go
│   │   │   ├── signals.go
│   │   │   └── wait.go
│   │   ├── http
│   │   │   └── error.go
│   │   └── price
│   │       ├── price.go
│   │       └── price_test.go
│   ├── orders
│   │   ├── application
│   │   │   └── orders.go
│   │   ├── domain
│   │   │   └── orders
│   │   │       ├── address.go
│   │   │       ├── address_test.go
│   │   │       ├── order.go
│   │   │       ├── order_test.go
│   │   │       ├── product.go
│   │   │       └── repository.go
│   │   ├── infrastructure
│   │   │   ├── orders
│   │   │   │   ├── memory.go
│   │   │   │   └── memory_test.go
│   │   │   ├── payments
│   │   │   │   ├── amqp.go
│   │   │   │   └── intraprocess.go
│   │   │   └── shop
│   │   │       ├── http.go
│   │   │       ├── intraprocess.go
│   │   │       └── intraprocess_test.go
│   │   └── interfaces
│   │       ├── private
│   │       │   ├── http
│   │       │   │   └── orders.go
│   │       │   └── intraprocess
│   │       │       └── payments.go
│   │       └── public
│   │           └── http
│   │               └── orders.go
│   ├── payments
│   │   ├── application
│   │   │   └── payments.go
│   │   ├── infrastructure
│   │   │   └── orders
│   │   │       ├── http.go
│   │   │       └── intraprocess.go
│   │   └── interfaces
│   │       ├── amqp
│   │       │   └── orders.go
│   │       └── intraprocess
│   │           └── orders.go
│   └── shop
│       ├── application
│       │   └── products.go
│       ├── domain
│       │   └── products
│       │       ├── products.go
│       │       ├── products_test.go
│       │       └── repository.go
│       ├── infrastructure
│       │   └── products
│       │       ├── memory.go
│       │       └── memory_test.go
│       ├── interfaces
│       │   ├── private
│       │   │   ├── http
│       │   │   │   └── products.go
│       │   │   └── intraprocess
│       │   │       ├── products.go
│       │   │       └── products_test.go
│       │   └── public
│       │       └── http
│       │           └── products.go
│       └── fixtures.go
├── tests
│   └── acceptance_test.go
├── docker-compose.yml
├── Dockerfile
├── go.mod
├── go.sum
├── Makefile
└── README.md
```

### [ruslantsyganok/clean_arcitecture_golang_example](https://github.com/ruslantsyganok/clean_arcitecture_golang_example) ![GitHub Repo stars](https://img.shields.io/github/stars/ruslantsyganok/clean_arcitecture_golang_example?style=flat)

```
.
├── api
│   ├── google
│   │   └── api
│   │       ├── annotations.proto
│   │       └── http.proto
│   ├── validate
│   │   └── validate.proto
│   ├── buf.gen.yaml
│   └── microservice.proto
├── cmd
│   └── main.go
├── internal
│   ├── app
│   │   ├── create_answer.go
│   │   ├── create_course.go
│   │   ├── create_indicator.go
│   │   ├── create_question.go
│   │   ├── create_section.go
│   │   ├── delete_answer.go
│   │   ├── delete_course.go
│   │   ├── delete_file.go
│   │   ├── delete_indicator.go
│   │   ├── delete_question.go
│   │   ├── delete_review.go
│   │   ├── delete_section.go
│   │   ├── delete_user.go
│   │   ├── email_verification_check_code.go
│   │   ├── email_verification.go
│   │   ├── get_answers.go
│   │   ├── get_course.go
│   │   ├── get_indicators.go
│   │   ├── get_poll.go
│   │   ├── get_questions.go
│   │   ├── get_reviews.go
│   │   ├── get_score.go
│   │   ├── get_sections.go
│   │   ├── get_user.go
│   │   ├── logout.go
│   │   ├── middleware.go
│   │   ├── new_payment.go
│   │   ├── service.go
│   │   ├── signin.go
│   │   ├── signup.go
│   │   ├── update_answer.go
│   │   ├── update_course.go
│   │   ├── update_indicator.go
│   │   ├── update_question.go
│   │   ├── update_section.go
│   │   ├── update_user.go
│   │   ├── upload_file.go
│   │   ├── upsert_review.go
│   │   └── upsert_score.go
│   ├── datastruct
│   │   ├── answer.go
│   │   ├── course.go
│   │   ├── course_section.go
│   │   ├── indicator.go
│   │   ├── payment.go
│   │   ├── person.go
│   │   ├── question.go
│   │   ├── review.go
│   │   ├── score.go
│   │   └── transaction.go
│   ├── dto
│   │   ├── answer.go
│   │   ├── course.go
│   │   ├── indicator_score.go
│   │   ├── person.go
│   │   ├── poll.go
│   │   ├── question.go
│   │   ├── review.go
│   │   └── section.go
│   ├── repository
│   │   ├── answer.go
│   │   ├── course.go
│   │   ├── dao.go
│   │   ├── indicator.go
│   │   ├── question.go
│   │   ├── review.go
│   │   ├── score.go
│   │   ├── section.go
│   │   ├── transaction.go
│   │   └── user.go
│   └── service
│       ├── answer.go
│       ├── auth.go
│       ├── course.go
│       ├── email.go
│       ├── file_uploader.go
│       ├── indicator.go
│       ├── payment.go
│       ├── poll.go
│       ├── question.go
│       ├── review.go
│       ├── score.go
│       ├── section.go
│       ├── token_manager.go
│       └── user.go
├── pkg
│   ├── google
│   │   └── api
│   │       ├── annotations.pb.go
│   │       ├── annotations.pb.validate.go
│   │       ├── annotations.swagger.json
│   │       ├── http.pb.go
│   │       ├── http.pb.validate.go
│   │       └── http.swagger.json
│   ├── validate
│   │   ├── validate.pb.go
│   │   ├── validate.pb.validate.go
│   │   └── validate.swagger.json
│   ├── microservice_grpc.pb.go
│   ├── microservice.pb.go
│   ├── microservice.pb.gw.go
│   ├── microservice.pb.validate.go
│   └── microservice.swagger.json
├── docker-compose.yml
├── Dockerfile
├── go.mod
├── go.sum
├── init.sql
├── Makefile
└── tools.go
```

### [AkbaraliShaikh/denti](https://github.com/AkbaraliShaikh/denti) ![GitHub Repo stars](https://img.shields.io/github/stars/AkbaraliShaikh/denti?style=flat)

```
.
├── cmd
│   └── server
│       ├── router.go
│       └── server.go
├── docker
│   └── docker-compose.yml
├── pkg
│   ├── config
│   │   ├── config.go
│   │   └── config.yml
│   ├── di
│   │   └── di.go
│   ├── http
│   │   └── rest
│   │       ├── health_handler.go
│   │       ├── login_handler.go
│   │       └── user_handler.go
│   ├── logger
│   │   ├── logger.go
│   │   └── zaplog.go
│   ├── login
│   │   ├── login.go
│   │   ├── repository.go
│   │   └── service.go
│   ├── patient
│   │   ├── patient.go
│   │   ├── repository.go
│   │   └── service.go
│   ├── storage
│   │   ├── orm
│   │   │   ├── login_repo.go
│   │   │   ├── patient_repo.go
│   │   │   └── user_repo.go
│   │   ├── driver.go
│   │   └── readme.txt
│   └── user
│       ├── repository.go
│       ├── service.go
│       └── user.go
├── denti.go
├── dockerfile
├── go.mod
├── go.sum
└── README.md
```

### [wesionaryTEAM/go_clean_architecture](https://github.com/wesionaryTEAM/go_clean_architecture) ![GitHub Repo stars](https://img.shields.io/github/stars/wesionaryTEAM/go_clean_architecture?style=flat)

```
.
├── bootstrap
│   ├── app.go
│   └── modules.go
├── console
│   ├── console.go
│   └── serve.go
├── docker
│   ├── custom.cnf
│   ├── db.Dockerfile
│   ├── run.sh
│   └── web.Dockerfile
├── domain
│   ├── constants
│   │   └── user.go
│   ├── models
│   │   └── user.go
│   ├── user
│   │   ├── api_error.go
│   │   ├── controller.go
│   │   ├── module.go
│   │   ├── repository.go
│   │   ├── route.go
│   │   └── service.go
│   └── module.go
├── hooks
│   └── pre-commit
├── migrations
│   ├── 20240606114654.sql
│   └── atlas.sum
├── pkg
│   ├── errorz
│   │   ├── base.go
│   │   ├── common_errors.go
│   │   ├── errors.go
│   │   └── type.go
│   ├── framework
│   │   ├── command.go
│   │   ├── context_constants.go
│   │   ├── env.go
│   │   └── logger.go
│   ├── infrastructure
│   │   ├── aws.go
│   │   ├── db.go
│   │   ├── module.go
│   │   └── router.go
│   ├── middlewares
│   │   ├── auth_middleware.go
│   │   ├── cognito_middleware.go
│   │   ├── middlewares.go
│   │   ├── rate_limit_middleware.go
│   │   └── upload_middleware.go
│   ├── responses
│   │   ├── handle_errors.go
│   │   ├── handle_errors_test.go
│   │   ├── mock_sentry_service_test.go
│   │   └── response.go
│   ├── services
│   │   ├── cognito.go
│   │   ├── module.go
│   │   ├── s3.go
│   │   └── ses_service.go
│   ├── types
│   │   ├── base.go
│   │   ├── binary_uuid.go
│   │   └── file_metadata.go
│   ├── utils
│   │   ├── aws_error_mapper.go
│   │   ├── custom_bind.go
│   │   ├── datatype_converter.go
│   │   ├── is_cli.go
│   │   ├── pagination.go
│   │   ├── send_sentry_msg.go
│   │   ├── sentry_service.go
│   │   └── status_in_list.go
│   └── module.go
├── seeds
│   ├── admin_seed.go
│   └── seeds.go
├── atlas.hcl
├── contributing.md
├── dbconfig.yml
├── docker-compose.yml
├── go.mod
├── go.sum
├── LICENSE
├── main.go
├── Makefile
├── README.md
└── SECURITY.md
```

### [caohoangnam/go-clean-architecture](https://github.com/caohoangnam/go-clean-architecture) ![GitHub Repo stars](https://img.shields.io/github/stars/caohoangnam/go-clean-architecture?style=flat)

```
.
├── app
│   ├── entity
│   │   ├── book.go
│   │   └── meow.go
│   ├── handler
│   │   ├── book.go
│   │   └── meow.go
│   └── repository
│       ├── book.go
│       └── meow.go
├── config
│   └── database.go
├── db
│   ├── Dockerfile
│   └── meowRepository.go
├── domain
│   ├── book.go
│   └── meow.go
├── events
│   ├── Dockerfile
│   ├── event.go
│   ├── message.go
│   └── nats.go
├── kibana
│   ├── custom_kibana.yml
│   └── Dockerfile
├── logstash
│   ├── custom_logstash.yml
│   └── logstash.conf
├── search
│   ├── custom_elasticsearch.yml
│   ├── Dockerfile
│   ├── elastic.go
│   └── repository.go
├── services
│   ├── client.go
│   ├── Dockerfile
│   ├── hub.go
│   └── messages.go
├── utils
│   └── response.go
├── _config.yml
├── docker-compose.yml
├── Dockerfile
├── example.env
├── go.mod
├── LICENCE
├── main.go
├── Makefile
└── README.md
```

### [daopmdean/todoapp-backend](https://github.com/daopmdean/todoapp-backend) ![GitHub Repo stars](https://img.shields.io/github/stars/daopmdean/todoapp-backend?style=flat)

```
.
├── build
│   └── docker
│       ├── Dockerfile
│       └── Dockerfile.test
├── cmd
│   ├── init
│   │   └── main.go
│   └── server
│       └── main.go
├── internal
│   ├── adapter
│   │   ├── http
│   │   │   └── rest
│   │   │       ├── create_todo.go
│   │   │       ├── delete_todo.go
│   │   │       ├── get_me.go
│   │   │       ├── get_todos.go
│   │   │       ├── login.go
│   │   │       ├── register.go
│   │   │       ├── server.go
│   │   │       └── toggle_todo.go
│   │   ├── memdb
│   │   │   ├── internal
│   │   │   │   └── util.go
│   │   │   ├── create_repos.go
│   │   │   ├── todo_repo.go
│   │   │   └── user_repo.go
│   │   ├── mongodb
│   │   │   ├── connection.go
│   │   │   ├── create_repos.go
│   │   │   ├── init.go
│   │   │   ├── todo_repo.go
│   │   │   └── user_repo.go
│   │   └── mssqldb
│   │       ├── connection.go
│   │       ├── create_repos.go
│   │       ├── todo_repo.go
│   │       └── user_repo.go
│   ├── common
│   │   └── config
│   │       ├── config.go
│   │       ├── mongodb.go
│   │       └── mssql.go
│   ├── entity
│   │   ├── internal
│   │   │   ├── hash_hmacsha256.go
│   │   │   └── ranstr.go
│   │   ├── todo.go
│   │   ├── todo_test.go
│   │   ├── user.go
│   │   └── user_test.go
│   └── usecase
│       ├── repo
│       │   ├── todo.go
│       │   └── user.go
│       ├── util
│       │   └── access_token
│       │       ├── access_token.go
│       │       └── access_token_test.go
│       ├── authenticate.go
│       ├── authenticate_test.go
│       ├── authorize.go
│       ├── create_todo.go
│       ├── create_todo_test.go
│       ├── delete_todo.go
│       ├── delete_todo_test.go
│       ├── get_me.go
│       ├── get_todo_list.go
│       ├── get_todo_list_test.go
│       ├── login.go
│       ├── login_test.go
│       ├── register.go
│       ├── register_test.go
│       ├── toggle_todo.go
│       └── toggle_todo_test.go
├── test
│   ├── api_rest_test
│   │   ├── internal
│   │   │   └── util.go
│   │   ├── create_todo_test.go
│   │   ├── delete_todo_test.go
│   │   ├── get_me_test.go
│   │   ├── get_todo_list_test.go
│   │   ├── login_test.go
│   │   ├── ping_test.go
│   │   └── toggle_todo_test.go
│   └── repomock
│       ├── todo_repo_mock_builder.go
│       ├── todo_repo_mock.go
│       ├── user_repo_mock_builder.go
│       └── user_repo_mock.go
├── go.mod
├── go.sum
├── Makefile
└── README.md
```

## Hexagonal architecture sample repositories trees

### [kantancoding/hexArchGoGRPC](https://github.com/kantancoding/hexArchGoGRPC) ![GitHub Repo stars](https://img.shields.io/github/stars/kantancoding/hexArchGoGRPC?style=flat)

```
.
├── cmd
│   └── main.go
├── internal
│   ├── adapters
│   │   └── framework
│   │       ├── left
│   │       │   └── grpc
│   │       │       ├── pb
│   │       │       │   ├── arithmetic_svc_grpc.pb.go
│   │       │       │   └── number_msg.pb.go
│   │       │       ├── proto
│   │       │       │   ├── arithmetic_svc.proto
│   │       │       │   └── number_msg.proto
│   │       │       ├── rpc.go
│   │       │       ├── rpc_test.go
│   │       │       └── server.go
│   │       └── right
│   │           └── db
│   │               └── db.go
│   ├── application
│   │   ├── api
│   │   │   ├── api.go
│   │   │   └── interfaces.go
│   │   └── core
│   │       └── arithmetic
│   │           ├── arithmetic.go
│   │           └── arithmetic_test.go
│   └── ports
│       ├── left.go
│       └── right.go
├── testdb
│   └── init.sql
├── docker-compose.yaml
├── Dockerfile
├── go.mod
├── go.sum
├── grpc_entrypoint.sh
└── README.md
```

### [solrac97gr/go-hexagonal-blog](https://github.com/solrac97gr/go-hexagonal-blog) ![GitHub Repo stars](https://img.shields.io/github/stars/solrac97gr/go-hexagonal-blog?style=flat)

```
.
├── cmd
│   └── main.go
├── internals
│   ├── core
│   │   ├── domain
│   │   │   └── user.go
│   │   ├── ports
│   │   │   └── user_ports.go
│   │   └── services
│   │       └── user_service.go
│   ├── handlers
│   │   └── user_handlers.go
│   ├── repositories
│   │   └── user_repository.go
│   └── server
│       └── server.go
├── go.mod
└── README.MD
```

### [charly3pins/eShop](https://github.com/charly3pins/eShop) ![GitHub Repo stars](https://img.shields.io/github/stars/charly3pins/eShop?style=flat)

```
.
├── application
│   ├── order.go
│   └── user.go
├── cmd
│   ├── migrations
│   │   └── main.go
│   └── server
│       └── main.go
├── domain
│   ├── base
│   │   ├── entity.go
│   │   ├── identity.go
│   │   └── repository.go
│   ├── order.go
│   └── user.go
├── infrastructure
│   ├── api
│   │   ├── order.go
│   │   ├── router.go
│   │   └── user.go
│   └── postgres
│       ├── client.go
│       ├── order.go
│       └── user.go
├── docker-compose.yml
├── go.mod
├── go.sum
├── Makefile
└── README.md
```

## Real world usage

### [Creatly/creatly-backend](https://github.com/Creatly/creatly-backend) ![GitHub Repo stars](https://img.shields.io/github/stars/Creatly/creatly-backend?style=flat)

```
.
├── cmd
│   └── app
│       └── main.go
├── configs
│   ├── main.yml
│   ├── prod.yml
│   └── stage.yml
├── deploy
│   ├── nginx
│   │   ├── docker-entrypoint.sh
│   │   ├── Dockerfile
│   │   └── nginx.conf.template
│   ├── docker-compose.yml
│   ├── Dockerfile
│   └── staging.yml
├── docs
│   ├── docs.go
│   ├── swagger.json
│   └── swagger.yaml
├── internal
│   ├── app
│   │   └── app.go
│   ├── config
│   │   ├── fixtures
│   │   │   └── main.yml
│   │   ├── config.go
│   │   └── config_test.go
│   ├── delivery
│   │   └── http
│   │       ├── v1
│   │       │   ├── fixtures
│   │       │   │   ├── ccc.pdf
│   │       │   │   ├── image.jpg
│   │       │   │   ├── image.png
│   │       │   │   └── large.jpeg
│   │       │   ├── 60e69c1f4bb5a43711c0ee98-image.png
│   │       │   ├── 60e69c448af06211ebfaba10-image.jpg
│   │       │   ├── 60e69c81be7bbc1184dd21d1-image.png
│   │       │   ├── 60e69cb986803c02115a55c5-image.jpg
│   │       │   ├── 60e69cb986803c02115a55c5-image.png
│   │       │   ├── 60e69cc243b3478089ed9f22-image.jpg
│   │       │   ├── 60e69cc243b3478089ed9f22-image.png
│   │       │   ├── admins.go
│   │       │   ├── admins_media.go
│   │       │   ├── admins_students.go
│   │       │   ├── admins_surveys.go
│   │       │   ├── admins_test.go
│   │       │   ├── admins_upload.go
│   │       │   ├── admins_upload_test.go
│   │       │   ├── courses.go
│   │       │   ├── handler.go
│   │       │   ├── middleware.go
│   │       │   ├── offer.go
│   │       │   ├── payment.go
│   │       │   ├── promocodes.go
│   │       │   ├── promocodes_test.go
│   │       │   ├── response.go
│   │       │   ├── settings.go
│   │       │   ├── students.go
│   │       │   ├── students_test.go
│   │       │   └── users.go
│   │       ├── handler.go
│   │       ├── handler_test.go
│   │       └── middleware.go
│   ├── domain
│   │   ├── course.go
│   │   ├── errors.go
│   │   ├── file.go
│   │   ├── offer.go
│   │   ├── order.go
│   │   ├── promocode.go
│   │   ├── query.go
│   │   ├── school.go
│   │   ├── session.go
│   │   ├── student.go
│   │   ├── survey.go
│   │   └── user.go
│   ├── repository
│   │   ├── mocks
│   │   │   └── mock.go
│   │   ├── admins_mongo.go
│   │   ├── collections.go
│   │   ├── courses_mongo.go
│   │   ├── files.go
│   │   ├── lessons_mongo.go
│   │   ├── modules_mongo.go
│   │   ├── offers_mongo.go
│   │   ├── orders_mongo.go
│   │   ├── packages_mongo.go
│   │   ├── promocodes_mongo.go
│   │   ├── repository.go
│   │   ├── schools_mongo.go
│   │   ├── student_lessons_mongo.go
│   │   ├── students_mongo.go
│   │   ├── survey_results_mongo.go
│   │   └── users_mongo.go
│   ├── server
│   │   └── server.go
│   └── service
│       ├── mocks
│       │   └── mock.go
│       ├── admins.go
│       ├── admins_test.go
│       ├── courses.go
│       ├── emails.go
│       ├── files.go
│       ├── lessons.go
│       ├── modules.go
│       ├── offers.go
│       ├── orders.go
│       ├── packages.go
│       ├── payments.go
│       ├── promocodes.go
│       ├── schools.go
│       ├── service.go
│       ├── student_lessons.go
│       ├── students.go
│       ├── surveys.go
│       └── users.go
├── pkg
│   ├── auth
│   │   └── manager.go
│   ├── cache
│   │   ├── cache.go
│   │   └── memory.go
│   ├── database
│   │   └── mongodb
│   │       └── mongodb.go
│   ├── dns
│   │   └── dns.go
│   ├── email
│   │   ├── mock
│   │   │   └── mock.go
│   │   ├── sendpulse
│   │   │   └── client.go
│   │   ├── smtp
│   │   │   └── smtp.go
│   │   ├── provider.go
│   │   ├── sender.go
│   │   └── validate.go
│   ├── hash
│   │   └── password.go
│   ├── limiter
│   │   └── limiter.go
│   ├── logger
│   │   ├── logger.go
│   │   └── logrus.go
│   ├── otp
│   │   ├── mock.go
│   │   └── otp.go
│   ├── payment
│   │   ├── fondy
│   │   │   └── fondy.go
│   │   └── provider.go
│   └── storage
│       ├── minio.go
│       └── storage.go
├── templates
│   ├── purchase_successful.html
│   └── verification_email.html
├── tests
│   ├── fixtures
│   │   ├── callback_approved.json
│   │   └── callback_declined.json
│   ├── admins_test.go
│   ├── courses_test.go
│   ├── data.go
│   ├── main_test.go
│   ├── payment_test.go
│   ├── promocodes_test.go
│   └── students_test.go
├── docker-compose.yml
├── Dockerfile
├── Dockerfile.debug
├── go.mod
├── go.sum
├── Makefile
└── README.md
```
