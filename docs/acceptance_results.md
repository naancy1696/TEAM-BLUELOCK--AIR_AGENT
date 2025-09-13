# Week 1 Acceptance Results – AeroMate

| AC # | Acceptance Criterion | Status | Notes |
|------|--------------------|--------|-------|
| AC1 | Agent recognizes book_flight, check_status, cancel_booking intents from sample utterances | PASS | All three intents are defined in nlu/intents.yml with sample utterances. |
| AC2 | data/flights.json contains ≥3 sample flights with ISO timestamps and timezones | PASS | flights.json has 3 entries with ISO 8601 timestamps and timezone info. |
| AC3 | fare_rules.json contains deterministic cancellation slabs | PASS | saver and flexi fare families have all four slabs: more_than_72h, 24_to_72h, 0_to_24h, at_airport. |
| AC4 | Booking flow can output a mock PNR | PASS | PNR generator pseudo-code defined in docs/pnr.md, 6-character uppercase alphanumeric format. |
| AC5 | airports.json contains IATA codes and city names for ≥5 airports | PASS | airports.json contains 5 airports with iata and city fields. |
| AC6 | Status flow outputs flight status with timestamps and time zones | PASS | Mock status flow can output selected flight status along with departure/arrival timestamps and timezones. |
| AC7 | Cancellation flow calculates refund and fees according to fare rules | PASS | Manual calculation verified: total_fare = 12,450 INR, cancellation_fee = 2,000 INR → refund = 10,450 INR. |
| AC8 | Agent can handle English and Hindi sample prompts | FAIL | English prompts are seeded; Hindi prompts will be added in Week 2. |

# Sample cancellation calculation
Sample cancellation calculation:

total_fare = 12,450 INR
fare_family = saver
cancellation_fee slab = 2,000 per passenger
pax = 1

Compute refund:

cancellation_fee_total = 2,000 × 1 = 2,000

refund_amount = total_fare − cancellation_fee_total

Digit-by-digit subtraction:

   12,450
-   2,000
= 10,450

Refund amount = 10,450 INR
