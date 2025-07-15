# 🎟️ Full Stack Developer Challenge - Event Booking Platform

## 📝 Project Description

You are tasked to build a **minimal event booking platform** where users can browse events, book tickets, and manage their bookings. The system should have an admin dashboard for event organizers to create and manage events.

The project will test your skills in **API design**, **database modeling**, **authentication**, and building a **React frontend**. You should use **TypeScript** for both backend and frontend.

---

## 🎯 Goals

Build a functional MVP (Minimum Viable Product) of an event booking system with the following features:

### 👥 User Roles
1. **Admin (Event Organizer):**
   - Can create, update, and delete events.
   - Can view all bookings for their events.

2. **Customer (Event Attendee):**
   - Can view a list of upcoming events.
   - Can view event details and book tickets.
   - Can manage (view/cancel) their own bookings.

---

## 📦 Functional Requirements

### 🗓️ Events
- An **event** should have:
  - `id`: UUID
  - `title`: string
  - `description`: string
  - `location`: string
  - `date`: DateTime
  - `capacity`: number (max attendees)
  - `price`: number

### ✅ Booking
- Users can book tickets for available events.
- Prevent overbooking (no more bookings once capacity is reached).
- Users can cancel their bookings.

### 🔐 Authentication
- Support **JWT-based authentication**.
- Admins and Customers should have different access levels.

### 🔄 API Endpoints
- **Public**
  - `GET /events` - List all upcoming events.
  - `GET /events/:id` - Get details for a specific event.
  - `POST /auth/register` - Register a new user.
  - `POST /auth/login` - Login and get JWT.

- **Customer Protected**
  - `POST /bookings` - Book a ticket.
  - `GET /bookings` - View my bookings.
  - `PUT /bookings/:id` - Cancel my booking.

- **Admin Protected**
  - `POST /events` - Create a new event.
  - `PUT /events/:id` - Update an event.
  - `GET /events/:id/bookings` - View all bookings for an event.

---

## 🛠 Tech Stack

### Backend
- Node.js + Express (with TypeScript)
- PostgreSQL (or MongoDB)
- TypeORM or Prisma
- JWT for authentication

### Frontend
- React (with TypeScript)
- TailwindCSS or Material-UI for styling is allowed

---

## ✨ Bonus Features (Optional)
- Payment integration for paid events.
- Email notifications for booking confirmation/cancellation.
- Pagination & filtering for events list.
- Admin dashboard UI with charts for event attendance.
- React Query (or SWR) for API calls
- Form management with React Hook Form
- If applicable, host on AWS EC2 (free tier)

---

## 📂 Deliverables
1. **Frontend** and **Backend** source code in a GitHub repository.
2. Tests on the backend at least 65% coverage
3. A README with:
   - Setup instructions.
   - API documentation (or Postman collection).

---

## ⚡ Challenge Expectations
This challenge is aimed at evaluating:
- Backend API design & database modeling.
- Frontend state management & component architecture.
- Authentication & role-based access control.
- Clean, reusable, and well-documented code.

