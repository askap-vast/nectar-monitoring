# VAST Systems Monitoring Stack

Monitoring operation and configuration files for the ASKAP-VAST computing
systems on Nectar, including notably the Docker compose files.

## Operation

If any of the VAST systems' monitoring stacks are down, this section details the
instructions to restore them.

Navigate to one of the VAST systems via

```
ssh vast-[system] -A
```

Navigate to this repository and the corresponding system's directory via

```
cd [todo]/nectar-monitoring/[system]
```

Ensure the repository is up to date via

```
git pull
```

Then, raise the system's corresponding services via

```
docker compose up -d
```

which won't affect already running services. The stack's status can be confirmed
via

```
docker compose ps
```

or by navigating to [the Grafana
website](https://grafana.vast-data.vast-survey.org) and opening the dashboard
for the system.

## Dashboards

[All dashboards can be found
here.](https://grafana.vast-data.vast-survey.org/dashboards)
|Dashboard|Description|
|:---|:---|
|Quick View|At-a-glance metrics for the system as a whole.|
|System|Per-system performance metrics, including CPU, memory, storage, I/O, and network.|
|Storage|Per-system storage metrics, including usage, location, and availability.|
|Docker|Per-system Docker metrics, including container status, performance, and storage.|

## Contributors

- [Hansen Jiang](https://github.com/hansenjiang), Sidrat Research
