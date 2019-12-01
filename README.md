freehck.k8s_amaizfinance_redis_cr
=========

Install redis into k8s cluster. Implicitly depends on AmaizFinance redis operator.

Description
-----------

This role installs redis into your k8s cluster. For now consider this role as a draft. You have only a few parameters like manifest template or replicas number to modify for your needs. This must be enough for a while.

Role Variables
--------------

`k8s_amaizfinance_redis_cr_replicas`: number of replicas, default `3`

zk8s_amaizfinance_redis_cr_manifest_template`:  template with manifest, default is `k8s_v1alpha1_redis_cr.yml`, this template is pre-baked into the role

`k8s_amaizfinance_redis_cr_manifest_file`: manifest will be stored into this file, default is `k8s_v1alpha1_redis_cr.yml`

`k8s_amaizfinance_redis_cr_namespace`: namespace to deploy redis, default is `default`

`k8s_amaizfinance_redis_cr_name`: the name of the Redis resource will be used as a label for all generated resources, and as the infix or suffix for them. Default is `redis`

Example
-------

    - role: freehck.k8s_amaizfinance_redis_cr
      k8s_amaizfinance_redis_cr_namespace: "redis"

Install
-------

This role can be installed from [Ansible Galaxy](https://galaxy.ansible.com/):

`ansible-galaxy install freehck.k8s_amaizfinance_redis_cr`

License
-------

MIT

Author Information
------------------

Dmitrii Kashin, <freehck@freehck.ru>
Alex Chistyakov, <alexclear@gmail.com>
