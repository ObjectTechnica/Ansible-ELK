Role Name
=========

Single Instance Elk Stack - Single instances are great for proof of concepts and small-business environments.

Components
------------

    - Elasticsearch: A NoSQL database and search server
    - Logstash: A log shipping and parsing service
    - Kibana: A web interface that connects users with the Elasticsearch database for visualization and search
    - NGINX: An open source, lightweight, high-performance web server or proxy server

Requirements
------------

    - Ansible 2.3
    - Updated inventory file
    - Pem key if you are deploying into aws.
    - Please remember to update the htacess file with actual credentials.  the file included is just a place marker with the command inside.
    - Updated hostnames in var.yml
    - Update the user in the si-elk.yml


Role Variables
--------------

This is a pretty vanilla deployment.  please update hostnames in var.yml

Dependencies
------------

None, unless you are deploying in aws on an ec2 host.  Then make sure you have all your connectivity and access setup prior

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: si-elk
      roles:
         - { role: si-elk, tags: si-elk }

ansible-playbook -i inventory/hosts.yml si-elk.yml

Pending
----------------

- More performance tuning.

- At the time of this commit the Ansible {Elasticsearch, Kibana, Logstash}-plugin module does not work.  So no X-Pack for you.  I will add it to this once I get a few clean runs in.


License
-------

MIT

Author Information
==================

Adam A. Valenzuela - Brevity is the Soul of Wit.
