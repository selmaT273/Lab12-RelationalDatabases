# Lab12-RelationalDatabases
Entity Relationship Diagram for hotel chain

# Entity Relationship Diagram
[Hotel Chain](HotelERD.jpg)

# Entity Relationship Diagram Explained

## Hotel
- Hotel table contains a HotelID (primary key), name, address, and phone number. It has a "1 : many" relationship with the other tables because each hotel has many rooms, several guests, varying room types, etc but they all belong to one hotel.

## Rooms
- Rooms table has a room number column as a primary key, room type, and hotelID is a foreign key back to the primary key on the hotel table. It has a 1 : many relationship with guests, a 1 : 1 relationship to room type, and  a many : 1 relationship with hotel.

## Room Type
- Room type table has a room type id which is a primary key, name, amenities, price, occupant limit, and hotelId (foreign key to hotel table). It has a 1 : many relationship with rooms and a many : many relationship with amenities.

## Amenities
- Ameneties table has an amenities id as its primary key and name. It has a many : many relationship with room type.

## Guests
- Guests table has guestID as a primary key, name, room number, booking id, and hotel id as a foreign key to hotel table. Guests has a many : 1 relationship with hotel and rooms, and a 1 : 1 relationship with bookings.

## Bookings
- Bookings table has a bookingId as a Primary Key, start date, duration of stay, guest ID (foreign key to guests table), total cost, room number (foreign key to rooms table), and HotelID (foreign key to hotel table). Bookings has many : 1 relationship with hotel, many : 1 relationship with guests, and 1 : many relationship with rooms.