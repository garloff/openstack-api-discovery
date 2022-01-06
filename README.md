# openstack-api-discovery

Simple script that does API discovery for OpenStack environments.

You need `OS_CLOUD` or (`OS_AUTH_URL` and `OS_USERNAME` and `OS_PASSWORD` and `OS_PROJECT` ... ) configured,
so that openstack catalog list works (without any additional arguments).

It queries your catalogue and then also discovers the versions / microversions of the services.
It maps some of the versions (nova, cinder, glance) to OpenStack releases.
It also knows how to query extensions for the OpenStack APIs (nova and cinder support this).

The output is a list of regions, availability zones (compute, storage, network),
the services with endpoints and versions and extensions.
It also displays info on the SSL certificate used.

This is a demonstrator to generate structured (JSON/JSON-LD\*) data for self-descriptions.
