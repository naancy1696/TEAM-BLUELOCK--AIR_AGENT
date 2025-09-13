# Week 1 Smoke Test - End-to-End Flight Booking

This is a manual test of the mock MediMate flight booking prototype using sample JSON data and NLU seeds.

---

## Test 1: Book Flight from Bengaluru (BLR) to Delhi (DEL)

2025-09-12T14:00:00+05:30 - intent_detected: book_flight  
slots_captured: origin_iata=blr, destination_iata=del, depart_date=2025-10-12, pax_adults=1, pax_children=0, cabin_class=economy  
selected_flight_id: fl_001  
fare_family: saver  
payment_reference_stub: pay_ZX1_001  
pnr: ZX1AB2  

2025-09-12T14:01:00+05:30 - intent_detected: check_status  
slots_captured: pnr=ZX1AB2  
status: confirmed  

2025-09-12T14:02:00+05:30 - intent_detected: cancel_booking  
slots_captured: pnr=ZX1AB2  
cancellation_fee: 500  
refund_amount: 11950  

---

## Test 2: Book Flight from Delhi (DEL) to Mumbai (BOM)

2025-09-12T15:00:00+05:30 - intent_detected: book_flight  
slots_captured: origin_iata=del, destination_iata=bom, depart_date=2025-10-13, pax_adults=2, pax_children=1, cabin_class=business  
selected_flight_id: fl_002  
fare_family: flexi  
payment_reference_stub: pay_ZX1_002  
pnr: AB123C  

2025-09-12T15:02:00+05:30 - intent_detected: check_status  
slots_captured: pnr=AB123C  
status: confirmed  

2025-09-12T15:03:00+05:30 - intent_detected: cancel_booking  
slots_captured: pnr=AB123C  
cancellation_fee: 1000  
refund_amount: 17640  

---

## Test 3: Book Flight from Hyderabad (HYD) to Chennai (CHE)

2025-09-12T16:00:00+05:30 - intent_detected: book_flight  
slots_captured: origin_iata=hyd, destination_iata=che, depart_date=2025-10-14, pax_adults=1, pax_children=1, cabin_class=economy  
selected_flight_id: fl_003  
fare_family: flexi  
payment_reference_stub: pay_ZX1_003  
pnr: ZX9YB3  

2025-09-12T16:01:00+05:30 - intent_detected: check_status  
slots_captured: pnr=ZX9YB3  
status: confirmed  

2025-09-12T16:02:00+05:30 - intent_detected: cancel_booking  
slots_captured: pnr=ZX9YB3  
cancellation_fee: 3000  
refund_amount: 11240  

---

### Notes:
- All timestamps are in ISO format with timezone.  
- Payment responses are mocked using `payment_stub.md`.  
- Cancellation fees are applied based on `fare_rules.json`.  
- This log validates that booking, status check, and cancellation flows work correctly with seeded NLU utterances.
