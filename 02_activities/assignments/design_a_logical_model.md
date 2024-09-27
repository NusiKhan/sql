# Assignment 1: Design a Logical Model

## Question 1
Create a logical model for a small bookstore. 📚

At the minimum it should have employee, order, sales, customer, and book entities (tables). Determine sensible column and table design based on what you know about these concepts. Keep it simple, but work out sensible relationships to keep tables reasonably sized. Include a date table. There are several tools online you can use, I'd recommend [_Draw.io_](https://www.drawio.com/) or [_LucidChart_](https://www.lucidchart.com/pages/).



![sqlassign1](https://github.com/user-attachments/assets/fe86310f-39de-46d9-a867-fdbb583d2216)

## Question 2
We want to create employee shifts, splitting up the day into morning and evening. Add this to the ERD.
![sqlassign2](https://github.com/user-attachments/assets/29888db3-902d-4a18-8964-e777a823c781)

## Question 3
The store wants to keep customer addresses. Propose two architectures for the CUSTOMER_ADDRESS table, one that will retain changes, and another that will overwrite. Which is type 1, which is type 2?

_Hint, search type 1 vs type 2 slowly changing dimensions._

Bonus: Are there privacy implications to this, why or why not?
```
Your answer...
```
type1
![sqltype1](https://github.com/user-attachments/assets/c040fa2b-76da-4c1e-8c26-926144ce8bd5)

![sqltype2](https://github.com/user-attachments/assets/77432c1f-00b0-431b-91b4-1483b34da8b9)
type 2
There are privacy concerns with both type 1 and 2 but more so with type 2. 
With type 1 incase there is a data breach or someone just wants to steal a customer's address they can just find it from the current address database.
With type 2 not only can they view the present address, but they can also track a history of changes in a customers addresses. Which in the case of a data breach
is more information lost. And unsafe for the customers. Especially given that it's a book store and probably doesn't have a lot of security. 

## Question 4
Review the AdventureWorks Schema [here](https://i.stack.imgur.com/LMu4W.gif)

Highlight at least two differences between it and your ERD. Would you change anything in yours?
```
Your answer...

The adventure works schema is a much larger more complicated logical model. It has a separate column for keeping track of primary and foreign keys. Which can be helpful when a logical model is as complex and detailed as the adventure works schema.
It also keeps a record of history for sales, purchases. And each table contains a lot more information, especially about the employees. 
In my bookstore ERD the model is not as complex, has simpler relationships between each table and does not contain so much personal information and history. 

I think the columns tracking changes in price history would be a good inclusion. The product category in the adventure works schema is also a good inclusion, except in our case maybe adding genre as a category would be very helpful. Adding an invetory table would also be useful.





    

Checklist:
- [ ] Create a branch called `model-design`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack at `#cohort-4-help`. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
