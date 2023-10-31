# Python-project-submission-Naveen

The provided code is a Python script that serves as a basic web scraper for retrieving and displaying the top 5 movies of a user-specified genre from IMDb (Internet Movie Database). Here's a breakdown of how the script works:

The script imports two Python libraries: requests and BeautifulSoup. requests is used for making HTTP GET requests to a website, and BeautifulSoup is used for parsing and extracting information from the HTML content of web pages.

It defines a function named get_top_movies_by_genre(genre) that takes a genre as its parameter. The purpose of this function is to fetch and return the top 5 movies of the specified genre.

Inside the function, it constructs a URL for IMDb's "Top Rated Movies by Genre" page by dynamically including the genre in the URL.

It sends an HTTP GET request to the constructed URL using the requests.get(url) method.

If the response status code is 200 (indicating a successful request), it proceeds to parse the HTML content of the page using BeautifulSoup. If the response code is not 200, it prints an error message and returns an empty list.

The script then uses BeautifulSoup to find all the movie containers on the webpage. The movie containers are identified by the class name "lister-item-content."

It iterates through the movie containers and extracts the titles of the top 5 movies, appending them to the top_movies list. It breaks the loop when it has collected 5 movie titles.

The function returns the top_movies list, which contains the titles of the top 5 movies of the specified genre.

After defining the function, the script prompts the user to input a genre of interest using input("Enter the genre you're interested in: ").

It calls the get_top_movies_by_genre function with the user-provided genre, and if top-rated movies are found, it prints them in a user-friendly format. If no movies are found for the specified genre, it prints an appropriate message.

In summary, this script is a basic web scraping tool that allows users to input a movie genre, and it then scrapes IMDb to retrieve and display the titles of the top 5 movies in that genre. It's a simple example of web scraping and can be extended or enhanced for more advanced use cases, error handling, or additional information retrieval
