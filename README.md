# Pre Owned Cars.

SELECT * FROM cars.car_dekho;
Use Cars;
-- Read Data--
Select * from car_dekho;

-- Total Cars: To get a count of total Recods--

Select count(*) From Car_dekho;

-- The manager asked employee how Many cars will be available in 2023? ---
Select count(*) From Car_dekho 
Where year = 2023;

-- The manager asked employee how Many cars will be available in 2020, 2021, 2022? ---
-- Group By--

Select count(*), year  From Car_dekho
Where year in (2020, 2021, 2022)
group by year;

-- Client Asked me to prient the total of all cars by years, I dont want to see other details.--

Select count(*), year  From Car_dekho
group by year;

-- Client asked to cars dealer that how many diesel cars will there be in 2020? --

Select count(*)  From Car_dekho
Where year = 2020 and fuel =  "Diesel";


Select count(*)  From Car_dekho
Where year = 2020 and fuel =  "Petrol";

-- The manager told the employee to give a print All the fuel cars (petrol, diesel, and CNG) come by all year. --

Select year, Count(*) from car_dekho where fuel = "petrol" group by year;
Select year, Count(*) from car_dekho where fuel = "Diesel" group by year;
Select year, Count(*) from car_dekho where fuel = "CNG" group by Year;

-- Manager said there were more than 100 cars in a given year, which year had more than 100 cars?--

Select year, Count(*) from car_dekho group by Year having count(*)>100;

-- The manager said to the employee All cars count details between 2015 and 2023; we need a complete list.

select count(*) from car_dekho where year between 2015 and 2023;

-- The manager said to the employee All cars details between 2015 to 2023 we need complete list--

Select*from car_dekho where year between 2015 and 2023;

-- END -- 


