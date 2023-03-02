# Week 2 — Distributed Tracing

##### Honeycomb setup

- create account in honeycomb
  - create environment
  - create api key
- add code to the backend flask to send tracing to honeycomb
  - https://docs.honeycomb.io/getting-data-in/opentelemetry/python/
  - add span
  - filter by visualization
  - add env to gitpod and docker-compose.yml

##### what is log?

- Current state of logging
  - on premise logs
    - infra
    - app
    - anti-virus
    - firewall
    - etc
  - cloud logs
    - app
    - anti-virus
    - firewall
    - etc
