[![Unit](https://github.com/Vera-Kibin/banking-api-testing-project/actions/workflows/python-app.yml/badge.svg?branch=main)](https://github.com/Vera-Kibin/banking-api-testing-project/actions/workflows/python-app.yml)
[![API](https://github.com/Vera-Kibin/banking-api-testing-project/actions/workflows/api-tests.yml/badge.svg?branch=main)](https://github.com/Vera-Kibin/banking-api-testing-project/actions/workflows/api-tests.yml)
[![Performance](https://github.com/Vera-Kibin/banking-api-testing-project/actions/workflows/test-api-perf.yml/badge.svg?branch=main)](https://github.com/Vera-Kibin/banking-api-testing-project/actions/workflows/test-api-perf.yml)

# Bank API Testing Project 💰

A backend banking simulation demonstrating TDD, automated testing, and CI workflows using Python and Flask.

## Overview

This repository demonstrates backend development and automated testing practices in a Python banking domain. The project focuses on implementing and testing core banking functionalities such as account management, transfers, and validation logic. It highlights skills in TDD, multi-level testing, and backend quality assurance.

While this is a secondary portfolio project, it showcases strong backend and testing practices. For a full-stack showcase, see the [Task Manager project](https://github.com/Vera-Kibin/task-manager-2025.git).

---

## Features

- **Account Management**: Personal and business accounts with registry functionality.
- **Transfers**: Incoming, outgoing, and express transfers.
- **Validation**:
  - PESEL uniqueness validation.
  - NIP validation using an external API.
- **Loan Logic**: Basic loan-related operations.
- **Account History**: Track account activity and send history via email (mocked SMTP).
- **Persistence**: Optional MongoDB integration for data storage.

---

## Testing Strategy

This project emphasizes a comprehensive testing approach:

- **Unit Tests**: Cover individual components and logic.
- **API Tests**: Validate REST API endpoints using `pytest` and `requests`.
- **BDD Tests**: Gherkin scenarios implemented with `Behave` for behavior-driven development.
- **Performance Tests**: Measure API performance under load.
- **Mocking**: Replace external dependencies (e.g., SMTP, MongoDB) with mocks for isolated testing.
- **Coverage**: Ensure high code coverage with `pytest-cov`.

---

## Quickstart

### Prerequisites

- Python 3.10+
- pip
- Docker + Docker Compose (optional, for MongoDB)

### Setup

1. **Install Dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

2. **(Optional) Start MongoDB**:

   ```bash
   docker compose -f mongo.yml up -d
   ```

3. **Run the Flask API**:

   ```bash
   export FLASK_APP=app/api.py
   export FLASK_ENV=development
   export PYTHONPATH=$PWD
   flask run
   ```

   The API will be available at [http://127.0.0.1:5000](http://127.0.0.1:5000).

---

## Running Tests

### Unit Tests (with Coverage)

Run all unit tests and generate a coverage report:

```bash
python -m coverage run --source=src -m pytest tests/unit
python -m coverage report -m
```

(Optional) Generate an HTML coverage report:

```bash
python -m coverage html
```

### API Tests

Ensure the Flask server is running, then execute:

```bash
python -m pytest tests/api
```

### Performance Tests

Run performance tests:

```bash
python -m pytest tests/perf
```

### BDD Tests

Execute Gherkin scenarios:

```bash
behave
```

---

## Tech Stack

- **Language**: Python
- **Framework**: Flask
- **Database**: MongoDB (optional, via Docker Compose)
- **Testing**:
  - Pytest
  - Behave (BDD)
  - Mocking with `pytest-mock`
- **Tools**:
  - Coverage
  - Requests
  - Docker / Docker Compose
- **CI/CD**: GitHub Actions

---

## Continuous Integration (CI)

The project uses GitHub Actions to automate:

- Linting and unit tests (with 100% coverage gate).
- API tests with MongoDB and a running server.
- Performance tests.

---

## Related Project

For a full-stack showcase, see my [Task Manager project](https://github.com/Vera-Kibin/task-manager-2025.git). While this repository focuses on backend testing practices, Task Manager demonstrates a complete full-stack application with frontend, backend, and deployment.

---

## Future Improvements

- Add more advanced loan-related features.
- Expand BDD scenarios for edge cases.
- Integrate a more robust database schema.
- Enhance performance testing with larger datasets.

---

## License

This project is licensed under the [MIT License](LICENSE).

---

_Crafted with precision and a touch of 🐾._
