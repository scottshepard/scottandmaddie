# scottandmaddie

This is the repo for my wedding website. It is hosted on AWS s3 and built 
using jekyll. You can visit the site [here](scottandmaddie.com)  

Running Locally
======

Download the code

	git clone git@github.com:eSpark/esparklearning.com.git  
	cd esparklearning.com

You will need RVM, Ruby, Xcode, and command line tools. 

First download Xcode

https://itunes.apple.com/us/app/xcode/id497799835?mt=12

While that is happening download and install Ruby and RVM

	\curl -sSL https://get.rvm.io | bash -s stable
	rvm install 2.1.1
	rvm use 2.1.1

Finally install Xcode command line tools

	xcode-select --install

This site is generated using jenkyll so you need to install jenkyll and build the code

	gem install jekyll  
	jekyll serve --watch

Go to localhost:4000 to view the site

Pushing the website
=======

First install s3cmd:

	brew install s3cmd  

Then put it recursively to the espark-refresh bucket:
  
	cd _site  
	s3cmd put --recursive * s3://scottandmaddie.com

Use your eSpark Amazon AWS credentials.