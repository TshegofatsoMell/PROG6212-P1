# Section B - API Endpoint Plan - Race Event System

| HTTP Method | Route | Description | Role Required | Request Body | Expected Response |
|---|---|---|---|---|---|
| POST | /api/auth/register | Register new user | Anonymous | {"fullName":"John Doe","email":"john@test.com","password":"P@ss123","role":"Athlete"} | 201 Created: userId and token |
| POST | /api/auth/login | Login and get JWT | Anonymous | {"email":"john@test.com","password":"P@ss123"} | 200 OK: token and role |
| GET | /api/users/me | Get my profile | Athlete, Admin | None | 200 OK: my user object |
| PUT | /api/users/me | Update my profile | Athlete, Admin | {"fullName":"New Name"} | 200 OK: updated user |
| GET | /api/users | Get all users | Admin | None | 200 OK: list of users |
| GET | /api/categories | Get all categories | All Auth | None | 200 OK: list of categories |
| POST | /api/categories | Create category | Admin | {"name":"Marathon","distanceKm":42} | 201 Created: category |
| PUT | /api/categories/{id} | Update category | Admin | {"name":"10km Run"} | 200 OK: updated |
| DELETE | /api/categories/{id} | Delete category | Admin | None | 204 No Content |
| GET | /api/events | Get all events | All Auth | None | 200 OK: list of events |
| GET | /api/events/{id} | Get single event | All Auth | None | 200 OK: event details |
| POST | /api/events | Create new event | Admin | {"title":"Comrades 2026","eventDate":"2026-06-14","location":"Durban","categoryId":1,"maxParticipants":1000} | 201 Created: event |
| PUT | /api/events/{id} | Update event | Admin | {"title":"Updated","location":"Pretoria"} | 200 OK: updated event |
| DELETE | /api/events/{id} | Delete event | Admin | None | 204 No Content |
| POST | /api/enrolments | Enrol for event | Athlete | {"eventId":1} | 201 Created: enrolment confirmed |
| GET | /api/enrolments/my | Get my enrolments | Athlete | None | 200 OK: my enrolments list |
| GET | /api/enrolments/event/{eventId} | Get enrolments for event | Admin | None | 200 OK: list of athletes |
| DELETE | /api/enrolments/{id} | Cancel enrolment | Athlete, Admin | None | 204 No Content |
| POST | /api/results | Add result | Admin | {"enrolmentId":1,"position":1,"finishTime":"02:30:15"} | 201 Created: result |
| GET | /api/results/event/{eventId} | Get event results | All Auth | None | 200 OK: leaderboard |
| GET | /api/results/my | Get my results | Athlete | None | 200 OK: my history |
| PUT | /api/results/{id} | Update result | Admin | {"position":2,"finishTime":"02:32:00"} | 200 OK: updated |
| DELETE | /api/results/{id} | Delete result | Admin | None | 204 No Content |