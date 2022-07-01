
# <p align="center">School Management App</p>

<p align="center">
    <img src="https://img.shields.io/badge/Code-JavaScript-informational?style=flat-square&logo=javascript&color=F7DF1E" alt="JavaScript" />
    <img src="https://img.shields.io/badge/Code-NodeJS-informational?style=flat-square&logo=node.js&color=339933" alt="NodeJS" />
   <img src="https://img.shields.io/badge/Code-NestJS-informational?style=flat-square&logo=nestjs&color=E0234E&logoColor=E0234E" alt="NestJS" />
  <img src="https://img.shields.io/badge/Code-GraphQL-informational?style=flat-square&logo=GraphQL&color=E10098&logoColor=E10098" alt="GraphQL" />
    <img src="https://img.shields.io/badge/Tools-MongoDB-informational?style=flat-square&logo=MongoDB&color=47A248" alt="MongoDB" />
    <img src="https://img.shields.io/badge/Tools-Docker-informational?style=flat-square&logo=docker&color=2496ED" alt="Docker" />
</p>

## 💬 About

This project was developed following Udemy's "[NestJS Zero to Hero - Modern TypeScript Back-end Development](https://www.udemy.com/course/nestjs-zero-to-hero/)" class.

## :computer: Technologies

- [Node.js](https://nodejs.org/en/)
- [Nest.js](https://nestjs.com/)
- [GraphQL](https://graphql.org/)
- [TypeORM](https://typeorm.io/)
- [MongoDB](https://www.mongodb.com/)
- [MongoDb Express](https://www.mongodb.com/products/mongo-express)
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

## :scroll: Requirements

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

## :cd: Installation

```sh
git clone git@github.com:filipe1309/ud-nestjs-school-management-app.git
```

```sh
cd ud-nestjs-school-management-app
```

## :runner: Running

```sh
docker-compose up
```

> Access http://localhost:3000  to see the application
> Access http://localhost:3000/graphql to see the GraphQL playground  
> Access http://localhost:8081 to see the MongoDB Express  

### GraphQL examples

#### Mutations

```graphql
mutation {
  createStudent(createStudentInput: {
    firstName: "John",
    lastName: "Doe"
  }) {
    id
    firstName
  }
}

mutation {
  createLesson(
    createLessonInput: {
      name: "NestJS5 with students",
      startDate: "2020-03-28T17:00:00Z",
      endDate: "2020-03-28T17:30:00Z",
      students:[
        "e1b4e577-c8c9-4c56-8c7e-05bbe33f7355",
        "b6836795-2238-4ff2-a682-8a378743bf28",
        "568dbaa7-6170-4a1a-921d-6f72fa779125"
      ]
    }
  ) {
    id
    name
    students {
      firstName
    }
  }
}

mutation {
  assignStudentsToLesson(assignStudentsToLessonInput: {
    lessonId: "3e4c25ee-f879-43f8-896d-4930f3ab04ef"
    studentIds: [
      "e1b4e577-c8c9-4c56-8c7e-05bbe33f7355",
      "b6836795-2238-4ff2-a682-8a378743bf28",
      "568dbaa7-6170-4a1a-921d-6f72fa779125"
    ]
  }) {
    name
    students {
      firstName
    }
  }
}
```

### Queries

```graphql
query {
  lesson(id: "cec57d7d-863f-4e98-a585-238749bac7c3") {
    name
  }
}
query {
  lessons {
    name
  }
}


query {
  student(id: "e1b4e577-c8c9-4c56-8c7e-05bbe33f7355") {
    firstName
  }
}

query {
  students {
    firstName
  }
}
```

<!-- ## :white_check_mark: Tests

After up the container:

```sh
docker-compose exec -t {{ CONTAINER_SERVICE_NAME }} ./vendor/bin/phpunit
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate. -->

## License

[MIT](https://choosealicense.com/licenses/mit/)

## About Me

<p align="center">
    <a style="font-weight: bold" href="https://github.com/filipe1309/">
    <img style="border-radius:50%" width="100px; "src="https://github.com/filipe1309.png"/>
    </a>
</p>

---

<p align="center">
    Done with&nbsp;&nbsp;:heart:&nbsp;&nbsp;by <a style="font-weight: bold" href="https://github.com/filipe1309/">Filipe Leuch Bonfim</a> 🖖
</p>

---

> @ Generated with [ShubcoGen Template™](https://github.com/filipe1309/shubcogen-template)   
> ❓ [Docs](./.shub/README.md)
