# Railway Reservation System

A modern, web-based railway reservation system built with Streamlit and SQLite. This application provides a comprehensive solution for managing train bookings, seat reservations, and train administration.

##  Features

### Train Management
- **Add New Trains**: Add trains with details like train number, name, departure date, and destinations
- **View All Trains**: Display all available trains in the system
- **Search Trains**: Search trains by train number or by source and destination
- **Delete Trains**: Remove trains from the system

### Ticket Booking & Management
- **Book Tickets**: Reserve seats with passenger details (name, age, gender)
- **Seat Selection**: Choose from different seat types (Window, Aisle, Middle)
- **Cancel Tickets**: Cancel existing reservations
- **View Seats**: Display seat availability and passenger details for any train

### Smart Seat Allocation
- **Automatic Seat Categorization**: Seats are automatically categorized as Window, Aisle, or Middle
- **Intelligent Booking**: System automatically allocates the next available seat of the requested type
- **Real-time Availability**: Check seat availability in real-time

##  Technology Stack

- **Frontend**: Streamlit (Python web framework)
- **Database**: SQLite (Lightweight, serverless database)
- **Data Processing**: Pandas (Data manipulation and analysis)
- **Language**: Python 3.x

##  Prerequisites

Before running this application, make sure you have the following installed:

- Python 3.9 or higher
- pip (Python package installer)

##  Installation & Setup

1. **Install required dependencies**
   ```bash
   pip install -r requirements.txt
   ```

2. **Run the application**
   ```bash
   streamlit run main.py
   ```

3. **Access the application**
   - Open your web browser
   - Navigate to `http://localhost:8501`
   - The application will automatically create the database and required tables

##  How to Use

### For Administrators

1. **Adding a Train**
   - Select "Add Train" from the sidebar
   - Fill in train details (number, name, date, destinations)
   - Click "Add Train" to create the train and its seat layout

2. **Managing Trains**
   - Use "View Trains" to see all available trains
   - Use "Search Train" to find specific trains
   - Use "Delete Train" to remove trains from the system

3. **Booking Management**
   - Use "Book Ticket" to make reservations
   - Use "Cancel Ticket" to cancel existing bookings
   - Use "View Seats" to check seat availability and passenger details

### Seat Allocation Logic

The system uses a smart seat categorization algorithm:
- **Window Seats**: Seats ending in 0, 4, 5, 9
- **Aisle Seats**: Seats ending in 2, 3, 6, 7
- **Middle Seats**: All other seats

Each train has 50 seats, and the system automatically allocates the next available seat of the requested type.

**Happy Traveling!**
