---
layout: post
title: Store PID of background process
categories: linux
---
Bash script to store pid of background process in file.
{% highlight bash %}
#!/bin/bash
long_running_process &
echo $! > pid_file
{% endhighlight %}

Later to kill process run
{% highlight bash %}
$ kill -9 $(cat pid_file)
{% endhighlight %}

