# Foodfinder
Meal Finder Website Documentation
Overview
The Meal Finder website is a platform that allows users to search for meals based on ingredients they have on hand. The website provides an intuitive user interface, integrates a backend system for data processing, and uses a database for storing info/concerns data. This documentation provides a detailed overview of the technologies and components used in building the website.
________________________________________
Features
1.	Search for Meals:
o	Users can enter an ingredient in the search bar to find relevant meals.
2.	Dynamic Results:
o	Search results are dynamically generated based on the entered ingredient.
3.	User-Friendly Interface:
o	Simple and clean design for ease of use.
4.	Responsive Design:
o	The website is responsive and can be accessed on different devices.
________________________________________
Technologies Used
Frontend:
•	HTML: 
o	Structure of the website.
o	Forms and layout elements.
•	CSS: 
o	Styling and design of the website.
o	Customization for responsiveness and aesthetics.
Backend:
•	JavaScript: 
o	Handles client-side interactivity and dynamic behaviors.
o	Sends requests to the backend server and handles responses.
•	PHP: 
o	Processes search requests from the frontend.
o	Queries the database for passing concerns.
Database:
•	MySQL (via XAMPP): 
o	Stores contact information and concerns
o	Retrieves meal data based on search queries.
________________________________________
Setup Instructions
Prerequisites:
1.	Install XAMPP to set up the local development environment.
2.	Ensure that MySQL and Apache services are running via the XAMPP control panel.
3.	Have a text editor or IDE (e.g., VS Code) installed for coding.
Database Setup:
1.	Open phpMyAdmin via XAMPP.
2.	Create a database (e.g.,foodfinder_db).
3.	Import or create a table for meals with the following fields: 
o	id (Primary Key)
o	meal_name (VARCHAR)
o	ingredients (TEXT)
o	recipe (TEXT)
Backend Configuration:
1.	Place the PHP files in the htdocs directory of XAMPP.
2.	Configure the database connection in the PHP file: 
3.	$servername = "localhost";
4.	$username = "root";
5.	$password = "";
6.	$dbname = "foodfinder_db";
7.	
8.	$conn = new mysqli($servername, $username, $password, $dbname);
9.	
10.	if ($conn->connect_error) {
11.	    die("Connection failed: " . $conn->connect_error);
12.	}
Frontend Setup:
1.	Ensure the HTML and CSS files are linked properly.
2.	Include JavaScript files for search functionality.
________________________________________
How It Works
1.	User Interaction:
o	Users enter an ingredient in the search bar and submit the query.
2.	Request Handling:
o	JavaScript captures the input and sends it to the server via an AJAX request.
3.	Server-Side Processing:
o	PHP receives the query, processes it, and queries the MySQL database for retrieving concerns.
4.	Response Delivery:
o	The server sends the results back to the JavaScript frontend, which dynamically updates the "Your Search Results" section.
________________________________________
Directory Structure
MealFinder/
|-- index.html        # Main HTML file
|-- About.html        # Second HTML file
|-- Contact.html        # 3rd HTML file
|-- style.css         # CSS file for styling
|-- script.js         # JavaScript file for interactivity
|-- Submit_form.php        # PHP file for handling concerns/info
|-- /assets/          # Folder for images and additional resources
________________________________________
Future Enhancements
1.	Add user authentication for personalized features.
2.	Allow users to save favorite recipes.
3.	Expand database to include nutritional information.
4.	Enhance search functionality with advanced filtering options.
________________________________________
Credits
•	Designed and developed by our group (BALANQUIT, DESTURA, RAYALA, DE LUNA, ESTIDO)

