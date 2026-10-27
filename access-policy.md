# Access policy

Read access is granted per system by its owner (see Service owners in the README). Write access to
production is out of scope here: ask in #infra.

## Asking

Ask in #help-eng or #infra, or file an OPS ticket titled "Access request: <system> for <person>". Say which
system, read or write, and why. Asking on someone's behalf (a new hire, a contractor) is fine.

## Granting

1. Check the owner of the system in the handbook. Only the owner approves; the prod read replica needs both
   of its owners.
2. Approve in the thread or the ticket.
3. Add the person to the system's reader group:
   - Grafana: `grafana-viewers`
   - infra repo: GitHub team `infra-readers`
   - auth-service repo: GitHub team `auth-readers`
   - web-app repo: GitHub team `web-readers`
   - prod read replica: `pg-prod-ro` role, 90-day expiry
4. Reply in the thread or comment on the ticket that it's done, and close the ticket.
