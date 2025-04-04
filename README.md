UnVolunteers Data Analysis

What is importance of non-profit organisation and how do they Benefit Data Analysis?
Nonprofit organizations play a crucial role in society by addressing social, 
economic, and environmental challenges. They focus on advancing public causes,
filling gaps that government or private sectors may not address, such as education,
healthcare, poverty alleviation, and environmental conservation. 
Their importance lies in their ability to create meaningful change
and uplift communities.


When it comes to data analysis, nonprofit organizations benefit significantly. Here’s how:
·	Informed Decision-Making: By analyzing data, nonprofits can better understand their target audience, 
   assess program impact, and allocate resources efficiently.
·	Optimizing Fundraising Efforts: Data insights help identify key donor trends, 
  allowing organizations to tailor campaigns and maximize donations.
·	Improved Transparency and Accountability: Sharing analyzed data with stakeholders
  builds trust and demonstrates the impact of their work.
·	Enhanced Program Effectiveness: By evaluating program performance through data, 
   nonprofits can adapt their strategies to achieve better outcomes.
   In essence, data analysis empowers nonprofits to amplify their positive impact and achieve their missions effectively.


   Data Cleaning
   In the power BI Query Editors we begin by removing duplicate values from the volunteers_id
   Column, Next, we replace any blank value with N/A for consistency, we the change the datatype
   of the volunteers_Id columns from text to  integer Additionally, we modify the datatype for
   Assignments Durations Age as per our requirements.

   In power Bi Query Editors we create new column for age_groups starting with range such as 
   18-20 upto 50-60+ Additionally, we Removed the rows where the Assignment Durations Equals to 2
   we change the formats of data columns from 01-06-2007 to 2007-06-01, we then extract the month,
   year,day from the date columns and splits the data into seperators columns for each attribute.

   Dax Formulas
   when working with the volunteers data for international and local (national Analysis) in your case
   ,you are calculating of efforts in your case, you are calculating and National Amount on the total
   number of volunteers and respective proprotions for international and national contributions

   = international = Round[Total_volunteers]* [international],-2)
   = National = Round[Total_Volunteers] *[national],-2)

   total volunteers = this is respresent the total Vounteers
   International = this is the proportions of percentage of volunteers
                   contributing to international efforts
  Rounds = the result of multiplication is rounded to the nearest hundered
           ,ensuring a cleaners and more presentable number

  (-2) : the indicate rounding two place before the decimal point rounding
          the decimal point(eg.rounding to the nearest 100)
