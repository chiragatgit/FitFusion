
# Project Goal

The goal of the project is to develop FitFusion, a fitness application that enables trainers to assign workouts and diets to customers through an online platform. Customers can securely log in, access their exercise routines, and follow them, facilitated by JWT authentication.

![fitfusionapp](https://github.com/chiragatgit/FitFusion/assets/119803371/afb208c5-49f9-41b3-8a01-f11acaa7f010)

## AuthController

### Public API:

- **POST** `/auth/login` (`@RequestBody JwtRequest jwtRequest`): This API allows users to log in.

## DietController

### TRAINER APIs:

- **GET** `/diet/all`: This API lets a trainer fetch all diets. It returns an OK response status.
- **GET** `/diet/{id}` (`@PathVariable Long id`): This API allows a trainer to fetch a diet by its ID. It returns an OK response status.
- **POST** `/diet/create/{userId}` (`@RequestBody DietDto dietDto`, `@PathVariable Long userId`): This API allows a trainer to create a diet for a user using the user’s ID. It returns a CREATED response status.
- **PUT** `/diet/{id}` (`@RequestBody DietDto dietDto`, `@PathVariable Long id`): This API allows a trainer to update a diet by its ID. It returns an OK response status.
- **DELETE** `/diet/{id}` (`@PathVariable Long id`): This API allows a trainer to delete a diet by its ID. It returns an OK response status.

## ExerciseController

### TRAINER APIs:

- **GET** `/exercise/all`: This API lets a trainer fetch all exercises. It returns an OK response status.
- **GET** `/exercise/{id}` (`@PathVariable Long id`): This API lets a trainer fetch an exercise by its ID. It returns an OK response status.
- **POST** `/exercise/create/{userId}` (`@RequestBody ExerciseDto exerciseDto`, `@PathVariable Long userId`): This API allows a trainer to create an exercise for a user by using the user’s ID. It returns a CREATED response status.
- **PUT** `/exercise/{id}` (`@RequestBody ExerciseDto exerciseDto`, `@PathVariable Long id`): This API allows a trainer to update an exercise by its ID. It returns an OK response status.
- **DELETE** `/exercise/{id}` (`@PathVariable Long id`): This API allows a trainer to delete an exercise by its ID. It returns an OK response status.

## UserController

### ADMIN APIs:

- **GET** `/user/all`: This API lets the admin fetch all users. It returns an OK response status.
- **GET** `/user/{id}` (`@PathVariable Long id`): This API allows the admin to fetch a user by its ID. It returns an OK response status.
- **PUT** `/user/{id}` (`@RequestBody UserDto userDto`, `@PathVariable Long id`): This API allows the admin to update a user by its ID. It returns an OK response status.
- **DELETE** `/user/{id}` (`@PathVariable Long id`): This API allows the admin to delete a user by its ID. It returns an OK response status.

### CUSTOMER APIs:

- **GET** `/user/exercise/{id}` (`@PathVariable Long id`): This API lets the customer fetch all his/her exercises by the userId. It returns an OK response status.
- **GET** `/user/diet/{id}` (`@PathVariable Long id`): This API lets the customer fetch all his/her diets by the userId. It returns an OK response status.

### PUBLIC APIs:

- **POST** `/user/register` (`@RequestBody UserDto userDto`): This API allows the user to register and be assigned a role.
