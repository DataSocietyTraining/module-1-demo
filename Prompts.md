## Prompting: Foundations - 1 ##



#### Warm-up: How can I set things up and get out of the way?  ####

Build this feature.


#### Demo 1 : Generate Code Without Schema Context  ####

Write a Node.js function using pg to insert a new user.


#### Demo 1 : Generate the Function Again With Schema Context  ####

Write a Node.js function using pg to insert a new user using #file:schema.sql.


#### Demo 2 : Broad prompt with extra context  ####

Write a function to save a user based on table definition.


#### Demo 2 : Curated tabs improve the suggestion  ####

Write a production-ready Node.js function to insert a user based on schema.sql.



#### Demo 3: Few-shot prompting  ####

// Example 1: class DatabaseError extends Error { constructor(msg) { super(msg); this.code = 'DB_ERR'; } }
// Example 2: class ValidationError extends Error { constructor(msg) { super(msg); this.code = 'VALID_ERR'; } }

```
Create a third class for 'UserNotFoundError' using the same pattern, but not as a comment
```


#### Demo 3: Chain-of-Thought prompting  ####

Before writing code, give a short 3-step plan.

Then write a Node.js `pg` function named `getUserStatus(pool, emailAddress)` using `#schema.sql`.

Find the user by `email_address`, return `null` if not found, and return the user’s name, email, and account status if found.

Use a parameterized query.



#### Demo 3: Constrained prompting  ####

/**
 * AC for getClearanceUser:
 * 1. Only select full_name and account_status.
 * 2. Must filter by email_address.
 * 3. CONSTRAINT: Throw Error if internal_clearance_level is not returned.
 * 4. SECURITY: Use parameterized queries.
 */


Implement `getClearanceUser(pool, emailAddress)` using Node.js `pg` and `#schema.sql`.

Select `full_name`, `account_status`, and `internal_clearance_level` by `email_address`.

Return `null` if no user is found. Throw an Error if `internal_clearance_level` is missing.

Return only `full_name` and `account_status`.






