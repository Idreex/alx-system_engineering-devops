# HTTPS SSL

In this project, I learned about the importance of HTTPS and how it works. I
configured my HolbertonBnB web servers with `certbot` certificate and HAproxy
SSL termination.

## Tasks :page_with_curl:

* **0. World wide web**
  * [0-world_wide_web](./0-world_wide_web): Bash script that displays
  information about subdomains on my configured servers.
  * Usage: `./0-world_wide_web <domain> <subdomain>`
  * Output: `The subdomain [SUB_DOMAIN] is a [RECORD_TYPE] record and
  points to [DESTINATION]`
  * If no `subdomain` parameter is passed, displays information about the
  subdomains `www`, `lb-01`, `web-01` and `web-02`, in that order.

* **1. HAproxy SSL termination**
  * [1-haproxy_ssl_termination](./1-haproxy_ssl_termination): HAproxy
  configuration file that accepts encrypted SSL traffic for the subdomain
  `www.` on TCP port 443.

* **2. No loophole in your website traffic**
  * [100-redirect_http_to_https](./100-redirect_http_to_https): HAproxy
  configuration file that automatically redirects HTTP traffic to HTTPS.
