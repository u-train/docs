# Introduction

The `client` class represents the individual app user. It has just four properties, which are all read-only. We can use these properties to provide user-based logic, such as a permissions system or access to certain aspects of the application.

## Example

```lua
if client.membership == "plus" then
  -- We can do anything with this data.
else if client.membership == "pro" then
  -- We can do something different here.
end
```

In this example, we are comparing the [membershipType](https://deviap.com/docs/enums/#membershipType) enum to an integer value in a conditional statement.

If the user's membership level is less than the Pro level, we can apply some logic we create for the application.
If the user's membership level **is** the Pro level, we apply alternative logic and rules.

For example, we can use this to create a "VIP" section or give these users specific benefits within the application.
