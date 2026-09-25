# Salon Appointment Scheduler

A Bash script that acts as a simple salon booking system, backed by a PostgreSQL database. Built for freeCodeCamp.

## What it does

- Shows a numbered menu of available services
- Asks for the customer's phone number
- If the phone isn't in the database, asks for their name and saves the new customer
- Asks for the appointment time
- Books the appointment and confirms it back to the user
 
## The database

Three tables:

- customers — customer_id, phone (unique), name
- services — service_id, name
- appointments — appointment_id, customer_id, service_id, time

customer_id and service_id in appointments are foreign keys.

## Files

- salon.sh — the interactive booking script
- salon.sql — dump of the database so it can be rebuilt

## Running it

Rebuild the database with salon.sql, then run salon.sh and follow the prompts.

## Example

~~~~~ MY SALON ~~~~~

Welcome to My Salon, how can I help you?
1) cut
2) color
3) perm
4) style
5) trim
1
What's your phone number?
555-555-5555
I don't have a record for that phone number, what's your name?
Fabio
What time would you like your cut, Fabio?
10:30

I have put you down for a cut at 10:30, Fabio.
