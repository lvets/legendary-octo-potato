# legendary-octo-potato
Consul server + agents + fabio + webservers.

How to reproducde:

1. Bring up all containers.

  ```
  $ docker-compose up --build
  ```

2. Wait until the Consul servers have elected a leader and Fabio has added the routes to the webservers.

3. In another terminal, exec the Consul 1.5.2 container and reload consul.

  - `$ docker exec -it <ID> sh`
  - `$ consul reload`

   No routes will be removed from Fabio.

4. Do the same as step 3, but for the container with Consul 1.5.3 or Consul 1.6.4. You will see that Fabio removes the routes from its routing table when you do `consul reload`.
