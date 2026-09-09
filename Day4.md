# Day 4 - Break Complex Tasks into Steps

## Prompt Engineering Learning Series

**Previous Topics:**
- Day 1 - Be Specific
- Day 2 - Give Context
- Day 3 - Give Examples / Few-Shot Prompting

**Today's Topic:** Break Complex Tasks into Steps

---

# 1. Introduction

In the previous days, we learned how to write better prompts by:

- Being specific
- Giving relevant context
- Providing examples

Today we will learn another important Prompt Engineering technique:

> **Break complex tasks into smaller steps.**

This technique is also called:

> **Task Decomposition**

The basic idea is simple:

Instead of asking the AI to solve a large and complicated problem in one step, divide the problem into smaller, manageable tasks.

---

# 2. What is Task Decomposition?

Task decomposition means breaking one large task into multiple smaller tasks or steps.

For example, instead of asking:

```text
Build a complete e-commerce application.
```

we can break it into:

1. Define requirements
2. Design database
3. Design API
4. Create backend
5. Create frontend
6. Implement authentication
7. Implement product management
8. Implement cart
9. Implement payment
10. Test the application

Each step is easier to understand and complete.

3. Why Do We Need to Break Complex Tasks?

Large tasks often contain many smaller problems.

For example:

Build a student management system.

This sounds like one task.

But actually it contains:

Requirements
     ↓
Database
     ↓
Backend
     ↓
Authentication
     ↓
APIs
     ↓
Frontend
     ↓
Validation
     ↓
Testing
     ↓
Deployment

If we ask the AI to do everything at once, the response may:

Become too large
Miss important requirements
Make assumptions
Mix different parts of the problem
Produce inconsistent results
Become difficult to review
Contain errors that are difficult to identify

Breaking the task into steps gives us more control.

4. Simple Example
Complex Prompt
Create a website for a college.

This is very broad.

The AI has to guess:

What pages?
What users?
What technology?
What database?
What features?
What design?
What authentication?
What content?
Decomposed Prompt

Instead, start with:

Step 1:

Define the requirements for a college
student management website.

Identify:
- Users
- Main features
- Pages
- Required data
- Authentication requirements

Then:

Step 2:

Based on the requirements, design the
database schema.

Then:

Step 3:

Design the REST APIs required by the application.

Then:

Step 4:

Create the backend structure.

Then:

Step 5:

Create the frontend structure.

Now each stage has a clear purpose.

## Sequential Task Decomposition

Sometimes the output of one step becomes the input for the next step.

Example:

Step 1
Requirements
   ↓
Step 2
Database Design
   ↓
Step 3
API Design
   ↓
Step 4
Backend Implementation
   ↓
Step 5
Frontend Implementation

This is called a sequential workflow.

Each step depends on the previous step.

## Parallel Tasks

Not every task needs to happen sequentially.

Some tasks can be independent.

For example, when planning an application:

                 Project
                    ↓
        ┌───────────┼───────────┐
        ↓           ↓           ↓
    Database     UI Design    API Design
        ↓           ↓           ↓
        └───────────┼───────────┘
                    ↓
               Integration

Database design, UI design and API planning can sometimes be worked on independently.

Then they can be combined.

# Hierarchical Task Decomposition

A large task can also be divided into major tasks and smaller subtasks.

Example:

Build E-commerce Application

1. Authentication
   1.1 Registration
   1.2 Login
   1.3 Logout
   1.4 Password Reset

2. Products
   2.1 Add Product
   2.2 Update Product
   2.3 Delete Product
   2.4 Search Product

3. Cart
   3.1 Add to Cart
   3.2 Remove from Cart
   3.3 Update Quantity

4. Orders
   4.1 Create Order
   4.2 View Orders
   4.3 Cancel Order

This is hierarchical decomposition.
