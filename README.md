# etl-challenge
-- Create Two Tables
CREATE TABLE gender_inequality (
 
 id INT PRIMARY KEY,
 
 gii_rank INT,
	
  country TEXT,
	
  gender_inequality_index INT,
	
  maternal_mortality_ratio INT,
	
  adolescent_bith_rate INT,
	
  percent_representation_in_parliament INT,
	
  population_with_secondary_education_female INT,
	
  population_with_secondary_education_male INT,
	
  labor_force_participation_rate_female INT,
	
  labor_force_participation_rate_male INT
);

--------------------------------------------------------------------------------------------------------------------

CREATE TABLE gender_development (
  
  id INT PRIMARY KEY,
  
  gdi_rank INT,
  
  country TEXT,
  
  gender_development_index INT,
	
  human_development_index_female INT,
	
  
  human_development_index_male INT,
	
  life_expectancy_at_birth_female INT,
	
  
  life_expectancy_at_birth_male INT,
	
  expected_years_of_education_female INT,
	
  expected_years_of_education_male INT,
	
  mean_years_of_education_female INT,
	
  mean_years_of_education_male INT,
	
  estimated_gross_national_income_per_capita_female INT,
	
  estimated_gross_national_income_per_capita_male INT
);

--------------------------------------------------------------------------------------------------------------------------------------------------------------

SELECT * FROM gender_inequality;

SELECT * FROM gender_development;

-- Join tables on country
SELECT gender_inequality.id, gender_inequality.gii_rank, gender_development.gdi_rank

FROM gender_inequality

INNER JOIN country

ON gender_inequality.country = gender_development.country
