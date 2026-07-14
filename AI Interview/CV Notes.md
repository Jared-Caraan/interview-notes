## 1. IBM Solutions Delivery, Inc. (Senior Data Engineer)

_Focus areas: Snowflake optimization, dbt architecture, and pipeline cost-efficiency._

- **On dbt Incremental Models & Materialization:**

  "You mentioned utilizing incremental materialization in dbt to streamline compute costs. Can you walk me through your strategies for choosing the right incremental strategy (e.g., merge vs. append vs. insert+overwrite) in Snowflake? How did you handle late-arriving dimensions or upstream schema changes in these pipelines?"

- **On Jinja Macros & DRY Code:**

  "In your dbt project, what was the most complex Jinja macro you implemented, and what specific problem did it solve? How did you ensure that using dynamic SQL via Jinja didn't make debugging more difficult for other team members?"
  
  **Probable answer:**

  The situation is our source data is from MFP (Managed Foundation Pipelines) materializing in Snowflake. In Snowflake, it is recognized as DL2. The data that we want is in a column called `SOURCE_DATA` and it is always in JSON format. Our task is to always read some of the key,value pairs inside those columns, because that's what we care about. Since the scenario is pretty much the same every monthly load, the action is to create a Jinja that reads the `SOURCE_DATA` column, reads selective key,value pairs and the result is another table.

- **On ML Ops & CI/CD Pipelines:**

  "You orchestrated ML model repository configurations and automated CI/CD workflows. Can you describe the technical architecture of this CI/CD pipeline? How did you handle environment-specific parameters, and how did you manage model versioning and rollback strategies in production?"
  
  **Probable answer:**
  
  I'm gonna give an example of a project. Let's call it the Issue Attribute Predictor. The situation is that given a situation in ServiceNOW we would want to categorize that incident. 
