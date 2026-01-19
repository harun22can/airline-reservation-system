## Airline Ticket Reservation and Management System

This project is a comprehensive system that manages airline ticket sales processes for both the **passenger side** and the **administrative (admin) side**.  
The project includes a **Java-based console reservation system** as well as **modern web interfaces** (passenger interface and admin panel).

---

### 🚀 Features

- **Console-Based Airline Ticket System (Java)**
  - List available flights
  - Route search (by departure/arrival cities)
  - Single ticket purchase
  - Multiple ticket purchase
  - List active tickets
  - Ticket cancellation
  - Admin login and admin menu:
    - System statistics
    - View all reservations
    - Generate reports by date range
    - Flight-based occupancy rates
    - List top-spending customers

- **Web Passenger Interface (`index.html` + `app.js`)**
  - City-based flight search
  - Step-by-step ticket purchasing flow:
    - Passenger information (ID, name, surname, email, phone, ticket type, etc.)
    - Flight and cabin class selection (Business / Economy)
    - Advanced seat map with:
      - Random seat assignment (free)
      - Manual seat selection (+100 TL)
    - Payment step (mock Visa / MasterCard form)
  - Single and multiple ticket purchase flows
  - Online check-in module:
    - Reading and accepting flight rules
    - Mini quiz related to flight rules
  - Listing active and cancelled tickets
  - Campaign code support and discount calculation
  - Multi-language support (🇬🇧 English, 🇹🇷 Turkish, 🇸🇦 Arabic)
  - Weather component (displays warnings based on weather conditions)
  - Modern UI:
    - Video background header (`plane.mp4`)
    - Seat map, payment summary, and notification components
    - Chatbot (“Flight Assistant”) for guidance
    - Cookie consent and notification component

- **Admin Panel (`admin-dashboard.html` + `admin-dashboard-real.js`)**
  - Login screen (username/password)
  - Role-based menu (super_admin, operations, accounting)
  - Dashboard:
    - Total number of reservations
    - Active flights
    - Occupancy rate
    - Daily / monthly revenue
    - Cancellation rate
    - Charts using Chart.js (revenue, reservation trends, most used routes)
  - Flight management:
    - Flight listing
    - Add / edit flights (frontend-side simulation)
  - Aircraft and seat management
  - Reservation management
  - Passenger management
  - Pricing and campaign management
  - Payments and accounting view
  - Notification and announcement broadcasting (designed for future email integration)
  - Admin user and role management, logging records
  - Reporting tab (profitable routes, occupancy, cancellation reports)
  - System settings (currency, time zone, tax rate, maintenance mode)

---

### 🧩 Project Structure (Summary)

- **Java (Console Application)**
  - `Main.java` – Entry point, user menus, and admin panel flow
  - `FlightBookingSystem.java`, `Flight.java`, `Reservation.java`, `Ticket.java`, `Passenger.java`, `Seat.java`, `SeatClass.java`, `TicketType.java`, etc.
  - `AirportData.java` – City/route data
  - `ReservationPriorityQueue.java` – Prioritized reservation structure
  - `EmailService.java` – Email sending logic (JavaMail)
  - `Admin.java`, `AdminDashboard.java`, `AdminPanel.java` – Administrative functionalities
  - `PassengerNameValidator.java` – Name validation

- **Web Interfaces**
  - Passenger side:
    - `index.html`
    - `app.js`
    - `plane.mp4` (background video)
  - Admin side:
    - `admin-dashboard.html`
    - `admin-dashboard.css`
    - `admin-dashboard-real.js`

- **Maven Configuration**
  - `pom.xml`  
    - Java 8 target
    - `javax.mail` (JavaMail API)
    - `javax.activation` dependencies

---

### 🛠 Technologies Used

- **Backend / Business Logic**
  - Java 8
  - Maven project structure
  - JavaMail (`javax.mail`) for email delivery

- **Frontend**
  - HTML5, CSS3, JavaScript (Vanilla)
  - Chart.js (for data visualization)
  - Axios (for HTTP requests – prepared for future backend integration)
  - Responsive, modern UI design

---

### 🔧 Installation and Execution

#### 1. Java Console Application

1. **Clone the repository:**
  
   git clone <repository-url>
   cd MODUL_PROJECT/modul

2. **Compile with Maven:**
  
   mvn compile

3. **Run using an IDE:**
   - Open the project as a **Maven project** in IntelliJ IDEA / Eclipse / VS Code.
   - Locate `Main.java`.
   - Run the `main` method (`Run Main.main()`).

4. **Run via command line (basic method):**
  
   cd MODUL_PROJECT/modul/src/main/java  
   javac Main.java  
   java Main  

   > Note: Depending on your directory structure, classpath configuration may be required. Using an IDE is generally the easiest approach.

---

#### 2. Web Passenger Interface

1. Locate `index.html` in the `MODUL_PROJECT/modul` directory.
2. Open `index.html` in a web browser (Chrome, Edge, Firefox, etc.).
3. Ensure that `plane.mp4` is located in the same directory as `index.html`.

> For a more professional setup, you may use a simple HTTP server (e.g., VS Code Live Server, `npx serve`, etc.).

---

#### 3. Admin Panel

1. Locate `admin-dashboard.html` in the `MODUL_PROJECT/modul` directory.
2. Open it in a web browser.
3. Ensure that `admin-dashboard.css` and `admin-dashboard-real.js` are in the same directory.

> Currently, the admin panel is a front-end simulation; it can be fully functional by integrating a real REST API.

---

### ✉️ Email and JavaMail

The project includes JavaMail integration via `EmailService.java` to send **ticket confirmations** or **notification emails**.  
For real-world usage:

- Configure SMTP server details (host, port, username, password),
- Optionally move configuration values to an external configuration file.

---

### 📚 Report (Documentation)

The file `MODULE_REPORT (3).pdf` is located in the `Report` folder.  
This report provides detailed analysis, design decisions, and usage scenarios of the project.

---

### 👤 Developers

- **Dila Kübra DİRİCANLI** – `230201039@sivas.edu.tr`  
- **Harun Can ELİAÇIK** – `230201043@sivas.edu.tr`  
- **Rümeysa YÜCEL** – `230201077@sivas.edu.tr`

---

### 📄 License

This project was developed as a **course/module project**.  
License information has not been added yet and can be updated via the `LICENSE` file on GitHub.
