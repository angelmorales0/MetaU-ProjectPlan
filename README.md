# MetaU-ProjectPlan
https://docs.google.com/document/d/1z3VNtQCeqah-ziPBTaUWMIGi3knVGfOFQyxfNEEABPo/edit?usp=sharing
Meta University Eng Project Plan Template     
Project Guide.
CrackedIt
What does the app do?
The app will function like a social media app with one key difference, you start with friends/connections. If a user makes an account and allows themselves to be ‘open to mentoring others’ then through some recommendation algorithm I will try to match them to a new user with similar goals as to what they are currently doing. This way students who feel ‘lost’ and don't know what to do can seek advice from someone who has already done it. This takes the hardest part of finding a mentor (actually finding someone  who is willing to help AND doing what you want to do) out of the equation and allows you to focus all your energy on professional development 
Recommendation algo could be a similarity score calculation based on the inputs we get from the user on their one time sign up.
Key Features 
DM Functionality 
User auth/ accounts 
A social wall for posts
Like + comment on these posts
Send dms 
A capability to create groups
Member directory 
Includes search functionality for specific users / organizations
Profile Editing 
Start with friends/connections through a recommendation algorithm
Technical Challenges:
Skills you have and opting in to help others master the skills.
Skills you want to learn.
If a skill you want to learn matches with someone else's mastered skill then you can auto send a friend request!
Same goes for if someone joins with a skill that you want to learn
Potential Idea (resume helper) [API integration]
Yuchen gave me the idea of having my social media apps cool feature being a ‘resume pad’ where it would basically be a version of google docs but optimized for resumes making it super easy to edit smaller things like spacing along your resume and allowing you to export it as a pdf. This is similar to how Leetcode has a built ‘coding pad’ to run your code. 
AI leveraged feedback on resume to help it pass ATS systems.


Try to get project idea mock up done on thursday 
Intern: Angel Morales
Intern Manager: Aishwarya Girish Paraspatki
Intern Director: Josh Katz
Peer(s): Mohaimin Gazi, Yuchen Ge
GitHub Repository Link: TBD
Overview
Category: Social Networking
Story: Users sign up to gain resources as to what their next steps should be in securing a role in today's software engineering market. Many students, including myself, enter college with no connections or prior experience in tech. If it weren’t for some people I've met along the way I wouldn’t be where I am today. This app aims to bridge that gap and give anyone access to information and resources allowing them to plan out their next steps in securing that first role instead of being lost.
Market: Students of any age group looking to land a role in tech
Habit: App will likely be used weekly to daily depending on how often users are wanting to message mentors and use the apps built in resources 
Scope: Professional Development
Product Spec
User Stories
Required (MVP)
User can login
User can create an account
Potentially signing up as a ‘mentor’ or ‘mentee’
Users can Access a member directory/ look up mentors
Users can edit their profiles
Upon sign up user is provided with a recommended user list  with ‘mentors’ based off their goals 
Additional Features? Need input on whether or not to implement 
Have a built-in ‘resume pad’
Allows users to edit a resume way better than gdocs and export as pdf
Potentially offers ai-assited resume advice
Timeline (WIP)
Week 1
Do user auth and allow users to log in and create accounts 
Allow users to look up mentors 
Allow users to edit their profiles
Week 2 + 3
DM Functionality 
Create auto recommendation algorithm so users start with friends 
Present algorithm idea often 
Week 4 NEED TO GET WEEK 4-5 IDEAS APPROVED 
Create a Resume pad feature ?
Week 5
Integrate automated resume advice/coach? 
Week 6 
Make it look pretty + submit
Screen Archetypes
ie. wireframes

1. Login / Signup Screen
Login with email and password


Sign up as a mentor or mentee


Include onboarding inputs for skills you have, skills you want to learn, and goals


2. Home Feed (Social Wall)
View posts from connections


Like and comment on posts


Quick access to write a post or browse groups


3. Profile Page
View/edit your profile: name, bio, goals, skills mastered, skills to learn, profile picture


See your mentor/mentee status


4. Member Directory
Search for users by name, skill, or tag (mentor/mentee)


Filter by available mentors


View user cards and send requests or DMs


5. DM / Chat
Real-time messaging with users


Search chats, create group chats


6. Recommendation Screen
Display recommended mentors based on skill and goal matching


Option to add them directly or view profile
Data Model
User data model
{
  id: Int,
  name: String,
  email: String,
  passwordHash: String,
  bio: String,
  skills_have: [String],
  skills_want: [String],
  goals: [String],
  profilePicUrl: string,
  connections: [UserId],
  posts: [PostId],
  messages: [MessageId]
}


Server Endpoints
For the users 
GET /api/users/:id – Get user profile

PUT /api/users/:id – Update user profile
body: { bio, skills_have, skills_want, goals, profilePic }

GET /api/users?search=query – Search users

GET /api/users/recommendations/:id – Get recommended users
Navigation

Project Requirements
[Based on the Project Guide, describe how your project is going to be fulfilling each of the base project requirements.]

Technical Challenges

Technical Challenge #1 -
What
What problem are you solving, and what parts go beyond what you learned in CodePath? 
How
Explain in words how you’ll solve this problem. 

You’re encouraged to expand on this section with pseudo-code, links to external frameworks, architecture / design diagrams, anything that you can use to explain this to others!
Technical Challenge #2 - 
What
How

Database Integration
[Describe what you are using for database storage. For example, Parse, MongoDB, Sequelize, etc.]

External APIs
[Describe at least one external API you’re using for your project. For example, Google Maps, Spoonacular, OpenWeather, etc.]

Authentication
[Describe how user authentication is handled for your project, including logging in and signing up. Also describe any kind of cookie / session management you’re doing and how you’re implementing it, and how this affects navigation between different screens by the same user.]

Visuals and Interactions
[Provide details on how your app is fulfilling the following UI craft requirements, and how these are technically accomplished.]

Interesting Cursor Interaction
UI Component with Custom Visual Styling
Loading State

Timeline
Project execution will start in Week 4 of MU. Based on the previously defined requirements, user stories and technical challenges, use the following table to scope out and plan a timeline for deliverables over Week 4 - 9. You can be as detailed as you need, ranging from simply mentioning the user stories, or dividing them into sub-tasks.

You are free to modify the table, add / remove rows or columns, whatever fits your style! The important thing here is that you focus and prioritize certain aspects of your project so you don’t get behind and are ready to deliver the MVP - remember your required features should be code complete before the end of Week 8, including both technical challenges!

We also encourage you to leverage project tracking tools such as GitHub Issues or Meta’s internal Tasks / GSD tooling to keep manage individual units of work.

MU Week
Project Week
Focus
User Stories
4
1
Focus on the components that will serve as the skeleton of your project. You will probably be using most of what you learned in CodePath to set up things like the client and server repositories, initial routing, login / registration, creating a database with object models, etc.
Example:
User can login
User can create an account
[Optional] User passwords are encrypted in the database for security

Week 5 and 6 should be where you focus on the specific requirements of your project.
Example:
User can create / edit / delete posts
User can chat with other users in real-time (e.g. technical challenge)
By this point, you should be getting started with your technical challenges as well.

You should focus on finishing your MVP and core requirements. By this point, you should be done with at least one of your technical challenges.

Continue work on finishing touches and stretch goals for your MVP. By this point, your core functionality and both TAPs should all be in place. It is also a good point to start working on stretch goals that could further expand on the functionality (and technical complexity) of your project.

This week you also have to submit your self-review, make sure you allocate enough time for this alongside your final submission for your project!

It’s time to show others what you have built! Work on a presentation and demo that you will present to other interns to showcase your work. You are also free to continue polishing and expanding on your project!

For this week, we have a bunch of extra activities prepared to give you a quick dive of what it is to work at Meta. You will find activities around using internal tools and frameworks, and even committing code to our internal repositories.

Create a Resume pad feature ?
Week 5
Integrate automated resume advice/coach? 
Week 6 
Make it look pretty + submit
