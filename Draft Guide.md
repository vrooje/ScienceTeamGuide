# Zooniverse Guide for Science Teams
### Robert Simpson (_April 2013_)
_______

## Introduction

This document aims to overview the process of creating a citizen science project with the Zooniverse team. It is not meant as a contract or rigid plan - but rather a chance to explain some terms and technologies that we use.

We don't work like many groups you might come across in academic or research institutions. In the past people have commented on this (usually in a very positive way!) and it seems like a good idea to get in writing some of the main milestones of creating a Zooniverse project, so that you know what to expect and roughly how the process works.

___

## Setting Up the Process

So your proposal has been accepted: congratulations! That means we're going to build an awesome citizen science project together.

### Key contacts at the Zooniverse

The Zooniverse consists of two main groups: one in the University of Oxford (UK) and one at the Adler Planetarium (Chicago, US). The Oxford group is lead by Chris Lintott (cjl@astro.ox.ac.uk) and the Chicago team by Arfon Smith (arfon@zooniverse.org). You'll be working with some combination of people in both these teams over the coming months.

In addition to our amazing developers, whom you will meet during the process of building your project, there are some other names that will come up over the course of this document:

- David Miller - Visual design miller@zooniverse.org
- Robert Simpson - Communication, web analytics, social media rob@zooniverse.org
- David Weiner - Project management david@citizensciencealliance.org
- Laura Whyte and Kelly Border - Education specialists laura@zooniverse.org and kelly@zooniverse.org

### JISCMail lists

As with all things, communication is vitally important in building Zooniverse projects. We are distributed around the world (and we travel too) and this is also true for most science teams. To keep in touch, we use the JISCMail LISTSERV service for our projects. Everyone that needs to, will be added to the list for your project and this will be set up early on by our team.

JISCMail allows the conversation to be inclusive and creates a record of the conversation at jiscmail.ac.uk. This can be useful in months and even years to come. People can be added to and removed from these lists as needed.

### Support Email

In addition to directly contacting team members, or using the project's JISCMail list, you might also have lower-priority requests or queries that can be answered by many members of the team. For these we encourage everyone to use our support@zooniverse.org email address. We use this ourselves with in the Zooniverse. Emails will be directed to the right person and dealt with within a few days.

### Amazon Web Services

At the Zooniverse we rely on Amazon Web Services for our core infrastructure. All our servers are virtual machines _in the cloud_ - this includes our webapps (i.e. the project itself) as well as our databases and other sites. We also stored the images and other data for projects on Amazon S3, a highly redundant and scalable online storage platform. This means that test sites, sample data, and other things, will often be found at amazonaws.com URLs.

We don't need you to create any Amazon accounts, or really think about this much at all, but it's worth noting that we use this service and that is a popular, and secure way to hosts large-scale websites.

### Agreeing a timeline

Early on in the process a rough timeline will be agreed regarding when to aim to launch the site and when to start work in ernest.

### Things You Can Do Now

- Play with existing Zooniverse projects http://zooniverse.org
- Use Talk (e.g. http://talk.snapshotserengeti.org)
- Join GitHub at http://www.github.com

___

## Stages of the Project

### General timeline

There is no 'Gantt Chart' or specific time-plan for a Zooniverse project - because they are all different. However the outline below shows the approximate order of proceedings and gives you an idea of how the work is done.

| Phase | Timescale                  | Outline                  |
|-------|-----------------------|--------------------------|
| Pre-development | Days to weeks  | Shared understanding of science goals. Requirements of classification interface.             |
| Interface Development | Weeks  |  Creating a useful and useable main interface for the project  |
| Website Development | Week to months | Creating a website around the main interface, with background information, team biographies, images and pictures |
| Alpha Site | 2-6 weeks before launch | Site is circulated around team for feedback. Test data reduction may happen at this stage. |
| Beta Site | 1-3 weeks before launch | Site released to limited members of the public for a 'practice' run and feedback from real users. Test data reduction should happen at this stage if not in previous stage. Test that site works as expected and decide on revisions needed or launch date. |
| **Launch** |  | **Site is released to the public!** Press plan executed, team online during initial days of activity. |
| First data reduction | Week after launch | Data delivered to science team from initial use of site. Communicate results to volunteers where possible. |
| Steady-state | As long as it takes | Site exists in a more-or-less steady state, with data reduction ongoing and communication with volunteers. Newsletters can be sent our periodically, and traffic may come in bursts if there is press interested. |
| Retiring the project | As required | If science goals have been completed and nothing further can be gained from the site it is 'retired' and it is made clear to users that clicks are no longer useful. |
| Archiving the project | As required | If a project is done and over it is retired and no longer available on Zooniverse home. A closing blog post or press release should be issued with remarks on the science that has been achieved and the legacy of the project. |

____

## Anatomy of a Zooniverse Project - Some Useful Terms

We have developed our own vocabulary over the years. Here are some terms that will be used and what they means:

#### User/Volunteer
People using the website are our volunteers. They are referred to as 'users' in our database but we think 'volunteer' is more respectful, since they are giving up their time to participate.

#### Subject
Volunteers are shown subjects on the site. Subjects are the unit of data to be classified. In Galaxy Zoo they are images of galaxies, in Planet Hunters they are light curves.

#### Annotation
Markings, transcriptions or answers to questions are 'annotations'. In Galaxy Zoo every answer is an annotation; in Planet Hunters every transmit box drawn. Annotations are the smallest thing a volunteer can add to a subject.

#### Classification
The complete set of annotations that a volunteers adds to a subject, form a classification.

#### Interface
The main classification tool used by the public on the project.

#### Backend/Frontend
We may talk a lot about front-end and back-end systems. The front-end is the main user interface (UI) and website that people see and use in their browser. The back-end refers to the database and API that serve subjects to the project and which saves data for reduction later on.

#### Main Site, Blog, Talk

Each project has a main site, where the classification interface sits and we give some background information. This is the **www.projectname.org** URL that will be shared around when the project is complete and is the public face of the project for virtually all people.

Nearly all projects have a discussion site at **talk.projectname.org**. All the project's subjects are shown here and users are usually prompted to talk about any interesting subjects they classify. About 40% of users will visit Talk at least once.

Finally, there will also be a blog for each site at **blog.projectname.org** where science teams are encouraged to blog background information, news and results. A smaller subset will visit the blog, and you can expect more dedicated and interested users to visit here.

Both the blogs and Talk are covered in more depth later in this document.

#### Database

There is a large, central Zooniverse database that stores each project's subjects, classifications and annotations as well as all user details and Talk discussions.

#### Ouroboros

Our main API system is called Ouroboros and is the backbone of the Zooniverse. It communicates with the database, saving results and logging-in users as needed. It also delivers subjects to users and stores the rules for the delivery and grouping of subjects.

#### Website 'Content'

Sooner or later we will come to you for 'content' for the site. In development terms this means the words and images on the site. We'll need text from you and can guide you on the style and length of this content. You can see examples on all current Zooniverse projects.

We'll be looking for a bit of background on the science and why it is important, as well as short biographies for the team.

___

## Interface Design

Once the project is under development we'll send round concepts and designs for the main classification interface. The team will require examples of subjects from your data to do this and the requirements the format of this data will be specific to each project.

### Example data 

When delivering example data to the team, consider that this will be used to determine the look and feel of the project and the nature of the main classification interface. So try to send representative data. If only 1 in 20 images are 'cool' please try to send a representative set and not just your 20 best images (thought we may ask for those later). Similarly if you have data from several sources, it may be worth including examples from each. This will make sure we create the right kind of user-interface and website design.

### Agile Development

We operate in a mode where we try to build stuff, show it to you, and implement feedback quite rapidly. We appreciate that this is _not_ how science, or scientific publication, operates.

This rapid turnaround means that we are always accepting comments and ideas in the early stages. It also means that things will not be complete until near the end. To that end have a system for ticketing issues for the project developers (see below).

During development will send you emails with links to long Amazon URLs. These often temporary URLs are usually only for sharing within the science and development teams and may cease to work when the next version comes along.

### GitHub

We use a collaborative coding, versioning system called Git and a website called GitHub (http://www.github.com). Each project has its own GitHub code repository (or just 'repo') and we use the same site to log development issues for everyone involved.

GitHub issues are a very powerful and effective way for everyone to log problems or suggestions whilst the site is under development. GitHub accounts are free and we encourage you to signup and let the team know your username. You can receive alerts when issues are discussed or completed and see if other people have already ticketed your idea or problem. GitHub links nicely with email so you don't need to keep logging into the site to see how things are going.

___

## Talk

There are two ways for volunteers to reach Talk: by visiting the front page of the site or by being linked to an 'object' page after completing a transcription such as this one. There will usually be a link to 'discuss' at the end of each task. 

There are some features in Talk that may seem a little unusual at first but can (and have) been used to do some excellent science.

### Every subject in the project usually has its own discussion page

One important thing to realise about Talk is that every record that is shown in the main project interface has a dedicated page that people can comment on. This means that object-specific discussion can happen right on the object and more general community discussion can happen elsewhere.

### You can tag and collect things

Talk supports tagging and user-generated collections of objects. Tagging is achieved using the Twitter convention of #tagname (with no spaces) when writing a comment. Tags are commonly used by the community and science team to identify similar objects in the data. For example, images from Snapshot Serengeti have been tagged by the community with #human when there is a person in the shot.

Collections are groups of objects that people use to group similar objects. Once you have some collections when you are on the object discussion page there are links to 'collect this' and add to one of your collections. An example collection is this collection of giraffes I made. Note that collections, like objects can be discussed also.

### Three types of discussion

Talk has three different 'types' of discussion. The first is general community questions/answers. These are on the boards and are globally split into Science, Help and Chat.

The second is short comments on an object or collection. People typically use these to quickly tag objects.

The third is more in-depth discussion which is for longer posts and again on this page you can see someone asking in the Chat board whether there is one or two porcupines in the image (the thread is call '2 or 1'). When people start these 'faceted' discussions they also show up in the boards under the same Chat heading. You can see the same discussion here.

### Talk is dynamic

When someone comments on an object and tags it then if this tag is used by a number of people it will become a 'popular' tag and will show up on the front page. When a critical mass of people start discussing an object or participating in a discussion on a board then the object or thread shows up in the trending sections of the front page. Basically Talk is designed to show you what's happening right now.

___

## Other Zooniverse Tools

### Dashboard (http://tools.zooniverse.org)

The dashboard - or _Zoo Tools_ - is a place where people can filter and plot data from Zooniverse projects, and other selected public datasets. For example, galaxies from Galaxy Zoo can be plotted using a variety of charts and filtered according their location or redshift metadata.

Not all data from all projects is currently supported in the dashboard. It is still under development but if you've got a cool use-case, speak with Arfon.

### Letters  (http://letters.zooniverse.org)

Letters is a place for citizen scientists to 'publish' short articles. These may be summaries of research they have undertaken individually or in groups, or outlines of useful tools or techniques.

___

## Data Preparation

### Discussing subject creation and delivery

Once the size and shape (or duration, in case of video/audio) of subjects has been established then we need to start shopping up your dataset accordingly.

It may be the case that you are able to do this, and this is often preferred as it helps assure you of the completeness and quality of the final dataset. It may also be the case that the development team need to modify or compress data.

Whatever the requirements, the science and development teams will come to an agreement on what is required and how it will be delivered. It may be that the science team upload files directly or that they deliver hard drives to one of the Zooniverse offices.

### Amazon S3

All of our subjects end up on Amazon S3. This is Amazon's ultra-reliable online storage platform and allows files to stored online and served globally and without hitting any of our servers. It is fast and highly redundant - meaning that subjects load as quickly as possible and are always available online.

All subjects have a unique, public, read-only Amazon URL on S3 which allows them to be used in the classification interface. All our databases store this URL with the subject meta data.

### MongoDB, MySQL and CSV

Our older projects (those launched before September 2012) are built as Ruby-on-Rails web-apps, running on their own servers and relying on their own MySQL database to store all subject, classifications, users etc.

Our recent projects are HTML5 apps (i.e. they run in the browser and not on servers) and access our custom API application Ouroboros. Ouroboros stores all data in a large MongoDB database server, which spans all projects. MongoDB is not a relation database, but a sophisticated document store for online systems just like ours.

We can import and export subjects, users and results from Ouroboros in CSV, SQL and native MongoDB binary. However we cannot allow everyone access to the system directly - for stability and security reasons. We are able to automated regular data dumps for some regular queries.

It is usually simplest for us to deliver data in the form of CSV files.

___

## Analysis of Results

### Database Scheme and Access
### Example Data
### Results from Other Projects
___

## Beta Testing

### Collecting Beta Users
### Feedback Form
### Provisional Launch Date

- Time commitments during launch days

### Press strategy

___

## Communicating with Users

### Blogging

Most of our projects have their own blogs at blog.projecturl.org. This is a Wordpress.com blog and anyone that wants to blog should signup for a free account at www.wordpress.com.

Blogging is useful for communicating with interested volunteers and for reporting preliminary results during data reduction. 

Some highlights from our existing blog network include the blogs for Planet Hunters (http://blog.planethunters.org), Snapshot Serengeti (http://blog.snapshotserengeti.org) and Moon Zoo (http://blog.moonzoo.org). It is worth reading some entries on this sites to get an idea of what a good Zooniverse blog looks like.

These three blogs are read by between 1,000 and 10,000 people a week and good chuck of those readers (about 40%) click through to the project or Talk.

### Social Media

In addition to the blogs, our projects are also present on the main social media platforms. These accounts automatically post links to blog posts by default and can be used to field simple questions from the community. They are a handy communication channel for lots of people online.

Casual, conversational updates with links to interesting URLs - including blog posts and Talk objects - seem to go down well. Regular updates (at least daily) result in a good channel for communicating with the public.

If you are interested in tweeting, or posting from your projects account (and we recommend that you do) then we will provide you access. Some of our projects have a dedicated following online. Galaxy Zoo has more than 8,000 followers on Twitter and Planet Hunters' Facebook community has nearly reached 10,000.

We usually support Twitter and Facebook pages for our sites. We're also working to support Google Plus too.


### Talk and Moderators

___

## Project Launch

### Launch timeline

- Go/no-go date and time
- Sharing the site before launch
