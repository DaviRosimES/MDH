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
git clone https://github.com/DaviRosimES/MDH.git
```

### 2. Build the Project

```bash
mkdir build && cd build
cmake ..
make
```

### 3. Run the Application

```bash
./MDH
```

### 4. Run Tests

```bash
ctest       # or ./MDHTests
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
