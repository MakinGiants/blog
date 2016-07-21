---
title: Publish maven Aar (android library) to private git repository (this case in bitbucket) NOT WORKING AGGRRRR
layout: post
date: 2015-06-03 20:01:00 UTC
updated: 2015-06-11 15:00:07 UTC
comments: false
categories: 
---

You will need 2 repositories:
1. Library code
2. Maven (where the compiled library will stay and other projects will get)

Clone both repositories and:

1. In your library gradle file (inside one):

{% highlight groovy %}
android {  
   lintOptions {  
        abortOnError false  
      }  
    }  
    uploadArchives {  
      repositories.mavenDeployer {  
        repository(url: "file:///&lt;absolute_path_to_maven_repo&gt;")  
        pom.version = "0.5"  
        pom.artifactId = "my_library"  
        pom.groupId = "com.yoursite"  
      }  
    }
}  
{% endhighlight %}

2. Do git push with all the deployed changes to your maven_repo
   With this settings you will need:

{% highlight groovy %}
repositories {  
	maven { 
		url 'https://bitbucket.org/&lt;repo_owner&gt;/&lt;repo_name&gt;/raw/master' }  
	}  
	dependecies {  
		compile 'com.yoursite:my_library:0.5@aar'  
  	}  
}
{% endhighlight %}

Note: the url is the HTTPS url that bitbucket offers (same for github).

Good luck :)

 <a href="http://downright-amazed.blogspot.com/2011/09/hosting-maven-repository-on-github-for.html">Source 1</a>
 <a href="http://cemerick.com/2010/08/24/hosting-maven-repos-on-github/">Source 2</a><br /><br />