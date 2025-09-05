Priority of variables
first priority: Local Variable:

 These are variables set within the pre-request or test scripts of a specific request using pm.variables.set(). They have the highest priority and are only available during the execution of that particular request or runner iteration. They are cleared once the request or runner completes.


Data Variable:

 These variables are sourced from a data file (e.g., CSV or JSON) used during a collection run. Each row in the data file provides a new set of values for the variables, and these values are applied to the requests within that run.


Environment Variable:

 Environment variables are defined within a selected environment in Postman. They are specific to that environment and can be used across multiple requests within that environment. If an environment is active, its variables take precedence over collection and global variables.


Collection Variable:

 Collection variables are defined at the collection level and are accessible to all requests within that collection. They provide a way to store values that are common to the entire collection.


last priority = Global Variable:

 Global variables are available throughout your entire Postman workspace. They have the broadest scope but the lowest priority.



