###Music Module Permissions
We are using a simple permission system that could easily be configured. Ene uses 4 different ranks each with different permissions.

| Ranks | Permission Description |
| ------------- | ------------- |
| 3:Admin  | Can change the Music configuration and edit permissions  |
| 2:DJ  | Can skip, can pause/unpause, can change repeat mode, can change shuffle mode, etc. **By default, `@everyone` is set to this permission.**  |
| 1:User | Can add tracks to the queue and can only skip their own tracks. Remove `@everyone` from the DJ permission to assign them as a User. |
| 0:Base | Given to everyone without higher ranks. Cannot modify the queue or player, but can still use commands like `.list`, `.np`, etc. |

###Special notes
- Users with the Discord "Administrator" permission and owners implicitly have all perms.
- Permissions are specific for a server, never a channel.
- Higher ranks also have lower rank permissions.
- Permissions can be granted to users or roles. This includes the `@everyone` role.
- By default, everyone has the DJ and User roles. Use the below commands to delete the `@everyone` role from the DJ list and make them Users.

###The permission commands
These are the commands:
```
.admin add <user/role>
.admin del <user/role>
.admin list
.dj add <user/role>
.dj del <user/role>
.dj list
.user add <user/role>
.user del <user/role>
.user list
```
The name of the command specifies which rank you are modifying or listing.

These commands are restricted to users with the ADMIN permissions, apart from the list subcommand. The add subcommand can be used to add usernames or roles to a permission rank.