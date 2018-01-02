# easyhttp
A minimal library for making http requests built with vanilla javascript

#HTTP Methods
get,
post,
put,
delete

#Usage
-Include the easyhttp library into your source file before your custom javascript file.
  <body>
    <h1>EasyHTTP Example</h1>

    <script src="easyhttp.js"></script>
    <script src="app.js"></script>
  </body> 

-Instantiate the library
const http = new easyHTTP();

-Basic barebone
http.get('API ENDPOINT', CALLBACK FUNCTION){}

-To make get request {api used in this example is Jsonplaceholder, a fake rest api}
//Get posts
 http.get('https://jsonplaceholder.typicode.com/posts', function(err, posts){
  if(err){
    console.log(err);
  } else{
    console.log(posts)
  }
 });

//Get single post
 http.get('https://jsonplaceholder.typicode.com/post/1', function (err, post) {
   if (err) {
     console.log(err);
   } else {
     console.log(post)
   }
 });


 -To make a post request

-Basic barebone
http.post('API ENDPOINT', DATA, CALLBACK FUNCTION){}

 //Create Data
const data = {
  title: 'Custom Post',
  body: 'This is a custom post'
};

//Create Post
 http.post('https://jsonplaceholder.typicode.com/posts', data, function(err, post){
   if (err) {
     console.log(err);
   } else {
     console.log(post)
   }
 });


-To make a put request

-Basic barebone
http.post('API ENDPOINT', DATA, CALLBACK FUNCTION){}

//Update post
 http.put('https://jsonplaceholder.typicode.com/posts/1', data, function(err,post){
   if (err) {
     console.log(err);
   } else {
     console.log(post)
   }
 });


-To make a delete request

-Basic barebone
http.post('API ENDPOINT', CALLBACK FUNCTION){}

//Delete post
http.delete('https://jsonplaceholder.typicode.com/posts/1', function (err, response) {
  if (err) {
    console.log(err);
  } else {
    console.log(response)
  }
});
