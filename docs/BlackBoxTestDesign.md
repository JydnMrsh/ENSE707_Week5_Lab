Equivalence partitions for doctor slots:
--

| Partition | Description | Representative Value |
| -------- | -------- | -------- |
| P1 - Invalid  | Negative slot count | -1 |
| P2 - Unavailable  | Zero slot count | 0 |
| P3 - Available | Positive slot count | 5 |

\
Boundary values around the change from invalid/unavailable/available slot counts:
--

| Partition | Description | Representative Value |
| -------- | -------- | -------- |
| Invalid -> Unavailable  | -1 (Invalid) / 0 (Valid, unavailable) | -1 should be rejected (cannot even represent a doctor); 0 should be accepted as a valid Doctor, but that doctor cannot take a booking |
| Unavailable -> Available  | 0 (Unavailable) / 1 (Valid, available) | 0 slots means booking should fail. 1 slot means booking should succeed. |