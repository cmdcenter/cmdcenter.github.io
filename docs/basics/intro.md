

### Command Center ?

CmdCenter is an infrastructure and application lifecycle managment tool optimized for developpers.

It lets you run complex, cloud agnostic infrastructure using developper friendly cli tool and json configuration. 

Written with real world applications in mind, it includes simple but powerful application lifecycle  managment tools.

Every command is designed to perfectly match what you want to do and give you the shortest path to do it.



### What kind of infrastructure ?

It manages all kind of server types:

- application servers, running docker containers
- mysql databases (mysql, postgresql, ...)
- nosql databases (mongodb, couchdb, ...)
- cache servers (memcache, ...)
- work queues (beanstalkd, ...)
- ci servers (jenkins, ...)
- distributes file systems (GlusterFS, BeeGFS, ...)
- S3 like object stores (RiakCS, ...)
- ...




### How is it better than writing my own bash scripts ?

You dont have to write it anymore, cmdcenter takes care of traslating simple commands into complex scripts that run serverside.

It saves you tons of time, especially if you manage a lot of projects involving varied software stacks.

Manually SSH to the server to make a change will become the exception rather than the rule


### I am affraid to lose control

Unlike other infrastructure tools on the marker selling you too much magic, cmdcenter requires you to understand what you are doing.

Every command is designed to perfectly match what you want to do and give you the shortest path to do it.




### You said applications ?

Yes, cmdcenter also manages application creation, deployment, continious integration, environments and backups

create:
```bash
cmdcenter.py create app nodejs --name myapp_staging --domain myapp.com --git git@github.com:someuser/myapp.git --wwwdir "src/www" --env staging --org myorg
```

deploy:
```bash
cmdcenter.py deploy app myapp_staging --org myorg
```

backup:
```bash
cmdcenter.py backup app myapp_staging --org myorg
```


### What kind of applications ?

You can literally run any stack or application you want using cmdcenter.

Under the hood, cmdcenter uses docker containers for each application.

Not happy with pregenerated Dockerfile ? Simply write your own !


### How about operations engeneers ?

CmdCenter works best inside organisations with strong devops culture.

However it doesn't force you to share access to staging/test/production environments, so you can still separate dev and ops if you want.



### Cloud agnostic ?

Yes, the only few requirements are:
- your server provider has to support private networking
- all server instances must live on same datacenter
- base server image must be ubuntu 14.04 LTS, which is available on any VPS/dedicated server provider

*NOTE:* Other base images will be supported later



### What if you dont support Y ?

CmdCenter is open source and MIT licenced, it can support virtualy any server type.

Feature and pull requests are more than welcome.


