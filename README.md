# world_population

In this SQL PROJECT, i have practiced some SQL queries with 2021_population of the world. In this project i have analyzed the data based on 2020 and 2021 population. 
The whole query was done on MYSQL. 

select * from 2021_population; 


select * from 2021_population
where 2021_last_updated = (select max(2021_last_updated) from 2021_population);   -- which country has the highest population in 2021
 
 select * from 2021_population
 where 2021_last_updated = (select min(2021_last_updated)from 2021_population);   -- which country has the least number of people in 2021

select * from 2021_population
where country = 'India';                                                          -- find the population of india with all details

select country,2021_last_updated from 2021_population
where country in ('Guinea', 'Nepal', 'Iran');                                      -- show the name and the population for Guinea, Nepal, Iran 

select avg(2021_last_updated) as average_popualtion 
from 2021_population;                                                              -- find the average population in whole world in 2021

 select iso_code,country,2021_last_updated - 2020_population as increased_population_count
 from 2021_population;                                                           -- find out how much population was increased from 2020-2021 for all countries
 
 select sum(2021_last_updated) as total_pop_2021,
 sum(2020_population) as total_pop_2020
 from 2021_population;                                                             -- find out the total population of the world in 2021 and 2020?
 
  select count(country)
  from 2021_population
  where area < 1000000; 
                                                                                   -- find countries whose area is less than 10 lakh sq_km
                                                                                   
                                                                                   
                                                                                   
 # the dataset is taken from kaggle.                                                                                 
                                                                                   
