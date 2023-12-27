// Include necessary modules
const express = require('express');
const cors = require('cors');

// Initialize express app
const app = express();

// Enable CORS for all routes
app.use(cors());

// Define a route that returns a JSON response
app.get('/api/fancy', (req, res) => {
 res.json({ message: 'You are viewing a fancy API!' });
});

// Start the server
const port = process.env.PORT || 3000;
app.listen(port, () => {
 console.log(`Server is running on port ${port}`);
});
