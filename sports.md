# FrontEnd Dev

"Rough" Idea for User-Interface (UI):

> Our goal is to effectively develop a movie database that not only recommends its user with numerous movies they would enjoy, but also store their favorite movies and develop a review system. We plan on using The Movie Database as an API for this project.

> As the frontend developer of my team, I am tasked with the job of constructing a suitable, user-friendly UI that entices more users to join the application. Our goal, however, as a team, is to lead the user to a movie that they would enjoy based on their current favorite movies. This way, they can continue to find more and more movies that fit their movie-taste. 

<html>
<head>
  <title>Movie Recommendation App</title>
</head>
<body>
  <h1>Welcome to the Movie Recommendation App!</h1>
  <p>Use the form below to search for movie recommendations based on a movie title:</p>

  <!-- HTML for the form -->
  <form id="movie-form">
    <label for="movie-title">Enter a movie title:</label><br>
    <input type="text" id="movie-title" name="movie-title" placeholder="e.g. The Shawshank Redemption"><br>
    <button type="submit">Submit</button>
  </form> 

  <!-- HTML for the movie recommendation list -->
  <h2>Movie Recommendations:</h2>
  <ul id="movie-list">
    <!-- The movie recommendations will be added here dynamically using JavaScript -->
  </ul>

  <!-- HTML for the loading spinner -->
  <div id="loading" style="display: none;">
    <img src="loading.gif" alt="Loading...">
  </div>

  <!-- JavaScript for handling form submission and retrieving movie recommendations -->
  <script src="app.js"></script>
</body>
</html>

### Once the user has inputted their movie, the output should look something like this:

<form style="width: 50%; margin: 0 auto; text-align: center;">
...
</form>

<ul id="movie-list" style="list-style: none; width: 50%; margin: 0 auto;">
  <li style="margin: 20px 0; font-size: 18px;">Movie 1</li>
  <li style="margin: 20px 0; font-size: 18px;">Movie 2</li>
  ...
</ul>

<p></p>
<p></p>
<p></p>
<p></p>
<p></p>

> Our goal is to effectively develop a movie database that not only recommends its user with numerous movies they would enjoy, but also store their favorite movies and develop a review system. We plan on using The Movie Database as an API for this project.

> As the frontend developer of my team, I am tasked with the job of constructing a suitable, user-friendly UI that entices more users to join the application. Our goal, however, as a team, is to lead the user to a movie that they would enjoy based on their current favorite movies. This way, they can continue to find more and more movies that fit their movie-taste. 

<p></p>



<form style="width: 50%; margin: 0 auto; text-align: center;">
  <input type="text" style="width: 60%; padding: 12px 20px; margin: 8px 0; box-sizing: border-box; border: 2px solid #ccc; border-radius: 4px;">
  <button type="submit" style="width: 20%; background-color: #4CAF50; color: white;">Submit</button>
</form>

Something like this, maybe? But obviously on a more professional scale. All options are still being considered. 

> Ideally, the design should be user-friendly, prompt the user with an input, and then deliver the movie recommendations with fluidity. For the frontend portion, however, I understand how important it is for the user interface to be well crafted and look credible. 


As for the favoriting system, which would allow users to search for a movie and "save" it to a favorite movie list, here is a template of the code we would use to fetch data, and customize the UI:

<img src="{{site.baseurl}}/images/favoritemovie.png">

> This code uses the TMDb API to search for movies with a given title and allows the user to add them to a list of favorite movies. Each movie is displayed in a separate div element with a poster image, title, and overview.
