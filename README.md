# Ansible Role: Blazegraph

An Ansible role that installs [Blazegraph](https://www.blazegraph.com/) in a Karaf container on:

* Centos/RHEL 7.x
* Ubuntu Xenial

## Role Variables

Available variables are listed below, along with default values:

```
# Blazegraph version
blazegraph_version: 2.1.4
# User to install with
blazegraph_user: tomcat8
# Where to install to
blazegraph_home_dir: /opt/blazegraph
# Servlet container home directory
blazegraph_tomcat_home: /var/lib/tomcat8
# Path to install the WAR to
blazegraph_war_path: "{{ blazegraph_tomcat_home }}/webapps/bigdata.war"
# Log4J template file
blazegraph_log4j_template: log4j.properties
# Log directory
blazegraph_log_dir: /var/log/tomcat8/blazegraph
# Path to install the log4k settings to
blazegraph_log4j_path: "{{ blazegraph_tomcat_home }}/webapps/bigdata/WEB-INF/classes/log4j.properties"
```

There are additional configuration options available and documented in [defaults/main.yml](defaults/main.yml)

## Dependencies

* Tomcat 8
  
## Example Playbook

    - hosts: webservers
      roles:
        - { role: islandora.blazegraph }

## License

MIT