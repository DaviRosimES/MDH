# MDH - Market Data Handler

**MDH** (Market Data Handler) is a modular C++ project designed to simulate the core of an electronic trading system by handling and distributing market data in real-time or from historical files.

The system serves as a foundation for developing trading algorithms, simulating order book environments, and feeding data into strategy engines — mimicking how real trading systems operate.

---

## 🏗️ Project Structure

```
MDH/
├── include/
│   └── datafeeder.h           # Abstract base class
├── src/
│   └── datafeeder.cpp         # Implementation (e.g., CSVFeeder)
├── tests/
│   └── test_datafeeder.cpp    # Unit tests using Google Test
├── main.cpp                   # Example usage of DataFeeder
├── CMakeLists.txt             # Build configuration
└── README.md
```

---

## 🚀 Getting Started

### 1. Clone the repo
``` bash
git clone 
```

### 1. Build the Project

```bash
mkdir build && cd build
cmake ..
make
```

### 2. Run the Application

```bash
./MDH
```

### 3. Run Tests

```bash
ctest       # or ./MDHTests
```

---

## 🧩 Example Use Case

In `main.cpp`, we instantiate a `CSVFeeder` to simulate live data replay from a file. Each data point is passed to a callback, which can be a strategy, an order book, or a logger.

```cpp
CSVFeeder feeder("data.csv");

feeder.setCallback([](const std::string& symbol, double price, int volume) {
    std::cout << symbol << " @ " << price << " (" << volume << " shares)" << std::endl;
});

feeder.start();
```

---

## 🛠️ Dependencies

- C++20
- CMake >= 3.22
- Google Test (fetched automatically via `FetchContent`)

---

## 📈 Goals

This project is intended to serve as a sandbox for:

- Market data simulation and experimentation
- Order book and strategy development
- Latency-aware data ingestion pipelines
- Education on trading system architecture

---

## 📬 Contributions

Pull requests and suggestions are welcome!  
Feel free to fork the repository and build your own strategy engine or feed connectors.

---

## 🧠 Author

**Davi Rosim**  
Trading systems enthusiast | Software Engineer
