# Workshopify

_simple tool to run technology-mediated workshops (prototype)_

## Terminology

* Workshop - a group activity where people sit down and follow instructions on the big screen to do exercises (some of the exercises are individual, some - group). Workshops are combined from Modules. Individual run of a workshop is called a Session.
* Module - a single piece of activity that a group is asked to do. There can be modules of different types: content, exercises, break etc.
* Session - a single run of a particular workshop (the same workshop can be run many times with different Participants)
* Participant - user attending and participating in a workshop session
* Host - a special typf of participant who is organizing the workshop session and running it

## User Epics

* As a corporate executive I need an easy way for my employees to go through group-learning (without flying over / using expensive facilitator etc.)
* As a corporate executive I need an easy and organized way for my employees to learn and align

## User Scenarios

### User:admin

* create a new workshop
* populate it with modules
* populate each module with content

### User:host

* start a session
* invite others
* pause a session
* put the session on a big screen
* input results of group exercises
* download the output

### User:participant

* get invited
* connect with a smart device
* input with a mobile device

## Modules

* content:video
* content:image
* content:text
* break
* groupWork:watchAndDiscuss
* individualWork:prioritize

## Schema

* user
* workshop
* module
* session

## Routes

* `/` - landing (type your name and email to create a new session)
* `/s/{sessionId}` - join a session
* `/s/{sessionId}/projector/{hostToken}` - project view of the session (protected by the hostToken)
* `/workshops/` - view all my workshops, run one of them (initiate a new session) or create (clone or from scratch) a new workshop from modules
* `/workshops/{workshopId}/configure` - build / configure a new workshop: add and configure modules, resequence them and add workshop meta: name etc.
* `/workshops/{workshopId}/sessions` - view all sessions ever run this workshop
* `/workshops/{workshopId}/sessions/{sessionId}/results` - view session stats and results

## Stack

* Meteor
* React

## TODO

## DONE

* init
* schema and basic doc
