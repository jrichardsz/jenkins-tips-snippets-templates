### reset job build number

```
def jobName = "Enter Job Name"
def job = Jenkins.instance.getItem(jobName)
job.getBuilds().each { it.delete() }
job.nextBuildNumber = 1
job.save()
```

https://linuxhelp4u.blogspot.com/2018/03/how-to-clean-or-reset-build-numbers-in.html
