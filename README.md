i have implemented with file structure which is running fine

the MongoDB wrapper i have written
its in 

/DB ==> for connection
/schmea ==> for schema
/services => for query



to get the query running we need to inject the code in the utils level

so for finding one or  all the users we need to do this in utls

const User = require('../schema/users.schema');

findOneDocument(User,{userName:"Rakesh"})
findAllDocuments(User,{userName:"Rakesh"})
findDocumentsWithPaging(User,{userName:"Rakesh"},1,100) = with serverside paging with variable page size
findDocumentsWithPaging(User,{userName:"Rakesh"},1)= with serverside paging without variable page size

