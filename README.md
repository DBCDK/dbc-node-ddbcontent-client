# dbc-node-ddbcontent-client

[![David](https://img.shields.io/david/DBCDK/dbc-node-ddbcontent-client.svg?style=flat-square)](https://david-dm.org/DBCDK/dbc-node-ddbcontent-client#info=dependencies)
[![David](https://img.shields.io/david/dev/DBCDK/dbc-node-ddbcontent-client.svg?style=flat-square)](https://david-dm.org/DBCDK/dbc-node-ddbcontent-client#info=devDependencies)

Client for fetching data from a ddb library

##How to use:
```javascript
import * as DdbContent from 'dbc-node-ddbcontent-client';
       

// Initialize service with required paramters. Returns methods on client
const ddbContent = DdbContent.init({
  endpoint: 'http://am.fs_rest.dev.inlead.dk/web',
  agency: 123456,
  key: 'abcdefg123456'
});

// make a query. This returns a promise.
ddbContent.getContentById({node: 1})
.then((result) => {
  console.log(result)
});
};
```

##Methods:

### ddbContent.getContentById({node})

* **node:** Id of the node that should be fetched **[REQUIRED]**

### ddbContent.getContentList({amount, sort})

* **amount:** Number of nodes to fetch (default = 10) **[REQUIRED]**
* **sort:** Sorting parameter (default = 'nid') **[REQUIRED]**

Documentation of service api can be found at [http://am.fs_rest.dev.inlead.dk/web](http://am.fs_rest.dev.inlead.dk/web)
