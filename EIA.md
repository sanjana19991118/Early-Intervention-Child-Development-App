# User Table 
Stores all users (admin, parent,doctor,special educator)

Fields: 
* id : UUID (Primary Key)
* username: str
* email: str
* password_hash: str
* role: str (Enum: admin, parent, doctor, special_educator)
* created_date: datetime
* updated_date: datetime
* created_by: UUID (FK to User)
* updated_by: UUID (FK to User)
* is_active : bool (for soft delete)
