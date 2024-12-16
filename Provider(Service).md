## Provider(service)
NestJS에서 Provider는 서비스(Service), 리포지토리(Repository), 팩토리(Factory), 헬퍼(Helper) 등을 의미하며, 애플리케이션의 비즈니스 로직을 캡슐화하고 재사용 가능한 로직을 구현하기 위한 기본 단위이다. Provider는 종속성 주입(Dependency Injection, DI)을 통해 컨트롤러나 Interface를 Provider에 주입되어 관련한 비즈니스 로직을 수행한다.

### Interface
Interface는 TypeScript에서 사용되는 데이터의 구조를 정의하기 위한 것이며 특정 객체가 어떤 속성과
타입을 가져야 하는지를 명확하게 하기위해 사용되며 Provider는 Interface에 설정된 속성으로 로직(method)을
구현한다.

```javascript
export interface User {
    name: string;
    password: string;
    email: string;
    gender: string;
    address: string;
}
```

### Service

```javascript
import { Injectable } from '@nestjs/common';
import { User } from './interface/users.interface';


@Injectable() // Dependency injection
export class UsersService {
    private readonly users: User[] = [];

    create(user: User){
        this.users.push(user);
    }

    findAll(): User[]{
        return this.users;
    }
}
```

### Controller

```javascript
import { Body, Controller, Delete, Get, Param, Post, Put } from '@nestjs/common';
import { CreateUserDto } from './CreateUsersDto';
import { UsersService } from './users.service';
import { User } from './interface/users.interface';

@Controller('users')
export class UsersController {
    constructor(private usersService: UsersService){

    }; // private는 선언과 동시에 이루어진다.

    @Get() //user
    findAll(): User[]{
        return this.usersService.findAll();
    }

    @Get(':id')
    findOne(@Param('id')id : string) : string{
        return `This action returns a #${id} users`
    }

    @Post()
    create(@Body() CreateUserDto: CreateUserDto){
        return this.usersService.create(CreateUserDto);
    }

    @Put(':id')
    update(@Param('id')id: string, @Body() CreateUserDto: CreateUserDto){
        return `This action update a #${id} users`;
    }

    @Delete(':id')
    remove(@Param('id')id: string){
        return `This action removes a #${id} users`
    }
}
```