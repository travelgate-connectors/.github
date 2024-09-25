# Business logic change (CancelPenalty)

Changes in business logic involve modifications to the rules and processes that govern how data is handled and processed within the system. These changes can have a significant impact on the functionality and behavior of the system.

## Fields of the Policy to Consider

Check the Attribute that has been modified:
- [ ] Deadline
- [ ] Amount
- [ ] CalculatedDeadline 
- [ ] Penalty type (Nights, Percentage, Amount)
- [ ] Penalty payment type  (MerchantPay, LaterPay, CardBookingPay, CardCheckInPay, PayX)
- [ ] Penalty currency

Review the vendor's documentation to confirm its accuracy and currency, ensuring that the latest version is being used. Examine the supplier's documentation to confirm that the HoursBefore field is correctly configured and up to date.

Validates that the [Deadline](https://docs.travelgate.com/kb/faqs/faqs-cancel-policies/cancel-policies-and-deadlines-closer-look?_highlight=deadline) field is in the correct format (ISO 8601), is correctly configured according to UTC-0 conversion logic and accurately reflects the appropriate UTC date and time, and is consistent with the metadata and CalculatedDeadline attribute.

Check that the **CalculatedDeadline** field is correctly set and is consistent with the metadata (if a specific timezone is currently set).

Confirm that the **Penalty** field and its attributes (type, currency, paymentType) are correctly interpreted and documented. Ensure that the penalty types (Nights, Percentage, Amount) are correctly applied and documented. Check that payment types (MerchantPay, LaterPay, CardBookingPay, CardCheckInPay, PayX) are correctly configured and documented. Ensure that changes do not adversely affect other cases, platform providers, services, or system components.

- [ ] This check confirms no accidental changes or discrepancies in the other CancelPenalty attributes.

## Checklist

- [ ] Perform unit tests (integration test specific for the case not the normal unittest) to verify that the changes do not introduce errors.
- [ ] Perform integration tests to ensure that the changes work correctly with other system components.
- [ ] Consult with the provider to obtain a test environment or credentials to perform a booking flow and verify with the provider that it is correct.
- [ ] Inform the providers about the proposed changes and obtain their feedback.
- [ ] Document all changes made and the reasons behind them.

## Provider Confirmation

- [ ] Confirm that the created or modified price correctly inform the client.
- [ ] Confirm that the price adequately interpret the information provided by the provider.
- [ ] In case of doubts or lack of information, notify the corresponding team to make them aware of the situation, especially if the code needs to be uploaded to live ( If the provider insists on proceeding despite the uncertainties, it must be clearly communicated that the provider will be responsible for any issues or problems that arise).

## Documentation of Changes

Please describe the changes made and the reasons behind them in the corresponding JIRA ticket titled "Documentation of Changes." The documentation should include:
- **Description of the Change**: A clear and concise explanation of the change.
- **Reason for the Change**: Justification for why the changes were made, including any resolved issues or implemented improvements.
- **Impact of the Change**: Description of how the changes affect the system and users.
- **Logs or Screenshots**: To justify the sections of the field to consider (Policies and/or price), checklist, and provider confirmation.