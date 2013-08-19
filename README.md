# Setup Riak CS to provide your own S3 storage

This is a example configuration for setting up Riak-CS on [Digital Ocean](http://www.digitalocean.com)

## Introduction

There are several options to setup your own cloud storage with S3 compatible API. I have looked at the Riak CS, Eucalyptus Walrus and OpenStack Swift, Cloudian, Apache Cloudstack, Ceph. See [this blogpost](http://www.bitelm.com/2013/08/setting-up-your-own-s3-storage-on-vps.html) why Riak CS is the best option to use on Digital Ocean.

A complete guide for setting up using this example configuration will soon be linked here.

## Comparison

If you used 512mb droplets on Digital Ocean you now have your very own S3 compatible fault tolerant storage for $15 per month with 1 TB transfer and about 10-12 gb storage. However, you will loose a bit of that data transfer due to riak internal transfers until Digital Ocean has Internal Networking setup. Not bad. It does not give you any cdn performance, but its yours, private and safe, and in some cases it is faster than S3.

If you like me needed to host the data on your own due to contractual reasons, this might be an option.

Here is what you get for $15 per month elsewhere:
HP Cloud (Openstack) 10 GB storage, 110 GB bandwidth, 1.000.000 get requests and 100.000 put/copy/post/list requests
Rackspace (Openstack) - 10 GB storage, 120 GB bandwidth (Unlimited requests and CDN backed.)
AWS (S3) - 10 GB storage, 110 GB bandwidth, 1.000.000 get requests and 100.000 put/copy/post/list requests

So is it worth setting up Riak CS/Riak on DI compared to using cloudstorage from a different vendor? You will get more bandwidth, your data is 100% yours and up to you to maintain. Scaling is about as easy.

Consider your requirements and go from there. If you are like me, single developer and sysadmin in a company, consider how many hours you would like to spend on developing and how many hours you would like ot spend on operations...

But running your own S3 storage is cool...
