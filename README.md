tessera

> a tessera is an individual tile in a mosaic

![alt text](image.png)

`tessera` is a framework + CLI for building modular monoliths on top of Cargo workspaces

modules talk to each other only through explicit contracts and `NEVER` by reaching into each other's internals

no microservices. no distributed-systems tax. just a monolith that doesn't rot

## why?

tired of inconsistency in my code. wanted robust and strict architecture. just generate all those boilerplate that I/you am/are sick of

## CLI usage

```bash
tessera new project-name        # scaffold workspace with a `contract` crate
tessera module add --contract module1   # generate a module + its facade in the `contract` crate
tessera module add module2              # generate a module with no public contract
tessera adapter add --template postgres --name UsersProvider module2 # generate a postgres adapter with name UsersProvider(trait) and PostgresUsersProvider(impl) for module2
```

## framework usage

> todo...

### inspirations

thank you guys

- nestjs
- spring modulith