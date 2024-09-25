# Business logic change (Price)

Changes in business logic involve modifications to the rules and processes that govern how data is handled and processed within the system. These changes can have a significant impact on the functionality and behavior of the system.

## Price Fields to Consider

Check the Attribute that has been modified:
- [ ] Binding
- [ ] Amount
- [ ] Commission
- [ ] Minimum selling price

Review the provider's documentation or provider contacts to ensure the price is correct and up-to-date. Our API information.
Currency: Ensure that the currency code is obtained from the correct tag and up to date, even if it has not been changed, it is crucial to verify its accuracy. 
- **Amount**: Verify that the amount is accurate and reflects the correct option price, ensuring that there have been no inadvertent changes. 
- **Binding**: Ensure that the binding field is set correctly according to the supplier's specifics, and the treatment for different clients as B2C or B2B, confirming that it is still correct. 
- **Commission**: Validate that the commission is correctly interpreted and documented, checking that there are no discrepancies with the supplier's documentation. Commission scenarios:
    - 0: The price returned is net.
    - -1: The supplier has not provided the sales price or commission.
    - Greater than 0: X = % of the commission applied to the amount.
- **minimumSellingPrice**: Ensure that the minimum selling price is correctly set and documented, verifying that it has been correctly changed. Minimum Selling Price Scenarios:
    - 0: No minimum selling price is provided.
    - -1: We have no information on the seller's minimum selling price.
    - Greater than 0: The lowest possible amount that can be sold commercially.

- [ ] This check confirms no accidental changes or discrepancies in the other Price attributes.

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