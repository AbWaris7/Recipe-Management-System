🍽️ Recipe Manager API
A multi-user web service built with Spring Boot that allows users to store, retrieve, update, and delete recipes securely. Whether you're preserving grandma’s cake or saving that viral recipe, this service keeps everything in one place!

🚀 Features
✅ User registration & login (with Spring Security)

🍲 CRUD operations for recipes (Create, Read, Update, Delete)

🔐 Access control (Users can only manage their own recipes)

🕒 Stores creation date with LocalDateTime

💾 In-memory H2 database for development

🧰 Uses Project Lombok to reduce boilerplate

📦 RESTful JSON API

🧠 Technologies & Concepts
Java 17+

Spring Boot 3+

Spring Security (Basic Auth)

H2 Database

Spring Data JPA

REST API + JSON

Project Lombok

LocalDateTime for timestamps


📂 API Endpoints
Method	Endpoint	Description	Auth Required
POST	/api/register	Register new user	❌ No
POST	/api/recipe/new	Create a new recipe	✅ Yes
GET	/api/recipe/{id}	Get a recipe by ID	✅ Yes
GET	/api/recipe/search?name=&category=	Search recipes	✅ Yes
PUT	/api/recipe/{id}	Update a recipe (owner only)	✅ Yes
DELETE	/api/recipe/{id}	Delete a recipe (owner only)	✅ Yes

🏗️ Project Structure

├── RecipeManager/
│   ├── controller/
│   ├── entity/
│   ├── repository/
│   ├── service/
│   ├── security/
│   └── RecipeManagerApplication.java


🔐 User Registration & Authentication
Users register via /api/register

Authentication via HTTP Basic Auth

Passwords are securely stored using BCrypt

📦 How to Run Locally
bash
Kopieren
Bearbeiten
# Clone the repo
git clone https://github.com/yourusername/RecipeManager.git
cd RecipeManager

# Build and run the application
./mvnw spring-boot:run
Visit: http://localhost:8080

H2 Console: http://localhost:8080/h2-console


Register User
json
Kopieren
Bearbeiten
POST /api/register
{
  "email": "user@example.com",
  "password": "securepass"
}


Create Recipe
json
Kopieren
Bearbeiten
POST /api/recipe/new
{
  "name": "Chocolate Cake",
  "category": "Dessert",
  "date": "2025-05-05T14:00:00",
  "description": "Rich and moist chocolate cake",
  "ingredients": ["Flour", "Eggs", "Chocolate"],
  "directions": ["Mix ingredients", "Bake for 30 mins"]
}


🧹 To-Do / Future Improvements
🌐 Deploy to Heroku or Railway

🧾 Swagger UI for documentation

🧪 Add unit and integration tests

☁️ Use PostgreSQL for production

🧑‍💻 Author
Abdul Waris Khan
📍 Zurich, Switzerland
👨‍💻 Backend & DevOps Enthusiast
