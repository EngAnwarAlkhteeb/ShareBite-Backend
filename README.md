# ShareBite Backend

The API backend for **ShareBite** — a location-based surplus-food distribution platform that connects food providers (individuals, restaurants, stores) with people who need it, to reduce food waste in Indonesia.

## Stack
Node.js + Express 4, MongoDB (Mongoose), JWT auth, bcrypt, Multer (image uploads), Stripe, Firebase config present for deployment.

## API
Base URL: `http://localhost:4000`

| Route | Purpose |
|---|---|
| `GET /` | Health check — "API Working" |
| `/api/food` | Food listings |
| `/api/user` | Users / auth |
| `/api/cart` | Cart |
| `/api/order` | Orders |
| `/images` | Uploaded food images (static) |

## Structure
```
├── server.js          # Express app, port 4000
├── config/db.js       # MongoDB connection
├── models/ controllers/ routers/ maddleware/
├── uploads/           # Uploaded images
├── firebase.json vercel.json
└── .env               # Not committed — see below
```

## Run it
```bash
npm install
node server.js
# or: npx nodemon server.js
```

Set `MONGODB_URI` (and any Stripe / JWT secrets) in a local `.env` file. Never commit real secrets — `.env` is gitignored.

## Notes
- This is the standalone backend repo. The full ShareBite app (frontend + this backend) lives in [Share-Bite](https://github.com/EngAnwarAlkhteeb/Share-Bite), and a NestJS version is in [Share-Bite-NestJs-NestJS](https://github.com/EngAnwarAlkhteeb/Share-Bite-NestJs-NestJS).
