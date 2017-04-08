ansible-acme-nginx-passenger
============================

Install Nginx+Passenger on Fedora/EL and issue a TLS cert from Let’s Encrypt.

Variables
---------

- `deploy_user` the user running the application; part of the `nginx`
  and `wheel` groups.  Defaults to `deploy`.

- `app_dir` the root directory of the web application; defaults to `/var/www`

- `app_root` the base directory for Nginx;
  defaults to `"{{ app_dir }}/current/public"`.
  Change to `"{{ app_dir }}/current"` for Node applications.

- `startup_file` the web application boot file;
  defaults to `"{{ app_dir }}/current/config.ru"`.
  Change to `"{{ app_dir }}/current/app.js"` for Node applications.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: all
  roles:
    - { role: dunn.acme-nginx-passenger, become: yes }
```

License
-------

MIT
