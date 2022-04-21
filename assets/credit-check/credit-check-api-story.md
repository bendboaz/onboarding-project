# Credit Check API Story at BigCo, Inc.

### Purpose

Allow BigCo, Inc. to determine the `spendingLimit` and `discountPercentage` for its client company accounts.

### Data

The service accepts `companyName` and determines the required `spendingLimit` and `discountPercentage`.

### Actions

The service will take the `companyName` given in the input and use the safe `checkCredit` method, 
which returns a `rating` parameter. This will then be used to determine the requesting company 
`spendingLimit` and `discountPercentage`.

### Rules

(should this be enforced here?)
The credit check should be run upon registering a new company, as well as January 1st in any following years.

### Processing

The service also logs the credit check - log records can be accessed by `companyName`, and contain
the following fields:
- `identifier`
- `companyName`
- `dateRequested`
- `rating`

