# Ansible Role: Blazegraph

An Ansible role that installs [Blazegraph](https://www.blazegraph.com/) in a Karaf container on:

* Centos/RHEL 7.x
* Ubuntu Xenial

## Role Variables

Available variables are listed below, along with default values:

Version to install:
```
blazegraph_version: 2.1.4
```

User to install with:
```
blazegraph_user: tomcat8
```

Home directory:
```
blazegraph_home_dir: /opt/blazegraph
```

Servlet container directory:
```
blazegraph_war_path: "{{ tomcat8_home }}/webapps/bigdata.war"
```

Log4J properties file:
```
blazegraph_log4j_template: log4j.properties
```

Log directory:
```
blazegraph_log_dir: /var/log/tomcat8/blazegraph
```

Where to place the log4j.properties file.
```
blazegraph_log4j_path: "{{ tomcat8_home }}/webapps/bigdata/WEB-INF/classes/log4j.properties"
```

## Dependencies

* None
  
## Example Playbook

    - hosts: webservers
      roles:
        - { role: islandora.blazegraph }

## License

MIT