
# snowflake_account_grant

<!-- These docs are auto-generated by code in ./docgen, run by with make docs. Manual edits will be overwritten. -->

**Note**: The snowflake_account_grant resource creates exclusive attachments of grants.
		Across the entire Snowflake account, all of the accounts to which a single grant is attached must be declared
		by a single snowflake_account_grant resource. This means that even any snowflake_account that have the attached
		grant via any other mechanism (including other Terraform resources) will have that attached grant revoked by this resource.
		These resources do not enforce exclusive attachment of a grant, it is the user's responsibility to enforce this.
		
## properties

|       NAME        |  TYPE  |                                         DESCRIPTION                                         | OPTIONAL | REQUIRED  | COMPUTED | DEFAULT |
|-------------------|--------|---------------------------------------------------------------------------------------------|----------|-----------|----------|---------|
| privilege         | string | The privilege to grant on the schema.                                                       | true     | false     | false    | "USAGE" |
| roles             | set    | Grants privilege to these roles.                                                            | true     | false     | false    |         |
| with_grant_option | bool   | When this is set to true, allows the recipient role to grant the privileges to other roles. | true     | false     | false    | false   |
