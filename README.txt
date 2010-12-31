; $Id$

Node Access Userreference Extended
----------------------------------

This module extends the grants given by Node Access Userreference by allowing
to set grants on content types referencing a type handled by Node Access
Userreference.

----------------------------------

Example:

* Content type "Division" has a userreference field that is used to grant
  permissions to nodes of this type ("view", "update", "delete").
* Content type "News" has a nodereference field to type "Division".

With "Node Access Userreference Extended" you are able to permit the users
referenced on "Division" to update or delete nodes of type "News" even if the
users aren't the node authors.

----------------------------------

More detailed example:

"Division A" has 2 referenced users: "User 1" and "User 2".
"Division A" is configured to grant "update" permissions to referenced users on
referencing nodes.
"Division B" has 2 referenced users: "User 2" and "User 3".
"Division B" is configured to grant "update" and "delete" permissions to
referenced users on referencing nodes.

"User 1" and "User 2" are permitted to create content of type "News" (by role
permission).
"User 3" has no further permissions (of course the user is allowed to access
content).

Because of the reference to "Division A" "User 1" and "User 2" are allowed to
update any content of type "News" that references "Division A".
Because of the reference to "Division B" "User 2" and "User 3" are allowed to
update and delete any content of type "News" that references "Division B".

----------------------------------

undpaul, 2010
