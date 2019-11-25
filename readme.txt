**********************************************
Summary of Approach
**********************************************
Having no experience in developing Web Services in MuleSoft, I followed the below steps:
- Studied the MuleSoft architecture
- Understood the design tools that I will be using for development (API DesignCenter and Anypoint Studio)
- Exercised 2 tutorials on MuleSoft portal:
	- Designing your first API
	- Developing your first Mule application
- Understand the basics of RAML and DataWeave languages

The above items helped me understand the basics needed to start developing the coding challenge.

**********************************************
Challenges
**********************************************
I was challenged on below items:
- Tranforming the database data to http response message

**********************************************
Accomplishments
**********************************************
I was able to complete the following items:
- Implement the API using RAML on DesignCenter for 2 methods:
	- GetWeather
	- GetCitiesByCountry
- Import API from Exchange into Mulesoft project
- Implement MuleSoft project using Anypoint Studio
- Configure HTTP listener
- Configure database extract from MySQL database
	
Created MySQL database and tables:

CREATE TABLE weather.temperature (
  `country_name` varchar(45) NOT NULL,
  `city_name` varchar(45) NOT NULL,
  `celcius` int(11) NOT NULL,
  PRIMARY KEY (`country_name`,`city_name`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

delete from weather.temperature;
insert into weather.temperature values ("Australia", "Sydney", "35");
insert into weather.temperature values ("Australia", "Melbourne", "19");
insert into weather.temperature values ("Australia", "Brisbane", "23");
insert into weather.temperature values ("Australia", "Perth", "33");
insert into weather.temperatutemperaturere values ("Australia", "Adelaide", "22");
insert into weather.temperature values ("Australia", "Gold Coast", "25");
insert into weather.temperature values ("Australia", "Canberra", "26");
select * from weather.temperature;


curl -X GET localhost:8081/api/GetWeather/Melbourne/Australia

curl -X GET localhost:8081/api/GetCitiesByCountry/Australia
Select t.city_name, t.celcius from temperature t where t.country_name = :country_name;