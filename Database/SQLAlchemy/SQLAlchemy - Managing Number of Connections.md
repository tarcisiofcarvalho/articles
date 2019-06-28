# SQLAlchemy - Managing Connections

Managing your connections to a database is an important task to avoid to exceed the maximum permitted by the database you are using. Below you can read some concepts and the way to do manage the number of connections in SQLAlchemy.
	

### Closing the session

After you request all database operations related to your scope of operations, you can close the session. 

If you are using **scoped_session**, handle the function below, it will call the *Session.close()* that will release any transaction/connection. 

```python
 scoped_session.remove()
 ```
If you are using just the **session_maker** object, you can call the function below

```python
session.close()
```


## References

[SQLAlchemy Pooling](https://docs.sqlalchemy.org/en/13/core/pooling.html "SQLAlchemy Pooling") 

	
	
	

