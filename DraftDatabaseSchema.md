# Vehicle Manager Schema
## User Table:
- user_id (Primary Key)
- username
- password (hashed)
- email
  
## Vehicle Table:
- vehicle_id (Primary Key)
- registration_number (Unique)
- state
- make
- model
- year
- color
- house_attached
- has_ramp
- user_id (Foreign Key, references User Table)
  
## Service Records Table:
- service_id (Primary Key)
- vehicle_id (Foreign Key, references Vehicle Table)
- service_date
- service_type
- service_description
- service_cost
  
## Comprehsive Insurance Table:
- insurance_id (Primary Key)
- vehicle_id (Foreign Key, references Vehicle Table)
- insurance_provider
- policy_number
- start_date
- end_date
- premium_amount

## Compulsory Third-Party Insurance Table:
- ctpinsurance-id
- vehicle_id (Foreign Key, references Vehicle Table)
- ctpinsurance_provider
- policy_number
- start_date
- end_date
- premium_amount
  
## Cleaning Schedule Table:
- cleaning_id (Primary Key)
- vehicle_id (Foreign Key, references Vehicle Table)
- cleaning_date
- cleaning_provider
- cleaning_description
  
## Registration Table:
- registration_id (Primary Key)
- vehicle_id (Foreign Key, references Vehicle Table)
- registering_state
- registration_date
- registration_end_date

## Ramp Service
- Ramp_service_id (Primary Key)
- vehicle_id (Foreign Key, references Vehicle Table)
- ramp_service_date




