# FOSSLight LDAP Test Server

**FOSSLight LDAP Test Server** is intended for testing LDAP-based authentication.

## What is OpenLDAP?

[OpenLDAP](https://www.openldap.org/) is the open-source solution for LDAP (Lightweight Directory Access Protocol). It is a protocol used to store and retrieve data from a hierarchical directory structure such as in databases.

## Quick Start

Create a new `.env` file in project root directory.

```bash
touch .env
```
Add environment variables to `.env` file.

```bash
# Timezone
TZ=<TIMEZONE>

# LDAP Configuration
LDAP_ORGANISATION=<LDAP_ORGANISATION>
LDAP_DOMAIN=<LDAP_DOMAIN>
LDAP_ADMIN_USERNAME=<LDAP_ADMIN_USERNAME>
LDAP_ADMIN_PASSWORD=<LDAP_ADMIN_PASSWORD>
LDAP_CONFIG_PASSWORD=<LDAP_CONFIG_PASSWORD>
LDAP_READONLY_USER_USERNAME=<LDAP_READONLY_USER_USERNAME>
LDAP_READONLY_USER_PASSWORD=<LDAP_READONLY_USER_PASSWORD>
```

You can start the containers with the `up` command in daemon mode (by adding `-d` as an argument) or by using the `start` command:

```
docker-compose up -d
```

You can also visit [http://127.0.0.1:8080](http://127.0.0.1:8080) (or [https://127.0.0.1:8443](https://127.0.0.1:8443)) to access [phpLDAPadmin](http://phpldapadmin.sourceforge.net/wiki/index.php/Main_Page) after starting the containers.

### Authentication

- Login DN: `cn=<USER>,dc=<DOMAIN_NAME>,dc=<TOP_LEVEL_DOMAIN>`
- Password: `<PASSWORD>`

## License

Licensed under the [MIT License](LICENSE).
