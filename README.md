# easyhttp
<strong>A minimal library for making http requests built with vanilla javascript</strong>

<h4>HTTP Methods</h4>
<p>get</p>
<p>post</p>
<p>put</p>
<p>delete</p>

<h4>Usage</h4>
<strong>Include the easyhttp library into your source file before your custom javascript file.</strong>
  <body>
    <h1>EasyHTTP Example</h1>

    <script src="easyhttp.js"></script>
    <script src="app.js"></script>

<h4>Instantiate the library</h4>

<h5>const http = new easyHTTP;</h5>

-Basic barebone

http.get('API ENDPOINT', CALLBACK FUNCTION){}

<h4>To make get request {api used in this example is Jsonplaceholder, a fake rest api} </h4>

```javascript
//Get posts
 http.get('https://jsonplaceholder.typicode.com/posts', function(err, posts){
  if(err){
    console.log(err);
  } else{
    console.log(posts)
  }
 });
 ```
```javascript
//Get single post
 http.get('https://jsonplaceholder.typicode.com/post/1', function (err, post) {
   if (err) {
     console.log(err);
   } else {
     console.log(post)
   }
 });
```

 <h4>To make a post request</h4>

-Basic barebone
http.post('API ENDPOINT', DATA, CALLBACK FUNCTION){}

```javascript
 //Create Data
const data = {
  title: 'Custom Post',
  body: 'This is a custom post'
};
```

```javascript
//Create Post
 http.post('https://jsonplaceholder.typicode.com/posts', data, function(err, post){
   if (err) {
     console.log(err);
   } else {
     console.log(post)
   }
 });
```

<h4>To make a put request</h4>

-Basic barebone
http.post('API ENDPOINT', DATA, CALLBACK FUNCTION){}

```javascript
//Update post
 http.put('https://jsonplaceholder.typicode.com/posts/1', data, function(err,post){
   if (err) {
     console.log(err);
   } else {
     console.log(post)
   }
 });
```


<h4>To make a delete request</h4>

Basic barebone
http.post('API ENDPOINT', CALLBACK FUNCTION){}

```javascript
//Delete post
http.delete('https://jsonplaceholder.typicode.com/posts/1', function (err, response) {
  if (err) {
    console.log(err);
  } else {
    console.log(response)
  }
}); ```