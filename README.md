# Railway Reservation System

A modern, web-based railway reservation system built with Streamlit and SQLite. This application provides a comprehensive solution for managing train bookings, seat reservations, and train administration.

## 🚂 Features

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

## 🛠️ Technology Stack

- **Frontend**: Streamlit (Python web framework)
- **Database**: SQLite (Lightweight, serverless database)
- **Data Processing**: Pandas (Data manipulation and analysis)
- **Language**: Python 3.x

## 📋 Prerequisites

Before running this application, make sure you have the following installed:

- Python 3.7 or higher
- pip (Python package installer)

## 🚀 Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/railway-reservation-stream.git
   cd railway-reservation-stream
   ```

2. **Install required dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application**
   ```bash
   streamlit run main.py
   ```

4. **Access the application**
   - Open your web browser
   - Navigate to `http://localhost:8501`
   - The application will automatically create the database and required tables

## 📊 Database Schema

The application uses SQLite with the following tables:

### Users Table
- `username` (TEXT): User login name
- `password` (TEXT): User password

### Employees Table
- `employee_id` (TEXT): Employee identifier
- `password` (TEXT): Employee password
- `designation` (TEXT): Employee role/position

### Trains Table
- `train_number` (TEXT): Unique train identifier
- `train_name` (TEXT): Name of the train
- `departure_date` (TEXT): Date of departure
- `starting_destination` (TEXT): Source station
- `ending_destination` (TEXT): Destination station

### Seats Table (Dynamic)
For each train, a separate seats table is created (`seats_{train_number}`):
- `seat_number` (INTEGER): Seat identifier (1-50)
- `seat_type` (TEXT): Window/Aisle/Middle
- `booked` (INTEGER): Booking status (0/1)
- `passenger_name` (TEXT): Name of the passenger
- `passenger_age` (INTEGER): Age of the passenger
- `passenger_gender` (TEXT): Gender of the passenger

## 🎯 How to Use

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

## 📁 Project Structure

```
railway-reservation-stream/
├── main.py                 # Main application file
├── requirements.txt        # Python dependencies
├── railway_system.db       # SQLite database (auto-generated)
└── README.md              # This file
```

## 🔧 Configuration

The application automatically:
- Creates the SQLite database (`railway_system.db`) on first run
- Sets up all required tables
- Initializes seat layouts for new trains

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🐛 Bug Reports

If you find a bug, please open an issue with:
- A clear description of the problem
- Steps to reproduce the issue
- Expected vs actual behavior
- Screenshots (if applicable)

## 🚀 Future Enhancements

- [ ] User authentication system
- [ ] Payment integration
- [ ] Email notifications
- [ ] Mobile-responsive design
- [ ] Advanced search filters
- [ ] Train schedule management
- [ ] Multi-language support
- [ ] Admin dashboard with analytics

## 📞 Support

If you have any questions or need help, please:
- Open an issue on GitHub
- Check the existing issues for solutions
- Contact the maintainers

---

**Happy Traveling! 🚂✨**
