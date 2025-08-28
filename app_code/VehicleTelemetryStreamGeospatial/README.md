# Vehicle Telemetry Streaming Solution

## Project Overview

This project simulates and streams real-time vehicle telemetry and geospatial data to a SQL Server database. It is designed for testing, demonstration, or development of vehicle data analytics platforms, and supports both basic sensor simulation and realistic route-based GPS streaming.

## Main Features

- **Configurable Database and API Integration**
  - Centralized configuration for SQL Server connection and OpenRouteService API key via `config.py`.

- **Vehicle Telemetry Data Simulation**
  - `VehicleTelemetryStream.py` simulates real-time vehicle sensor data (engine temperature, oil pressure, battery voltage, fuel level, tire pressure, RPM, speed, acceleration, odometer, etc.).
  - Streams data to a SQL Server database, with each sensor value mapped to a database sensor ID.

- **Geospatial Telemetry Streaming**
  - `VehicleTelemetryStreamGeospatial.py` simulates GPS data for a vehicle trip in a selected city (San Francisco or San Diego).
  - Streams latitude and longitude points to the database, mimicking a moving vehicle.

- **Realistic Route Generation (Optional)**
  - `VehicleTelemetryStreamGeospatial_osmnx.py` uses the OpenRouteService API to generate realistic driving routes between two points in a city.
  - Streams the generated route’s GPS points to the database for more lifelike telemetry.

- **Automated Multi-Process Streaming**
  - `subprocess_start.py` launches multiple telemetry streaming scripts in parallel, allowing simultaneous simulation of different data streams.

- **Robust Error Handling and Resource Management**
  - Each script includes error handling for database operations and ensures proper cleanup of resources.

## Prerequisites

- Python 3.8 or higher
- SQL Server (local or remote instance)
- (Optional) [OpenRouteService API key](https://openrouteservice.org/sign-up/)
- Required Python packages:
  - `pyodbc`
  - `openrouteservice` (for route generation)
- Access to modify and query the target SQL Server database

## Installation

1. **Clone the repository:**

2. **Install dependencies:**

3. **Configure database and API keys:**
   - Edit `config.py` to set your SQL Server connection details and OpenRouteService API key.

## Usage

- **Simulate vehicle sensor data:**

- **Simulate geospatial (GPS) data:**

- **Simulate realistic route-based GPS data:**

- **Run multiple streams in parallel:**

## Project Structure

- `config.py` – Central configuration for database and API keys
- `VehicleTelemetryStream.py` – Simulates and streams vehicle sensor data
- `VehicleTelemetryStreamGeospatial.py` – Simulates and streams GPS data
- `VehicleTelemetryStreamGeospatial_osmnx.py` – Streams GPS data along realistic routes
- `subprocess_start.py` – Launches multiple streaming scripts in parallel

## Configuration

Edit `config.py` to set:
- SQL Server driver, server, database, username, and password
- OpenRouteService API key

## Examples

- Run/F5 `subprocess_start.py` to start subprocess streaming vehicle Telemetry & GEO data.
	- Example output from `VehicleTelemetryStream.py`:
	- Example output from `VehicleTelemetryStreamGeospatial.py`:

## Troubleshooting

- **Database connection errors:**  
  Ensure your SQL Server is running and the credentials in `config.py` are correct.
- **Missing dependencies:**  
  Install required Python packages using `pip install pyodbc openrouteservice`.
- **API key issues:**  
  Verify your OpenRouteService API key is valid and has not exceeded its usage limits.

## Contributing

Contributions are welcome! Please fork the repository, create a feature branch, and submit a pull request.

## License

Specify your license here (e.g., MIT, Apache 2.0).

## Authors & Acknowledgments

- Vision and engineering by **Hans Esquivel**
- Powered by **Python**

## Contact / Support

For questions or support, please open an issue or discussion on the repository or contact the moderator.

 