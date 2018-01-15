<!-- .slide: data-state="title" -->
# Hosting on Github

---

## How hosting works

- Servers have needs
- Own/Rent/Services

> > Author Notes:

Although every computer on the internet can be a server, not all of them should be. A laptop would be a horrible server because any site hosted in it would go down every time you closed it. So a server needs to have:

- Constant power
- Fast connection
- Maintenance/updates

Most companies do not own their own servers because it takes a lot of very specialized knowledge to run and maintain servers. So they either rent servers to perform a variety of web functions or simply pay for specific apps or services like email, file storage, or http hosting.

---

# Git/Github

- Social Coding
- SCM/VCS
- Distributed
- Flat file hosting

> > Author Notes:

Github is a website created to help developers use and work with others to manage code. It's based on a techology called Git, so it provides a number of features that visualize the way that Git works and makes it easier to manage online

Git is a software configuration management or SCM piece of software which means that it is designed to help you manage how your software works. There are many kinds of SCM software and Git is known as a VCS or Version Control System.

One of the things that makes git unique is that it is a distributed system, which means that the code can be stored on different machines.

Git allows multiple people to work on different parts or versions of the software simultaneously. So instead of an assembly line model where each person works on a car right after someone else is done, git will allow someone to paint the car, while someone else installs the engine and someone else puts in the seats. 

Three things that wouldn't normally be able to be accomplished at the same time. In this way, Git is like being able to crete alternate universes, where different people can work on copies of the same code without stepping on each others' toes. Once each person is done, they can submit their version of what they have done to a site like Github, which would manage the project.

One of the features that Github provides is the ability to host simple flat-file sites to the web for free. Flat-file sites mean sites that don't constantly need to make requests to a server for data. It's more than what we'll need for this class.


---

# Git/Github Language
- Repository
- Branches/Forks
- Commit
- Pull Request/Merge
- Issues

> > Author Notes:

In this class, we're going to be working exclusively with Github. Git is an avanced topic outside of the scope of this class, but since Github is based on git, let's talk about the language you use when working with Git and Github.

A Repository or repo is the place where your code is hosted. It's the grand central station for you code. Github is designed to allow multiple people to have access to the code and a central location for all of that code makes sense. A github repo has it's own URL that has your username and the name of the repo. Github uses this URL as the basis for many features.

Github allows you to create and manage branches and most of the work on repos is done in one of these. Think of each branch as an alternate universe where different people work on versions of code. Each of these branches is known as a `fork`; dont think of it as a kitchen fork, but more of like a fork in a tree.. So you could have one branch for people working on painting the car, while another branch for people installing the engine. Every project gets on branch which is called the `master` branch. It's where the current official version of the project is.

Within each of these branches we can store sub-versions of the work into something called commits. Commits are markers that define different states or our code. So, for example, if we had a branch called `painting` we could create a commit for when we finished painting the hood of the car. Once we finished painting the drivers side, we could have another commit called 'driverside', etc.

Using git and github we can navigate back and forth through these commits, so that we could go back and take a look at how the care looked before it was painted and after each of the different parts of the car were painted by moving through the commits. In code this also means that we can see the difference between commmits. So you can think of commits like having access to a time machine that lets you move back and forth through the history of the project.

Once someone is finishes working with a branch, it's time to merge the project back to the master branch. We do this through a mechanism called a `pull request`. A pull request is a way to request that the master branch be updated with the latest version of the code that has been worked on in other branches. So it's like you telling the boss you've finished with your painting and to add your painting code to the car.

This step is important because it's possible for two people to be working on the same part of the code. Think of someone installing the glass in one of the windows while someone else is painting the door. They both made changes to the door and will both need to merge their changes with the main project.

Another important concept in Github is the ability for people to file issues. Issues are notes that people can write to call attention to something or to work with tasks related to organizing a project. So, if someone notices a typo on a website, you can create an issue that let's the owner know where to fix it.

Better yet, you can fork the project, fix the typo and then issue a pull request with the changes yourself. This is what makes Github really useful. Lot's of people can work on the same project and contribute easily and effectively.

---

# Github Repos

- Public/private
- `README.md` file
- Hosting strategy

> > Author Notes:

Github offers unlimited free hosting for public projects. You can also host private projects in some of the paid plans. A lot of the web's most important projects are hosted on Github.

One of the most important files in any projects is the README.md file. This is a file with information about the project. Sort of the homepage for your project on Github. It's written in a format called [markdown](https://guides.github.com/features/mastering-markdown/). It's a pretty simple format to [learn](https://www.lynda.com/Web-Development-tutorials/Up-Running-Markdown/438888-2.html). It's just simple text with some minor special characters that add formatting.

Github's process for setting up hosting is called Github Pages. It will direct a special URL generated by Github or even your own URL(additional setup required) to show whatever is on your repository.

You can set up your URL to point to whatever is on your `master` branch, a `docs` folder insider your master branch, a specially named `gh-pages` branch. The link for your project will be `username.github.io` by default, although it's configurable to also be it's own URL.