# IoT Deployment Repository

Deploys a dashboard + server that displays historical or real time sensor data.


## Run full application using Docker

**Prerequisites**:  
- Docker 
- Docker compose
- Backend: https://github.com/arvid-e/iot-backend
- Frontend: https://github.com/arvid-e/iot-frontend
- Deploy: https://github.com/arvid-e/iot-deploy 

**Steps**:  

1. Setup folder structure:
```
app/
├── iot-frontend/
├── iot-backend/
└── iot-deploy/
```
2. Setup broker and hardware
3. Set environment variables
```
DOMAIN_NAME
MONGO_USER
MONGO_PASSWORD
VITE_MQTT_BROKER_URL
VITE_MQTT_USERNAME
VITE_MQTT_PASSWORD
DEVICE_PASSWORD
MQTT_BROKER_URL
EMQX_DASHBOARD_PASSWORD
MQTT_BACKEND_USER
MQTT_BACKEND_PASSWORD
```
3. `cd app/iot-deploy`
4. `docker compose up -d --build`