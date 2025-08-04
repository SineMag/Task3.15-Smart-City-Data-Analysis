# **TASK 1: The Five V’s of Big Data**


### 1. Variety:
The JSON data sample provided is in structured data since it’s organized and displayed in a certain format. 
Examples: 
(a) The sensor_id is a string and has a specified id for that object. 
(b) The data_source_veracity is also a part of the object, and is a number data-type.

### 2. Velocity:
Managing the velocity of big data is important because it ensures that the flow is quick and data is digested and analyzed quickly, and made available in real-time.

### 3. Veracity:
 The field is likely to represent the possibility of accuracy of the data. If the data_source_veracity is closer to 1, its accuracy becomes higher. The record with a higher problem of veracity is sensory_id: TC-05-GER.

### 4. Volume:
The computing power could limit us from generating and analyzing our big data.

### 5. Value:
Timestamp. This value provides real-time data, making its accuracy higher and its possibility of being reliable higher.


# **TASK 2: Data Quality Assessment**

**Question 1.** 
Data Quality  is the data’s ability to meet the requirements of its purpose, and have zero errors.

**Question 2.** 
The first issue is at the sensory_ids with data accuracy as null or none at all. This makes it hard to know the reliability of the data analysis.
Another issue is the one JSON data having a value with a string or unit while the rest only contain values of numbers. The system might miscalculate the data, return and error, or decrease the level of accuracy.
The last issue is the structure of the date for the timestamp. Even with this too, the computation might be different from the rest, not allowing the data quality to meet its purpose.

**Question 3.** 

    Prompt user to "Enter a date (YYYY-MM-DD)"
    Store input in variable dateInput

    Create dateObj as a new Date object using dateInput

    If dateObj is a valid date:
    Set T to "T"
    Set Z to "Z"
    
    Extract day from dateObj
    If day < 10, prepend "0" to day

    Extract month from dateObj (add 1 since months are 0-based)
    If month < 10, prepend "0" to month

    Extract year from dateObj

    Extract hour from dateObj
    If hour < 10, prepend "0" to hour

    Extract minute from dateObj
    If minute < 10, prepend "0" to minute

    Extract second from dateObj
    If second < 10, prepend "0" to second

    Concatenate year, "-", month, "-", day, T, hour, ":", minute, ":", second, Z
    Store in resultDate

    Output resultDate
Else:
    Output "Invalid date format."



# **Task 3: Data Governance & Security**


**Question 1.** 

[
  {
    "sensor_id": "AQ-01-GER",
    "timestamp": "2025-07-29T08:45:10Z",
    "location": { "latitude": -26.2253, "longitude": 28.1613 },
    "data": { "type": "air_quality", "value": 45.5, "unit": "AQI" },
    "data_source_veracity": 0.95,
    "system_and_data_access": "Public"
  },    


  {
    "sensor_id": "TC-05-GER",
    "timestamp": "2025-07-29T08:46:15Z",
    "location": { "latitude": -26.2260, "longitude": 28.1620 },
    "data": { "type": "traffic_count", "value": 152, "unit": "vehicles_per_minute" },
    "data_source_veracity": null,
    "system_and_data_access": "Public"
  },


  {
    "sensor_id": "TEMP-02-GER",
    "timestamp": "29/07/2025 08:47:00",
    "location": { "latitude": -26.2255, "longitude": 28.1615 },
    "data": { "type": "temperature", "value": "16.2C", "unit": "celsius" },
    "data_source_veracity": 0.80,
    "system_and_data_access": "Public"
  },


  {
    "sensor_id": "AQ-01-GER",
    "timestamp": "2025-07-29T08:50:05Z",
    "location": { "latitude": -26.2253, "longitude": 28.1613 },
    "data": { "type": null, "value": 48.0, "unit": "AQI" },
    "data_source_veracity": 0.95,
    "system_and_data_access": "Private"
  },


  {
    "sensor_id": "NL-03-GER",
    "timestamp": "2025-07-29T08:52:30Z",
    "location": { "latitude": -26.2271, "longitude": 28.1633 },
    "data": { "type": "noise_level", "value": 65, "unit": "dB" },
    "data_source_veracity": 0.99,
    "system_and_data_access": "Public"
  },


  {
    "sensor_id": "TC-05-GER",
    "timestamp": "2025-07-29T08:55:01Z",
    "location": { "latitude": -26.2260, "longitude": 28.1620 },
    "data": { "type": "traffic_count", "value": null, "unit": "vehicles_per_minute" },
    "data_source_veracity": 0.91,
    "system_and_data_access": "Public"
  },


  {
    "sensor_id": "HUM-01-GER",
    "timestamp": "2025-07-29T08:58:45Z",
    "location": { "latitude": -26.2258, "longitude": 28.1618 },
    "data": { "type": "humidity", "value": 34.8, "unit": "%" },
    "data_source_veracity": 0.98,
    "system_and_data_access": "Private"
  },


  {
    "sensor_id": "TEMP-02-GER",
    "timestamp": "2025-07-29T09:01:00Z",
    "location": { "latitude": -26.2255, "longitude": 28.1615 },
    "data": { "type": "temperature", "value": 17.1, "unit": "celsius","system_and_data_access": "Private" }
    
  },


  {
    "sensor_id": "AQ-01-GER",
    "timestamp": "2025-07-29T09:05:15Z",
    "location": { "latitude": -26.2253, "longitude": 28.1613 },
    "data": { "type": "air_quality", "value": -10, "unit": "AQI" },
    "data_source_veracity": 0.75,
    "system_and_data_access": "Restricted"
  },


  {
    "sensor_id": "NL-03-GERM",
    "timestamp": "2025-07-29T09:08:00Z",
    "location": { "latitude": -26.2271, "longitude": 28.1633 },
    "data": { "type": "noise_level", "value": 70, "unit": "dB" },
    "data_source_veracity": 0.99,
    "system_and_data_access": "Private"
  },


  {
    "sensor_id": "RAIN-01-GER",
    "timestamp": "2025-07-29T09:10:00Z",
    "location": { "latitude": -26.2280, "longitude": 28.1640 },
    "data": { "type": "rainfall", "value": "false", "unit": "boolean" },
    "data_source_veracity": 1.0,
    "system_and_data_access": "Restricted"
  },


  {
    "sensor_id": "TC-08-GER",
    "timestamp": "July 29 2025, 09:15:03 AM",
    "location": { "latitude": -26.2291, "longitude": 28.1652 },
    "data": { "type": "traffic_count", "value": 98, "unit": "vehicles_per_minute" },
    "data_source_veracity": 0.88,
    "system_and_data_access": "Private"
  }
]

**Question 2.** 
(a) It's bad for the business's reputation to have a data breach because it potrays the campany as having weak security. The shareholders/investors might not want to associate with our company, they might go with our competition.
(b) Our private data as indivudual members of the company is in jeopardy. 

**Question 3.** 
Data Protection Officer is responsible for maintaining the quality of the data. For a "Public" access level, the Information Officer or Deputy takes charge, however, for a "Private" access-level, the head of Information assigns the levels.