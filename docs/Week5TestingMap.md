
====================================

***Existing test/evidence:*** Doctor: negative slots\
***Level:*** Unit\
***Type/Focus:*** Input validation/Guard clause for the doctor available slots\
***Technique/Perspective:*** Black box, negative testing, boundary value analysis\
***What it provides evidence for:*** That the doctor object doesn't construct with a negative slot count.\
***Important gap:*** It doesn't test at the boundry, ie. when the slots = 0

====================================

***Existing test/evidence:*** Booking: no slots\
***Level:*** Unit\
***Type/Focus:*** Input validation/Guard clause for the booking available slots\
***Technique/Perspective:*** Black box, boundary value analysis\
***What it provides evidence for:*** That a booking isn't created when a doctor has no available slots\
***Important gap:*** Doesn't return a helpful message if the booking fails for a different reason.

====================================

***Existing test/evidence:*** Patient: preffered display name\
***Level:*** Unit\
***Type/Focus:*** Functional\
***Technique/Perspective:*** Black box, equivalence partitioning\
***What it provides evidence for:*** That a patient's preferred name is correctly prioritized over their legal name when one is present\
***Important gap:*** Doesn't cover the case where the preferred name is empty space, or special characters.

====================================

***Existing test/evidence:*** Request: appointment date in past\
***Level:*** Unit\
***Type/Focus:*** Input validation/Guard clause \
***Technique/Perspective:*** Black box, boundary value analysis\
***What it provides evidence for:*** That a request with an appointment date in the past is rejected\
***Important gap:*** No tests for a date that is exactly the current date, same day, or for a date that is far in the future.

====================================

***Existing test/evidence:*** Booking: helpful success message\
***Level:*** Unit\
***Type/Focus:*** Functional/Output validation\
***Technique/Perspective:*** Black box, content assertion\
***What it provides evidence for:*** That a helpful success message is displayed when a booking is created successfully\
***Important gap:*** If the preferred name doesn't set correctly, then the test will fail because it's comparing the outputted display name.

====================================

***Existing test/evidence:*** Booking: decreases slot count\
***Level:*** Unit\
***Type/Focus:*** Functional/State based verification\
***Technique/Perspective:*** White box, state verification\
***What it provides evidence for:*** That the slot count is correctly decreased when a booking is created\
***Important gap:*** It doesn't verify that the slot count is decreased by the correct amount or that it doesn't go below zero.