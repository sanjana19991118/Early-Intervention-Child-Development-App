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

# Child Details Table

  Stores Information about the children registered by parents

  Fields:
  * id: UUID (Primary Key)
  * parent_id: UUID (FK to User)
  * name : str
  * date_of_birth: date
  * gender: str
  * special_abilities: str (description)
  * created_date: datetime
  * updated_date: datetime
  * created_by: UUID
  * updated_by: UUID
  * is_active: bool

# Screening Table
    Stores Screening results for each child

    Fields:
    * id : UUID (Primary Key)
    * child_id: UUID (FK to Child)
    * screening_date: datetime
    * condition_identified: str (FK to Condition)
    * screening_result: str(summary or JSON)
    * created_date: datetime
    * updated_date:datetime
    * created_by: UUID
    * updated_by:UUID
    * is_active: bool

# Condition Table

Defines possible conditions/disorders.
   Fields: 
   * id: UUID (Primary Key)
   * condition_id: UUID (FK to Condition)
   * question_text: str
   * created_date: datetime
   * updated_date: datetime
   * created_by: UUID
   * updated_by: UUID
   * is_active: bool

# Recomendation Table

Stores recommendation (medication, education, exercise) for each condition.

Fields: 
   * id : UUID (Primary Key)
   * condition_id: UUID (FK to Condition)
   * type: str(Enum: medication,education,tutorial,exercise)
   * description: str
   * created_date: datetime
   * updated_date: datetime
   * created_by: UUID
   * updated_by: UUID
   * is_active: bool

# Service Coordination Table

Tracks coordination between admin, parents, doctorsm educators.

Fields: 
   * id: UUID (Primary Key)
   * child_id: UUID (FK to Child)
   * admin_id: UUID (FK to User)
   * doctor_id: UUID(FK to User, nullable)
   * educator_id: UUID (FK to User, nullable)
   * status: str(Enum: pending, active,completed)
   * notes: str
   * created_date: datetime
   * updated_date: datetime
   * created_by: UUID
   * updated_by:UUID
   * is_active: bool
