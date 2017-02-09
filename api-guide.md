#CKAN DataStore API

####Base Url : https://data.opendevelopmentmekong.net/api/action/datastore_search

##DataStore Search

The datastore_search action allows you to search data in a resource. DataStore resources that belong to private CKAN resource can only be read by you if you have access to the CKAN resource and send the appropriate authorization.

#####Parameters:	
- **resource_id** (string) – id or alias of the resource to be searched against
- **filters** (dictionary) – matching conditions to select, e.g {“key1”: “a”, “key2”: “b”} (optional)
- **q** (string or dictionary) – full text query. If it’s a string, it’ll search on all fields on each row. If it’s a dictionary as {“key1”: “a”, “key2”: “b”}, it’ll search on each specific field (optional)
- **distinct** (bool) – return only distinct rows (optional, *default: false*)
- **plain** (bool) – treat as plain text query (optional, *default: true*).Setting the `plain` flag to false enables the entire PostgreSQL [full text search query language](https://www.postgresql.org/docs/9.1/static/datatype-textsearch.html#DATATYPE-TSQUERY).
- **language** (string) – language of the full text query (optional, default: english)
- **limit** (int) – maximum number of rows to return (optional, default: 100)
- **offset** (int) – offset this number of rows (optional)
- **fields** (list or comma separated string) – fields to return (optional, default: all fields in original order)
- **sort** (string) – comma separated field names with ordering e.g.: “fieldname1, fieldname2 desc”

#####Response

The result of this action is a dictionary with the following keys:

**Parameters:**

**fields** (list of dictionaries) – fields/columns and their extra metadata
**offset** (int) – query offset value
**limit** (int) – query limit value
**filters** (list of dictionaries) – query filters
**total** (int) – number of total matching records
**records** (list of dictionaries) – list of matching results

Ref : http://docs.ckan.org/en/latest/maintaining/datastore.html#ckanext.datastore.logic.action.datastore_search

#####Where to find resource_id ?

data.opendevelopmentmekong.net/dataset/**{dataset_id}**/resource/**{resource_id}**
