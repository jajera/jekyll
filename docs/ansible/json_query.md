---
layout: default
title:  Json Query
date:   2023-09-17 21:19:00 +0000
permalink: docs/ansible/json_query
parent: Ansible
---

{% highlight yaml %}
{% raw %}
---
- name: Json_query usage demo
  hosts: localhost
  gather_facts: false

  tasks:
    - name: Set value of jarray_1
      ansible.builtin.set_fact:
        jarray_1: |
          [
            {
              "name": "dev-svr1",
              "group": "frontend",
              "env": "development"
            },
            {
              "name": "dev-svr2",
              "group": "backend",
              "env": "development"
            },
            {
              "name": "prod-svr1",
              "group": "frontend",
              "env": "production"
            },
            {
              "name": "prod-svr2",
              "group": "backend",
              "env": "production"
            }
          ]

    - name: Set value of jarray_2
      ansible.builtin.set_fact:
        jarray_2: |
          { "servers": [
              {
                "name": "dev-svr1",
                "group": "frontend",
                "env": "development"
              },
              {
                "name": "dev-svr2",
                "group": "backend",
                "env": "development"
              },
              {
                "name": "prod-svr1",
                "group": "frontend",
                "env": "production"
              },
              {
                "name": "prod-svr2",
                "group": "backend",
                "env": "production"
              }
            ]
          }

    - name: Extract name from jarray_1
      ansible.builtin.debug:
        msg: "{{ jarray_1 | from_json | community.general.json_query('[*].name') }}"

    - name: Extract name and group from jarray_1
      ansible.builtin.debug:
        msg: "{{ jarray_1 | from_json | community.general.json_query('[*].{name: name, group: group}') }}"

    - name: Extract name from jarray_2
      ansible.builtin.debug:
        msg: "{{ jarray_2 | from_json | community.general.json_query('servers[*].name') }}"

    - name: Extract name and group from jarray_2
      ansible.builtin.debug:
        msg: "{{ jarray_2 | from_json | community.general.json_query('servers[*].{name: name, group: group}') }}"
{% endraw %}
{% endhighlight %}