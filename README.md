Hello and welcome! This GitHub repository contains a collection of tests for a Booking API(https://restful-booker.herokuapp.com), organized and tested to demonstrate the functionality of the API endpoints using the Postman API testing tool. The tests cover various HTTP methods i.e. POST, GET, DELETE, and PUT, offering a complete assessment of the functionalities of API testing and calling.
## Description of API calls and tests

Create Booking: POST method HTTP request is used here in order to create booking data and dynamic data is used using Pre-request script. These dynamic data are saved in environment variables as well for future validation. From the response body, bookingid is fetched and stored as environment variable id1.
- Create Booking: POST method HTTP request is used here in order to create booking data and dynamic data is used using Pre-request script. These dynamic data are saved in environment variables as well for future validation. From response body, bookingid is fetched and stored as environment variable id1.

![App Screenshot](https://github.com/SultanaMargia/Restful_API_Testing/blob/main/pic/create.png)

- Get Booking Info: GET method HTTP request is used here to fetch Booking data that was created before. A number of API testings are performed for Status code validation, as well as validation of all data that is recieved in response body with stored environment variables.

![App Screenshot](https://github.com/SultanaMargia/Restful_API_Testing/blob/main/pic/get.png)

- Token: POST method HTTP request is used here to enter username and password data for receiving the token. This token will be used as permission for updating existing data as well as deleting stored data.

![App Screenshot](https://github.com/SultanaMargia/Restful_API_Testing/blob/main/pic/token.png)

- Update Booking Info: PUT method HTTP request is used here to override the existing Booking data with new data. For update access permission, token is entered in the header. Here static data is given as input for variation.

![App Screenshot](https://github.com/SultanaMargia/Restful_API_Testing/blob/main/pic/update.png)

- Get Booking Info Updated: GET method HTTP request is used here to fetch new Booking data. Here status code validation as well as data validation is made for the updated Booking info.

![App Screenshot](https://github.com/SultanaMargia/Restful_API_Testing/blob/main/pic/updateget.png)

- Delete Booking: DELETE method HTTP request is used here to delete the data associated with id1. For delete access permission, the token is entered in the header.

![App Screenshot](https://github.com/SultanaMargia/Restful_API_Testing/blob/main/pic/delete.png)

## Newman Report Generation

At first, API collection as well as API environment is exported in a folder for Newman report generation. Using the command-line interface inside the exported directory folder, the following command-line is used for Newman report generation:

Newman run Marzia_API_Test.postman_collection.json -e Marzia_api_test.postman_environment.json -r cli,htmlextra

![App Screenshot](https://github.com/SultanaMargia/Restful_API_Testing/blob/main/pic/report.png)

## Usage

- Clone the repository to your local environment.
- Import the provided Postman collection to access the pre-configured test suite.
- Run the test suite using Postman to execute the tests against the Booking API.
- View the generated test report to gain insights into the API's behavior and performance.
