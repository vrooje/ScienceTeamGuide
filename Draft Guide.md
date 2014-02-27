# Zooniverse Guide for Science Teams
### Robert Simpson (_Created April 2013_, Edited February 2014)
_______

## Contents

1. [Introduction](#introduction)
- [Setting Up the Process](#setting_up)
- [Stages of a Project](#stages_project)
- [Anatomy of a Project](#anatomy_project)
- [Interface Design](#interface_design)
- [Talk](#talk)
- [Other Zooniverse Tools](#other_tools)
- [Data Preparation](#data_prearation)
- [Analysis of Data](#analysis)
- [Project Analytics](#analytics)
- [Project Launch and Beta Testing](#launch_and_beta)
- [Communicating with Users](#communication)
- [After Launch](#after_launch_changes)
- [Closing Down the Project](#closing_down)
- [Summary](#summary)

___

## <a id="setting_up"></a> Setting Up the Process

So we're building your project: congratulations! That means we're going to build an awesome citizen science project together.

### Key contacts at the Zooniverse

The Zooniverse consists of two main groups: one in the University of Oxford (UK) and one at the Adler Planetarium (Chicago, US). The Oxford group is led by Chris Lintott (cjl@astro.ox.ac.uk) and the Chicago team by Laura Whyte (laura@zooniverse.org). You'll be working with some combination of people in both these teams over the coming months.

In addition to our amazing developers, whom you will meet during the process of building your project, there are some other names that will may be useful:

- Chris Snyder - Porject Manager cs@zooniverse.org
- Robert Simpson - Communications lead rob@zooniverse.org
- Kelly Borden - Education specialists kelly@zooniverse.org
- Heath Van Singel - Visual design heath@zooniverse.org

### JISCMail lists

As with all things, communication is vitally important in building Zooniverse projects. We are distributed around the world (and we travel too) and this is also true for most science teams. To keep in touch, we use the JISCMail LISTSERV service for our projects. This is a kind of email exploder, that you interact with via email or the web. Only those on the list can send or receive messages. Everyone that needs to will be added to the list for your project and this will be set up early on by our team.

JISCMail allows the conversation to be inclusive and creates a record of the conversation at jiscmail.ac.uk. This can be useful in months and even years to come. When writing a paper in two or more years' time, you'll want to be able to find that detailed discussion about data selection without having to search everyone's email. People can be added to and removed from these lists as needed.

### Support Email

In addition to directly contacting team members, or using the project's JISCMail list, you might also have lower-priority requests or queries that can be answered by many members of the team. For these we encourage everyone to use our support@zooniverse.org email address. We use this ourselves with in the Zooniverse. Emails will be directed to the right person and dealt with within a few days. **This address is for use after the site is live and public. Discussion about development should be kept to GitHub and email**.

### Amazon Web Services

At the Zooniverse we rely on Amazon Web Services for our core infrastructure. All our servers are virtual machines _in the cloud_ - this includes our webapps (i.e. the project itself) as well as our databases and other sites. We also store the images and other data for projects on Amazon S3, a highly redundant and scalable online storage platform. This means that test sites, sample data, and other things, will often be found at amazonaws.com URLs.

We don't need you to create any Amazon accounts, or really think about this much at all, but it's worth noting that we use this service and that is a popular, and secure way to hosts large-scale websites.

### Agreeing a timeline

Early on in the process a rough timeline will be agreed regarding when to aim to launch the site and when to start work in ernest.

### Things You Can Do Now

- Play with existing Zooniverse projects http://zooniverse.org
- Use Talk (e.g. http://talk.spacewarps.org), http://talk.galaxyzoo.org
- Create an account with GitHub at http://www.github.com and take a look around.
- Start thinking about publications you aim to write with this data and the publication policy for this project.

___

## <a id="stages_of_project"></a> Stages of the Project

### General timeline

There is no 'Gantt Chart' or specific time-plan for a Zooniverse project - because they are all different. However the outline below shows the approximate order of proceedings and gives you an idea of how the work is done.

| Phase | Timescale                  | Outline                  |
|-------|-----------------------|--------------------------|
| Pre-development | Days to weeks  | Shared understanding of science goals. Requirements of classification interface.             |
| Interface Development | Weeks  |  Creating a useful and useable main interface for the project  |
| Website Development | Week to months | Creating a website around the main interface, with background information, team biographies, images and pictures |
| Alpha Site | 2-6 weeks before launch | Site is circulated around team for feedback. Test data reduction may happen at this stage. |
| Beta Site | 1-3 weeks before launch | Site released to limited members of the public for a 'practice' run and feedback from real users. A test data reduction should ideally happen at this stage if not in the previous stage. Test that site works as expected and decide on revisions needed or launch date. |
| **Launch** |  | **Site is released to the public!** Press plan executed, team online during initial days of activity. |
| First data reduction | Week after launch | Data delivered to science team from initial use of site. Communicate results to volunteers where possible. |
| Steady-state | As long as it takes | Site exists in a more-or-less steady state, with data reduction ongoing and communication with volunteers. Newsletters can be sent our periodically, and traffic may come in bursts if there is press interested. |
| Retiring the project | As required | If science goals have been completed and nothing further can be gained from the site it is 'retired' and it is made clear to users that clicks are no longer useful. |
| Archiving the project | As required | If a project is done and over it is retired and no longer available on Zooniverse home. A closing blog post or press release should be issued with remarks on the science that has been achieved and the legacy of the project. The site remains up for education and reference use. |

____

## <a id="anatomy_project"></a> Anatomy of a Zooniverse Project

We have developed our own vocabulary over the years. Here are some terms that will be used and what they means:

#### User/Volunteer
People using the website are our volunteers. They are referred to as 'users' in our database but we think 'volunteer' is more respectful, since they are giving up their time to participate.

#### Subject
Volunteers are shown subjects on the site. Subjects are the unit of data to be classified. In Galaxy Zoo they are images of galaxies, in Planet Hunters they are light curves.

#### Annotation
Markings, transcriptions or answers to questions are 'annotations'. In Galaxy Zoo every answer is an annotation; in Planet Hunters every transit box drawn. Annotations are the smallest thing a volunteer can add to a subject.

#### Classification
The complete set of annotations that a volunteers adds to a subject form a classification.

#### Interface
The main classification tool used by the public on the project.

#### Application Programming Interface (API)
A system by which one can interact with software - in our case the main Zooniverse software, Ouroboros. An API is the way to directly communicate with the app that handles the database, without just clicking on the websites. APIs exists for many services online.

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

## <a id="interface_design"></a> Interface Design

Once the project is under development we'll send round concepts and designs for the main classification interface. The team will require examples of subjects from your data to do this and the requirements the format of this data will be specific to each project.

### Example data 

When delivering example data to the team, consider that this will be used to determine the look and feel of the project and the nature of the main classification interface. So try to send representative data. If only 1 in 20 images are 'cool' please try to send a representative set and not just your 20 best images (thought we may ask for those later). Similarly if you have data from several sources, it may be worth including examples from each. This will make sure we create the right kind of user-interface and website design.

### Agile Development

We operate in a mode where we try to build stuff, show it to you, and implement feedback quite rapidly. We appreciate that this is not often how science, or scientific publication, operates.

This rapid turnaround means that we are always accepting comments and ideas in the early stages. It also means that things will not be complete until near the end. To facilitate this, we have a system for ticketing issues for the project developers (see below).

During development will send you emails with links to long Amazon URLs. These often temporary URLs are usually only for sharing within the science and development teams and may cease to work when the next version comes along.

### GitHub

We use a collaborative coding, versioning system called Git and a website called GitHub (http://www.github.com). Each project has its own GitHub code repository (or just 'repo') and we use the same site to log development issues for everyone involved.

GitHub issues are a very powerful and effective way for everyone to log problems or suggestions whilst the site is under development. GitHub accounts are free and we encourage you to signup and let the team know your username. You can receive alerts when issues are discussed or completed and see if other people have already ticketed your idea or problem. GitHub links nicely with email so you don't need to keep logging into the site to see how things are going.

___

## <a id="talk"></a> Talk

Talk is our custom-built discussion tool. Users are encouraged to comment on, and collect, items they see on the project. The idea is to facilitate the collection of interesting subjects and their discussion. Talk is designed such that if you find a subject interesting or odd then you can quickly see if anyone else has commented on it before and what they said.

There are two ways for volunteers to reach Talk: by visiting the front page of the site or by being linked to an 'object' page after completing a transcription such as this one. There will usually be a link to 'discuss' at the end of each task. 

![Planet Four Talk](http://zooniverse-resources.s3.amazonaws.com/science_team_guide/p4talk.png)

There are some features in Talk that may seem a little unusual at first but can (and have) been used to do some excellent science.

### Every subject in the project usually has its own discussion page

One important thing to realise about Talk is that every record that is shown in the main project interface has a dedicated page that people can comment on. This means that object-specific discussion can happen right on the object and more general community discussion can happen elsewhere.

### You can tag and collect things

Talk supports tagging and user-generated collections of objects. Tagging is achieved using the Twitter convention of #tagname (with no spaces) when writing a comment. Tags are commonly used by the community and science team to identify similar objects in the data. For example, images from Snapshot Serengeti have been tagged by the community with #fire when there are flames visible or a wildfire, as this not something asked for in the main interface.

Collections are groups of objects that people use to group similar objects. Once you have some collections, then when you are on the object discussion page there are links to 'collect this' and add to one of your collections. Note that collections, like objects can be discussed also.

### Three types of discussion

Talk has three different 'types' of discussion. The first is general community questions/answers. These are on the boards and are globally split into Science, Help and Chat.

The second is short comments on an object or collection. People typically use these to quickly tag objects.

The third is more in-depth discussion for specific objects or collection which is for longer posts. When people start these 'faceted' discussions they also show up in the boards under the same Chat heading.

### Talk is dynamic

If many people are using the same tag it will become a 'popular' tag and will show up on the front page. When a critical mass of people start discussing an object or participating in a discussion on a board then the object or thread shows up in the trending sections of the front page. Basically Talk is designed to show you what's happening right now.

___

## <a id="other_tools"></a> Other Zooniverse Tools

### Dashboard (http://tools.zooniverse.org)

![Screenshot of the Dashboard](http://zooniverse-resources.s3.amazonaws.com/science_team_guide/tools.png)

The dashboard - or _Zoo Tools_ - is a place where people can filter and plot data from some Zooniverse projects, and other selected public datasets. For example, galaxies from Galaxy Zoo can be plotted using a variety of charts and filtered according their location or redshift metadata.

Not all data from all projects is currently supported in the dashboard. It is still under development but if you've got a cool use-case, speak with Arfon.

### Letters  (http://letters.zooniverse.org)

![Screenshot of Letters](http://zooniverse-resources.s3.amazonaws.com/science_team_guide/letters.png)

Letters is a place for citizen scientists to 'publish' short articles. These may be summaries of research they have undertaken individually or in groups, or outlines of useful tools or techniques.

___

## <a id="data_preparation"></a> Data Preparation

### Discussing subject creation and delivery

Once the size and shape (or duration, in case of video/audio) of subjects has been established then we need to start chopping up your dataset accordingly.

It may be the case that you are able to do this, and this is often preferred as it helps assure you of the completeness and quality of the final dataset. It may also be the case that the development team need to modify or compress data.

Whatever the requirements, the science and development teams will come to an agreement on what is required and how it will be delivered. It may be that the science team upload files directly or that they deliver hard drives to one of the Zooniverse offices.

### Amazon S3

All of our subjects end up on Amazon S3. This is Amazon's ultra-reliable online storage platform and allows files to stored online and served globally and without hitting any of our servers. It is fast and highly redundant - meaning that subjects load as quickly as possible and are always available online.

All subjects have a unique, public, read-only Amazon URL on S3 which allows them to be used in the classification interface. All our databases store this URL with the subject meta data.

### MongoDB, MySQL and CSV

Our older projects (those launched before September 2012) are built as Ruby-on-Rails web-apps, running on their own servers and relying on their own MySQL database to store all subject, classifications, users etc.

Our recent projects are HTML5 apps (i.e. they run in the browser and not on servers) and access our custom API application Ouroboros. Ouroboros stores all data in a large MongoDB database server, which spans all projects. MongoDB is not a relational database, but a sophisticated document store for online systems just like ours.

We can import and export subjects, users and results from Ouroboros in CSV, SQL and native MongoDB binary. However we cannot allow everyone access to the system directly - for stability and security reasons. We are able to automated regular data dumps for some regular queries.

If you can't handle MongoDB, it is usually simplest for us to deliver data in the form of CSV files.
___

## <a id="launch_and_beta"></a> Project Launch and Beta-Testing

As development nears completion we will begin discussing a timeline for launching the site to the public. The first step is to select a good time to perform a beta test of the project.

The Beta is a dry-run of the website with a small group of volunteers (usually about 100-200 people). It is a chance to check that the web-app is working, that people understand the task and that the results make sense.

### Collecting Beta Users

When we are ready to launch a Beta we usually send a Zooniverse newsletter and ask for volunteers to email us if they wish to take part in the test of a new project. Those people that volunteers for this are usually our more dedicated and sensible participants. We can also use people known to the science team if that is preferred.

These people will then be sent a secret URL, told the aims of the project and asked to fill out a feedback form when they have had a go. The data in a beta is usually a limited sample of the full set. This is done to keep the beta small and manageable and also so that we get a representative set of results.

### Feedback and Beta Results

The feedback form we ask them to fill in can be customised and the results will be shared. We usually ask about how they found the site, whether they understood the task and like the idea.

We can use this form, and the beta classifications data to determine if the site is ready for launch and if so, how long the development and science teams need to make it happen.

### Press strategy

After testing has been underway and a launch date is being discussed, we can start talking about press releases and how best to coordinate the website's launch. In most cases the press release should come from the science team - after all, you're better equipped to deal with your own science than we are.

We have found that the best model is to have one institute issue a press release and for any other institutions to coordinate with the lead. This varies project to project.

We will also send a newsletter to appropriate Zooniverse users and get existing projects to blog/tweet where appropriate.

### Launch timeline

With a launch date agreed, we usually establish a go/no-go date and time. This is a time at which we pass a point of no return and must launch the website. There are no priority issues pending at this time, and everyone should be happy with the site going live. At this time press releases are issued (often with press embargoes) and everyone is prepared for launch.

Launch day is often very busy - particularly if press do pick up on the story - so it is important to have members of the science team online and ready to answer development team queries, and more importantly answer volunteers' queries on Talk. We find that solid, lasting Talk communities are honed and established during the days after launch.

Engaged science teams are essential in allowing this to happen. If the volunteers see that you're around for launch, then they are likely to be much more committed to the project.

___

## <a id="communication"></a> Communicating with Users

### Newsletters

We have the capability to send emails to all our users, either across the Zooniverse or per-project. With hundreds-of-thousands of emails going out in one go, these are not sent lightly. We try to limit newsletters to once a month per project, although exceptions have been known.

We generate lists of users and keep them internally in order to keep users' personal data private. As such we need to send newsletters and do so in coordination with project teams. We also try to send periodic Zooniverse-wide newsletters.

### Blogging

Most of our projects have their own blogs at blog.projecturl.org. This is a Wordpress.com blog and anyone that wants to blog should signup for a free account at www.wordpress.com.

Blogging is useful for communicating with interested volunteers and for reporting preliminary results during data reduction. 

Some highlights from our existing blog network include the blogs for Planet Hunters (http://blog.planethunters.org), Snapshot Serengeti (http://blog.snapshotserengeti.org) and Moon Zoo (http://blog.moonzoo.org). It is worth reading some entries on these sites to get an idea of what a good Zooniverse blog looks like.

These three blogs are read by between 1,000 and 10,000 people a week and good chuck of those readers (about 40%) click through to the project or Talk.

### Social Media

In addition to the blogs, our projects are also present on the main social media platforms. These accounts automatically post links to blog posts by default and can be used to field simple questions from the community. They are a handy communication channel for lots of people online.

Casual, conversational updates with links to interesting URLs - including blog posts and Talk objects - seem to go down well. Regular updates (at least daily) result in a good channel for communicating with the public.

If you are interested in tweeting, or posting from your projects account (and we recommend that you do) then we will provide you access. Some of our projects have a dedicated following online. Galaxy Zoo has more than 8,000 followers on Twitter and Planet Hunters' Facebook community has nearly reached 10,000.

We usually support Twitter and Facebook pages for our sites. We're also working to support Google Plus too.

### Talk and Moderators

The Talk platform begins with the science team answering queries and commenting on the public's discussions. It can be a lot of fun! During the first days the science team's interactions on Talk will help build a core of users who are known and learn common answers. Many of them will, in turn, begin answering the queries of others and lightening the load on the science team. When you spot these people - keep any eye on them: they may become your moderators. If you spot potential moderators who should communicate with them and see if they are interested in participating further.

Once promoted, moderators have powers to delete posts, ban users and highlight content to others more easily. They are marked as moderators in Talk and often become community leaders on the project's Talk site. They can become very useful contacts for you and in some cases moderators have even joined the main team mailing list.

If you see users you think should become moderators, let us know. We have a Zooniverse-wide moderators email list and it may be useful to put them in touch. Moderators do not have to be enthusiastic participants, in some projects they are undergrads from relevant research groups, for example.
___

## <a id="analysis"></a> Analysis of Results

### Database Schema and Access

Very early on the process it is possible for us to give you example results data. Once the classification interface has been implemented it is possible to outline how the classifications will be structured. This means that you can begin working on data reduction before the project even begins.

### Example Data

We suggest using a set of sample classifications to get a handle on crunching your data before the Beta even goes live. This means that when you get the results from the Beta test you can see if the project is working and tweak your reduction.

### Results from Other Projects

There are many people working on past and current Zooniverse projects that are able to help you get started crunching data. Depending on the setup of the site, there may be even be code that can be usefully shared.

A *Zooniverse scientists* JISCMail listserv exists  - and an accompanying, private blog. If you want access them please conttact rob@zooniverse.org.

For some older projects there are published results, with papers outlining user-weighting schemes and clustering techniques. You can find a complete list of Zooniverse publications at http://www.zooniverse.org/publications.

Some notable Zooniverse data reduction papers that may be useful are:
- [Lintott+11, Galaxy Zoo Paper](http://adsabs.harvard.edu/abs/2011MNRAS.410..166L)
- [Schwamb+12, Planet Hunters Paper](http://adsabs.harvard.edu/abs/2012ApJ...754..129S)
- [Simpson+12, Milky Way Project Paper](http://adsabs.harvard.edu/abs/2012MNRAS.424.2442S)


### Results

It is a good idea to get a quick publication and authorship policy written up for your project. This is the responsibility of the project PI, although there will be Zooniverse team members that deserve authorship credit for the first N papers and science team members will need to agree about how this will work.

Publication is something we;re very keen on at the Zooniverse! It is how we show the scientific community what Zooniverse projects can do, and it shows our volunteers that what they are contributing to something real and worthwhile.

To that end it is always worth blogging about publications, and anything you can share about parts of those results beforehand online are always appreciated by the volunteers. We often use results a a chance to email a site's users and remind them about the project.

We try to maintain a policy of producing publicly accessible data on the projects own domain, in addition to publishing in formal channels. This means that anyone can access the data and gives us a chance to frame it for the public. You can see examples at http://data.galaxyzoo.org and http://data.milkywayproject.org.

_____

## <a id="analytics"></a> Project Analytics

### Analytics

For all our new projects there exists a status page, supported by Ouroboros, at api.zooniverse.org/projects/XXXXX/status where we can tell you what XXXXX is for your site (e.g. https://api.zooniverse.org/projects/galaxy_zoo/status).

![Ouroboros Analytics Example](http://zooniverse-resources.s3.amazonaws.com/science_team_guide/apidashboard1.png)

![Ouroboros Analytics Example](http://zooniverse-resources.s3.amazonaws.com/science_team_guide/apidashboard2.png)

Every project uses Google Analytics to track website use and traffic. This lets us monitor who uses the site and when and how long people spend on the main site, Talk and the blog.

We will provide summaries of the status of the project once in a while, to keep your project up to date. If you ever want to know more about how things are going - don't hesitate to ask.
___

## <a id="after_launch_changes"></a> After Launch

### Changes to the Project

We have always considered Zooniverse websites to be parts of the experiment. The way users interact with the tools they are given defines the nature of the classifications - as does the way those tools are explained and placed in context. For this reason it is generally not a good idea to change a project once it is live. Correcting text, updating team biographies and other small changes are usually fine, but any changes to the main interface could affect the results of the project and need careful consideration.

Similarly, once a project is up and running and a community is building up around it, the Zooniverse team will shift gear into a 'steady state' and will be focussing on new upcoming projects for development. We will continue to provide support but after launch the science team take the lead.

___

## <a id="closing_down"></a> Closing Down Projects

Hopefully the Beta test and early days of the project will give everyone a good idea of how long a project needs to run to complete the target science goals. For busy projects, those goals may be achieved earlier than expected, and for other projects it may be known from the start that there is a virtually limitless supply of data available for classification. Many projects run for years - and others only a few weeks! There are also projects that can be effectively 'paused' whilst new data is expected.

We can decide a project is over if some of the following are true:

- The project has enough classifications to complete its science goals.
- The project science team is no longer able to provide support or do research with the data.
- Traffic to the project has diminished such that it is no longer viable to continue running the project (and avenues to correct this have been explored).

In these cases archiving or retiring the project become the best options. Action like this is only taken in consultation between the Zooniverse team and the science team.

### Archiving Projects

If a project is deemed to be complete then in the first instance it will be 'archived'. Archived projects are modified to include a prominent message to volunteers that the site is no longer collecting useful data. The project remains on the Zooniverse homepage and we continue post social media updates, and support the blog and Talk.

### Retiring Projects

When a project is retired a prominent message is displayed to visitors that this site is longer active.. Users's favourites and recents remain accessible but the database is essentially 'disconnected'.

A date is agreed when the blog and Talk will be frozen and a final blog post is written explaining the project's retirement. Social media and newsletter activities come to an end.

Data from the project (including archives of the blog, tweets etc) are made available to the Zooniverse and science teams.

___

## <a id="summary"></a> Summary

Zooniverse projects are a lot of fun and really engage the public with discovery and with your science. We're looking forward to building your project with you.

If you have any questions about this guide contact rob@zooniverse.org.

___
