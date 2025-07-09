# QA Test Cases for Milk Delivery Salesforce App

| Test Case ID | Test Case | Description | Expected Result | Actual Output | Status | Comment |
|-|-|-|-|-|-|-|
| TC_MD_01 | Create new milk delivery | Add a new milk delivery record with all required fields | Record is saved and listed under Milk Deliveries | Record saved and appears in list | Pass | Works as expected |
| TC_MD_02 | Validate mandatory photo upload | Try to save delivery record without photo using flow | Error message should display: 'Photo Upload is required' | Error displayed correctly | Pass | Validation rule working fine |
| TC_MD_03 | Lookup customer record | Use lookup to search and select a customer | Customer list loads and selection is successful | Lookup returns correct customer results | Pass | Lookup field functioning well |
| TC_MD_04 | Date format validation | Enter invalid date format in 'Delivery Date' field | System should not allow saving and show validation error | Record not saved, error appears | Pass | Correct date validation |
| TC_MD_05 | Field character limit validation | Enter 500+ characters in Delivery Notes field | System should restrict input and throw error | Text truncated, warning shown | Pass | Limit enforced |
| TC_MD_06 | User permission to edit record | Login as user with 'Standard User' profile and try to edit record | Edit option should be restricted or limited as per profile settings | Edit not allowed | Pass | Role restriction working |
| TC_MD_07 | Auto-population of delivery date | Check if today's date is auto-filled when creating a new record | Delivery Date defaults to current date | Today's date shown by default | Pass | Expected behavior |
| TC_MD_08 | Add delivery record via mobile | Use Salesforce mobile app to add delivery | Record gets saved and synced in desktop view as well | Successfully saved and visible | Pass | Mobile app compatible |
| TC_MD_09 | Invalid image format upload | Try to upload a .txt file as photo | System should reject unsupported file types | File upload failed with proper error | Pass | File type check in place |
| TC_MD_10 | Duplicate entry prevention | Enter same data twice for same day & customer | System flags duplicate or prevents saving | Duplicate warning shown | Pass | Duplicate logic works |
