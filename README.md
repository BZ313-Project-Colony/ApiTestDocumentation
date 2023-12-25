# QRPass API Test Documentation

This documentation provides information on the API endpoints for the QRPass project.

## Endpoints

### Login

- **Endpoint:** `{{BASE_URL}}/auth/login`
- **Method:** `POST`
- **Body:** 
```json
{
    "username": "admin",
    "password": 12345678
}
```
- **Description:** This endpoint is used to login to the system.

### Create Event

- **Endpoint:** `{{BASE_URL}}/events`
- **Method:** `POST`
- **Auth:** `Bearer Token`
- **Body:** 
```json
{
    "title": "Example",
    "time": 1701353686000,
    "place": "Example Place",
    "imageUrl": "https://t4.ftcdn.net/jpg/00/53/45/31/360_F_53453175_hVgYVz0WmvOXPd9CNzaUcwcibiGao3CL.jpg",
    "maxParticipantNumber": 50
}
```
- **Description:** This endpoint is used to create a new event.

### Get Events

- **Endpoint:** `{{BASE_URL}}/events`
- **Method:** `GET`
- **Auth:** `Bearer Token`
- **Description:** This endpoint is used to get all events.

### Get Event

- **Endpoint:** `{{BASE_URL}}/events/{id}`
- **Method:** `GET`
- **Auth:** `Bearer Token`
- **Description:** This endpoint is used to get a specific event.

### Enable Event

- **Endpoint:** `{{BASE_URL}}/events/{id}/enable`
- **Method:** `POST`
- **Auth:** `Bearer Token`
- **Description:** This endpoint is used to enable a specific event.

### Disable Event

- **Endpoint:** `{{BASE_URL}}/events/{id}/disable`
- **Method:** `POST`
- **Auth:** `Bearer Token`
- **Description:** This endpoint is used to disable a specific event.

### Register Event

- **Endpoint:** `{{BASE_URL}}/events/register`
- **Method:** `POST`
- **Body:** 
```json
{
    "eventId": 2,
    "name":"Ahmet Faruk",
    "surname":"Çuha",
    "email": "ahmetfarukcuha@gmail.com"
}
```
- **Description:** This endpoint is used to register for a specific event.

### Delete Event

- **Endpoint:** `{{BASE_URL}}/events/{id}`
- **Method:** `DELETE`
- **Auth:** `Bearer Token`
- **Description:** This endpoint is used to delete a specific event.

### Get Tickets Of Event

- **Endpoint:** `{{BASE_URL}}/events/{id}/tickets`
- **Method:** `GET`
- **Auth:** `Bearer Token`
- **Description:** This endpoint is used to get all tickets of a specific event.

### Confirm Ticket

- **Endpoint:** `{{BASE_URL}}/tickets/confirm`
- **Method:** `POST`
- **Auth:** `Bearer Token`
- - **Body:** 
```json
{
    "eventId": 2,
    "email": "ahmetfarukcuha@gmail.com"
}
```
- **Description:** This endpoint is used to confirm ticket.

### Disable Ticket

- **Endpoint:** `{{BASE_URL}}/tickets/{ticket_id}/disable`
- **Method:** `POST`
- **Auth:** `Bearer Token`
- **Description:** This endpoint is used to disable ticket.

Please replace `{{BASE_URL}}` with the base URL of the API.
