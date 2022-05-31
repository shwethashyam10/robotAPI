# REST API Robot application

One of SVT's microservices calculates which robot should transport a pallet from point A to point B based on which robot is the closest and has the most battery left if there are multiple in the proximity of the load's location. You'll use a provided API endpoint to create a simplified robot routing API.

This is the endpoint to retrieve a list of robots in our robot fleet: https://60c8ed887dafc90017ffbd56.mockapi.io/robots. Note: if that URL doesn't work, a mirror is available here - https://svtrobotics.free.beeceptor.com/robots.

The provided API returns a list of all 100 robots in our fleet. It gives their current position on an xy-plane along with their battery life. Your job is to write an API with an endpoint which accepts a payload with a load which needs to be moved including its identifier and current x,y coordinates and your endpoint should make an HTTP request to the robots endpoint and return which robot is the best to transport the load based on which one is closest the load's location. If there is more than 1 robot within 10 distance units of the load, return the one with the most battery remaining.

## Requirements
 python3

    pip3 install flask
    pip install flask_cors 

## Run the app

    # For Mac/Linux
	export FLASK_APP=flaskr
	export FLASK_ENV=development
	# Make sure to run this command from the project directory (not from the flaskr)
	flask run

The REST API to the example app is described below.

## Get closest robot

### Request

`POST http://127.0.0.1:5000/api/robots/closest/`

    

### Response

    Request URL: http://127.0.0.1:5000/api/robots/closest/
	Request Method: POST
	Status Code: 200 OK
	Remote Address: 127.0.0.1:5000


## To test API

	An HTML form can be accessed at http://127.0.0.1:5000/ which submits the payload to above API


# Next things to do

- I would further create more unit testing and intergration testing
- I would like to use object oriented programming with better code formmatting and doc strings
- Adding more security
