# Day 5 - Define Constraints and Requirements

## Prompt Engineering Learning Series

**Previous Topics:**

* Day 1 - Be Specific
* Day 2 - Give Context
* Day 3 - Give Examples / Few-Shot Prompting
* Day 4 - Break Complex Tasks into Steps

**Today's Topic:** Define Constraints and Requirements

---

# 1. Introduction

In the previous four days, we learned how to create better prompts:

### Day 1 - Be Specific

Tell the AI exactly what you want.

### Day 2 - Give Context

Give the AI the information it needs.

### Day 3 - Give Examples

Show the AI examples of the expected behavior.

### Day 4 - Break Complex Tasks into Steps

Divide a large task into smaller, manageable steps.

Today we will learn another important Prompt Engineering technique:

> **Define Constraints and Requirements.**

This means telling the AI:

* What it must do
* What it must not do
* What limitations it has
* What rules it must follow
* What technologies it should use
* What technologies it should not use
* How long the response should be
* What format the output should have
* What assumptions it should avoid

---

# 2. What is a Constraint?

A constraint is a rule or limitation that tells the AI what boundaries it must follow.

For example:

```text
Use Python only.
```

This is a constraint.

Another example:

```text
Do not use external libraries.
```

This is also a constraint.

Another:

```text
Keep the explanation suitable for a beginner.
```

Again, this defines a boundary.

---

# 3. Simple Definition

A simple way to remember:

> **Instruction = What the AI should do.**

> **Constraint = What the AI must follow while doing it.**

Example:

```text
Instruction:
Create a Python program that calculates the average.

Constraint:
Use only basic Python.
Do not use NumPy or Pandas.
```

The instruction tells the AI the goal.

The constraints tell the AI the rules.

---

# 4. Real-World Analogy

Imagine your teacher gives you an assignment.

The teacher says:

> Create a presentation about Artificial Intelligence.

This is the main task.

Then the teacher gives rules:

```text
- Maximum 10 slides
- Use simple English
- Include 3 real-world examples
- Do not copy from Wikipedia
- Submit as PDF
- Presentation should take 5 minutes
```

These are constraints and requirements.

Without these rules, you could create a 50-slide presentation.

The same idea applies to AI prompts.

---

# 5. Why Are Constraints Important?

AI models can have many possible ways to complete a task.

For example:

```text
Create a login page.
```

The AI may choose:

* React
* HTML/CSS
* Bootstrap
* Tailwind
* Material UI
* JavaScript
* TypeScript

But maybe you specifically want:

```text
React + Bootstrap
```

So we need to tell the AI.

Example:

```text
Create a login page using React and Bootstrap.

Constraints:

- Use React.
- Use Bootstrap.
- Do not use Tailwind.
- Do not use Material UI.
- Keep the design responsive.
```

Now the AI has clear boundaries.

---

# 6. Instruction vs Constraint

Let's understand the difference.

### Instruction

```text
Create a REST API for user registration.
```

### Constraints

```text
Use Node.js and Express.

Use MongoDB.

Use JWT authentication.

Do not use Firebase.

Do not use SQL.

Keep the API structure modular.
```

Combined:

```text
Create a REST API for user registration.

Constraints:
- Use Node.js.
- Use Express.
- Use MongoDB.
- Use JWT.
- Do not use Firebase.
- Do not use SQL.
- Keep the structure modular.
```

---

# 7. Types of Constraints

There are many types of constraints.

Common types include:

1. Technology constraints
2. Output constraints
3. Length constraints
4. Formatting constraints
5. Style constraints
6. Scope constraints
7. Content constraints
8. Time constraints
9. Audience constraints
10. Resource constraints
11. Negative constraints
12. Quality requirements

Let's understand each one.

---

# 8. Technology Constraints

Technology constraints specify which technologies should be used.

Example:

```text
Build the backend using:

- Node.js
- Express
- MongoDB
```

You can also specify what should NOT be used.

```text
Do not use:

- Firebase
- MySQL
- Django
```

---

# 9. Example - React

### Without Constraints

```text
Create a React dashboard.
```

The AI may use any UI library.

### With Constraints

```text
Create a React dashboard.

Requirements:

- Use React.
- Use Bootstrap.
- Use functional components.
- Use React Hooks.
- Use CSS modules for custom styling.

Constraints:

- Do not use Tailwind.
- Do not use Material UI.
- Do not use class components.
```

Now the implementation choices are much more controlled.

---

# 10. Output Length Constraints

You can control how long the response should be.

Example:

```text
Explain JavaScript closures.

Constraints:

- Use simple English.
- Maximum 300 words.
- Include one example.
```

The AI knows that the answer should remain short.

Another example:

```text
Explain REST APIs.

Requirements:

- Maximum 5 bullet points.
- Each bullet should contain one sentence.
- Include one example.
```

---

# 11. Format Constraints

You can specify the exact format.

Example:

```text
Explain the following topic.

Output format:

Definition:
Example:
Advantages:
Disadvantages:
Use Cases:
```

Now the response should follow that structure.

---

# 12. Example - JSON Format

Suppose you need structured data.

Instead of:

```text
Give me information about this employee.
```

Use:

```text
Return the employee information in JSON format.

Use exactly these fields:

{
  "name": "",
  "age": 0,
  "department": "",
  "role": ""
}

Do not include any additional fields.
```

The last sentence is an important constraint.

---

# 13. Length + Format Together

You can combine multiple constraints.

Example:

```text
Explain MongoDB.

Constraints:

- Use simple English.
- Maximum 200 words.
- Use headings.
- Include one real-world example.
- Include one code example.
- Do not use advanced database terminology unless you explain it.
```

This is much more controlled than:

```text
Explain MongoDB.
```

---

# 14. Style Constraints

You can specify the style of the answer.

Example:

```text
Explain Python decorators.

Constraints:

- Beginner-friendly.
- Conversational tone.
- Use simple examples.
- Avoid unnecessary technical terminology.
- Explain each code example.
```

The AI now knows how the explanation should feel.

---

# 15. Audience Constraints

The same topic can be explained differently to different audiences.

For example:

```text
Explain Artificial Intelligence.
```

This doesn't tell the AI who the explanation is for.

Instead:

```text
Explain Artificial Intelligence to a student
who has never studied computer science.

Constraints:

- Use simple English.
- Avoid mathematical formulas.
- Use real-world examples.
- Explain technical terms.
```

Now the AI knows the audience.

---

# 16. Beginner vs Expert

Compare these prompts.

### Beginner

```text
Explain APIs to a complete beginner.

Constraints:

- Use simple language.
- Use a real-world analogy.
- Avoid advanced terminology.
- Give one simple example.
```

### Experienced Developer

```text
Explain API design for an experienced backend developer.

Constraints:

- Focus on architecture.
- Discuss authentication.
- Discuss versioning.
- Discuss error handling.
- Discuss scalability.
```

Same topic.

Different constraints.

Different output.

---

# 17. Scope Constraints

Scope constraints tell the AI what to include and what to exclude.

Example:

```text
Review my React component.

Focus only on:

- Performance
- Readability
- State management

Do not review:

- CSS
- Project structure
- Backend
- Database
```

This prevents the AI from going outside the requested scope.

---

# 18. Example - Code Review

### Bad Prompt

```text
Review my code.
```

This is very broad.

### Better Prompt

```text
Review this React component.

Focus only on:

1. Bugs
2. Performance
3. React best practices

Constraints:

- Do not rewrite the entire component.
- Do not change the UI.
- Do not change the API.
- Suggest the smallest possible changes.
- Explain each suggested change.
```

This gives the AI a clear boundary.

---

# 19. Negative Constraints

A negative constraint tells the AI what NOT to do.

Examples:

```text
Do not change the existing API.
```

```text
Do not rewrite the entire code.
```

```text
Do not use external libraries.
```

```text
Do not add unnecessary features.
```

```text
Do not change the database schema.
```

Negative constraints are very useful when working with existing projects.

---

# 20. Example - Existing Code

Suppose you have an existing application.

You want to fix one bug.

### Bad Prompt

```text
Fix this code.
```

The AI may rewrite large parts of the application.

### Better Prompt

```text
Fix the bug in this React component.

Requirements:

- Fix only the reported bug.
- Keep the existing component structure.
- Keep the existing API.
- Keep the existing CSS.
- Do not introduce new dependencies.
- Do not rewrite unrelated code.
- Explain exactly what was changed.
```

This is much safer.

---

# 21. Resource Constraints

Sometimes you have limited resources.

For example:

```text
Create a solution using only:

- Python standard library
- No external packages
```

Or:

```text
Design the application assuming:

- Small development team
- Limited budget
- One database server
```

These constraints affect the solution.

---

# 22. Example - Coding Without Libraries

### Prompt

```text
Create a Python program to remove duplicate
items from a list.

Constraints:

- Use only Python's standard features.
- Do not use external libraries.
- Keep the solution beginner-friendly.
- Explain the time complexity.
```

The AI should not suggest Pandas, NumPy, or another external library.

---

# 23. Time Constraints

You can specify a time limitation.

Example:

```text
Create a JavaScript interview preparation plan.

Constraint:

I have only 7 days.

Each day should require no more than 2 hours.
```

Now the AI needs to design the plan within that limitation.

---

# 24. Word Count Constraints

You can specify exact or approximate length.

Examples:

```text
Write a 100-word introduction.
```

```text
Write between 150 and 200 words.
```

```text
Summarize this article in 5 bullet points.
```

```text
Give me a 30-second interview answer.
```

These are all output constraints.

---

# 25. Example - Interview Answer

Suppose you are preparing for an interview.

### Basic Prompt

```text
Explain React.
```

### Better Prompt

```text
Explain React as an interview answer.

Constraints:

- Suitable for a fresher.
- Maximum 45 seconds when spoken.
- Use simple English.
- Start with a definition.
- Mention 2 important features.
- Give one practical example.
- Do not go into advanced React topics.
```

This produces a much more useful answer.

---

# 26. Content Constraints

You can specify exactly what content must be included.

Example:

```text
Explain REST API.

Must include:

- Definition
- HTTP methods
- Status codes
- One example
- Advantages
```

You can also specify content that should not be included.

```text
Do not discuss GraphQL.
```

---

# 27. Quality Constraints

You can define what "good" means.

Example:

```text
Write a professional email.

Requirements:

- Clear
- Polite
- Professional
- Concise
- Grammatically correct
```

These are quality requirements.

---

# 28. Example - Resume Project Description

Suppose you want a project description.

### Basic

```text
Write a description for my project.
```

### With Constraints

```text
Write a resume project description.

Constraints:

- Maximum 3 bullet points.
- Professional tone.
- Use action verbs.
- Mention the technologies used.
- Focus on what I built.
- Avoid generic statements.
- Do not exaggerate results.
```

Now the AI has clear requirements.

---

# 29. Constraints for Accuracy

You can tell the AI not to make assumptions.

Example:

```text
Analyze my project.

Constraints:

- Use only the information I provide.
- Do not invent features.
- Do not assume technologies that are not mentioned.
- If information is missing, clearly state that it is missing.
```

This is very useful.

---

# 30. Why "Don't Assume" Is Important

Suppose you say:

```text
Create documentation for my application.
```

If you haven't provided the application details, AI may make assumptions.

Instead:

```text
Create documentation using only the information I provide.

Do not invent:
- Features
- APIs
- Database tables
- Technologies

If information is missing, ask me for it.
```

Now the AI has a clear boundary.

---

# 31. Example - Project Documentation

```text
Create README documentation for my Node.js project.

Requirements:

- Include project description.
- Include installation steps.
- Include environment variables.
- Include how to run the project.
- Include API overview.

Constraints:

- Use only the information I provide.
- Do not invent API endpoints.
- Do not invent environment variables.
- Use Markdown.
- Keep the documentation beginner-friendly.
```

---

# 32. Constraint Hierarchy

A prompt can contain multiple types of instructions.

For example:

```text
Role
 ↓
Context
 ↓
Task
 ↓
Requirements
 ↓
Constraints
 ↓
Output Format
```

Example:

```text
Role:
You are a senior React developer.

Context:
I have an existing React application.

Task:
Fix a filtering bug.

Requirements:
- Selected filters should remain visible.
- API should receive the selected values.

Constraints:
- Do not change the API structure.
- Do not modify unrelated components.
- Do not add dependencies.

Output:
1. Explain the problem.
2. Show the required changes.
3. Explain why the changes work.
```

This is a highly controlled prompt.

---

# 33. Must vs Should

This is an important distinction.

### MUST

Use "must" when something is required.

```text
The solution must use React.
```

### SHOULD

Use "should" when something is preferred.

```text
The solution should use reusable components.
```

### MUST NOT

Use this for strict restrictions.

```text
The solution must not use jQuery.
```

This makes your requirements clearer.

---

# 34. Example

```text
Build a login page.

Requirements:

- The page must use React.
- The page must be responsive.
- The form must validate email.
- The form must validate password.

Preferences:

- The design should be modern.
- Components should be reusable.

Restrictions:

- Do not use jQuery.
- Do not use additional UI libraries.
```

Now we have three levels:

```text
Must
 ↓
Required

Should
 ↓
Preferred

Must Not
 ↓
Forbidden
```

---

# 35. Constraints vs Preferences

Not every requirement is equally important.

Example:

```text
Use React.
```

This may be mandatory.

But:

```text
Use a dark theme.
```

may simply be a preference.

You can make this clear:

```text
Mandatory:
- React
- Bootstrap

Preferred:
- Dark theme
- Rounded cards
- Modern layout

Do not:
- Use Tailwind
- Use Material UI
```

This helps the AI prioritize correctly.

---

# 36. Example - Website Design

```text
Create a dashboard UI.

Mandatory requirements:

- React
- Bootstrap
- Responsive layout
- Sidebar navigation

Preferred:

- Modern design
- Dark theme
- Rounded cards
- Clean spacing

Do not:

- Use Tailwind
- Use Material UI
- Add unnecessary animations
```

This gives the model flexibility while maintaining important boundaries.

---

# 37. Constraints + Examples

We can combine Day 3 and Day 5.

Example:

```text
Convert employee data into JSON.

Constraints:

- Use exactly these fields:
  name
  age
  role

- Do not add additional fields.

Example:

Input:
Rahul, 25, Developer

Output:
{
  "name": "Rahul",
  "age": 25,
  "role": "Developer"
}

Now convert:

Priya, 28, Designer
```

The example demonstrates the format.

The constraints ensure the format stays consistent.

---

# 38. Constraints + Task Decomposition

We can combine Day 4 and Day 5.

Example:

```text
Help me build a Node.js application.

Work in these steps:

Step 1:
Create project structure.

Step 2:
Create database models.

Step 3:
Create APIs.

Step 4:
Add authentication.

Step 5:
Create tests.

Constraints:

- Use Node.js and Express.
- Use MongoDB.
- Use JWT.
- Do not use Firebase.
- Do not add unnecessary dependencies.
- Explain each step before writing code.
- Do not modify previous steps unless necessary.
```

Now we have both:

```text
Task Decomposition
+
Constraints
```

---

# 39. Combining Day 1 to Day 5

We can now create a much stronger prompt.

```text
Role:
You are a senior Node.js developer.

Context:
I am a beginner learning backend development.
I am building an employee management system.

Task:
Help me implement user authentication.

Requirements:

- Registration
- Login
- Password hashing
- JWT authentication

Steps:

1. Explain the architecture.
2. Create the required database model.
3. Create registration API.
4. Create login API.
5. Add JWT authentication.
6. Explain how to test the APIs.

Examples:
Show one request and response example for each API.

Constraints:

- Use Node.js.
- Use Express.
- Use MongoDB.
- Use bcrypt for password hashing.
- Do not use Firebase.
- Do not use SQL.
- Keep the code beginner-friendly.
- Do not add unnecessary dependencies.

Output format:

For each step provide:

1. Explanation
2. Code
3. Example
4. Expected result
```

Let's identify what we used:

```text
Day 1 → Specific instructions
Day 2 → Context
Day 3 → Examples
Day 4 → Steps
Day 5 → Constraints
```

This is a strong Prompt Engineering foundation.

---

# 40. Bad Prompt vs Good Prompt

## Bad Prompt

```text
Create a Python web application.
```

Problems:

* Which framework?
* Which database?
* Who is the user?
* What features?
* What design?
* What API?
* What output?
* What restrictions?

The AI has to guess.

---

## Good Prompt

```text
Role:
You are a Python backend developer.

Context:
I am building a small employee management application.

Task:
Create the backend API.

Requirements:

- Employee registration
- Employee login
- Employee listing
- Employee deletion

Steps:

1. Design the folder structure.
2. Design the database.
3. Create the API routes.
4. Implement authentication.
5. Implement employee APIs.
6. Explain how to test the APIs.

Constraints:

- Use Python.
- Use FastAPI.
- Use MongoDB.
- Use JWT authentication.
- Do not use Django.
- Keep the code beginner-friendly.
- Do not add unnecessary features.

Output:

For every step:
- Explanation
- Code
- Example
```

This prompt gives the AI much less room to guess.

---

# 41. Common Mistakes

## Mistake 1 - Too Many Constraints

Do not create unnecessary restrictions.

Bad:

```text
Use exactly 17 lines.
Use exactly 3 functions.
Use exactly 2 comments.
Use exactly 5 variables.
```

If these aren't necessary, they can make the task harder.

---

## Mistake 2 - Conflicting Constraints

Example:

```text
Explain in maximum 50 words.

Include 20 detailed examples.
```

These requirements conflict.

---

## Mistake 3 - Vague Constraints

Bad:

```text
Make it good.
```

Better:

```text
Keep the explanation beginner-friendly,
concise and practical.
```

---

## Mistake 4 - Forgetting Important Restrictions

If you don't want a technology used, say so.

```text
Do not use Tailwind.
```

---

## Mistake 5 - Changing the Scope

If you want one bug fixed:

```text
Fix only the filtering bug.

Do not modify unrelated functionality.
```

---

# 42. How to Write Good Constraints

A good constraint should be:

### Clear

Bad:

```text
Keep it simple.
```

Better:

```text
Use beginner-friendly language and avoid
advanced terminology.
```

### Specific

Bad:

```text
Make the code efficient.
```

Better:

```text
Avoid unnecessary database queries and
explain the time complexity.
```

### Relevant

Only add constraints that actually matter.

### Testable

A good constraint should allow you to check whether it was followed.

Example:

```text
Maximum 500 words.
```

You can check this.

---

# 43. Constraint Checklist

Before sending a complex prompt, ask yourself:

```text
What must the AI do?

What must the AI not do?

Which technology must it use?

Which technology must it avoid?

Who is the output for?

How long should the answer be?

What format should the output have?

What information must be included?

What information should be excluded?

What assumptions should the AI avoid?
```

---

# 44. Practical Exercise 1

Improve this prompt:

```text
Create a React login page.
```

Add:

* Technology
* UI requirements
* Validation requirements
* Restrictions
* Output format

---

# 45. Practical Exercise 2

Improve:

```text
Explain Python.
```

Add constraints for:

* Beginner audience
* Length
* Examples
* Language
* Topics to include
* Topics to exclude

---

# 46. Practical Exercise 3

Improve:

```text
Fix my code.
```

Create a prompt with:

```text
Scope
 ↓
Requirements
 ↓
Restrictions
 ↓
Expected output
```

Make sure the AI does not rewrite unrelated code.

---

# 47. Practical Exercise 4

Create a prompt for:

> Build an AI Expense Tracker using MERN.

Your prompt should include:

### Technology

* React
* Node.js
* Express
* MongoDB

### Requirements

* Add expenses
* Categorize expenses
* View expenses
* Charts
* Monthly summary

### Constraints

* Do not use SQL.
* Do not use Firebase.
* Keep components reusable.
* Use REST APIs.

### Output

Ask AI to first create the project plan instead of immediately writing code.

---

# 48. Day 5 Challenge 🔥

Create a prompt for this situation:

> You have an existing React application with a filtering issue. You want AI to fix only that issue.

Your prompt should include:

```text
1. Role
2. Context
3. Exact problem
4. Requirements
5. Constraints
6. Things AI must NOT change
7. Expected output format
```

Example structure:

```text
Role:
...

Context:
...

Problem:
...

Requirements:
...

Constraints:
...

Do not:
...

Output:
...
```

The goal is to prevent the AI from making unnecessary changes.

---

# 49. Real-World Developer Example

Imagine you are working on an existing project.

You tell AI:

```text
Fix the filter issue.
```

AI might:

* Rewrite the component
* Change API calls
* Change CSS
* Change state management
* Add a library
* Change unrelated functionality

Instead:

```text
You are working on an existing React application.

Problem:
The selected Billing Status filter is not being
sent correctly to the API.

Requirements:

- Fix only the Billing Status filter.
- Keep the existing filter UI.
- Keep the existing API structure.
- Preserve other filters.

Constraints:

- Do not rewrite the component.
- Do not change unrelated filters.
- Do not add a new dependency.
- Do not modify the backend.
- Keep the existing coding style.

Output:

1. Identify the problem.
2. Explain the cause.
3. Show only the required code changes.
4. Explain why the fix works.
```

This is a much safer development prompt.

---

# 50. Important Rule

> **Don't only tell AI what to do. Tell AI the boundaries within which it should do it.**

Think:

```text
Goal
+
Requirements
+
Constraints
=
Controlled Task
```

---

# 51. Day 5 Mental Model

Remember this simple model:

```text
WHAT?
   ↓
Instruction

WHY / BACKGROUND?
   ↓
Context

SHOW ME
   ↓
Examples

HOW?
   ↓
Steps

RULES / LIMITS?
   ↓
Constraints
```

This is a very useful way to think about Prompt Engineering.

---

# 52. Day 1 to Day 5

Your Prompt Engineering foundation is now:

```text
DAY 1
Be Specific
        ↓
Tell AI exactly what you want.

DAY 2
Give Context
        ↓
Give AI the necessary background.

DAY 3
Give Examples
        ↓
Show AI what the desired result looks like.

DAY 4
Break Complex Tasks into Steps
        ↓
Divide large tasks into smaller tasks.

DAY 5
Define Constraints
        ↓
Tell AI the rules and boundaries.
```

---

# 53. Complete Prompt Formula

A useful beginner-friendly formula is:

```text
ROLE
+
CONTEXT
+
TASK
+
REQUIREMENTS
+
EXAMPLES
+
STEPS
+
CONSTRAINTS
+
OUTPUT FORMAT
```

You don't always need every part.

Use the parts that are relevant to your task.

---

# 54. Final Example

Here is a complete prompt using everything learned so far:

```text
Role:
You are a senior React developer and mentor.

Context:
I am a beginner React developer.
I have an existing React application with a
filtering component.

Task:
Help me fix a bug where the selected filter value
is not being sent correctly to the API.

Requirements:

- Preserve the existing UI.
- Preserve the existing filter behavior.
- Send the selected filter value correctly.
- Do not break other filters.

Steps:

1. Understand the existing code.
2. Identify how the filter value is stored.
3. Identify how the API parameters are created.
4. Find where the value is lost or incorrectly assigned.
5. Suggest the smallest fix.
6. Explain how to test the fix.

Example:

Current:
billingStatus = "Approved"

Expected API parameter:
status=Approved

Constraints:

- Do not rewrite the entire component.
- Do not modify unrelated filters.
- Do not change the backend.
- Do not add dependencies.
- Do not change the UI.
- Use the existing coding style.

Output format:

1. Problem
2. Cause
3. Required code change
4. Explanation
5. Testing steps
```

This prompt uses almost everything you have learned during Days 1-5.

---

# 55. What I Learned Today

After completing Day 5, I should understand:

* What a constraint is.
* What a requirement is.
* Difference between instructions and constraints.
* How to specify technologies.
* How to specify output length.
* How to specify output format.
* How to specify audience.
* How to specify style.
* How to define scope.
* How to tell AI what NOT to do.
* How to prevent unwanted assumptions.
* How to define mandatory requirements.
* How to define preferences.
* How to combine constraints with examples.
* How to combine constraints with task decomposition.
* How to create controlled prompts for software development.

---

# 56. Quick Revision

### What is a Constraint?

A rule or limitation that defines the boundaries of a task.

### Example

```text
Use Python only.
```

### Negative Constraint

```text
Do not use external libraries.
```

### Output Constraint

```text
Maximum 300 words.
```

### Format Constraint

```text
Return the answer as JSON.
```

### Scope Constraint

```text
Review only the authentication code.
```

---

# 57. Key Terms

| Term                | Meaning                                          |
| ------------------- | ------------------------------------------------ |
| Constraint          | Rule or limitation                               |
| Requirement         | Something that must be included or achieved      |
| Instruction         | Tells AI what to do                              |
| Restriction         | Tells AI what it cannot do                       |
| Scope               | Defines what is included in the task             |
| Output Format       | Defines how the result should look               |
| Audience            | Person for whom the response is intended         |
| Mandatory           | Something that must be followed                  |
| Preference          | Something that is preferred                      |
| Assumption          | Something AI guesses when information is missing |
| Negative Constraint | Rule describing what AI must not do              |

---

# 58. Day 5 Checklist

* [ ] Understand constraints
* [ ] Understand requirements
* [ ] Understand positive constraints
* [ ] Understand negative constraints
* [ ] Practice technology constraints
* [ ] Practice output constraints
* [ ] Practice length constraints
* [ ] Practice format constraints
* [ ] Practice scope constraints
* [ ] Practice audience constraints
* [ ] Practice "do not" instructions
* [ ] Create a coding prompt with constraints
* [ ] Create a learning prompt with constraints
* [ ] Create a debugging prompt with constraints
* [ ] Complete the Day 5 challenge
* [ ] Save my experiments in GitHub

---

# 59. Final Takeaway

The most important lesson from Day 5 is:

> **A good prompt does not only describe the goal. It also defines the boundaries.**

Think of prompting like giving a developer a task.

Instead of saying:

```text
"Build something good."
```

say:

```text
Build X.

Use A and B.

Include C and D.

Do not use E.

Keep it under X words.

Follow this format.

Do not modify unrelated parts.
```

The more important the boundaries are, the more clearly you should communicate them.

However:

> **Do not add constraints just to make your prompt longer.**

Every constraint should have a purpose.

---

# Day 5 Summary

```text
             PROMPT
                |
       +--------+--------+
       |        |        |
      Goal    Rules    Output
       |        |        |
     What?   Limits?   Format?
       |
       ↓
   AI performs
   the task
       |
       ↓
 Controlled Result
```

**Core Technique #5: Define Constraints and Requirements**

> Tell the AI not only what you want, but also the rules,
> limitations, boundaries, requirements, and restrictions
> it must follow while completing the task.
