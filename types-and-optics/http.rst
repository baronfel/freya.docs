HTTP
====

The Arachne ``Arachne.Http`` library implements types which represent the semantics of the following standards:

* `RFC 7230 -- Message Syntax and Routing <http://tools.ietf.org/html/rfc7230>`_
* `RFC 7231 -- Semantics and Content <http://tools.ietf.org/html/rfc7231>`_
* `RFC 7232 -- Conditional Requests <http://tools.ietf.org/html/rfc7232>`_
* `RFC 7233 -- Range Requests <http://tools.ietf.org/html/rfc7233>`_
* `RFC 7234 -- Caching <http://tools.ietf.org/html/rfc7234>`_
* `RFC 7235 -- Authentication <http://tools.ietf.org/html/rfc7235>`_

This set of RFCs covers basic types present in HTTP requests and responses, principally the data found in the headers of HTTP messages. Strongly typed representations and parsers are given.

The ``Freya.Lenses.Http`` library provides optics from the ``FreyaState`` to the various aspects of the request and response defined within the RFCs. These optics are usable directly within a ``freya`` computation expression, working with the optic functions detailed in :doc:`/core/optics`.

The HTTP optics and types are likely to be the most commonly used optics dealing with request and response data. To use the optics and types, the following modules should be opened:

.. code-block:: fsharp

   // Working with Freya optics
   open Freya.Lenses.Http

   // Working directly with the types if required
   open Arachne.Http

The optics are all provided under the ``Request`` and ``Response`` modules (e.g. ``Request.path_``), along with sub-modules for headers (e.g. ``Request.Headers.accept_``).

.. note::

   Full documentation for the individual type designs within Arachne is not currently available, but will be added at a later stage. Inspecting the values returned however should be straightforward and logical, and all typed representations map very closely to the logical design/grammar defined within the appropriate RFC or Recommendation.
