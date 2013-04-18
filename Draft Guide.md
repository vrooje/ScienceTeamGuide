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

### Useful terms

We have developed our own vocabulary over the years. Here are some terms that will be used and what they means:

- User/Volunteer
-- People using the website are our volunteers. They are referred to as 'users' in our database but we think 'volunteer' is far more respectful, since they are giving up their time to participate.

- Subject
-- Volunteers are shown subjects on the site. Subjects are the unit of data to be classified. In Galaxy Zoo they are images of galaxies, in Planet Hunters they are light curves.

- Annotation
-- Markings, transcriptions or answers to questions are 'annotations'. In Galaxy Zoo every answer is an annotation; in Planet Hunters every transmit box drawn. Annotations are the smallest thing a volunteer can add to a subject.

- Classification
-- The complete set of annotations that a volunteers adds to a subject, form a classification.

- Interface
-- The main classification tool used by the public on the project.

- Backend/Frontend
-- We may talk a lot about front-end and back-end systems. The front-end is the main user interface and website that people see and use in their browser. The back-end refers to the database and API that serve subjects to the project and which saves data for reduction later on.

___

## Anatomy of a Zooniverse Project

### Key Components

Zooniverse projects have a common structure.

- UI
- Database
- Ouroboros
- Talk(?)
- Subjects, Classifications and Annotations

### Website 'Content'

- We need text from you
- Images, videos and biographies

___

## Interface Design

### Example data

- Importance of a good example dataset

### Agile Development

- Rapid turnaround
- Amazon EC2 URLs

### GitHub

- Issues and ticketing problems

___

## Talk and Other Zooniverse Tools

### What is Talk?
### Dashboard
### Letters
___

## Data Preparation

### Discussing subject creation and delivery
### Amazon S3
### MongoDB, MySQL and CSV

- Why we aren't using MySQL
- Data I/O methods and how often it can be done
- We like simple data formats
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
