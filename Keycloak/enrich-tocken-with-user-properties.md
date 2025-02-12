# Enrich Token with User Properties

This is a two-step process.

### Step 1: Add the Desired Properties to the User or Role

- Navigate to **Users** and search for the desired user.
- Go to the **Attributes** tab and add the desired attribute.
- **TODO:** Try adding the property to an entire role and check if it is inherited by all users.

### Step 2: Map the Property to the "userinfo"

- Navigate to **Client Scopes → userinfo_attributes**.
- Go to the **Mappers** tab.
- Click **Add Mapper** and choose **By configuration**.
- For the **User Attribute**, map the user attribute to the Token Claim Name.
