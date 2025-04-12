# Server Statistics Dashboard

Interactive dashboard for displaying server statistics with modern design and additional features.

## Main Features

### Server Statistics
- Player count display
- Room count
- Server uptime
- Platform and version information

### Chat
- Public chat for all users
- Auto-refresh every 5 seconds
- Auto-clear every 5 minutes
- XSS attack protection
- Message length limit (500 characters)

### News
- Latest news display
- Auto-refresh every 5 minutes
- News appearance animation
- Responsive design

### Visual Effects
- Animated video background
- Animated header
- Track animation with moving cars
- Mobile-responsive design

### Multilingual Support
- Russian and English language support
- Language preference saving
- Automatic interface switching

## Technical Requirements

- PHP 7.4 or higher
- MySQL 5.7 or higher
- Web server (Apache/Nginx)
- Modern browser with JavaScript support

## Installation

1. Clone the repository:
```bash
git clone [repository-url]
```

2. Configure database connection in `config.php`

3. Create required database tables:
```sql
CREATE TABLE IF NOT EXISTS chat_messages (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) NOT NULL,
    message TEXT NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

CREATE TABLE IF NOT EXISTS news (
    id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(255) NOT NULL,
    content TEXT NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

4. Set file permissions:
```bash
chmod 755 -R .
chmod 777 -R data/
```

5. Configure web server for PHP

## Project Structure

```
├── config.php          # Database configuration
├── index.php          # Main application file
├── chat.php          # Chat handler
├── news.json         # News file
├── assets/           # Static files
│   ├── css/         # Styles
│   ├── js/          # JavaScript files
│   ├── images/      # Images
│   └── videos/      # Video files
└── data/            # Application data
```

## Security

- SQL injection protection
- XSS attack protection
- Input validation
- Message length restrictions
- Automatic chat clearing

## License

MIT License

## Author

Perce - [GitHub](https://github.com/theperce) 
