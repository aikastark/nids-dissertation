# Constraint table (the core of the project)

Idea: for every feature the model sees, decide if an attacker can REALLY change it, and how.

| Feature (from dataset) | Can attacker change it directly? | Which real action changes it | Allowed range / limit | Other features that change automatically |
|---|---|---|---|---|
| Inter-arrival time (IAT) mean | Yes | Timing jitter (delay packets) | e.g. up to +X ms, attack must still work | Flow duration, packets/s |
| Packet length mean | Yes (increase only) | Padding | e.g. up to MTU | Total bytes |
| Flow duration | No (derived) | — | — | Follows from timing |
| Total bytes | No (derived) | — | — | Follows from padding |
| ... | | | | |

Draft this first, then check it with the supervisor.
