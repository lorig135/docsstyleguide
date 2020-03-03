# Overview

Think of minimal writing like a recipe in a cookbook. Recipes include precisely enough information about how to make something (like a cake), as well as the steps you need to follow to do so. The goal is to make  complex information simple to understand and easy to follow, so our users can complete their work-related tasks quickly and effectively. 

When writing minimally, you provide only/exactly as much information as the user needs to either understand a concept or a reference, or to accomplish a task. Note that the amount and complexity of information to include may vary, but it needs to be as specific and succinct as possible.  

Note that the following recommendations will be piloted with FR-hosted docs (FRaaS). Although  preliminary and likely to change, here are some early attempts by the FRaaS team at implementing minimal writing: https://developer.forgerock.com/docs/identity-cloud. 

It will take some time to implement and refine our writing style during the pilot phase. Once we have a good idea of what that will look like, we can begin work on a minimal writing style for self-hosted docs (not based in the cloud). 

A minimal writing style for self-hosted docs might look different than that of the FR-hosted docs, given the differences in audiences (noobs vs. SMEs), the look and feel of the UI, the differences in content, as well as how it is consumed. 

For example, what does specific and succinct writing look like for subjects like security considerations, for which we have many paragraphs or pages, and an audience that wants to deep-dive into the subject matter? These are some of the reasons we it will take time to create and implement this new style. 

## Minimal Writing Structure: Concepts, Tasks, and References 

Minimal writing is topic-based, and includes three types of topics: concepts, tasks, and references. When we write about any of these topics, they should be written as independent chunks of information that can stand alone (meaning little or no context is needed), and can also (eventually) be repurposed, and/or connected with other, independent and reusable chunks of information.

Following are guidelines for structuring a concept, task, and reference, and examples of what that might look like. Note that 


### Concepts
Concepts explain what something is, what it means, or how it is used. We currently use them in our product docs at the beginning of chapters, where we introduce, define, and elaborate on an element of our products, such as a feature. Some examples of concepts are what a throttling filter is and the different ways to configure it, or how Identity Governance and Administration manages and reduces user risk. 

#### Minimal Writing Structure
Topic title: H1 or H2, in gerund, preposition, or present tense. For example, Understanding Access Management, Access Management. 

Topic paragraph: Two to three sentences (or whatever amount is enough information for the user to understand) about the topic. 

#### Example of a Concept
Access Management

Access management is the process of controlling access to resources through authentication and authorization. Authentication confirms a user's identity and credentials. Authorization determines whether a user has sufficient privileges to access a resource. Learn more here.

### Tasks
Tasks show how to use a feature or an element of our products to accomplish a task or a goal. We usually do this with a numbered or bulleted list. Some examples of tasks are authenticating from a browser, or installing the CDM on a small cluster. 


#### Structure
Task title: H1 or H2, in gerund, preposition, or present tense. 
Examples: Setting Up/Set Up Your Environment, About the Environment

Task paragraph (optional): Two to three sentences about the topic. Each sentence should complete a step or a task. Use shortcuts like greater than arrows for menu selections (Click Applications > New Application).   

Task steps: Step-by-step instructions for accomplishing a task or a goal.

#### Example of a Task
Setting Up Your Environment

Add a tenant, application, and authentication service:
1. Access your tenant URL: https://my company.forgerock.com and sign in. 
1. Click New Application. The New Applications page displays.  
1. Click an app type in the New Applications page. ForgeRock loads the recommended default settings for your app.
1. Add an authentication service to your app by clicking User Hosted Pages or Use the ForgeRock SDK. 
1. Click Save. Your environment is now set up. 

### References
References are used to research and find detailed information, which is often formatted as tables or in an appendix. Some examples of references are timers, and their rates of execution times for queries and CRUD operations, or severe and fatal error messages for servers and their tools. 

#### Structure
Topic title: H1 or H2, the name of the subject. 
Examples: Supported Standards, authrate utility

Paragraph: One to three sentences about the topic. 

#### Example of a Reference
authrate utility

Used to measure bind throughput and response time of a directory service using user-defined bind or search-then-bind operations. Example: 

authrate -p 1389 -D 'uid=user.{},ou=people,dc=example,dc=com' \
-w password -f -c 10 -g 'rand(0,2000)'

# Moving Toward a Minimal Writing Style
Here are some steps you can take to move your writing toward a minimalist style. 

In headings: 
Use 

In sentences: Use active voice wherever possible. Active voice drives succinct writing and is easier to translate. Examples:
- Passive voice: The startup.sh script enables you to specify the following elements of a running instance.
- Active voice: The startup.sh script lets you specify the following elements of a running instance.
- Note that sometimes passive voice is unavoidable. 

Use ger

Notice that we do not use infinitives in headings. The reason for this is the language of search queries. When users use search engines within ForgeRock or outside of it, their search terms are often worded as questions; such as, "How do I upgrade from AM 6.0 to 6.5?" or verb statements, such as, "Upgrade AM", or "Upgrading AM". We hope that using this language will also improve our findability. Also note that titles and the paragraphs of each topic type can include a tooltip, a collapse, or a link for users who want more
 
Use fewer words, as they reduce cognitive load and the wall of text:
- Ex.: After installation steps are complete, it is recommended that the installer ZIP and the created installation folders and files be removed from the server.
- Rewrite: After installation is finished, remove the installer ZIP and the installation files from the server. 
      
Break down complicated complicated sentences. 
- Example: The setup screen is displayed.
- Rewrite: The setup screen displays.

Check each preposition. Can the sentence be written without them? See https://www.dailywritingtips.com/5-ways-to-reduce-use-of-prepositions/ for tips.

Eliminate unnecessary words:
- Example: If calling the default browser for front-channel communications is not acceptable, enabling persistent cookies for session management could be an option in the authorization server configuration. 
- Rewrite 1: If calling the default browser for front-channel communications is not an option, try enabling persistent cookies for session management.

When writing steps, ensure each sentence helps the user complete a task. (user-focused content). See https://www.stilo.com/2017/04/30/converting-to-dita-mastering-the-task/. 
