Needs worked on
# Actors
- Customer
	- People who want to use the laundromat
- Laundromat Employees
	- Monitor machine status
	- Monitor machine availability 
- 
# Use Cases 
- UC1- Check machine availability
- UC2 - Reload loyalty card
- UC3 - Use NFC to start machines
  - Business Requirement: BR1
  - I think this is one of the use cases because our client want to get rid of the need for change and make payments digital. Before you can start a machine you need to pay, so using the NFC payment enables a machine to be "awakened" or started so using NFC to start machines is a use case.
  - Actors: customers
  - Flow:
    - Customer loads laundry into machine
    - Customer opens app with loaded payment card
    - Customer can scan a QR code to the machine or tap it's NFC reader
    - Funds will be transferred from the customers card to the laundromat
    - Machine will wake up and be able to be started by the customer
- UC4 - See locations on a map
  - Business RequirementL BR1
  - This is a use case because one of the parts of the project description is that users should be able to compare locations in terms of distance and availability. To make this possible the customers should be able to see the locations on a map and see how many machines are available at each location so this is a use case.
  - Actors: Customers and possibly employees
  - Flow:
    - Customer opens the app
    - Clicks on map tab
    - Map view will show all Clean Stream laundromats in relative position
    - Tapping on a location will display the number of washers and dryers available.
- UC5 - Get notified when my cycle ends
- UC6 - Track transaction history
  - Business Requirement: BR1
  - I think this is one of the use cases becasue our client emphasized to us that we should be tracking transaction history.
    This data will mostly be used by the laundromat employees. The flow of this will be that when a transation is made that
    the transaction data will be stored somewhere inside of our database. 
- UC7 - Ability to unlock doors for afterhours use
