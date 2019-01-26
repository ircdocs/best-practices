---
title: TLS Guidelines
copyrights:
  -
    name: "Ryan Heywood"
    email: "ryan@hashbang.sh"
---

# Overall TLS Guidelines

Many IRC networks offer TLS connectivity on the now-standardized port 6697,
from RFC 7194. It should be safe to assume that if an IRC server is running on
port 6667 for a host, and a connection is possible for port 6697, that any
connections made to port 6697 should connect to the same IRC server.

Given the above assumption, clients should be able to probe for connectivity on
port 6697 for a given server, and inform the user that a secure connection to
the server is possible. Additionally, upon the first secure connection to the
server, the client should store the fingerprint of the server certificate, to
verify it on further connections. The client should also provide a way to show
the certificate to the user so the user can perform external verification.

On later connections, if the fingerprint is different, the client should then
display a message explaining that the server either changed their certificate
or someone could be performing an attack on the server. Networks should ensure
that the same certificate is synchronized across all servers using the same
domain name, and publish through some third party mechanism, such as a blog
post, that the TLS certificate has changed.
