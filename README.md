# Mini-Spring: A Lightweight Java Dependency Injection and Configuration Framework

Welcome to **Mini-Spring**! This project is a lightweight framework inspired by Spring, aiming to provide core features such as **Dependency Injection (DI)** and **configuration management** using `application.yml` files.

## Features

- **Dependency Injection**: A simple yet flexible DI container to manage and inject dependencies in your Java applications.
- **YAML Configuration**: Read and parse properties from `application.yml` files, supporting hierarchical configurations.
- **Annotations Support**: Use custom annotations to define and inject beans seamlessly.

## Getting Started

### Prerequisites

- Java 8 or higher
- Maven or Gradle for dependency management

### Installation

Clone the repository:

```bash
git clone https://github.com/your-username/mini-spring.git
cd mini-spring
```

### Usage

1. **Define Your Beans:**

Create Java classes with custom annotations (`@MiniComponent`, `@MiniAutowired`) to define beans and dependencies.

```java
@MiniComponent
public class MyService {
    @MiniAutowired
    private MyRepository myRepository;
}
```

2. **Configure Application Properties:**

Create an `application.yml` file in the `resources` directory to define your configurations.

```yaml
server:
  port: 8080
database:
  host: localhost
  port: 5432
```

3. **Run the Application:**

Use the provided `MiniSpringApplication` class to bootstrap your application.

```java
public class Main {
    public static void main(String[] args) {
        MiniSpringApplication.run(Main.class, args);
    }
}
```

## Roadmap

- [ ] Support for advanced DI features (e.g., constructor-based injection)
- [ ] Add support for `application.properties` file format
- [ ] Integrate logging and more robust error handling
- [ ] Enhance annotation capabilities (e.g., custom scopes)

## Contributing

Contributions are welcome! Feel free to open issues, submit pull requests, or provide feedback to help make this project better.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
