# Sample Log Format

timestamp: 2025-09-12T14:00:00+05:30
user_input: "Book a flight from BLR to DEL on 12 Oct for 2 adults"
intent_detected: book_flight
slots_captured:
  origin_iata: "blr"
  destination_iata: "del"
  depart_date: "2025-10-12"
  pax_adults: 2
  cabin_class: "economy"
selected_flight_id: "fl_001"
pnr_generated: "ZX1AB2"
payment_stub: {"payment_reference_stub":"pay_ZX1_001","status":"success"}
decision_reason: "Selected cheapest saver fare"
