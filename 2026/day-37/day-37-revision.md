## Self-Assessment Checklist
Mark yourself honestly — **can do**, **shaky**, or **haven't done**:

- [x] Run a container from Docker Hub (interactive + detached)
- [x] List, stop, remove containers and images
- [x] Explain image layers and how caching works
- [x] Write a Dockerfile from scratch with FROM, RUN, COPY, WORKDIR, CMD
- [x] Explain CMD vs ENTRYPOINT
- [x] Build and tag a custom image
- [x] Create and use named volumes
- [x] Use bind mounts
- [x] Create custom networks and connect containers
- [x] Write a docker-compose.yml for a multi-container app
- [x] Use environment variables and .env files in Compose
- [x] Write a multi-stage Dockerfile
- [x] Push an image to Docker Hub
- [x] Use healthchecks and depends_on

---

## Quick-Fire Questions
Answer from memory, then verify:

1. What is the difference between an image and a container?
   --->  An image is a blueprint, a container is an actual running instance of an image.

2. What happens to data inside a container when you remove it?
   ---> It is gone. As containers are ephemeral by nature.

4. How do two containers on the same custom network communicate?
  ---> Containers can communicate using built-in DNS name resolution (container name → IP)

5. What does `docker compose down -v` do differently from `docker compose down`?
  ---> `docker compose down -v` : Docker compose down -v removes the volume of the container
  ---> `docker compose down` : It only removes the container but the Volume is still attached 

7. Why are multi-stage builds useful?
  ---> Multi Stage build is useful for Reducing the docker image size so that anybody can use it and it will be light weight.

8. What is the difference between `COPY` and `ADD`?
  ---> `COPY` : COPY commands copy the whole file from local to docker 
  ---> `ADD` : also copies from web or any tar.

10. What does `-p 8080:80` mean?
  ---> `-p 8080:80` : -p means post is getting exposed to world on port. `hostport:containerport`

11. How do you check how much disk space Docker is using?
  ---> docker system df 

---

## Build Your Docker Cheat Sheet
Create `docker-cheatsheet.md` organized by category:
- **Container commands** — run, ps, stop, rm, exec, logs
- **Image commands** — build, pull, push, tag, ls, rm
- **Volume commands** — create, ls, inspect, rm
- **Network commands** — create, ls, inspect, connect
- **Compose commands** — up, down, ps, logs, build
- **Cleanup commands** — prune, system df
- **Dockerfile instructions** — FROM, RUN, COPY, WORKDIR, EXPOSE, CMD, ENTRYPOINT

Keep it short — one line per command, something you'd actually reference on the job.

---

## Revisit Weak Spots
Pick **2 topics** you marked as shaky and redo the hands-on tasks from that day.

---
