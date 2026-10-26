# Smart India Hackathon Workshop
# Date: 26/10/2026
## Register Number: 212223220060
## Name: MOHAN KRISHNA J
## Problem Title
SIH 1710: Enhancing Navigation for Railway Station Facilities and Locations
## Problem Description
Background: Railway stations are complex environments with numerous facilities and locations such as ticket counters, platforms, restrooms, food courts, and waiting areas. Passengers often face difficulties in navigating these spaces, especially in large or unfamiliar stations. Efficient and user-friendly navigation systems are crucial for improving passenger experience, reducing congestion, and ensuring timely travel connections. Description: The problem involves developing a comprehensive navigation solution for railway stations that assists passengers in locating various facilities and destinations within the station premises. This includes creating detailed maps, providing real-time directions, and integrating features such as accessibility options for individuals with disabilities. The solution should be intuitive, easy to use, and accessible via multiple platforms, including mobile devices and digital kiosks. Key challenges include updating navigation information in real-time, ensuring accuracy, and accommodating the diverse needs of all passengers. Expected Solution: The expected solution is a multi-platform navigation system that provides detailed, real-time directions to all facilities and locations within a railway station. This system should include: A mobile application with 3D interactive maps and step-by-step navigation. Digital kiosks located throughout the station with touch-screen interfaces. Voice-guided navigation for visually impaired passengers. Regular updates to reflect changes in station layout and facility locations. Integration with existing railway apps and services for seamless user experience. The solution should enhance the overall passenger experience by reducing confusion, saving time, and improving accessibility within the station.

## Problem Creater's Organization
Ministry of Railway

## Idea

**RailWayfinder** is a multi-platform indoor navigation system for railway stations. It combines a mobile app with 3D maps, touch-screen kiosks and voice guidance. Passengers get live, step-by-step directions to platforms, ticket counters, restrooms, food courts, waiting rooms, lifts and exits. Routes adapt to crowding, platform changes and closures, and a dedicated accessible mode provides step-free routes plus audio and haptic guidance. It plugs into existing railway apps so a passenger can go from "my train is on Platform 7" straight to "take me there."

**What makes it different**
- Real-time rerouting based on crowd density and platform changes
- Accessibility built in from the start, not added later
- Admin dashboard so station staff can update maps and facilities without developers
- Offline map packs for stations with poor connectivity

---


## Proposed Solution / Architecture Diagram



<img width="2800" height="1660" alt="image" src="https://github.com/user-attachments/assets/3cea4208-623c-47ab-a85a-fd422b6a1c58" />



## Use Cases

1. **First-time traveller in a large station:** Searches "Platform 9" or "Waiting Room" and gets step-by-step directions.
2. **Last-minute platform change:** The app alerts the passenger and reroutes with an estimated walking time.
3. **Visually impaired passenger:** Hands-free voice navigation with haptic feedback and tactile-path cues.
4. **Wheelchair user or senior citizen:** Step-free route via lifts and ramps, with the nearest accessible restroom and assistance desk.
5. **Passenger with heavy luggage or family:** Avoids stairs and finds trolleys, cloakrooms and baby-care rooms.
6. **Kiosk user without a smartphone:** Touch-screen kiosk with a "You are here" map and a QR code to continue on a phone.
7. **Multilingual passengers:** Text and voice in English, Hindi and regional languages.
8. **Emergency or crowd management:** Staff push closure and evacuation routes instantly; crowd heatmaps help reduce congestion.
9. **Station authority:** Analytics on popular destinations and bottlenecks to plan facilities.

---

## Technology Stack


| Layer | Technologies |
|---|---|
| Mobile app | Flutter or React Native; Unity or Mapbox/Three.js for 3D maps; ARCore/ARKit (optional AR) |
| Kiosk UI | React.js web app in kiosk mode on Android/Linux touch-screen devices |
| Backend | Node.js (Express) or Python (FastAPI); REST + WebSockets |
| Routing and maps | A* / Dijkstra on a graph (NetworkX, pgRouting); GeoJSON; Blender for 3D station models |
| Database | PostgreSQL + PostGIS; Redis for caching and live state |
| Positioning | BLE beacons (iBeacon/Eddystone), Wi-Fi RTT/fingerprinting, QR anchors, sensor fusion |
| Voice and accessibility | TalkBack/VoiceOver support; Google/Bhashini TTS and STT for Indian languages |
| AI/ML (optional) | OpenCV/YOLO on CCTV feeds for crowd density; ML for dwell-time prediction |
| Admin dashboard | React + Leaflet/Mapbox editor, role-based access |
| Cloud and DevOps | Docker, Kubernetes, AWS/Azure or MeitY-empanelled cloud; CI/CD via GitHub Actions |
| Security | OAuth2/JWT, HTTPS/TLS, anonymised location data |

---


## Dependencies

- **Station data:** Accurate floor plans, CAD/BIM data and facility lists from the railway authority
- **Hardware:** BLE beacons, kiosk screens and Wi-Fi coverage in the station
- **Railway integrations:** APIs for train running status, platform allocation and ticketing (e.g. NTES, IRCTC)
- **Third-party services:** Map SDKs, TTS/STT services such as Bhashini, and cloud hosting
- **Devices:** Smartphones with Bluetooth and sensors; minimum Android/iOS versions
- **Operations:** Station staff trained to maintain maps through the admin dashboard
- **Policy and compliance:** Data-privacy rules for location data; accessibility standards (WCAG, Rights of Persons with Disabilities Act)
- **Connectivity:** Offline map packs as a fallback in low-network areas
