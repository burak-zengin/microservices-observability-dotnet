# Microservices Observability with .NET

A practical observability sample for .NET microservices using **OpenTelemetry**, **Jaeger**, **Prometheus**, and **Docker Compose**.

This repository demonstrates how to trace requests across multiple services and collect telemetry data in a local development environment.

---

## 🎯 Goal

The goal of this project is to show how observability works in a distributed system.

It focuses on:

- Distributed tracing
- Request correlation
- OpenTelemetry instrumentation
- Jaeger trace visualization
- Prometheus metrics collection
- Docker-based local observability stack

---

## 🧠 Architecture

```text
Client
  ↓
Gateway / API
  ↓
Service A
  ↓
Service B

Telemetry
  ↓
OpenTelemetry
  ↓
Jaeger / Prometheus
```

---

## 🔍 What is Observability?

Observability helps us understand what is happening inside a distributed system by collecting:

- **Traces**: request flow across services
- **Metrics**: system and application measurements
- **Logs**: application events and errors

---

## ⚙️ Tech Stack

- .NET / ASP.NET Core
- OpenTelemetry
- Jaeger
- Prometheus
- Docker Compose

---

## 🚀 Running the Project

Start the full environment:

```bash
docker compose up -d
```

Run the services from Visual Studio or CLI.

---

## 🔎 Jaeger UI

Jaeger is used to visualize distributed traces.

```text
http://localhost:16686
```

Use Jaeger to inspect request flow between services.

---

## 📊 Prometheus UI

Prometheus is used to collect metrics.

```text
http://localhost:9090
```

---

## 🔁 Request Flow

```text
HTTP Request
  ↓
API Service
  ↓
Downstream Service
  ↓
OpenTelemetry creates spans
  ↓
Jaeger displays distributed trace
```

---

## 📂 Project Structure

```text
src/
  ApiGateway/
  ServiceA/
  ServiceB/

docker-compose.yml
```

> Folder names may vary depending on the actual service names.

---

## ✅ What This Project Demonstrates

- Instrumenting .NET services with OpenTelemetry
- Propagating trace context between services
- Visualizing traces in Jaeger
- Collecting metrics with Prometheus
- Running observability tools locally with Docker Compose

---

## ⭐ Future Improvements

- Add structured logging with Serilog
- Add Grafana dashboard
- Add correlation ID propagation
- Add health checks
- Add custom business metrics
- Add error tracing examples
- Add integration tests

---

## 📌 Why This Repository Matters

Debugging microservices without observability is difficult.

This project provides a simple foundation for understanding how telemetry flows through a distributed .NET system.
