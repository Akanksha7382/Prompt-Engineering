# Day 6 - Ask for Clarification and Avoid Assumptions

## Prompt Engineering Learning Series

**Previous Topics:**

* Day 1 - Be Specific
* Day 2 - Give Context
* Day 3 - Give Examples / Few-Shot Prompting
* Day 4 - Break Complex Tasks into Steps
* Day 5 - Define Constraints and Requirements

**Today's Topic:** Ask for Clarification and Avoid Assumptions

---

# 1. Introduction

During the previous five days, we learned how to create better prompts.

We learned:

### Day 1 - Be Specific

Tell the AI exactly what you want.

### Day 2 - Give Context

Give the AI the background information it needs.

### Day 3 - Give Examples

Show the AI examples of the expected result.

### Day 4 - Break Complex Tasks into Steps

Divide a large task into smaller steps.

### Day 5 - Define Constraints

Tell the AI the rules and boundaries it must follow.

Today we will learn another very important technique:

> **Tell the AI what to do when information is missing or unclear.**

This means teaching the AI:

* When to ask questions
* When not to guess
* Which information is required
* Which information is optional
* How to handle missing information
* How to identify ambiguity
* How to identify conflicting requirements
* How to request clarification before proceeding

---

# 2. What Is an Assumption?

An assumption is when someone decides that something is true without having enough information to know that it is true.

For example:

```text
Build a website for my company.
```

There is a lot of missing information.

The AI does not know:

* What type of company?
* What pages are required?
* What colors should be used?
* Who are the customers?
* What technology should be used?
* Is authentication required?
* Is there an existing design?
* Is there an existing project?

If the AI guesses these details, those guesses are assumptions.

---

# 3. Simple Definition

Remember:

> **Assumption = Guessing missing information.**

> **Clarification = Asking for missing information before proceeding.**

Example:

```text
User:
Create a dashboard for my application.

AI:
What type of application is it?
What information should the dashboard display?
Which technology are you using?
```

The AI is asking for clarification instead of guessing.

---

# 4. Why Is This Important?

AI can generate an answer even when the prompt is incomplete.

That can be useful sometimes.

But it can also create incorrect results.

For example:

```text
Create an API for my application.
```

The AI might assume:

```text
Node.js
Express
MongoDB
JWT
```

But perhaps your application actually uses:

```text
Python
FastAPI
PostgreSQL
OAuth
```

The answer could look technically correct while still being completely wrong for your project.

Therefore:

> **A confident answer is not always a correct answer.**

---

# 5. Real-World Analogy

Imagine you ask a developer:

> "Fix the login problem."

The developer asks:

> "What exactly is happening?"

You say:

> "Users cannot log in."

The developer asks:

> "What error do they see?"

You say:

> "Invalid credentials."

The developer asks:

> "Does this happen for all users or only some users?"

This conversation continues until enough information is available.

The developer should not immediately rewrite the entire authentication system.

AI should work similarly.

---

# 6. Bad Prompt

Consider:

```text
Fix my React application.
```

This is too vague.

The AI does not know:

* What is broken?
* Which component?
* What error?
* What should happen?
* What currently happens?
* Is the problem frontend or backend?
* Should the existing architecture remain unchanged?

---

# 7. Better Prompt

```text
You are a React developer helping me debug my application.

If the information I provide is insufficient,
do not guess.

Ask me the necessary questions before suggesting
a solution.

Only provide a fix after you have enough information.
```

This changes the behavior of the AI.

Instead of immediately producing code, it should first identify missing information.

---

# 8. The "Don't Guess" Instruction

One of the most useful instructions is:

```text
Do not make assumptions.
```

But you can make it even better:

```text
Do not make assumptions about information that I have
not provided.

If important information is missing, ask me for it
before proceeding.
```

This is much clearer.

---

# 9. Example - Coding

### Bad Prompt

```text
Create a login API.
```

There are many unanswered questions:

* Which language?
* Which framework?
* Which database?
* Authentication method?
* User fields?
* Password hashing?
* Response format?

### Better Prompt

```text
Create a login API.

Before writing code:

1. Identify the information you need.
2. Ask me for any missing information.
3. Do not assume the technology stack.
4. Do not assume the database.
5. Do not assume the authentication method.

Only write the implementation after I provide
the required information.
```

---

# 10. Required vs Optional Information

Not every missing piece of information is equally important.

For example, suppose you want a login API.

### Required information

```text
Programming language
Framework
Database
Authentication method
User schema
```

### Optional information

```text
Preferred variable names
Comment style
Exact function names
```

If required information is missing, the AI should ask.

If optional information is missing, the AI may be able to choose a reasonable default.

---

# 11. A Useful Rule

Think about missing information like this:

```text
Is the information necessary?

        |
       YES
        ↓
Ask for clarification.

        |
       NO
        ↓
Use a reasonable default.
```

However, if the decision could significantly change the result, asking is usually better.

---

# 12. Example - Website Design

User says:

```text
Create a website for my business.
```

Important questions might include:

```text
1. What type of business is it?
2. Who is the target audience?
3. What pages are required?
4. Do you have a preferred technology?
5. Do you have existing branding?
6. What functionality is required?
```

Instead of guessing, ask.

---

# 13. Example - Resume Writing

Suppose the user says:

```text
Write my resume.
```

The AI needs important information.

For example:

```text
- Education
- Skills
- Experience
- Projects
- Certifications
- Contact information
- Target job role
```

A good prompt could be:

```text
Help me create my resume.

Before writing it:

- Ask me for any missing important information.
- Do not invent experience.
- Do not invent skills.
- Do not invent certifications.
- Do not exaggerate my achievements.

If something is missing, ask me first.
```

---

# 14. Why "Do Not Invent" Is Important

Suppose someone says:

```text
Create my resume.
I know JavaScript.
```

The AI should not automatically write:

```text
Expert in JavaScript
```

or:

```text
5 years of JavaScript experience
```

Those facts were never provided.

Instead, it should only use the information given.

This is especially important for:

* Resumes
* Reports
* Documentation
* Academic work
* Legal information
* Financial information
* Technical specifications
* Project documentation

---

# 15. Example - Project Documentation

Bad:

```text
Create a README for my project.
```

The AI might invent:

* API endpoints
* Environment variables
* Features
* Installation commands
* Database structure

Better:

```text
Create a README for my project.

Use only the information I provide.

Do not invent:

- Features
- APIs
- Environment variables
- Database tables
- Technologies
- Commands

If any important information is missing,
ask me before writing the README.
```

---

# 16. Ambiguous Instructions

Sometimes the information exists, but the instruction itself can have multiple meanings.

This is called ambiguity.

Example:

```text
Make the button bigger.
```

What does "bigger" mean?

Maybe:

```text
Wider
```

Maybe:

```text
Taller
```

Maybe:

```text
Larger font
```

Maybe:

```text
All of the above
```

The AI should ask:

```text
Do you want the button to be wider, taller,
or both?
```

---

# 17. Another Example

Consider:

```text
Make the application faster.
```

What does faster mean?

Possible meanings:

* Faster page loading
* Faster API response
* Faster database queries
* Faster rendering
* Faster startup
* Faster search

A better prompt would define the target.

Or ask:

```text
Which part of the application is currently slow?
```

---

# 18. Ambiguous Coding Request

User:

```text
Optimize my API.
```

This is ambiguous.

The AI should ask:

```text
What problem are you seeing?

- Slow response time?
- High CPU usage?
- High memory usage?
- Too many database queries?
- Large response payloads?
- High traffic?
```

Now the AI can identify the actual problem.

---

# 19. Clarification Before Code

This is especially important in software development.

Instead of:

```text
Here is some code. Fix it.
```

Use:

```text
Review the code first.

If the problem is not clear:

1. Identify what information is missing.
2. Ask clarification questions.
3. Wait for the answers.
4. Then suggest the smallest possible fix.

Do not rewrite the code before understanding the problem.
```

---

# 20. Don't Ask Unnecessary Questions

There is another important lesson.

You should not tell AI to ask questions about everything.

Bad:

```text
Ask me 20 questions before answering anything.
```

This makes the interaction slow and unnecessary.

Instead:

```text
Ask only the questions that are necessary
to complete the task accurately.
```

This is much better.

---

# 21. Good Clarification Rule

A useful instruction is:

```text
If critical information is missing, ask for it.
If the missing information is not critical,
make a reasonable assumption and clearly state it.
```

This gives the AI flexibility while preventing dangerous guesses.

---

# 22. Assumption + Disclosure

Sometimes you want the AI to proceed even when information is missing.

In that case, tell it to clearly state assumptions.

Example:

```text
If some non-critical information is missing,
make a reasonable assumption.

Clearly list all assumptions before providing
the final answer.
```

Example response:

```text
Assumptions:

1. The application uses React.
2. The API uses REST.
3. MongoDB is the database.
```

Now you know what the AI assumed.

---

# 23. Three Ways to Handle Missing Information

There are three common strategies.

### Strategy 1 - Ask

Use when the missing information is important.

```text
Ask me before proceeding.
```

### Strategy 2 - Assume

Use when the missing information is not important.

```text
Make a reasonable assumption.
```

### Strategy 3 - Assume + Explain

Use when you want the AI to continue but remain transparent.

```text
Make reasonable assumptions and list them clearly.
```

---

# 24. Strategy Comparison

| Situation                    | Best Approach         |
| ---------------------------- | --------------------- |
| Critical information missing | Ask                   |
| Minor information missing    | Reasonable assumption |
| Need answer immediately      | Assume + disclose     |
| Safety-sensitive information | Ask / verify          |
| Coding architecture decision | Usually ask           |
| Simple formatting decision   | Usually assume        |
| Resume facts                 | Never invent          |
| Project features             | Never invent          |

---

# 25. Example - SQL Query

User:

```text
Write a SQL query to get employee salary.
```

Missing information:

* Table name
* Salary column
* Employee identifier
* Database type

A good AI should ask:

```text
What is the table name?

What is the salary column name?

Which employee should be selected?

Which SQL database are you using?
```

---

# 26. Example - React Bug

User:

```text
My button isn't working. Fix it.
```

Possible questions:

```text
1. What should happen when the button is clicked?
2. What currently happens?
3. Is there a browser console error?
4. Can you provide the button code?
5. Is the click handler attached?
```

This is much more useful than randomly changing the code.

---

# 27. Example - Database Problem

User:

```text
My database is slow.
```

Possible clarification questions:

```text
1. Which database are you using?
2. Which query is slow?
3. How many records are involved?
4. Do you have indexes?
5. How long does the query currently take?
6. What response time do you expect?
```

Now the problem becomes measurable.

---

# 28. Clarification Questions Should Be Specific

Bad:

```text
Can you provide more information?
```

This is too vague.

Better:

```text
Please provide:

1. Your database type.
2. The slow query.
3. Approximate number of records.
4. Existing indexes.
5. Current query execution time.
```

Specific questions make the conversation faster.

---

# 29. One Question vs Multiple Questions

Sometimes one missing piece is enough.

Example:

```text
Should I write this solution in Python or JavaScript?
```

There is no need to ask ten more questions immediately.

But sometimes several pieces are missing.

Example:

```text
Build a complete authentication system.
```

Then a group of questions may be appropriate.

The goal is:

> **Ask enough questions to remove important uncertainty, but not so many that the conversation becomes unnecessary.**

---

# 30. Clarification Gate

A useful technique is to create a "clarification gate."

Example:

```text
Before starting the task:

1. Check whether all critical information is available.
2. If something important is missing, ask me.
3. Do not continue until I provide it.
4. Once enough information is available, proceed.
```

This creates a controlled workflow.

---

# 31. Example - Building an Application

```text
I want to build an employee management system.

Before writing any code:

1. Identify the required information.
2. Ask me about the technology stack.
3. Ask me about required features.
4. Ask me about user roles.
5. Ask me about the database.
6. Ask me about authentication.
7. Ask only questions that affect the architecture.

Do not write code until the requirements are clear.
```

This is much better than immediately generating hundreds of lines of code.

---

# 32. Requirements Discovery

In real software development, developers often don't start coding immediately.

They first understand:

```text
Requirements
     ↓
Users
     ↓
Features
     ↓
Architecture
     ↓
Implementation
```

Prompt Engineering can follow the same process.

```text
Prompt
  ↓
Identify missing information
  ↓
Ask questions
  ↓
Clarify requirements
  ↓
Generate solution
```

---

# 33. Avoiding Hallucinated Details

A hallucinated detail is information generated by AI that was not supported by the provided information.

For example:

User:

```text
My application has three user roles.
```

AI:

```text
The roles are Admin, Manager and Employee.
```

Unless the user provided those names, the AI should not assume them.

Better:

```text
You mentioned three user roles but did not provide
their names.

Please provide the role names before I create
the authorization logic.
```

---

# 34. Example - API Documentation

Suppose you provide:

```text
GET /users
POST /users
```

The AI should not automatically invent:

```text
GET /users/:id
DELETE /users/:id
PUT /users/:id
```

unless those endpoints actually exist.

Use:

```text
Document only the API endpoints I provide.

Do not invent additional endpoints.

If information about an endpoint is missing,
mark it as missing or ask me for clarification.
```

---

# 35. Example - Academic Work

Suppose you ask:

```text
Write my assignment based on my research.
```

If the research is missing, the AI should not invent research results.

Better:

```text
Use only the research information I provide.

Do not invent:
- Statistics
- Results
- Citations
- Experiments
- Conclusions

If information is missing, tell me what is required.
```

---

# 36. Example - Data Analysis

User:

```text
Analyze this dataset and tell me why sales decreased.
```

A good prompt can say:

```text
Analyze the dataset I provide.

Requirements:

- Identify possible factors affecting sales.
- Support conclusions with the available data.

Constraints:

- Do not claim causation without evidence.
- Do not invent missing data.
- Clearly separate facts from hypotheses.
- If the data is insufficient, explain what additional
  information is needed.
```

This is a powerful technique.

---

# 37. Fact vs Hypothesis

This distinction is important.

### Fact

Supported directly by the information.

```text
Sales decreased by 15%.
```

### Hypothesis

Possible explanation that needs further evidence.

```text
A decrease in marketing activity may have contributed
to the decline.
```

A good prompt can ask AI to separate them.

```text
Separate your response into:

Facts
Possible explanations
Missing information
```

---

# 38. Example - Debugging

A strong debugging prompt:

```text
You are a senior software engineer.

I will provide:
- Error message
- Code
- Expected behavior
- Actual behavior

First determine whether enough information is
available.

If critical information is missing, ask me for it.

Do not guess the cause.

Once enough information is available:

1. Identify the likely cause.
2. Explain the reasoning.
3. Suggest the smallest fix.
4. Explain how to test it.
```

This creates a much more reliable debugging workflow.

---

# 39. Example - Learning

Suppose you are learning Python.

Instead of:

```text
Teach me Python.
```

Use:

```text
You are my Python mentor.

First ask me about:

- My current Python level
- My programming experience
- My learning goal
- How much time I can study each day

Do not assume my skill level.

After understanding my background,
create a learning plan.
```

The AI can personalize the plan properly.

---

# 40. Clarification + Day 1

Day 1 taught us:

> Be specific.

Day 6 adds:

> If something important is not specific enough, ask for clarification.

Example:

```text
Be specific about the task.

If my request is still ambiguous,
ask me a clarification question instead
of guessing.
```

---

# 41. Clarification + Day 2

Day 2 taught us:

> Give context.

Day 6:

```text
I will provide the context.

If the context is insufficient to complete
the task accurately, ask me for the missing
information.
```

---

# 42. Clarification + Day 3

Day 3 taught us:

> Give examples.

Now we can say:

```text
If the examples I provide are inconsistent
or unclear, ask me which behavior I want.
```

---

# 43. Clarification + Day 4

Day 4 taught us:

> Break complex tasks into steps.

Now:

```text
Before beginning the steps, verify that all
critical requirements are available.

If something important is missing,
ask me before starting.
```

---

# 44. Clarification + Day 5

Day 5 taught us:

> Define constraints.

Now we can combine both:

```text
Constraints:

- Use React.
- Use Bootstrap.
- Do not add dependencies.
- Do not modify the backend.

If any requirement is unclear,
ask me before implementing the solution.

Do not make assumptions.
```

---

# 45. Complete Prompt Using Day 1-6

Here is a strong prompt using everything we have learned.

```text
Role:
You are a senior React developer and mentor.

Context:
I am working on an existing React application.
I am a beginner and want to understand the fix.

Task:
Help me debug a filtering problem.

Requirements:

- Preserve the existing UI.
- Preserve existing filter behavior.
- Fix only the reported problem.
- Explain the solution clearly.

Steps:

1. Understand the problem.
2. Review the provided code.
3. Identify the likely cause.
4. Explain the cause.
5. Suggest the smallest fix.
6. Explain how to test it.

Example:

Current behavior:
The selected filter appears in the UI but is not
included in the API request.

Expected behavior:
The selected filter should be included in the
API request.

Constraints:

- Do not rewrite the entire component.
- Do not modify unrelated filters.
- Do not change the backend.
- Do not add dependencies.
- Do not change the UI.

Clarification rule:

- Do not assume missing information.
- If critical information is missing, ask me first.
- Ask only questions necessary to understand the problem.
- Do not write the final fix until enough information
  is available.

Output:

1. Problem
2. Missing information, if any
3. Cause
4. Required code change
5. Explanation
6. Testing steps
```

Notice how powerful this prompt is.

It doesn't just tell AI:

```text
Fix my bug.
```

It tells AI:

```text
What to do
+
What information it has
+
What information is missing
+
When to ask
+
What not to assume
+
What not to change
+
How to present the result
```

---

# 46. Common Mistakes

## Mistake 1 - Saying "Don't Assume" but Not Saying What to Do

Weak:

```text
Don't assume anything.
```

Better:

```text
Do not assume missing information.

If critical information is missing,
ask me for it before proceeding.
```

---

## Mistake 2 - Asking Too Many Questions

Avoid:

```text
Ask me everything before doing anything.
```

Better:

```text
Ask only questions that are necessary
to complete the task accurately.
```

---

## Mistake 3 - Asking Vague Questions

Weak:

```text
Please give more information.
```

Better:

```text
Please provide:

1. The framework you are using.
2. The database type.
3. The exact error message.
```

---

## Mistake 4 - Allowing AI to Invent Facts

Avoid:

```text
Complete the missing project details.
```

If accuracy matters, use:

```text
Do not invent missing project details.
Ask me for them instead.
```

---

## Mistake 5 - Treating Every Missing Detail as Critical

Not every missing detail requires a question.

For example:

```text
Should the heading have 16px or 18px font?
```

If the user has not specified it, a reasonable default may be fine.

---

# 47. Practical Exercise 1

Improve this prompt:

```text
Create a website for my business.
```

Your improved prompt should tell AI:

```text
- What information to ask for
- What not to assume
- When to start designing
```

---

# 48. Practical Exercise 2

Improve:

```text
Fix my Node.js API.
```

Create a prompt that tells AI to ask for:

```text
- Error message
- Expected behavior
- Actual behavior
- Relevant code
- API endpoint
```

---

# 49. Practical Exercise 3

Create a prompt for:

> "My React page is slow."

Tell AI:

```text
- What information to request
- What metrics to check
- What it should not assume
- When it should provide recommendations
```

---

# 50. Practical Exercise 4

Create a prompt for:

> "Create my resume."

Tell AI:

```text
- What information it should request
- What information it must not invent
- What it can assume
- What it should do when information is missing
```

---

# 51. Day 6 Challenge 🔥

Create a prompt for this situation:

> You have a bug in an existing MERN application, but you have not yet provided enough information to AI.

Your prompt should tell AI:

```text
1. Identify missing critical information.
2. Ask clarification questions.
3. Do not guess the technology or architecture.
4. Do not invent project behavior.
5. Wait until enough information is available.
6. Then analyze the problem.
7. Suggest the smallest possible fix.
```

Try to make your prompt specific enough that AI behaves like a careful developer rather than immediately generating code.

---

# 52. Bonus Challenge 🔥🔥

Create a prompt that allows reasonable assumptions.

Example requirement:

```text
If information is not critical,
make a reasonable assumption.

However, clearly list all assumptions
before providing the solution.

If an assumption could significantly
change the solution, ask me first.
```

This is a more advanced version of today's technique.

---

# 53. Quick Revision

### What is an assumption?

A guess made when information is missing.

### What is clarification?

Asking for missing information before proceeding.

### When should AI ask?

When critical information is missing or the request is ambiguous.

### Should AI ask about everything?

No.

It should ask only about information that materially affects the result.

### Can AI make assumptions?

Yes, when appropriate and when the missing information is not critical.

### What should AI do with important assumptions?

Clearly disclose them.

---

# 54. Key Terms

| Term                  | Meaning                                       |
| --------------------- | --------------------------------------------- |
| Assumption            | A guess about missing information             |
| Clarification         | Asking for additional information             |
| Ambiguity             | A statement with multiple possible meanings   |
| Critical Information  | Information necessary for an accurate result  |
| Optional Information  | Information that is helpful but not essential |
| Hallucination         | Unsupported or invented information           |
| Disclosure            | Clearly stating assumptions                   |
| Clarification Gate    | Checking requirements before starting         |
| Requirement Discovery | Finding out what the task actually needs      |
| Scope                 | The boundaries of the task                    |

---

# 55. Day 6 Checklist

* [ ] Understand assumptions
* [x] Understand clarification
* [ ] Understand ambiguity
* [ ] Learn when AI should ask questions
* [ ] Learn when AI can make assumptions
* [ ] Learn how to prevent invented information
* [ ] Learn how to disclose assumptions
* [ ] Practice clarification prompts
* [ ] Practice debugging prompts
* [ ] Practice coding prompts
* [ ] Practice resume prompts
* [ ] Practice project documentation prompts
* [ ] Complete the Day 6 challenge
* [ ] Save my experiments in GitHub

---

