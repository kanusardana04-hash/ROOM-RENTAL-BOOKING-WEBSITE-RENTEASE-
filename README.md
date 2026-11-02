# RentEase – Room Rental Booking Website

RentEase is a responsive, multi-page room rental website built with **HTML, CSS and vanilla JavaScript**. Users can search rooms by location and budget, view room details, submit a booking request, and track or cancel it. An admin dashboard lets the administrator approve or reject requests and read customer messages.

This is a client-side project made as a Web Programming mini project at Chandigarh University. It has no backend or database. All data is stored in the browser's `localStorage`.

## Features

- Search rooms by location and maximum monthly rent (Home page and Explore Rooms page)
- Room details page (the room id is passed in the URL, e.g. `details.html?id=1`)
- Booking form with validation:
  - 10-digit mobile number
  - past move-in dates are blocked
- Unique booking ID (`RE` + timestamp) and a status for every request: **Pending**, **Approved**, **Rejected** or **Cancelled**
- Booking confirmation page
- My Bookings page to track and cancel requests
- Contact form that saves customer messages
- Admin dashboard with total bookings, pending requests, message count, and Approve / Reject buttons
- Responsive layout for desktop, tablet and mobile

## Pages

| File | Description |
|------|-------------|
| `index.html` | Home page with hero section, search form and featured properties |
| `rooms.html` | Explore Rooms with location and budget filters |
| `details.html` | Details of the selected room |
| `booking.html` | Booking request form |
| `confirmation.html` | Booking confirmation with booking ID |
| `mybookings.html` | Booking history, status and cancellation |
| `contact.html` | Contact form |
| `admin.html` | Admin dashboard (has its own styles and script) |

## Technologies Used

- HTML5
- CSS3 (Grid, Flexbox, media queries)
- JavaScript (ES6)
- Browser `localStorage` (JSON)
- Images from [Unsplash](https://unsplash.com)


## How to Run

1. Download or clone the repository:
   2. Open the `RentEase` folder.
3. Open `index.html` in a web browser (Chrome, Edge or Firefox).

No installation or server is required. An internet connection is needed only to load the room images.

## How It Works

1. A user searches for a room and opens its details page.
2. Clicking **Book This Room** saves the room in `localStorage` and opens the booking form.
3. After a valid submission, a booking with the status **Pending** is saved and the confirmation page is shown.
4. The user can see the request on **My Bookings** and cancel it.
5. The administrator opens `admin.html` to approve or reject pending requests and read messages.

### localStorage keys

| Key | Content |
|-----|---------|
| `bookings` | Array of all booking requests |
| `latestBooking` | Most recent booking (shown on the confirmation page) |
| `selectedRoom` | Room chosen on the details page |
| `contactMessages` | Messages sent from the contact form |
| `searchLocation`, `searchBudget` | Values typed in the Home page search form |


## Limitations

- Data is saved only in the browser of one device and is not shared between users.
- The admin dashboard has no login.
- Room listings are fixed in `js/script.js`.
- No online payment or email / SMS notification.

## Future Scope

- Backend and database (Node.js with MongoDB, or PHP with MySQL)
- User registration, login and a protected admin login
- Owners can add, edit and delete room listings
- Online payment and email / SMS notifications
- Maps, reviews and more filters

## Author

**Kashish**
UID: 26MCA20152
MCA, University Institute of Computing, Chandigarh University
