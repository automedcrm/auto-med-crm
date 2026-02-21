# BOT_ARCHITECTURE

## Telegram Bot Architecture

This document outlines the architecture of the Telegram bot used in the AutoMedCRM application, including its initialization, message handling, user roles, and keyboard interfaces.

### Overview
The Telegram bot is built to manage interactions between users and the AutoMedCRM system efficiently. The diagram below showcases the entire architecture.

```mermaid
graph TD;
    A[Start] --> B[Initialization];
    B --> C{Message Handler};
    C -->|Text Message| D[Process Text];
    C -->|Callback Query| E[Process Callback];
    C -->|Inline Query| F[Process Inline];
    D --> G{User Role};
    G -->|Admin| H[Admin Interface];
    G -->|Operator| I[Operator Interface];
    H --> J[Admin Keyboard];
    I --> K[Operator Keyboard];
    E --> L[Process Callback Result];
    F --> M[Process Inline Result];
    J --> N[Send Feedback];
    K --> O[Submit Request];
    N --> P[End];
    O --> P;
``` 

### Components
1. **Bot Initialization**: Initializes the bot and sets up necessary configurations.
2. **Message Handlers**: Captures and processes different types of messages received from users.
3. **User Roles**: Determines whether the user is an admin or operator and directs them to the appropriate interface.
4. **Keyboard Interfaces**: Provides the respective keyboards for the admin and operator for easy access to functionalities.

### User Roles
- **Admin**: Has full control over the bot, able to manage settings and user queries.
- **Operator**: Limited access to handle user inquiries and support requests.

### Conclusion
Understanding the bot architecture is crucial for maintaining and enhancing the functionality of the bot within the AutoMedCRM application.