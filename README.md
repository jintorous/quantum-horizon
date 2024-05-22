
A sincere request
please remove the Script which was shown in correction.png.. i added the Joi .. but forget to remove the  validation in controller level  and the spelling are missmatching which was done in a hurry.

utils\users.utils.js

  line no 95 to 100 (if (!checkStatus(details.Status)) ...})

----------------------------------------------------------------------------------


I've implemented The problem given with file structure  where there are two json files ..users.json and Task.json..  that's currently running smoothly

However the mongodb wrappers also i have written .but its not tested as i dont have the Mongo in my system..
its in 

/DB ==> for connection

/schmea ==> for schema

/services => for generalise functions which execute the mongo query



to get the query running we need to inject the functions in the utils level

Lets take an example

finding one or  all the users we need to do this in utls

const User = require('../schema/users.schema');

findOneDocument(User,{userName:"Rakesh"})

findAllDocuments(User,{userName:"Rakesh"})

findDocumentsWithPaging(User,{userName:"Rakesh"},1,100) = with serverside paging with variable page size

findDocumentsWithPaging(User,{userName:"Rakesh"},1)= with serverside paging without variable page size

