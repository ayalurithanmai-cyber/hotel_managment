
# Hotel Management System - Java

A comprehensive hotel management system built with Java featuring room booking, food ordering, and billing.

## Project Structure

```
hotel-management-java/
│
├── README.md
├── Main.java             (Entry point)
├── Hotel.java            (Core hotel operations)
├── Food.java             (Food model)
├── Singleroom.java       (Single room model)
├── Doubleroom.java       (Double room model)
├── holder.java           (Data holder for serialization)
├── NotAvailable.java     (Custom exception)
└── write.java            (Thread for data persistence)
```

## Features

- **Room Management**
  - 4 types of rooms: Luxury Double, Deluxe Double, Luxury Single, Deluxe Single
  - 60 total rooms (10 luxury double, 20 deluxe double, 10 luxury single, 20 deluxe single)
  
- **Booking System**
  - Check room availability
  - Book rooms with customer details
  - Support for single and double occupancy
  
- **Food Ordering**
  - In-room food service
  - Menu items: Sandwich (₹50), Pasta (₹60), Noodles (₹70), Coke (₹30)
  
- **Billing & Checkout**
  - Automated bill generation
  - Combined room charges and food charges
  - Checkout process with payment summary
  
- **Data Persistence**
  - Serialization for data backup
  - Auto-save on exit
  - Load previous data on startup

## Room Details

### Luxury Double Room (Rooms 1-10)
- Double bed: 1
- AC: Yes
- Free breakfast: Yes
- Charge: ₹4000/day

### Deluxe Double Room (Rooms 11-30)
- Double bed: 1
- AC: No
- Free breakfast: Yes
- Charge: ₹3000/day

### Luxury Single Room (Rooms 31-40)
- Single bed: 1
- AC: Yes
- Free breakfast: Yes
- Charge: ₹2200/day

### Deluxe Single Room (Rooms 41-60)
- Single bed: 1
- AC: No
- Free breakfast: Yes
- Charge: ₹1200/day

## Compilation & Execution

### Compile all files:
```bash
javac *.java
```

### Run the application:
```bash
java Main
```

## Usage

1. **Display Room Details** - View features and pricing of different room types
2. **Display Room Availability** - Check how many rooms are available
3. **Book a Room** - Reserve a room with customer details
4. **Order Food** - Place food orders for occupied rooms
5. **Checkout** - Check out and generate bill
6. **Exit** - Save data and exit application

## Technical Details

- **Language**: Java
- **Persistence**: Object serialization
- **Threading**: Multi-threaded data saving
- **Exception Handling**: Custom exceptions for booking validation

## File Descriptions

- **Main.java**: Application entry point with main menu loop
- **Hotel.java**: Contains all business logic for hotel operations
- **Food.java**: Model class for food items with pricing
- **Singleroom.java**: Model for single occupancy rooms
- **Doubleroom.java**: Model for double occupancy rooms (extends Singleroom)
- **holder.java**: Container class for all room arrays
- **NotAvailable.java**: Custom exception for room unavailability
- **write.java**: Runnable thread for saving data to backup file

## Data Persistence

The application automatically:
- Loads previous data from `backup` file on startup
- Saves all data to `backup` file on exit using a separate thread

## GitHub Setup

```bash
# Initialize repository
git init

# Add all files
git add *.java README.md

# Commit
git commit -m "Initial commit: Hotel Management System"

# Add remote and push
git remote add origin https://github.com/YOUR-USERNAME/hotel-management-java.git
git branch -M main
git push -u origin main
```

## Example Usage Flow

```
1. Start application
2. Choose option 3 (Book a room)
3. Select room type (e.g., 1 for Luxury Double Room)
4. Enter available room number
5. Provide customer details
6. Choose option 4 (Order food)
7. Enter room number
8. Select food items and quantities
9. Choose option 5 (Checkout)
10. Enter room number to checkout
11. View bill and confirm checkout
```

## Future Enhancements

- GUI implementation
- Database integration
- Payment gateway integration
- Room service management
- Employee management
- Reporting and analytics
- Online booking system
- Customer loyalty program

## Contributing

Feel free to fork this project and submit pull requests for any improvements.

## License

MIT License

## Author

Your Name

## Contact

For questions or suggestions, please open an issue on GitHub.
