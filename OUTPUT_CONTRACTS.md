# Output Contract Validation

## Overview
When a prompt requires structured output such as JSON, XML, or typed responses, the receiving AI must validate its output against a formal contract before delivery.

## Contract Description

An output contract specifies:
- The format of the output such as JSON, XML, YAML, TypeScript interfaces, or Protocol Buffers.
- The schema describing what fields must exist, what types they must be, and what constraints apply to each.
- Validation rules that check correctness across the entire output.

## Schema Description (Natural Language)

A schema defines the shape of the output using plain English descriptions:

- The output must be an object containing specific fields.
- Each field has a name, a required or optional status, a data type, and optional constraints.
- Data types include string, number, boolean, array, or nested object.
- Constraints include minimum and maximum length for strings, numeric ranges, allowed values from a fixed set, pattern matching using regular expressions, and format requirements such as email addresses, web addresses, dates, or unique identifiers.
- The schema may specify whether additional fields beyond those defined are permitted or forbidden.
- Required fields must always be present. Optional fields may be omitted.

## Validation Steps

### Step 1: Schema Check
Verify that the output contains all required fields and no forbidden additional fields. Confirm that every field matches its declared data type.

### Step 2: Type Validation
For string fields, check that values stay within minimum and maximum length limits and match any specified patterns. For number fields, verify values fall within allowed ranges and have correct precision. For boolean fields, ensure only true or false values appear. For array fields, check that item counts stay within limits and every item matches the expected type. For object fields, recursively apply the same validation rules.

### Step 3: Format Compliance
Date values must use ISO eight-six-zero-one format. Email addresses must comply with standard email format. Web addresses must follow URI standards. Unique identifiers must match UUID standards. Values from enumerated sets must belong to the allowed list.

### Step 4: Cross-Field Consistency
Verify that related fields make sense together. Start dates must come before end dates. Minimum values must be less than maximum values. Related fields such as country and timezone must be compatible.

### Step 5: Edge Case Handling
Check behavior with null values, empty collections, and maximum length boundaries. Determine whether null means the same as missing or if they are handled differently. Verify that empty arrays are either explicitly allowed or correctly rejected.

## Failure Handling

If validation fails:
1. Record the specific field that failed, which validation rule was violated, what value was expected, and what value was actually produced.
2. Return to the Build step for the output unit that failed.
3. Fix either the output to match the contract or the contract to match legitimate output needs.
4. Run validation again.
5. Allow up to three validation attempts. If validation still fails after three attempts, escalate to the user with full details of what failed and why.

## Example Contract (Descriptive)

A user profile contract might specify:
- An identifier field that is required, must be a string, and must follow UUID format.
- A name field that is required, must be a string, must have at least one character, and must not exceed one hundred characters.
- An email field that is required, must be a string, and must follow standard email format.
- A role field that is required, must be a string, and must be one of the allowed values: admin, user, or guest.
- A creation timestamp that is required, must be a string, and must follow date-time format.
- An optional preferences object containing a theme field that must be one of light, dark, or auto, and an optional notifications field that must be a boolean.
- No additional fields beyond those specified are permitted.
