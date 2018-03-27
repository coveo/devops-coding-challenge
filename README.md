# Coveo DevOps Challenge

## The Challenge

Your challenge, should you choose to accept it, is to develop an AWS S3 storage analysis tool. To test your tool, you will have to create a free [Amazon](http://aws.amazon.com/en/free/) account (if you don't already have one).

## Specifications

The tool is a shell command line utility that returns information over all [S3](https://aws.amazon.com/documentation/s3/) buckets in an Amazon account.

- Your tool must work on Linux, OSX and Windows.
- It must be easy to install and use.
- Ideally, your tool won't require installation of any other tools / libraries / frameworks to work.
- Time is money, we cannot afford running a tool that takes hours to complete, your solution should return results within seconds (or minutes if you are willing to test our patience :-).

## Time allowed

People who have successfully passed the challenge and are now happy members of the Coveo team usually took from 4 to 10 hours to complete it.

Remember the KISS principle...

### The tool must return the following information

- Bucket name
- Creation date (of the bucket)
- Number of files
- Total size of files
- Last modified date (most recent file of a bucket)
- And the most important of all, **how much does it cost**

### The following options should be supported

- Ability to get the size results in bytes, KB, MB, ...
- Organize the information by [storage type](https://docs.aws.amazon.com/AmazonS3/latest/dev/storage-class-intro.html) (Standard, IA, RR)
- Filter the results in a list of buckets (bonus point for regex support)
- Ability to group information by [regions](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html)

### Some additional features that could be useful (optional)

It would be nice to support prefix in the bucket filter (e.g.: s3://mybucket/Folder/SubFolder/log*). It may also be useful to organize the results according to the [encryption type](https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingEncryption.html), get additional buckets information (life cycle, cross-region replication, etc.) or take into account the [previous file versions](https://docs.aws.amazon.com/AmazonS3/latest/UG/enable-bucket-versioning.html) in the count + size calculation.

Some statistics to check the percentage of space used by a bucket, or any other good ideas you could have, are more than welcome.

## Rules

- Your are free to use the programming language and the [SDK](https://aws.amazon.com/tools/) of your choice, but remember that installation must not require us to install external tools in order to test the result of your work.
- We will test your work over our environment (which contains **several millions of files**). The overall performance of your tool will be evaluated.
- Your code must be made available on GitHub or any other public version control software. Your project must be a standalone project (i.e. **do not fork it from our challenge or any other project**).

## Advice

- **Try to design and implement your solution as you would do for real production code**. Show us how you create clean, maintainable code that does awesome stuff. Build something that we'd be happy to contribute to. This is not a programming contest where dirty hacks win the game.
- Feel free to add more features! Really, we're curious about what you can think of. We'd expect the same if you worked with us.
- Documentation and maintainability is a plus.
- Don't you forget those unit tests.
- We don’t want to know if you can do exactly as asked (or everybody would have the same result). We want to know what **you** bring to the table when working on a project, what is your secret sauce. More features? Best solution? Thinking outside the box?
