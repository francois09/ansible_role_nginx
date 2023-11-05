NGINX Ansible role
==================

Role to manage NGINX.

Requirements
------------

No requirements

Role Variables
--------------

* `nginx__install` For install only (default: False)
* `nginx__configure` For configuration  (default: False)
* `nginx__use_ssl` Use SSL config for nginx  (default: False)
* `nginx__conf` Define configuration like hostnames, redirects, etc. See below

Example of configuration:

```
nginx__conf:
  vhost:
    - hostname: site1.domain.org
      redirect_request:
        - from: /Films
          to: https://cloud.domain.org/index.php/s/oghHewjBNtJKleR
          code: 302
        - from: /Musics
          to: https://cloud.domain.org/index.php/s/BNoeraZDxtyUPkG
          code: 302

    - hostname: site2.domain.org
```

This conf creates 2 sites into `domain.org` and for the first one declare 2 redirections.


Dependencies
------------

None

Example Playbooks
-----------------

License
-------

GPL v3

Author Information
------------------

François TOURDE
