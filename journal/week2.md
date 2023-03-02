# Week 2 — Distributed Tracing

<<<<<<< Updated upstream
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
=======
###### Homework
- Instrument Honeycomb for the frontend-application to observe network latency between frontend and backend[HARD]
- Add custom instrumentation to Honeycomb to add more attributes eg. UserId, Add a custom span
- Run custom queries in Honeycomb and save them later eg. Latency by UserID, Recent Traces
>>>>>>> Stashed changes
