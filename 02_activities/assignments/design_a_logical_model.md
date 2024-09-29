# Assignment 1: Design a Logical Model

## Question 1
Create a logical model for a small bookstore. 📚
![Entity-Relationship Diagram (ERD) for Bookstore drawio](https://github.com/user-attachments/assets/965d52bb-ad36-4ed3-ab99-e865b938da71)

At the minimum it should have employee, order, sales, customer, and book entities (tables). Determine sensible column and table design based on what you know about these concepts. Keep it simple, but work out sensible relationships to keep tables reasonably sized. Include a date table. There are several tools online you can use, I'd recommend [_Draw.io_](https://www.drawio.com/) or [_LucidChart_](https://www.lucidchart.com/pages/).

## Question 2
We want to create employee shifts, splitting up the day into morning and evening. Add this to the ERD.
![Entity-Relationship Diagram (ERD) for Bookstore drawio (1)](https://github.com/user-attachments/assets/812946df-f259-4f99-b0b2-60e2754d6861)


## Question 3
The store wants to keep customer addresses. Propose two architectures for the CUSTOMER_ADDRESS table, one that will retain changes, and another that will overwrite. Which is type 1, which is type 2?

_Hint, search type 1 vs type 2 slowly changing dimensions._

Bonus: Are there privacy implications to this, why or why not?
```
Your answer...
```
![Entity-Relationship Diagram (ERD) for Bookstore drawio Q3](https://github.com/user-attachments/assets/543b08ed-7473-42ca-8c11-b3a78cda7674)

![Entity-Relationship Diagram (ERD) for Bookstore drawio (3)](https://github.com/user-attachments/assets/818b1a08-7103-47de-9ad0-34d356a60e30)

# Question 4
Review the AdventureWorks Schema [here](https://i.stack.imgur.com/LMu4W.gif)

Highlight at least two differences between it and your ERD. Would you change anything in yours?
```
Difference 1: 

Bookstore ERD: In the bookstore ERD, customer details such as name, contact information, and address were all in a single table (or separated to a lesser degree). This results in some level of data redundancy.

Difference 2: 
AdventureWorks Schema: The Address table in the AdventureWorks schema links to other tables (Customer) through a relationship, and the schema appears to manage addresses by associating them with a specific order or entity, possibly allowing multiple addresses per customer.
Bookstore ERD: The proposed architecture for handling customer addresses included two options: one overwriting the previous address (Type 1) and another retaining address history (Type 2).
Potential Change: Inspired by the AdventureWorks schema, we could add an OrderAddress table that links Address to specific orders, making it possible to track which address was used for each specific order. This change can help if the bookstore wants to maintain records of past addresses in relation to sales.

Summary of Changes to Consider
Address Tracking: Implement an OrderAddress table to link addresses to individual orders, thereby retaining more specific history related to sales.
These changes would align the bookstore’s schema more closely with best practices and would be beneficial for scalability and detailed record-keeping, as exemplified by the AdventureWorks model.

# Criteria

[Assignment Rubric](./assignment_rubric.md)

# Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `September 28, 2024`
* The branch name for your repo should be: `model-design`
* What to submit for this assignment:
    * This markdown (design_a_logical_model.md) should be populated.
    * Two Entity-Relationship Diagrams (preferably in a pdf, jpeg, png format).
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sql/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `model-design`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack at `#cohort-4-help`. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
