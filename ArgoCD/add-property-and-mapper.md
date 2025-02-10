# Enrich tocken with user properties

This is a two step process.

First you need to add the desired properties to the user or the role.
1. Users-> search the desired user.
2. Tab Attributes -> add the desired attribute

TODO: try to add to the whole Role the property and check if it's hereditated from all the users.

Second you need to map the property to the "userinfo"
1. Client scopes -> userinfo_attributes
2. Tab Mappers
3. Add Mapper -> By configuration
4. user attribute
5. map the `User Attribute` with the `Token Claim Name`

