Import express from "express";
import cors from "cors";
const app = express();
const PORT = process.env.PORT || 5000;
app.use(cors());
app.use(express.json());
app.get("/api", (req, res) => {
res.json({ message: "Welcome to ModernVueSite API 🚀" });
});
app.post("/api/contact", (req, res) => {
const { name, email, message } = req.body;
console.log("Contact form submission:", { name, email, message });
res.json({ status: "success", message: "Message received!" });
});
app.listen(PORT, () => console.log(`✅ Server running on port ${PORT}`));
{
"name": "modernvuesite-server",
"version": "1.0.0",
"main": "index.js",
"type": "module",
"scripts": {
"start": "node index.js",
"dev": "nodemon index.js"
},
"dependencies": {
"cors": "^2.8.5",
"express": "^4.18.2"
},
"devDependencies": {
"nodemon": "^3.0.1"
}
}
{
"name": "modernvuesite",
"private": true,
"workspaces": [
"client",
"server"
],
"scripts": {
"install:all": "npm install --workspaces",
"start": "npm run start --workspace server",
"dev": "concurrently \"npm run dev --workspace client\" \"npm run dev --workspace
server\""
},
"devDependencies": {
"concurrently": "^8.2.0"
}
}