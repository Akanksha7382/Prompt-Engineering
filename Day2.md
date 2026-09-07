# Day 2 - Give Context

## Prompt Engineering Learning Series

**Previous Topic:** [Day 1 - Be Specific](./Day-01.md)

**Today's Topic:** Give Context

---

# 1. What is Context?

Context is the background information that we provide to an AI model so that it can better understand our situation, requirements, goal, or problem.

In simple words:

> Context tells the AI what it needs to know before it decides how to answer.

An AI model does not automatically know our complete situation.

For example:

```text
Explain Python.
```
This prompt does not tell the AI:

Who is learning Python?
What is their current knowledge?
Why do they want to learn Python?
What topics should be covered?
Should the explanation be basic or advanced?
Should examples be included?
Is the user preparing for an interview or an exam?

2. Why is Context Important?

Context helps the AI understand what we actually need.

Compare these two prompts.

Without Context
Teach me SQL.

The AI does not know:

My current SQL knowledge
My goal
My experience
What topics I need
How I prefer to learn
With Context
I know basic SQL SELECT queries, but I don't understand
JOINs and subqueries.

I am learning SQL for software developer interviews.

Teach me JOINs first using a simple employee database.
Use practical examples and give me practice questions.

Now the AI understands:

Current skill level
Weak area
Goal
Topic to teach
Learning style

Therefore, the response can be much more relevant.

3. Simple Definition

A useful definition to remember:

Context is relevant background information given to an AI model to help it understand the situation and produce a more appropriate response.

4. Real-World Analogy

Imagine that you ask a teacher:

Teach me programming.

The teacher might ask:

What programming language do you know?

Are you a beginner?

Why do you want to learn programming?

Are you preparing for an exam or interview?

What topics do you already know?

The teacher needs this information before creating a lesson.

This information is the context.

The same idea applies to AI.

Human Teacher
      ↓
Needs information about student
      ↓
Understands student's situation
      ↓
Provides suitable teaching

Similarly:

AI Model
      ↓
Receives context
      ↓
Understands user's situation
      ↓
Generates more relevant response
5. Context vs Instruction

Context and instructions are related, but they are not the same.

Context

Context is information that the AI needs to know.

Example:

I am a beginner in JavaScript.

This tells the AI about my current situation.

Instruction

An instruction tells the AI what to do.

Example:

Explain JavaScript functions.

This tells the AI the task.

Example
I am a beginner in JavaScript.

Explain JavaScript functions using simple examples.

Here:

Context:
I am a beginner in JavaScript.

Instruction:
Explain JavaScript functions using simple examples.
6. Context vs Constraint

A constraint is a rule that the AI must follow.

Example:

I am learning JavaScript.

This is context.

Do not use external libraries.

This is a constraint.

Example:

I am learning JavaScript and I want to understand
how arrays work.

Write a solution without using external libraries.

Here:

Context → I am learning JavaScript
Task → Explain arrays
Constraint → Don't use external libraries
7. Context vs Output Format

Output format tells the AI how the answer should be structured.

Example:

I am a beginner in Python.

Explain Python functions.

Give the answer in this format:

1. Definition
2. Syntax
3. Example
4. Explanation
5. Practice Questions

Here:

Context:
I am a beginner in Python.

Task:
Explain Python functions.

Output Format:
Definition → Syntax → Example → Explanation → Questions
8. Different Types of Context

There are many types of context that can be useful in a prompt.

8.1 User Context

Tell the AI about the person using it.

Examples:

I am a beginner in Python.
I have two years of experience with React.
I am a computer engineering student.
I already understand basic SQL.

This allows the model to adjust its response according to the user's level.

9. Skill-Level Context

One of the most useful types of context is your current knowledge level.

For example:

Beginner
I have never worked with APIs before.
Intermediate
I understand REST APIs and HTTP methods,
but I don't understand authentication.
Advanced
I have experience designing REST APIs
and working with OAuth and JWT.

The same question can produce very different answers depending on this context.

10. Goal Context

Tell the AI why you need the information.

For example:

I am learning Python for data analysis.

or:

I am learning Python for a software developer interview.

or:

I need Python for my college project.

These three goals may require different learning approaches.

11. Project Context

When working on a project, give the AI information about the project.

Example:

I am building a student management system.

Frontend:
React

Backend:
Node.js

Database:
MongoDB

The application allows teachers to add,
update and delete student records.

Now you can ask:

Suggest a database structure for my project.

The AI can use the project context when answering.

12. Technical Context

Technical context is especially important when asking programming questions.

Example:

I am building a web application using:

Frontend: React
Backend: Node.js
Database: MongoDB
Build Tool: Vite

Then:

How should I implement authentication?

This is much better than:

How do I implement authentication?

because the model knows the technology stack.

13. Environment Context

Sometimes the environment matters.

For example:

I am using Windows 11.

My project is a React application created using Vite.

I am using Node.js 20 and npm.

Then:

How can I install Axios?

Now the AI knows the environment.

Without this information, the answer may contain instructions that are not appropriate for your setup.

14. Problem Context

When debugging, explain the actual problem.

Bad Prompt
My API is not working.

This provides almost no useful context.

Better Prompt
I am building a React application.

I have a filter component.

When I select a filter, the selected value
appears correctly in the UI.

However, when I click the Apply button,
the API request is not triggered.

The state is updating correctly.

I want to find out why the API function
is not being called.

Now the AI knows:

Technology:
React

Feature:
Filter

Expected Behavior:
API should be called

Actual Behavior:
API is not called

State:
Updating correctly

Goal:
Find the reason for the missing API call

This is useful context.

15. Desired Outcome as Context

Sometimes we should explain what result we want.

For example:

I am learning SQL.

I want to become comfortable solving
SQL interview questions within 30 days.

Then:

Create a learning plan for me.

The goal provides important context.

16. Audience Context

When asking AI to create educational or professional content, tell it who will read the content.

Example:

Explain machine learning to first-year
computer engineering students who have
basic programming knowledge.

Now the AI knows:

Audience
Knowledge level
Topic

Compare that with:

Explain machine learning.

The second prompt leaves the audience unknown.

17. Context Can Change the Answer

This is one of the most important concepts in Prompt Engineering.

Consider:

Explain machine learning.

The model may give a general explanation.

Now add:

I am a first-year engineering student
and I have no machine learning background.

The explanation will likely be simpler.

Now change the context:

I am preparing for a machine learning interview.

I already understand regression,
classification and neural networks.

The explanation can become much more advanced.

Therefore:

The same task + different context = different appropriate response.

18. Before and After Examples
Example 1 - Python
Without Context
Teach me Python.
With Context
I know basic programming concepts such as
variables, loops and conditions.

I am new to Python.

I want to learn Python for backend development.

Start by teaching me functions and modules.
Use simple examples.
19. Example 2 - React
Without Context
Explain React hooks.
With Context
I know JavaScript and React components,
but I am new to React Hooks.

I am currently building a React application.

Explain useState and useEffect first.

Use practical examples and explain each
line of code.
20. Example 3 - SQL
Without Context
Explain SQL JOINs.
With Context
I understand SELECT, WHERE and GROUP BY,
but I don't understand JOINs.

I am learning SQL for software developer interviews.

Explain INNER JOIN, LEFT JOIN and RIGHT JOIN.

Use an employee and department database
for all examples.

Start with simple examples before moving
to interview-level problems.
21. Example 4 - Debugging
Without Context
Fix my code.
With Context
I am building a React application using
class components.

I have a filter modal.

The selected filter is displayed correctly,
but after clicking Apply, the API request
does not happen.

I have already verified that the state is
being updated.

Review the relevant code and identify
why the API call is not being triggered.
22. Example 5 - Interview Preparation
Without Context
Prepare me for an interview.
With Context
I am preparing for a frontend developer interview.

I have experience with:

- HTML
- CSS
- JavaScript
- React

I have 15 days to prepare.

My weak areas are:
- JavaScript asynchronous programming
- React hooks
- Performance optimization

Create a 15-day preparation plan.

The second prompt gives the AI enough information to create a much more useful plan.

23. How Much Context Should I Give?

A common beginner mistake is thinking:

"More context is always better."

That is not true.

The goal is:

Give relevant context, not unnecessary context.

Too Little Context
Help me with React.

Problem:

The AI doesn't know what you need.

Too Much Irrelevant Context
I woke up at 7 AM.

I had breakfast.

I opened my laptop.

My laptop is black.

I use Windows.

I like coffee.

I started coding at 10 AM.

I am using React.

Help me fix my component.

Most of this information is irrelevant.

Good Context
I am working on a React application using
class components.

The filter state updates correctly,
but the API call does not happen after
clicking Apply.

Help me identify the problem.

This is focused and relevant.

24. The Context Selection Rule

Before adding context, ask yourself:

"Does the AI need this information to answer my question correctly?"

If the answer is yes, include it.

If the answer is no, leave it out.

25. A Simple Context Formula

A useful formula for beginners is:

CONTEXT

Who am I?
+
What do I know?
+
What am I working on?
+
What am I trying to achieve?
+
What problem am I facing?
+
What have I already tried?

You don't need every item in every prompt.

Use only the information that is relevant.

26. Combining Day 1 and Day 2

In Day 1, we learned:

Be Specific

In Day 2, we are learning:

Give Context

Now combine both.

Example:

Act as a senior JavaScript instructor.

I am a beginner in JavaScript.
I understand variables, loops and functions,
but I am still learning arrays.

Teach me the map(), filter() and reduce()
methods.

Use simple examples.

For each method:
1. Explain the concept.
2. Show the syntax.
3. Give an example.
4. Explain the code line by line.
5. Give me two practice questions.

Do not use advanced concepts.

Let's identify the components.

Role
Act as a senior JavaScript instructor.
Context
I am a beginner in JavaScript.
I understand variables, loops and functions,
but I am still learning arrays.
Task
Teach me map(), filter() and reduce().
Constraints
Do not use advanced concepts.
Output Format
1. Concept
2. Syntax
3. Example
4. Explanation
5. Practice questions
27. Context Does Not Mean Giving the Answer

This is another important point.

Context should help the model understand the situation.

For example:

I am struggling to understand recursion.

This is context.

You don't need to tell the model the solution.

Then:

Explain recursion using a simple analogy.

This is the task.

28. Context for AI Learning

You can also give context about how you want to learn.

Example:

I am learning Prompt Engineering from scratch.

I prefer practical examples over theoretical
explanations.

After each concept, I want:
- A simple explanation
- A real-world analogy
- Bad prompt
- Improved prompt
- Practice exercise

This context helps AI behave more like a personal teacher.

29. Context for Professional Work

Suppose you want AI to write a message.

Without Context
Write a message to my manager.
With Context
I need to inform my manager that I completed
the assigned development task.

The changes have been tested locally and
are ready for staging deployment.

Write a short professional message.

Now the AI knows the situation.

30. Context for Data Analysis

Suppose you have sales data.

Without Context
Analyze this data.
With Context
This dataset contains monthly sales data
for a retail company.

Columns include:
- Product
- Region
- Month
- Revenue
- Units Sold

The business wants to identify products
with declining sales.

Analyze the data and identify important trends.

Now the AI understands the business objective.

31. Context for Image Understanding

Context can also be useful when working with images.

For example:

This is a screenshot of my React application.

The issue I am investigating is the large
empty space between the filter tags and
the filter button.

Analyze the screenshot and identify
possible UI/CSS causes.

The context tells the model what to look for.

32. Context for Documents

Suppose you give AI a document.

Instead of:

Summarize this document.

You can say:

I am preparing for an exam.

The following document contains lecture notes
for my subject.

Create revision notes focusing on:
- Important definitions
- Key concepts
- Examples
- Possible exam questions

Keep the explanations simple.

Now the model knows the purpose of the summary.

33. A Professional Prompt Structure

A useful structure is:

# ROLE

Who should the AI act as?

# CONTEXT

What does the AI need to know?

# TASK

What should the AI do?

# REQUIREMENTS

What must be included?

# CONSTRAINTS

What should the AI avoid?

# OUTPUT FORMAT

How should the final answer be structured?

Example:

# ROLE
Act as a senior Python instructor.

# CONTEXT
I am a beginner in Python.
I know basic programming concepts.

# TASK
Teach me Python functions.

# REQUIREMENTS
Explain parameters, return values and
default arguments.

# CONSTRAINTS
Use simple examples.
Avoid advanced Python features.

# OUTPUT FORMAT
1. Explanation
2. Example
3. Code walkthrough
4. Practice questions
34. Context Checklist

Before submitting a prompt, ask:

 Did I explain my situation?
 Did I tell the AI my knowledge level?
 Did I explain my goal?
 Did I provide relevant technical details?
 Did I explain the actual problem?
 Did I mention what I already tried?
 Did I provide important constraints?
 Did I remove irrelevant information?
35. Common Mistakes
Mistake 1: Giving Too Little Context
Fix my code.
Better

Explain:

Technology
Problem
Expected behavior
Actual behavior
Error
Relevant code
Mistake 2: Giving Irrelevant Context

Don't provide information that has nothing to do with the task.

Mistake 3: Assuming AI Knows Your Project

AI does not automatically know your entire project.

Tell it the relevant:

Architecture
Technology
Requirements
Current behavior
Expected behavior
Mistake 4: Assuming AI Knows Your Skill Level

Tell it whether you are:

Beginner
Intermediate
Advanced
Mistake 5: Giving Context After the Model Already Answered

Ideally, provide important context before asking the model to solve the problem.

36. Practical Exercise 1

Start with this:

Teach me JavaScript.

Improve it by adding:

Current knowledge:
Goal:
Topic:
Learning preference:
Difficulty:
Output format:
37. Practical Exercise 2

Start with:

Fix my API.

Improve it by adding:

Frontend:
Backend:
Database:
Expected behavior:
Actual behavior:
Error:
What I already tried:
Goal:
38. Practical Exercise 3

Start with:

Prepare me for an interview.

Add:

Job role:
Experience:
Technologies:
Interview date:
Strong areas:
Weak areas:
Goal:
Available preparation time:
Preferred learning style:
39. Day 2 Challenge

Create a prompt for this situation:

You are learning JavaScript and have a frontend developer interview in 15 days.

Your prompt should include:

Role
Context
Skill level
Goal
Available time
Technologies
Weak areas
Learning preference
Requirements
Output format

Try writing the prompt yourself before asking AI to improve it.

40. Prompt Improvement Challenge

After creating your prompt, give it to an AI model and ask:

Review my prompt.

Identify any missing context.

Tell me which parts are ambiguous.

Explain what information I should add
and why.

Do not completely rewrite my prompt.

This exercise teaches you to evaluate prompts, not just write them.

41. Day 2 Key Learnings

Today I learned:

Context gives the AI relevant background information.
Context reduces ambiguity.
Context helps the AI understand the user's situation.
Context can include skill level, goal, project, environment, audience and problem details.
Context should be relevant.
More context does not always mean better context.
Context is different from instructions.
Context is different from constraints.
Context can change the type and level of response.
Good context helps the AI produce a more relevant answer.
42. Important Rule to Remember

Give the AI enough relevant information to understand the situation, but don't overload the prompt with unnecessary information.

Because this information is missing, the model has to make assumptions.
