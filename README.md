<h1 align="center">KTU S5 DBMS LAB(CSL333) </h1>
<h2>👉Lab Cycle 1</h2>

<h3>1.Design a normalized database schema for the following requirement.</h3>
<h3>The requirement:</h3>A library wants to maintain the record of books, members, book issue, book return, and fines collected for late returns, in a database. The database can be loaded with book information. Students can register with the library to be a member. Books can be issued to students with a valid library membership. A student can keep an issued book with him/her for a maximum period of two weeks from the date of issue, beyond which a fine will be charged. Fine is calculated based on the delay in days of return. For 0-7 days: Rs 10, For 7 – 30 days: Rs 100, and for days above 30 days: Rs 10 will be charged per day.

<h3>Sample Database Design</h3>
BOOK (Book_Id, Title, Language_Id, MRP, Publisher_Id, Published_Date, Volume, Status) //Language_Id, Publisher_Id are FK (Foreign Key)


AUTHOR(Author_Id, Name, Email, Phone_Number, Status) 

BOOK_AUTHOR(Book_Id, Author_Id) // many-to-many relationship, both columns are PKFK(Primary Key and Foreign Key) 

PUBLISHER(Publisher_id, Name, Address) 

MEMBER(Member_Id, Name, Branch_Code, Roll_Number, Phone_Number, Email_Id, Date_of_Join, Status) 

BOOK_ISSUE(Issue_Id, Date_Of_Issue, Book_Id, Member_Id, Expected_Date_Of_Return, Status) // Book+Id and Member_Id are FKs 

BOOK_RETURN(Issue_Id, Actual_Date_Of_Return, LateDays, LateFee) // Issue_Id is PK and FK

LANGUAGE(Language_id, Name) //Static Table for storing permanent data

LATE_FEE_RULE(FromDays, ToDays, Amount) // Composite Key

<h2>EXERCISES</h2>
   <h3>1.Create a normalized database design with proper tables, columns, column types, and constraints </h3>
   <h3>2. Create an ER diagram for the above database design.</h3>
   <h3>3.Write SQL commands to
     <h4>a. Create a database by name Library. Drop the database and re-create it.</h4>
     <h4>b. Create DDL statements and create the tables and constraints (from the design) in the database created in step-a (Library)</h4>
          Notes: [ Create a script file and execute it. Create the script file in such a way that,,if the table exists, drop the tables and recreate )]
     <h4>c. Create and execute DROP TABLE command in tables with and without FOREIGN KEY constraints.</h4>
     <h4>d. Create and execute ALTER TABLE command in tables with data and without data.</h4>
     <h4>e. Create and execute SQL commands to build indices on Member_Id and Book_Id on table Book_Issue.</h4>
     <h4>f. Create and execute GRANT/REVOKE commands on tables.</h4>
     <h4>g. Create and execute SQL commands to insert data into each of the tables designed</h4>
     <h4>h. Learn and execute bulk import of data to tables from CSV files (insert 1000 records of books into the BOOK table from a CSV file).</h4>
     <h4>i. Create and execute UPDATE/DELETE commands on tables. Try to update/delete rows with Primary and Foreign Keys. Try bulk updates or deletes using SQL UPDATE statement      </h4>
   <h3>4.Write SQLQuery to retrieve the following information</h3>
     <h4>a. Get the number of books written by a given author.</h4>
     <h4>b. Get the list of publishers and the number of books published by each publisher. </h4>
     <h4>c. Get the names of authors who jointly wrote more than one book.</h4>
     <h4>d. Get the list of books that are issued but not returned.</h4>
     <h4>e. Get the list of students who reads only ‘Malayalam’ books</h4>
     <h4>f. Get the total fine collected for the current month and current quarter </h4>
     <h4>g. Get the list of students who have overdue (not returned the books even on due date)</h4>
     <h4>h. Calculate the fine (as of today) to be collected from each overdue book.</h4>
     <h4>i. Members who joined after Jan 1 2021 but has not taken any books.</h4>
  <h2>👉Lab Cycle 2</h2>
  

