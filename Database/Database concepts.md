# Database concepts


### Session

A session makes all conversation with the database. It works as a "holding zone" where all database objects operations requested as update, delete, etc will be hold until the "commit" command to this session. It avoid many database connections, being more effective, sending many database operations in one database request connection. It flushes all pending changes to the database, it is known as the Unit of Work pattern.