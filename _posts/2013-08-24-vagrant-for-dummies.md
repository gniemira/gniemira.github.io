# Vagrant for Dummies

[Vagrant])(http://www.vagrantup.com/) is a tool that let's you quickly spin up virtual machines. Now, whenever I start a new project, I like to include a Vagrantfile and spin up a virtual machine for a few reasons. However, the distance between starting projects is just long enough that I forget how to do it. So here's a reminder to myself:

## Step 1 - RTFM

The [Vagrant docs are here](http://docs.vagrantup.com/v2/).

## Step 2 - Get set up

My plan is almost always to set up a new rails project and set up a new box that's a copy of Heroku's cedar stack. 

After creating your new rails app, change over to that app's root directory and 

```
vagrant init other_stuff
```
