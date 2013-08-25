# Vagrant for Dummies

[Vagrant])(http://www.vagrantup.com/) is a tool that let's you quickly spin up virtual machines. Now, whenever I start a new project, I like to include a Vagrantfile and spin up a virtual machine for a few reasons. However, the distance between starting projects is just long enough that I forget how to do it. So here's a reminder to myself:

## Step 1 - RTFM

The [Vagrant docs are here](http://docs.vagrantup.com/v2/).

## Step 2 - Get set up

My plan is almost always to set up a new rails project and set up a new box that's a copy of Heroku's cedar stack. Thanks to the internet, there's such a box for you to grab [here](http://dl.dropbox.com/u/1906634/heroku.box). 

After creating your new rails app, change over to that app's root directory and 

```
$ vagrant init heroku http://dl.dropbox.com/u/1906634/heroku.box
```

Once you've done that, you should see

```
A `Vagrantfile` has been placed in this directory. You are now
ready to `vagrant up` your first virtual environment! Please read
the comments in the Vagrantfile as well as documentation on
`vagrantup.com` for more information on using Vagrant.
```

Now you have a Vagrantfile in your root directory. Good for you! Now you should 

```
$ vagrant up
```

## Step 3 - A few vagrantfile tweaks

Open up your new Vagrantfile and make sure the following line is uncommented:

```
config.vm.network :forwarded_port, guest: 3000, host: 3000
```

With port forwarding on, you should be able to open up your browser to localhost:3000 as usual and see your site.

Since you've changed your Vagrantfile, you should reload:

```
$ vagrant reload
```

## Step 4 - SSH into your shiny new box

Easy as pie:

```
$ vagrant ssh
$ cd /vagrant
```
Now you're in your app's root directory on your virtual box.

## Other Resources

Ryan Bates made a [Railscast about Vagrant](http://railscasts.com/episodes/292-virtual-machines-with-vagrant)
