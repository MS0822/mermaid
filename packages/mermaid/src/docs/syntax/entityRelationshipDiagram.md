[mermaid]
erDiagram
  Blood {
    * Blood_Type
      Give
      Receive
      Storage_Requirements
  }
  Donor {
    * Donor_ID
    Name
    Address
    Phone
    Email
    * Blood_Type
  }
  Recipient {
    * Recipient_ID
    Name
    Address
    Phone
    Email
    * Blood_Type
    Medical_Condition
  }
  Blood_Inventory {
    * Blood_Type
    Quantity
    Expiration_Date
  }
  Blood_Requests {
    * Request_ID
    Recipient_ID
    * Blood_Type
    Quantity
    Date_of_Request
  }
  Blood_Donations {
    * Donation_ID
    Donor_ID
    * Blood_Type
    Quantity
    Date_of_Donation
  }
  Blood_Transfusions {
    * Transfusion_ID
    Recipient_ID
    * Blood_Type
    Quantity
    Date_of_Transfusion
  }
  Donor -> Blood
  Recipient -> Blood
  Blood_Inventory -> Blood
  Blood_Requests -> Recipient
  Blood_Requests -> Blood
  Blood_Donations -> Donor
  Blood_Donations -> Blood
  Blood_Transfusions -> Recipient
  Blood_Transfusions -> Blood
[/mermaid]
