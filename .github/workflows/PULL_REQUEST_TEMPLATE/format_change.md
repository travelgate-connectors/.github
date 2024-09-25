# Format Change

Formatting changes refer to modifications to the structure or presentation of data without altering the underlying logic or behavior of the system. These changes are generally superficial and do not affect the functionality of the business.

## API Documentation format and standards

The following standards and formats have been taken into account in the change of **price or policy** format:
- Change in currency representation: Ensure that the currency code follows the ISO-3 standard.
- Adjustments in date display: Format dates according to ISO 8601 standard (e.g., 2016-07-01T05:00:00Z).
- Modification in data structure: Rearrange data fields without changing their content or meaning.
- Ensure that numeric values, such as CancelPenalty/HoursBefore, are in a consistent format (e.g., always as integers or decimals as appropriate).

- [ ] This check confirms that the changes follow the formats and standards established in the [API documentation](https://docs.travelgate.com/docs/get-started/introduction)

## Coherence and consistency of the changes

To ensure that format changes made in other parts of the integration are coherent and consistent, I have revised the coherence and consistency of the changes. Please refer to the [TGX documentation](https://docs.travelgate.com/docs/get-started/introduction).

Make sure the change does not affect some fields in the metadata and I have made the necessary adjustments, and the other way around.
When a change in the reservation flow affects the format, it must be ensured that the static data returned by the same API remains consistent. This implies that any changes to the structure or presentation of the data in the reservation flow must be consistently reflected in the calls to the static data, and the other way around.

- [ ] This check confirms that the changes keep consistency and coherence between booking flow, metadata, and static data.