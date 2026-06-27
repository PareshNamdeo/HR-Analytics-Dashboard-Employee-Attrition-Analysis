# HR-Analytics-Dashboard-Employee-Attrition-Analysis

select * from `hr_analytics (1)` ;
SELECT * FROM `hr analytics`.`hr_analytics (1)`;
select count(*) from  `hr_analytics (1)` ;

1. Total Employees
SELECT COUNT(*) AS total_employees
FROM `hr_analytics (1)`;

2. Total Attrition Employees
select count(*) from `hr_analytics (1)`
where Attrition = 'yes' ;

3. Attrition Rate
select 
ROUND(100.0*sum(case when attrition = 'yes' then 1 else 0 end)/ count(*),2 as attrition_rate from `hr_analytics (1)` ;

4. Department Wise Employee Count
select department,count(*) as total_emp from `hr_analytics (1)`
group by department ;

5. Department Wise Attrition
select department,count(*) as total_emp from `hr_analytics (1)`
where attrition = 'yes'
group by department ;

6. Average Salary by Department
select department,avg(MonthlyIncome) as Avg_sal from `hr_analytics (1)`
group by department ;

7. Top 10 Highest Paid Employees ï»¿EmpID
select ï»¿EmpID,MonthlyIncome as max_sal from `hr_analytics (1)` 
order by  MonthlyIncome desc
limit 10;

8. Gender Distribution
select gender ,count(*) as total_emp from `hr_analytics (1)`
group by gender;

9. Overtime vs Attrition
select OverTime, count(*) from `hr_analytics (1)`
where Attrition = 'yes'
group by Overtime ;

10. Average Years At Company
select avg(YearsAtCompany) from `hr_analytics (1)`;




