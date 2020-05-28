# Weather-Bot
A  telegram robot that can answer you about the real-time weather around the world.

This procedure has realized a simple artificial intelligence procedure.By asking the robot about the weather in different cities, the robot responds to the current weather in the corresponding city.

If the name of the city the questioner visits exists in more than one country, the robot will list all the countries that contain the city, providing a reference for the questioner.According to these countries, the questioner chooses the country in which he wants to get the information city.Based on the questioner's answer, the robot gives the required weather conditions for the city.If the city the questioner is asking about does not exist, or if the country he is answering does not exist, the robot will tell the questioner that it cannot find the information he needs.

This is a screenshot of the program in action, which contains what it does when it encounters incorrect input.
![procedure runing result](https://github.com/a-lazy-cat/Weather-Bot/blob/master/show.jpg)

Defination of different functions.

get_city_information(city,country,time):
By sending city name,country name and time, this function will return the weather information of the city in the country that argument gives. Time often be set as 'now'. Which represents that the function returns the current weather information.

get_city_name(message):
By sending the message that user types, this function will interpret the city name from this message.

city_to_countries(city_name):
This function can find the country name, by recieving the city name. Then, it will return the country name.

iscity(city_name):
By sending the city name into this function, this function can tell wheather this name is a city name. If ture, it will retrun True, else return False.

iscountry(country_name):
By sending the country name into this function, this function can tell wheather this name is a country name. If ture, it will retrun True, else return False.

get_weather_info(countries_list,city,time):
Explaination of the arguments:
countries_list: a list that stores country name.
city: city name.
time: often be set as 'now'
When countries_list contains more than one country name or less than one country name, this function will return different values like 'none' or 'more cities'. When the countries_list contains only one country name, this function will reutrn the city's current weather information.

send_message(state, message,new_response,policy,city_name):
This function is used to send response to the user. In this function, states will be changed basing on different conditions. 
Explaination of the arguments:
state: Represent the state of current communication.
message: The message that user tpyes in.
new_response: Represent last time response.
policy: the policy of state transformation
city_name: The city that user want to know its weather

 respond(policy, state, message,city_name):
 Used to generate the respond message
 Explaination of the arguments:
 policy: the policy of state transformation
 state: Represent the state of current communication.
 message: The message that user tpyes in.
 city_name: The city that user want to know its weather
 
 interpret(message):
 By sending user's message, this function will interpret the details of the message. To be specific, the function will interpret the message's intends, entities in this message and so on.
