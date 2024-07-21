# Wander Abode

Wander Abode is a mini Airbnb-type website where users can list their properties for renting out. This project utilizes Node.js, Express, EJS, HTML, CSS, JavaScript, Bootstrap, and Mongoose for building and managing the platform.

## Features

- Users can post listings with details including title, description, image, price, location, and country.
- Default image provided if none is specified.
- Responsive design using Bootstrap for an optimal user experience across devices.

## Schema

The schema for the listings is defined as follows:

```javascript
const listingSchema = new Schema({
  title: {
    type: String,
    required: true,
  },
  description: String,
  image: {
    type: String,
    default:
      "https://tse4.mm.bing.net/th?id=OIP.aV3_1sg9QEdADlu5byNWbwAAAA&pid=Api&P=0&h=220",
    set: (v) =>
      v === ""
        ? "https://tse4.mm.bing.net/th?id=OIP.aV3_1sg9QEdADlu5byNWbwAAAA&pid=Api&P=0&h=220"
        : v,
  },
  price: Number,
  location: String,
  country: String,
});
```

## Technologies Used

- **Backend**: Node.js, Express
- **Frontend**: EJS, HTML, CSS, JavaScript, Bootstrap
- **Database**: Mongoose (MongoDB)
