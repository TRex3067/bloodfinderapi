# bloodFinderApi
This is an Express Application providing REST API for a blood-donor finder web application, with jwt authentication.

## Local Setup

1. Run `npm install`
2. Change configuration in the bin/config.js file
3. Run `npm start`

# API

The users are registered under two categories either as a "Donor" or as a "Medical Organization", and the API exposes certain end points to them based on the category.

## Routes

* **/donor**
  * `/donor/` - fetch the profile information
  * `/donor/register` - register as a donor
  * `/donor/login` - login as a donor
  * `/donor/incoming` - get all the incoming requests from the user's inbox
  * `/donor/accept/:req_id` - accept a particular request from inbox
  * `/donor/reject/:req_id` - reject a particular request from inbox
  
* **/med**
  * `/med/` - fetch the profile information
  * `/med/register` - register user as a medical organization
  * `/med/login` - login as a medical organization
  * `/med/requests` - fetch all the requests generated by the user
  * `/med/requests/generate` - generate a new request
  * `/med/search` - fetch all the donors in the vicinity of the medical organization upto certain distance
  * `/med/requests/req_id` - fetch or delete a particular request
  * `/med/requests/:req_id/response` - view the user responses to a request
