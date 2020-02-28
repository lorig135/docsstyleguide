# Writing Minimally

Think of minimal writing like a recipe in a cookbook. Recipes include precisely enough information about how to make something (like a cake), as well as the steps you need to follow to do so. 

When writing minimally, you provide only or exactly as much information as the user needs to either understand a concept or to accomplish a task. Note that the amount and complexity of information to include may vary, but it needs to be as specific and succinct as possible. 

Minimal writing is topic-based. There are three types of topics we will write about: concepts, tasks, and references. When we write about any of these topics, they should independent chunks of information that can stand alone (meaning little or no context is needed), and can also (eventually) be repurposed, and/or connected with other, independent and reusable chunks of information. 

Note that the following recommendations currently apply to FR-hosted docs (PaaS). It will take some time to refine our writing style during the pilot phase. Once we have a good idea of what that will look like, we can begin work on a minimal writing style for self-hosted docs (not based in the cloud). 

A minimal writing style for self-hosted docs might look different than that of the FR-hosted docs, given the differences in audiences (noobs vs. SMEs), the differences in content, as well as how it is consumed. 

For example, what does specific and succinct writing look like for deep-dive subjects like security considerations and other subjects for which we have many paragraphs or pages, and an audience that wants more information? These are some of the reasons we will implement this new style incrementally.

## The Foundation: Concepts, Tasks, and References 

Concepts explain what something is, what it means, or how it is used. We currently use them in our product docs at the beginning of chapters, where we introduce, define, and elaborate on an element of our products, such as a feature. Some examples of concepts are what a throttling filter is and the different ways to configure it, or how Identity Governance and Administration manages and reduces user risk. 

Tasks explain how to use a feature or an element of our products to accomplish a task or a goal. We usually do this with a numbered or bulleted list. Some examples of tasks are authenticating from a browser, or installing the CDM on a small cluster. 

References are used to research and find detailed information, which is often formatted as tables or in an appendix. Some examples of references are timers, and their rates of execution times for queries and CRUD operations, or severe and fatal error messages for servers and their tools. 

Following are guidelines for structuring a concept, task, and reference, and examples of what that might look like. Notice that we do not use infinitives in headings. The reason for this is the language of search queries. When users use search engines within ForgeRock or outside of it, their search terms are often worded as questions; such as, "How do I upgrade from AM 6.0 to 6.5?" or verb statements, such as, "Upgrade AM", or "Upgrading AM". We hope that using this language will also improve our findability. Also note that titles and the paragraphs of each topic type can include a tooltip, a collapse, or a link for users who want more.

### Concepts

#### Structure
Topic title: H1 or H2, in gerund, preposition, or present tense. 
Examples: Understanding Access Management, and Access Management. 

Topic paragraph: Two to three sentences about the topic. 
Example
Access Management
Access management is the process of controlling access to resources through authentication and authorization. Authentication confirms a user's identity and credentials. Authorization determines whether a user has sufficient privileges to access a resource. Learn more here.

### Tasks

#### Structure
Task title: H1 or H2, in gerund, preposition, or present tense. 
Examples: Setting Up/Set Up Your Environment, About the Environment

Task paragraph (optional): Two to three sentences about the topic. Each sentence should complete a step or a task. Use shortcuts like greater than arrows for menu selections (Click Applications > New Application).   

Task steps: Step-by-step instructions for accomplishing a task or a goal.

Example
Setting Up Your Environment
Add a tenant, application, and authentication service:
Access your tenant URL: https://my company.forgerock.com and sign in. 
Click New Application. The New Applications page displays.  
Click an app type in the New Applications page. ForgeRock loads the recommended default settings for your app.
Add an authentication service to your app by clicking User Hosted Pages or Use the ForgeRock SDK. 

### References

#### Structure
Topic title: H1 or H2, the name of the subject. 
Examples: Supported Standards, Command-Line Tools

Paragraph: One to three sentences about the topic. 
Example
authrate utility
Used to measure bind throughput and response time of a directory service using user-defined bind or search-then-bind operations. Example: 

authrate -p 1389 -D 'uid=user.{},ou=people,dc=example,dc=com' \
-w password -f -c 10 -g 'rand(0,2000)'

# General Writing Guidelines
The goal is to make the complex information simple to understand and easy to follow, so our users can complete their work-related tasks effectively:


Use active voice wherever possible. Active voice drives succinct writing and is easier to translate. Examples:
Passive voice: The setup screen is displayed.
Active voice: The setup screen displays.
Sometimes passive voice is unavoidable. Example: The screen is hidden. 

Use fewer words, as they reduce cognitive load and the wall of text:
Ex.: ForgeRock Identity Platform™ serves as the basis for our simple and comprehensive Identity and Access Management solution.
Rewrite 1: ForgeRock Identity Platform™ is the basis of our simple and comprehensive Identity and Access Management solution.
Rewrite 2: ForgeRock Identity Platform™ is the basis of our IAM solution.

Break down complicated complicated sentences.
Example: The setup screen is displayed.
Rewrite: The setup screen displays.

Check each preposition. Can the sentence be written without them? If yes, then do so.

Eliminate unnecessary words:
Example: If calling the default browser for front-channel communications is not acceptable, enabling persistent cookies for session management could be an option in the authorization server configuration. 
Rewrite 1: If calling the default browser for front-channel communications is not an option, try enabling persistent cookies for session management.
When writing steps, ensure each sentence helps the user complete a task. (user-focused content)
See also, "Converting to DITA – mastering the task". 
