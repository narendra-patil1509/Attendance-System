# ONATTENDI - Digital Marketing Attendance Portal

A fully featured, real-time Employee Attendance Management system tailored for the **ONATTENDI Digital Marketing** ecosystem. It features live QR code scanning, manual entry overrides, bulk employee updates via Excel, and dynamic attendance reports.

## 🚀 Features

### **Admin Dashboard**
- **Strict Session Isolation**: Prevents concurrent logins across tabs using localized `sessionStorage`.
- **Live QR Scanner**: Uses Socket.io to instantly receive and verify employee check-ins in real-time.
- **Manual Entry**: Search and manually approve or reject employee attendance records.
- **Manage Employees**: Securely upload and sync `.xlsx` employee databases via drag-and-drop.
- **Attendance Reports**: View, search, filter, and export daily attendance logs directly to Excel.

### **Employee Portal**
- Generate dynamic QR codes for check-in that expire automatically.
- Receive real-time push confirmations indicating approval or rejection of attendance.

---

## 🛠️ Technology Stack

- **Frontend**: React (Vite), Tailwind CSS v4, Shadcn UI Components, Lucide Icons, Axios.
- **Backend**: Node.js, Express.js, MySQL.
- **Real-Time Communication**: Socket.IO.
- **Authentication**: JWT (JSON Web Tokens).
- **File Parsing**: Multer, ExcelJS.

---

## ⚙️ Installation & Setup (Step-by-step)

### 1. Database Configuration
1. Install **MySQL** (e.g., via XAMPP or native installer).
2. Start the MySQL service.
3. The backend script will automatically attempt to create the `attendance_db` database and its necessary tables (`admins`, `employees`, `attendance`) upon starting.

### 2. Backend Setup
1. Open a terminal and navigate to the backend directory:
   ```bash
   cd backend
   ```
2. Install the required Node.js dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file in the `backend` folder and configure the following variables:
   ```env
   PORT=yourPORT
   DB_HOST=YOURHOST
   DB_USER=YOURUSER
   DB_PASSWORD=YOURPASSWORD
   DB_NAME=YOURDBNAME
   JWT_SECRET=your_super_secret_jwt_key
   ```
4. Start the backend server:
   ```bash
   # For development (auto-reloads on file changes string)
   npm run dev
   # Or standard start
   npm start
   ```
   > You should see a success message indicating the database is connected and tables are synchronized.

### 3. Frontend Setup
1. Open a new terminal window and navigate to the frontend directory:
   ```bash
   cd frontend
   ```
2. Install the frontend dependencies:
   ```bash
   npm install
   ```
3. Start the Vite development server:
   ```bash
   npm run dev
   ```
4. The application will be available at `http://localhost:5173`.

---

## 📖 Usage Guide

1. **Initial Access**: 
   - Visit `http://localhost:5173/admin/signup` to securely create your first ONATTENDI Administrator account.
2. **Setup Employees**:
   - Go to the **Manage Employees** tab and upload your `.xlsx` employee database.
3. **Daily Operations**:
   - Leave the `http://localhost:5173/admin/dashboard` on the **Live Scanner** screen at your front desk.
   - Employees visit the main page (`http://localhost:5173/`) on their mobile devices to generate and present their daily QR.
4. **End of Day**:
   - Navigate to the **Report** tab to search, review, and export the day's total attendance directly to Excel!

---

*Designed and Developed for ONATTENDI Digital Marketing.*
