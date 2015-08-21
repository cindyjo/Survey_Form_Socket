# Survey Form Socket

An application that hs the form for the user to fill out

- The user fills out the form and submits.
- The form information is EMITTED to the server with the event name "posting_form".
- The server listens for an event 'posting_form' and when this event gets triggered, organizes all the emitted information to form a single message and sends this single message with the event called 'updated_message'. It also EMITs an event called 'random_number' with random number between 1-1000.
- The client listens for an event called 'random_number' and when this event gets triggered, shows the number in the HTML.
- The client listens for an event called 'updated_message' and when this event gets triggered, displays the message somewhere in the HTML.