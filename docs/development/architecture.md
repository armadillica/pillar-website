# Architecture overview

Pillar is designed around a flat data storage, using a layered access approach.
The stack, in terms of services, looks like this:

* mongo datastore: all data (not files) is stored here
* pillar (server): provides REST API to access data
* pillar-web: web interface for pillar (uses the pillar-python-sdk)

We chose to keep the REST API service very separate from the web interface in
order to limit the scope of both applications' requirements and in an effort to
keep things simple.

## Pillar server
The Pillar server is a Python web application based on the python-eve library,
which brings in most of the functionality to easily create a RESTful API.
We extend this functionality by providing our own permission system, as well as
a flexible data model that uses the Cerberus library as validation tool.

Pillar server is the only component that communicates with the Mongo data store,
as well as with the file storage.

## Pillar web
Pillar web is a Flask application that provides web access to the Pillar server.
It does not have data or file storage as it is meant to be only a *View*
component for Pillar. Pillar web is based on the original work done for Blender
Cloud v1.

### Role and action-based view
Instead of working on a separate user/admin interface, we push for a context
based approach when rendering a page. This allows us to have less views, that
look slighlty different depending on the user roles (subscriber, admin) and the
action performed (view, edit, create, etc.).

## Pillar Python SDK
The Python SDK, inspired by the PayPal REST SKD, is meant to be a library
capable of providing a standard way to communicate with the Pillar server.
This library should be used as a dependency to any tool that wants to connect
to the server to read and write data.

Currently the Python SDK is used in Pillar Web and in the Blender Cloud add-on.
