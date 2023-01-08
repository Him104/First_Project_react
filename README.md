# First_Project_react
Blogging wesbite


The features we are going to build into this project are:-

1. Fetching blogs from a local JSON server and displaying the blogs in list form.

2. Fetching details about individual blogs and displaying them.

3. Adding new blogs.

4. Deleting blogs.

Phase I Models Author Model 

{ fname: { mandatory}, lname: {mandatory}, title: {mandatory, enum[Mr, Mrs, Miss]}, email: {mandatory, valid email, unique}, password: {mandatory} } Blogs Model { title: {mandatory}, body: {mandatory}, authorId: {mandatory, refs to author model}, tags: {array of string}, category: {string, mandatory, examples: [technology, entertainment, life style, food, fashion]}, subcategory: {array of string, examples[technology-[web development, mobile development, AI, ML etc]] }, createdAt, updatedAt, deletedAt: {when the document is deleted}, isDeleted: {boolean, default: false}, publishedAt: {when the blog is published}, isPublished: {boolean, default: false}}

Make sure the authorId is a valid authorId by checking the author exist in the authors collection.

Return HTTP status 201 on a succesful blog creation. Also return the blog document. The response should be a JSON object like this

Create atleast 5 blogs for each author

Return HTTP status 400 for an invalid request with a response body like this

GET /blogs Returns all blogs in the collection that aren't deleted and are published Return the HTTP status 200 if any documents are found. The response structure should be like this If no documents are found then return an HTTP status 404 with a response like this Filter blogs list by applying filters.
