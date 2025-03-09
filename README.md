## 🚀 AlgoSprint - Real-time Coding Progress Tracker

### 📌 Introduction :

AlgoSprint is an advanced real-time coding progress tracker designed for LeetCode, GeeksforGeeks, and other coding platforms. It provides users with leaderboards, performance graphs, and authentication to track and improve their problem-solving skills. The platform is implemented using Java (Spring Boot) and MySQL, ensuring scalability and efficiency.

### ✨ Features :

- 📊 Real-time Coding Progress Tracking for LeetCode and GeeksforGeeks.

- 🏆 Leaderboard System to compare rankings with other users.

- 🔐 User Authentication using secure login and session management.

- 📈 Performance Graphs to visualize coding consistency and growth.

- 🗄 Database-Driven Storage using MySQL for secure and structured data.

- ⚡ RESTful API Integration for fetching coding statistics dynamically.

- 🎯 Goal-Setting and Achievement Tracking to stay motivated.

- 📧 Email Notifications for updates, milestones, and leaderboard changes.

### 🛠 Technologies Used :
- ☕ Java (Spring Boot) – Backend framework for handling API requests and business logic.

- 🗄 MySQL – Relational database for storing user data and coding progress.

- 🌐 React.js (Optional) – Frontend for an interactive user experience.

- 🔐 JWT Authentication – Secure login and user session management.

- 📡 REST APIs – Fetching and updating real-time coding progress.

- 📊 Chart.js/Recharts – Data visualization for performance graphs.

### 🏗 Installation & Setup
  #### Prerequisites

- Java 17+

- MySQL Server

- Maven

- IDE (IntelliJ IDEA, VS Code, or Eclipse)

#### Steps to Run the Project

###### 1. Clone this repository:

```bash
git clone https://github.com/swathi-57/AlgoSprint
```
##### 2. Navigate to the project directory:
```bash
cd algosprint
```
###### 3. Configure the application.properties file with MySQL credentials:

```bash
spring.datasource.url=jdbc:mysql://localhost:3306/algosprint
spring.datasource.username=root
spring.datasource.password=yourpassword
```

##### 4. Run the application:
```bash
mvn spring-boot:run
```

##### 5. Access the API at:
```bash
http://localhost:8080/api/
```
    

### 📌 Usage Example
```bash
@RestController
@RequestMapping("/user")
public class UserController {
    @Autowired
    private UserService userService;

    @GetMapping("/progress")
    public ResponseEntity<UserProgress> getProgress(@RequestParam Long userId) {
        return ResponseEntity.ok(userService.getUserProgress(userId));
    }
}
```

###  🎯 API Endpoints
| Method | Endpoint    | Description                |
| :-------- | :------- | :------------------------- |
| `POST` | `/auth/register` | Register a new user
| `POST` | `/auth/login` | User login
| `GET` | `/auth/progress` | Fetch user progress
| `GET` | `/leaderboard` | Retrieve leaderboard rankings
| `POST` | `/goals/set` | Set coding goals
| `GET` | `/stats/graph` | Fetch performance graph data




### 🤝 Contributing

 If you want to contribute, feel free to fork this repository and submit a pull request.

### 📜 License

This project is licensed under the MIT License.
