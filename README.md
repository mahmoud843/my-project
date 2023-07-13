<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <h1 class="main_head">Hotel Booking Registration</h1>
    <form id="booking-form">
      <!-- customer detials -->
      <h1 class="customer_detials">Customer Detials</h1>
      <section id="customer-detials">
        <div class="form-group">
          <label for="customer-name">Customer Name:</label>
          <input type="text" id="customer-name" required />
        </div>
        <div class="form-group">
          <label for="check-in-date">Check-in Date:</label>
          <input type="date" id="check-in-date" required />
        </div>
        <div class="form-group">
          <label for="total-days">Total No of Days:</label>
          <input type="number" id="total-days" required />
        </div>
        <div class="form-group">
          <label for="total-persons">Total No of Persons:</label>
          <input type="number" id="total-persons" required />
        </div>
      </section>
      <!-- room details -->
      <h1>Select Room Type</h1>
      <section id="room_section">
        <!-- room 1 -->
        <div id="room-photo">
          <img src="IMG/room1.jpg" alt="Room 1" />
          <p>Price: 2500/-</p>
          <label for="deluxe-room">
            <input
              type="radio"
              id="deluxe-room"
              name="room-type"
              value="deluxe"
              required
            />Deluxe Room
          </label>
        </div>
        <!-- room 2 -->
        <div id="room-photo">
          <img src="IMG/room2.jpg" alt="Room 2" />
          <p>Price: 4000/-</p>
          <label for="suite-room">
            <input
              type="radio"
              id="suite-room"
              name="room-type"
              value="suite"
            />Suite Room
          </label>
        </div>
      </section>
      <!-- Amenities -->
      <h1>Select Amenities</h1>
      <section id="amenities">
        <div id="amenities-photo">
          <img src="IMG/AC.png" alt="AC" />
          <p>Price: 1000/-</p>
          <label for="ac"
            ><input type="checkbox" id="ac" value="ac" /> AC</label
          >
        </div>
        <div id="amenities-photo">
          <img src="IMG/locker.png" alt="locker" />
          <p>Price: 300/-</p>
          <label for="locker"
            ><input type="checkbox" id="locker" value="locker" /> Locker</label
          >
        </div>
      </section>
      <!-- Advance Amount -->
      <h1>Advance Amount</h1>
      <div class="form-group">
        <label for="advance-amount">Advance Amount:</label>
        <input type="number" id="advance-amount" required />
      </div>
      <div class="form-group">
        <button type="submit">Register</button>
      </div>
    </form>

    <div id="booking-details" class="hidden">
      <h2>Booking Details</h2>
      <div id="customer-info">
        <p>
          <strong>Customer Name:</strong>
          <span id="customer-name-output"></span>
        </p>
        <p>
          <strong>Check-in Date:</strong>
          <span id="check-in-date-output"></span>
        </p>
        <p>
          <strong>Total No of Days:</strong>
          <span id="total-days-output"></span>
        </p>
        <p>
          <strong>Total No of Persons:</strong>
          <span id="total-persons-output"></span>
        </p>
      </div>
      <div id="room-info">
        <p><strong>Room Type:</strong> <span id="room-type-output"></span></p>
      </div>
      <div id="amenities-info">
        <p><strong>Amenities:</strong> <span id="amenities-output"></span></p>
      </div>
      <div id="booking-info">
        <p>
          <strong>Total Room Cost:</strong>
          <span id="total-room-cost-output"></span>
        </p>
        <p>
          <strong>Total Amenities Cost:</strong>
          <span id="total-amenities-cost-output"></span>
        </p>
        <p>
          <strong>Additional Charges:</strong>
          <span id="additional-charges-output"></span>
        </p>
        <p><strong>Total Cost:</strong> <span id="total-cost-output"></span></p>
        <p>
          <strong>Advance Amount:</strong>
          <span id="advance-amount-output"></span>.hidden {
  display: none;
}

#room_section,
#amenities,
#advance {
  display: flex;
  justify-content: space-around;
  align-items: center;
  border: 0.1rem solid black;
  padding: 1em;
}

#room-photo,
#amenities-photo {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  text-align: center;
}

img {
  width: 50%;
  height: auto;
  margin-right: 10px;
  border-radius: 0.5rem;
}

.form-group {
  display: flex;
  justify-content: space-around;
  align-items: center;
  text-align: center;
  margin-bottom: 10px;
}

button {
  margin-top: 10px;
  background-color: #000;
  color: #fff;
  text-transform: uppercase;
  padding: 10px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #3cff00;
}

h1,
h2 {
  font-family: Poppins, sans-serif;
  margin-bottom: 1rem;
  background-color: #000;
  color: white;
  font-size: 1rem;
  padding: 1em;
  text-align: center;
}

.main_head,
#booking-details {
  background: none;
  color: #000;
  font-size: 1.2rem;
  padding: 0.5em;
  border: 0.1rem solid #000;
}

#booking-details p {
  display: flex;
  justify-content: space-around;
  align-items: center;
}
#booking-details span,
strong {
  width: 50%;
  text-align: start;
}
        </p>
        <p><strong>Balance:</strong> <span id="balance-output"></span></p>
      </div>
    </div>

    <script src="script.js"></script>
  </body>
</html>
