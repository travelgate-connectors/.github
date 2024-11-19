# Connectors Pull Request

## Policy Fields
- [ ] Review the provider's documentation to confirm its format and currency
- [ ] Ensure that the most recent version of the provider's documentation is being utilized
- [ ] Verify that all modifications comply with internal policies and procedures
- [ ] Examine the provider's documentation to confirm that the HoursBefore field is correctly configured and up-to-date
- [ ] Validate that the Deadline field is in the correct format (ISO 8601) and accurately reflects the appropriate UTC date and time
- [ ] Check that the CalculatedDeadline field is properly configured according to the UTC-0 conversion logic
- [ ] Confirm that the Penalty field and its attributes (type, currency, paymentType) are correctly interpreted and documented
- [ ] Ensure that the penalty types (Nights, Percentage, Amount) are correctly applied and documented
- [ ] Review the payment types (MerchantPay, LaterPay, CardBookingPay, CardCheckInPay, PayX) correctly configured and documented
- [ ] Ensure that the changes do not adversely affect other cases
- [ ] Ensure that the changes do not adversely affect other providers on the platform

## Price Fields
- [ ] Review the provider's documentation to ensure the currency code (currency) is correct and up-to-date
- [ ] Verify that the amount (amount) is accurate and reflects the correct price of the option
- [ ] Check that the binding field is correctly configured according to the provider's policies
- [ ] Validate that the commission (commission) is correctly interpreted and documented
- [ ] Ensure that the minimum selling price (minimumSellingPrice) is correctly established and documented
- [ ] Review that all modifications are aligned with internal policies and procedures
- [ ] Validate that the changes comply with applicable compliance requirements and regulations

### Checklist
- [ ] Perform unit tests (integration test specific for the case not the normal unittest) to verify that the changes do not introduce errors
- [ ] Perform integration tests to ensure that the changes work correctly with other system components
- [ ] Consult with the provider to obtain a test environment or credentials to perform a booking flow and verify with the provider that it is correct

### Internal and Provider Communication
- [ ] Notify the corresponding team to make them aware of the situation, especially if the code needs to be uploaded to live
- [ ] Communicate the modifications to the provider using [this mail template](https://travelgatex.atlassian.net/wiki/x/AQBLtQ) and await its feedback

## Documentation of Changes (Price and/or Policies)
Please provide a detailed description of the changes made and the reasons behind them in the corresponding JIRA ticket titled "Documentation of Changes." The documentation should include:
- **Description of the Change**: A clear and concise explanation of what has been changed.
- **Reason for the Change**: Justification for why the changes were made, including any issues that were resolved or improvements that were implemented.
- **Impact of the Change**: Description of how the changes will affect the system and users.
- **Logs or Screenshots**: To justify the sections of the field to consider (Policies and/or price), checklist, and provider confirmation.
