# Design Philosophy
## Step 1: Define the Problem
State what you are trying to accomplish/the problem you are trying to solve. Remember, we program to help the business, not because it is cool. This is necessary to make sure that you are working towards something that will actually be needed.

The problem should be high level, user story type statements.

## Step 2: Define Requirements
Brainstorm constraints that must be satisfied. Focus on functionality, reliability, speed, etc, not the "how" of implementation detail.

This is where the definition of done is established.

## Step 3: Break it Down
Use either top-down or bottom-up problem solving to break the problem down into more manageable bits.  You *don't* want to tackle too much at once. ==Remember, working software that meets some requirements is better than non-working software that *might* meet some requirements.==

### Create a Task Hierarchy
This will define the flow of the program. Once this is done, you have a rough outline of how you can attack the problem.

## Step 4: Implementation
Using the task hierarchy, begin stubbing out the program and then implement the stubs.

## Step 5: Testing
Test to ensure the logic is correct. Don't just test the happy path. 
Beat your code up for correctness and understandability. Don't spare yourself, spare your coworkers and the user.

## Tips
- Focus on one area at a time. Make it correct, then move on.
- Optimize for maintainability, not performance.
- Test as you go.
