# Acceptance Criteria – Airline AI Agent Prototype

AC1: Agent recognizes `book_flight`, `check_status`, and `cancel_booking` intents from sample utterances.

AC2: `data/flights.json` contains ≥3 sample flights with ISO timestamps and time zones.

AC3: `data/fare_rules.json` contains deterministic cancellation slabs with clear refund calculations.

AC4: Booking flow can generate a mock PNR for each flight reservation.

AC5: `data/airports.json` contains IATA codes, city names, and airport names for ≥5 airports.

AC6: Status flow outputs flight status (scheduled, delayed, departed, landed, canceled) with timestamps and time zones.

AC7: Cancellation flow calculates refund and fees according to fare rules and outputs a clear summary.

AC8: Agent can respond to user queries in both English and Hindi sample prompts.
