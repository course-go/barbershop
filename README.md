# Barbershop

Barbershop is an implementation of the Sleeping barber problem. This project serves as a template for the second homework assignment. To learn more about the homework assignments in general, visit the [homework](https://github.com/course-go/homework) repository.

## Assignment

Throughout this homework assignment you will implement a solution of the [Sleeping barber problem](https://en.wikipedia.org/wiki/Sleeping_barber_problem). This problem was proposed by [Edsger W. Dijkstra](https://en.wikipedia.org/wiki/Edsger_Dijkstra) in his work [Cooperating sequential processes](https://www.cs.utexas.edu/users/EWD/transcriptions/EWD01xx/EWD123.html).

### Specification

The problem is specified as follows:

Picture a barbershop that has a single barber, a single barber chair on which the barber gives cuts, and a **N** chairs in the waiting room.

![Barbershop diagram](assets/barbershop.svg)

The problem then has the following rules:
- The barber sleeps whenever there are no clients.
- If a client arrives and the barber is asleep, he wakes him up.
- If a client arrives and the barber is bussy giving a cut he sits in the waiting room.
    - If there are no chairs left, he leaves the shop.
- Whenever barber finishes giving a haircut, he checks that waiting room for clients.
    - If it is empty, he sleeps.
    - If there are clients, he chooses one and gives him a cut.

### Bonus

- Implement support for multiple barbers.
    - That is M barbers with M barber chairs.

## Requirements

The application has to demonstate the functionallity of the barbershop as specified by the assignment. A short demo should also be created. The code must have no race conditions or possible deadlocks. Lastly, stress is given on writting idiomatic code.

## Motivation

The main goal of this homework is to practice working with the concurrency model that Go offers.

## Packages

- I highly recommend to implement a proper logging, so the application can be easily monitored. You can checkout the standard logging libraries like [log](http://pkg.go.dev/log) and slog [slog](http://pkg.go.dev/log/slog).
- You might also want to inspect the [sync](https://pkg.go.dev/sync) package for synchronization primitives. However, think thoroughly if they are required for the implementing the solution.
