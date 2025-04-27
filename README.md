# Pterodactyl Manager API Wrapper

![GitHub license](https://img.shields.io/github/license/v7an/pterodactyl-manager)
![GitHub stars](https://img.shields.io/github/stars/v7an/pterodactyl-manager)
![GitHub issues](https://img.shields.io/github/issues/v7an/pterodactyl-manager)

A powerful and easy-to-use API wrapper for Pterodactyl's API, providing a seamless integration of server management and user administration functionalities.

## Features
 
- **User Management**: Effortlessly manage users with create, update, delete, and retrieval capabilities.
- **Server Manipulation**: Control servers with options for creation, suspension, reinstallation, and more.
- **File Operations**: Manage files and directories on servers, including read, write, and folder creation.
- **Server Information**: Retrieve detailed information about servers and users.
- **Discord Support**: Need help or have questions? Join our [Discord server](https://discord.gg/altvine) for support and discussions.

## Installation

```bash
npm install pterodactyl-manager
```

# Usage

```js
const PteroManager = require('pterodactyl-manager');

// Initialize the wrapper
const ptero = new PteroManager('your-api-key', 'https://your-ptero-instance.com');

// Example usage
(async () => {
  const newUser = await ptero.createUser({
    username: 'newuser',
    email: 'newuser@example.com',
    password: 'securepassword'
  });

  const newServer = await ptero.createServer({
    name: 'My New Server',
    user: newUser.id,
    // ... other server properties
  });

  // ... more examples of wrapper functions
})();
```

# Documentation
Check out the [full documentation](https://github.com/v7an/pterodactyl-manager/docs) for detailed usage examples.

# Support

Join our [Discord server](https://discord.gg/altvine) for support and discussions.
