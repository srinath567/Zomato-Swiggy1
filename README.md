# Zomato-chronicles

## Introduction
Zomato Chronicles is a Django project that simulates an online food ordering system. It allows users to browse available dishes, add them to their cart, place orders, and track their order history. This project demonstrates the implementation of a food delivery platform using Django, complete with user authentication, database models, and a responsive user interface.

## Features
- **User Registration and Authentication**: Users can register for an account, log in, and log out securely. Passwords are hashed for security.
- **Dish Management**: Admins can add, update, and delete dishes, including details like name, description, price, and availability.
- **Shopping Cart**: Users can add dishes to their shopping cart, view and edit their cart items, and place orders.
- **Order History**: Users can view their order history, including order status and total cost.
- **Search Functionality**: Users can search for dishes by name.
- **Responsive UI**: The user interface is responsive, ensuring a seamless experience on various devices.

## Prerequisites
Before you begin, make sure you have the following installed:
- Python (3.x)
- Django (install using `pip install Django`)
- Required Python packages from `requirements.txt`

## Screenshots


### Home Page
![Home Page](https://github.com/Amanastel/Zomato-django/blob/main/assest/img/Screenshot%202023-09-16%20at%2012.01.16%20PM.png?raw=true)

### Dish Management
![Dish Management](https://github.com/Amanastel/Zomato-django/blob/main/assest/img/Screenshot%202023-09-16%20at%2012.09.03%20PM.png?raw=true)

### Shopping Cart
![Shopping Cart](https://github.com/Amanastel/Zomato-django/blob/main/assest/img/Screenshot%202023-09-16%20at%2012.01.58%20PM.png?raw=true)

### About US
![About US](https://github.com/Amanastel/Zomato-django/blob/main/assest/img/Screenshot%202023-09-16%20at%2012.01.32%20PM.png?raw=true)

## Getting Started
Follow these steps to install and run the project:

1. Clone the repository: `git clone https://github.com/Amanastel/Zomato-django.git`
2. Navigate to the project directory: `cd Zomato-django`
3. Create a virtual environment: `python -m venv venv`
4. Activate the virtual environment:
   - On Windows: `venv\Scripts\activate`
   - On macOS and Linux: `source venv/bin/activate`
5. Install project dependencies: `pip install -r requirements.txt`
6. Apply database migrations: `python manage.py migrate`
7. Create a superuser for admin access: `python manage.py createsuperuser`
8. Start the development server: `python manage.py runserver`

## Usage
- Access the application at: `http://localhost:8000/`
- Admin panel is available at: `http://localhost:8000/admin/`

## API Endpoints
### Authentication
- **User Registration:** `POST /register/`
  - *Description:* Allows users to register for an account.

- **User Login:** `POST /login/`
  - *Description:* Allows users to log in securely.

- **User Logout:** `GET /logout/`
  - *Description:* Allows users to log out.

### Dish Management
- **Add a Dish:** `POST /addDish/`
  - *Description:* Allows admins to add a new dish to the menu.

- **Update Dish Availability:** `POST /update_availability/<int:dish_id>/`
  - *Description:* Allows admins to update the availability status of a dish.

- **Update Dish Details:** `POST /update_dish/<int:dish_id>/`
  - *Description:* Allows admins to update the details of a dish.

- **Delete a Dish:** `POST /delete-dish/<int:id>/`
  - *Description:* Allows admins to delete a dish from the menu.

- **List Dishes:** `GET /dish/`
  - *Description:* Retrieves a list of available dishes.

### Cart
- **View Cart:** `GET /view_cart/`
  - *Description:* Allows users to view the contents of their shopping cart.

- **Update Cart Item:** `POST /update_cart_item/<int:item_id>/`
  - *Description:* Allows users to update the quantity of items in their cart.

- **Add to Cart:** `POST /add_to_cart/<int:dish_id>/`
  - *Description:* Allows users to add a dish to their shopping cart.

- **Place an Order:** `POST /place_order/`
  - *Description:* Allows users to place an order for items in their cart.

- **Order History:** `GET /order_history/`
  - *Description:* Retrieves the order history for a user.

## Custom User Model
The project uses Django's built-in User model for user authentication.

## Models
- **Dish**: Represents food dishes with details such as name, price, availability, and image.
- **Menu**: Associates dishes with users and allows users to set the quantity.
- **Order**: Represents user orders, including the dishes, quantity, total price, and order status.
- **Cart**: Stores user cart items with dish details and quantity.

## Technology Stack
- Django
- Python
- Django REST framework
- HTML/CSS
- Bootstrap

