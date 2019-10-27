gitlab-pipeline-schedule
=========

Ansible role to update the gitlab pipeline schedules, it will be useful in projects where we need to update 
the pipelines schedules of multiple projects manually. With this role it can be updated in one go. 

Requirements
------------

curl command is required to execute the API commands of gitlab.

Role Variables
--------------

gitlab_token : API token from gitlab
gitlab_host :  Gitlab host, IP address or the dns for example, gitlab.example.com
cron_schedule : cron schedule to update on the project schedule. eg. "0 2 15 * *"
projects.project_id : gitlab project id which is assigned to particular repository.
projects.schedule_id : gitlab schedule id for which we need to update the cron schedule.

Dependencies
------------

None

Example Playbook
----------------
    - hosts: 127.0.0.1
      connection: local
      roles:
        - gitlab-pipeline-schedules

License
-------

Apache License
