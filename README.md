# SIH 1710: Enhancing Navigation for Railway Station Facilities and Locations

## Date
26 October 2026

## Register Number
212225040414

## Name
Sifiz A

## Problem Title
**SIH 1710: Enhancing Navigation for Railway Station Facilities and Locations**

## Problem Description
Railway stations are complex environments containing platforms, ticket counters, waiting halls, restrooms, food courts, lifts, escalators, and other passenger facilities. Passengers, particularly first-time visitors, elderly people, and persons with disabilities, may find it difficult to locate these facilities and reach their destinations on time.

The objective is to develop an accessible and user-friendly indoor navigation system that helps passengers identify station facilities, view indoor maps, and follow step-by-step directions to their destinations.

## Problem Creator's Organization
Ministry of Railways

## Idea
**RailGuide: Smart and Accessible Railway Station Navigation System**

RailGuide is a digital navigation platform designed to help passengers find facilities and navigate railway stations with ease. Users can select their current location and destination, view a station map, and receive step-by-step directions.

The system will prioritize accessibility by offering wheelchair-friendly routes, text-based directions, and voice guidance. It will also provide facility search, route information, and a simple interface suitable for passengers of different age groups.

The initial prototype will focus on one railway station using a manually prepared indoor map and verified facility locations. Additional stations and advanced real-time positioning can be incorporated in future versions.

## Proposed Solution / Architecture
![alt text](<RailGuide AI Navigation System Infographic.png>)
### 1. Passenger Interface
- Provide a responsive web application accessible through mobile phones and computers.
- Display an interactive indoor station map.
- Allow users to search for platforms and facilities.
- Show step-by-step directions from the selected starting point to the destination.
- Provide clear instructions and estimated walking distances where map data is available.

### 2. Indoor Mapping and Route Planning
- Represent the station as a network of connected locations and walkable paths.
- Store the locations of platforms, ticket counters, restrooms, lifts, food courts, and waiting areas.
- Calculate routes between selected locations using a graph-based pathfinding algorithm such as Dijkstra's algorithm or A*.
- Support accessible routing by avoiding stairs when a suitable lift or ramp route is available.

### 3. Accessibility Features
- Provide voice-guided instructions and readable text directions.
- Use clear icons, sufficient contrast, and large touch-friendly controls.
- Offer wheelchair-accessible routes based on verified station map information.
- Design the interface to support keyboard navigation and screen readers.

### 4. Station Administration
- Provide an authorized interface for updating facility locations and walkable paths.
- Allow station information to be corrected when facilities move or routes become unavailable.
- Display the last-updated time for map information.
- Add live facility or route status only when a reliable data source is available.

### 5. Future Enhancements
- Integrate QR codes at station entrances and important locations to help passengers identify their starting points.
- Extend the application to digital kiosks and native mobile applications.
- Explore indoor positioning technologies such as Bluetooth beacons or Wi-Fi positioning.
- Integrate with railway information services where official APIs or authorized data access are available.

### Proposed Architecture Flow

Passenger / Kiosk → Web Application → Navigation API → Route Planning Engine → Station Map and Facility Database → Directions and Accessibility Instructions

An administrator updates station information through a protected management interface. The navigation service uses the updated map data to generate routes.

## Use Cases

1. **Finding a platform:** A passenger searches for a platform and receives directions from the station entrance or another selected location.
2. **Locating facilities:** Passengers find ticket counters, restrooms, drinking water, food courts, waiting halls, lifts, and escalators.
3. **Accessible navigation:** Wheelchair users can request routes that avoid stairs and use mapped ramps or lifts.
4. **Voice-guided assistance:** Visually impaired passengers receive spoken navigation instructions along mapped routes.
5. **QR-based starting location:** A passenger scans a QR code at a designated station location to select a known starting point.
6. **Station information updates:** Authorized staff update facility locations and mark routes as temporarily unavailable.
7. **Digital kiosk navigation:** Passengers use a larger touchscreen interface to search for destinations and view directions.
8. **Future multi-station support:** The system can be extended to include indoor maps for additional railway stations.

## Technology Stack

### Frontend
- HTML5
- CSS3
- JavaScript
- Leaflet or another suitable mapping library, with an indoor-map layer or custom station map

### Backend
- Python
- Flask REST API

### Database
- SQLite for the initial prototype
- PostgreSQL for future multi-station deployment

### Routing and Mapping
- Graph-based representation of walkable paths
- Dijkstra's algorithm or A* for route calculation
- GeoJSON or a suitable custom data format for storing map features

### Accessibility
- Browser Text-to-Speech API for voice instructions
- Semantic HTML, keyboard navigation, high-contrast design, and screen-reader-friendly labels

### Development and Deployment
- Visual Studio Code
- Git and GitHub for version control
- A suitable web hosting service for deployment

## Dependencies

The initial prototype may use the following dependencies:

- Flask — backend web framework and API development.
- Flask-CORS — enables cross-origin requests if the frontend and backend are hosted separately.
- Leaflet — interactive map rendering, subject to suitable indoor-map integration.
- SQLite — lightweight database for station locations and paths.
- Python's built-in graph or data-processing structures — for the initial route-planning implementation.
- Browser Web Speech API — for voice guidance in supported browsers.

The exact dependencies will be finalized during implementation. Package versions and installation instructions will be documented in a `requirements.txt` file and project README as the prototype develops.

## Expected Outcome

RailGuide aims to reduce passenger confusion and the time spent searching for railway station facilities. By combining indoor maps, route planning, and accessibility-focused directions, the proposed system will provide a more convenient navigation experience.

The initial prototype will demonstrate facility search, map visualization, route calculation, and accessible route options using verified sample station data. Real-time positioning, live facility updates, native mobile applications, and kiosk integration will be treated as future enhancements unless the required hardware and data sources are available.
