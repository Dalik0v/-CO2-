# -CO2-


+-------+         --> REST         +---------------+         --> REST         +---------------+
| ESP32 | -----------------------> |     Backend   | -----------------------> |    Frontend   |
|Sensor |                          |      (BE)     |                          |      (FE)     |
+-------+                          +---------------+                          +---------------+
                                        |
                                        |
                                        v
                                 +---------------+
                                 |   Database    |
                                 +---------------+

+-------------------+      +-------------------+      +-------------------+
|   Measurements    |      |      Devices      |      |       Users       |
+-------------------+      +-------------------+      +-------------------+
| measurement_id PK |      | device_id PK      |      | user_id PK        |
| device_id FK      |      | name              |      | username          |
| timestamp         |      | location          |      | password_hash     |
| temperature       |      | registered        |      +-------------------+
| CO2               |      | user_id FK        |
| humidity          |      +-------------------+
+-------------------+

