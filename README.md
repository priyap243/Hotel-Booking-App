# Hotel Booking App

This Python application allows users to book a hotel, validate credit card details, and even add a spa package to their reservation. The app provides an interactive experience for users looking to book a stay at a hotel and enjoy additional amenities.

## Prerequisites

* Python 3.x
  
* pandas library (installed via requirements.txt)

## Usage

1. Clone the repository or download the files: `main.py`, `hotels.csv`, `cards.csv`, and `card_security.csv`.
   
2. Install all dependencies:
   
```bash
pip install -r requirements.txt
```

3. Run the application:
   
```bash
python main.py
```

## Description

* `main.py`: The main Python script that runs the hotel booking process. It includes classes for managing hotels, reservations, credit card validation, and spa bookings.
  
* `hotels.csv`: A CSV file containing hotel information such as ID, name, city, capacity, and availability status.
  
* `cards.csv`: A CSV file storing credit card details for validation.
  
* `card_security.csv`: A CSV file storing the authentication details (passwords) for secure credit card validation.

## How it works

1. The app starts by loading the hotel data from the `hotels.csv` file and lists the available hotels.

2. Users are prompted to enter the hotel ID they wish to book.
   
3. If the selected hotel is available, the user is asked to enter their credit card details.
   
4. The app validates the card information using the data in `cards.csv` and performs a secure authentication through the `card_security.csv` file.
   
5. If the payment and authentication are successful, the hotel booking is confirmed and saved.
   
7. The user can choose to book a spa package, and if they confirm, a separate spa reservation ticket is generated.
   
## Classes

* **Hotel**: Represents a hotel and provides methods to check availability and book the hotel.
  
* **SpaHotel**: A subclass of `Hotel` that adds functionality for booking spa packages (currently not implemented).
  
* **ReservationTicket**: Generates a booking ticket with the customer's name and hotel details.
  
* **CreditCard**: Handles credit card validation and checks whether a card exists in the `cards.csv` file.
  
* **SecureCreditCard**: A subclass of `CreditCard` that adds authentication via password.
  
* **SpaTicket**: Generates a spa booking ticket with the customer's name and hotel details.
  
## Configuration

* Ensure the `hotels.csv`, `cards.csv`, and `card_security.csv` files exist in the same directory as the app files.
  
* Modify the CSV files to add more hotel, card, and security details as needed.
  
## Example CSV Data

**hotels.csv**

```csv
id,name,city,capacity,available
134,Tourist Sunny Apartment,Anchorage,4,no
188,Snow Palace,New Delhi,5,no
655,City Break Inn,Porto-Novo,3,no
```
**cards.csv**

```csv
number,expiration,cvc,holder
1234567890123456,12/26,123,JOHN SMITH
5678,12/28,456,JANE SMITH
```

**card_security.csv**

```csv
number,password
1234567890123456,mypass
```
## Author 

Priya Patel 

Github: priyap243
