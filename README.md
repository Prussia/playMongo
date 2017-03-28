# playMongo

## Mongodb user management:

### roles list

        read
        readWrite
        dbAdmin
        userAdmin
        clusterAdmin
        readAnyDatabase
        readWriteAnyDatabase
        userAdminAnyDatabase
        dbAdminAnyDatabase
### create user
        ```
        db.createUser(user, writeConcern)

        db.createUser({ user: "user",
          pwd: "pass",
          roles: [
            { role: "read", db: "database" } 
          ]
        })
        update user:

        db.updateUser("user",{
          roles: [
            { role: "readWrite", db: "database" } 
          ]
        })
        drop user:

        db.removeUser("user")
        or

        db.dropUser("user")
        view users:

        db.getUsers();
        ```
more information: https://docs.mongodb.com/manual/reference/security/#read
                  https://docs.mongodb.com/manual/tutorial/enable-authentication/
