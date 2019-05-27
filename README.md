# beans
Temporary repository to log bean creation

Adds a different logback.xml to allow specific logging.

## How to use it
Manually build the docker image and push it to `registry.molgenis.org/molgenis-app:<custom tag>`
Then deploy it with the standard molgenis chart as follows:
* Set advanced to true
* Point at the registry.molgenis.org
* specify the custom tag
* Add to catalinaOpts: `-Dlogback.configurationFile=/root/logback.xml`

The logging can be copied from the cluster to your local drive using
`kubectl cp <podname>:/usr/local/tomcat/logs/molgenis.log .`
