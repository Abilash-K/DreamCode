
There are certain rules for SQL which would ensure consistency and functionality across databases. By following these rules, queries will be well formed and well executed in any database.

- ****Statement Termination:**** Every SQL statement ends with a semicolon (;), signaling the DBMS to execute the command.
- ****Case Insensitivity:**** SQL keywords (e.g., SELECT, INSERT) are case-insensitive, but database names and column names may be case-sensitive depending on the DBMS.
- ****Whitespace Flexibility:**** SQL statements can span multiple lines, but keywords and identifiers must be separated by at least one space.
- ****Unique Identifiers:**** Reserved words (e.g., SELECT, FROM) cannot be used as table or column names unless enclosed in double quotes (“) or backticks (`), depending on the DBMS.
- ****Comments:**** Comments enhance readability:
    - Single-line comments: —
    - Multi-line comments: /* … */
- ****Data Integrity:**** Constraints like NOT NULL, UNIQUE, and PRIMARY KEY must be defined correctly to maintain data consistency.
- ****String Literals:**** String values must be enclosed in single quotes (‘).
- ****Valid Identifiers:**** Table and column names must:
    - Begin with an alphabetic character.
    - Contain up to 30 characters.
    - Avoid special characters except underscores (_).