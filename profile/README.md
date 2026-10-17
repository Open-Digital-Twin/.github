# Open-Digital-Twin

Repository inventory index of the public code, models, datasets, and research artifacts maintained in the [Open-Digital-Twin](https://github.com/Open-Digital-Twin) GitHub organization.
Inventory last updated on 2026-10-17.

For academic projects, author and advisor names below come from the project's own documentation. Where no formal author list is provided, the people listed are the main commit authors visible in the repository history; this is contributor evidence, not a claim of formal paper authorship. Third-party projects are attributed to their upstream communities.

## Project overview

The repositories document two related generations of digital twin software:

- The dt-* services implement a service-based Digital Twin architecture, with MQTT clients, twin instances, configuration APIs, shared modules, and database setup.
- KTWIN is a Kubernetes-based platform built around Knative serverless workloads and DTDL/CRD models. Its repositories provide the operator, twin services, device publishers, dispatchers, event storage, graph access, and Smart Cities deployment artifacts.
- Other repositories contain federated-learning experiments, Smart Cities ontologies, academic work, integration tests, research data, and supporting or upstream software.

## KTWIN platform

**Authors and people involved:** [Alexandre Gustavo Wermann (@agwermann)](https://github.com/agwermann), [Juliano Araujo Wickboldt (@julianowick)](https://github.com/julianowick)

| Repository | Purpose |
|---|---|
| [ktwin-article](https://github.com/Open-Digital-Twin/ktwin-article) | KTWIN overview, research paper reference, experiments, plots, and raw experiment artifacts. The paper is “KTWIN: A serverless Kubernetes-based Digital Twin platform” (Computer Networks, 2025). |
| [ktwin-operator](https://github.com/Open-Digital-Twin/ktwin-operator) | Kubernetes operator that manages KTWIN resources and their custom resource definitions. |
| [ktwin-smart-cities-services](https://github.com/Open-Digital-Twin/ktwin-smart-cities-services) | Go and Python services for the KTWIN Smart Cities use case, including device, neighborhood, parking, pole, and streetlight services. |
| [ktwin-smart-cities-devices](https://github.com/Open-Digital-Twin/ktwin-smart-cities-devices) | Go and Python Smart Cities device implementations and MQTT publishers, including pole, streetlight, parking-spot, EV-charging, and battery examples. |
| [ktwin-dispatchers](https://github.com/Open-Digital-Twin/ktwin-dispatchers) | MQTT and CloudEvents dispatchers that route messages between physical devices and virtual services in the KTWIN cluster. |
| [ktwin-event-store](https://github.com/Open-Digital-Twin/ktwin-event-store) | Backend service for the KTWIN serverless platform that stores data events exchanged between twins. |
| [ktwin-graph-cache](https://github.com/Open-Digital-Twin/ktwin-graph-cache) | KTWIN Graph Store service, with an API for retrieving twin-graph data. |

## Smart Cities models and deployment artifacts

**Authors and people involved:** [Alexandre Gustavo Wermann (@agwermann)](https://github.com/agwermann), [Juliano Araujo Wickboldt (@julianowick)](https://github.com/julianowick)

| Repository | Purpose |
|---|---|
| [ktwin-smart-cities-dtd](https://github.com/Open-Digital-Twin/ktwin-smart-cities-dtd) | Deployable DTDL models and use-case instances for KTWIN Smart Cities, including neighborhood, pole, parking, device, and streetlight models. |
| [ktwin-opendigitaltwins-smartcities](https://github.com/Open-Digital-Twin/ktwin-opendigitaltwins-smartcities) | DTDL Smart Cities ontology based on open city models and standards such as ETSI NGSI-LD and SAREF4CITY. Its README describes collaboration with OASC and Sirus and credits Smart Data Models, FIWARE Foundation, and TM Forum. The repository was forked from [Azure/opendigitaltwins-smartcities](https://github.com/Azure/opendigitaltwins-smartcities) by Alexandre Gustavo Wermann. |

## dt-* architecture

**Authors and people involved:** [Francisco Paiva Knebel (@FranciscoKnebel)](https://github.com/FranciscoKnebel), [Rafael Trevisan (@raTrevisan)](https://github.com/raTrevisan), [Juliano Araujo Wickboldt (@julianowick)](https://github.com/julianowick)

| Repository | Purpose |
|---|---|
| [dt-client](https://github.com/Open-Digital-Twin/dt-client) | Rust MQTT test client that simulates a device publishing data to a twin instance. |
| [dt-client-bytes](https://github.com/Open-Digital-Twin/dt-client-bytes) | Byte-oriented Rust MQTT client variant for generating test data and exercising the acquisition path. |
| [dt-client-replay](https://github.com/Open-Digital-Twin/dt-client-replay) | Replays timestamped CSV data to an MQTT broker. |
| [dt-instance](https://github.com/Open-Digital-Twin/dt-instance) | Digital Twin instance service for MQTT data acquisition, storage, and processing. |
| [dt-instance-webserver](https://github.com/Open-Digital-Twin/dt-instance-webserver) | Optional REST API for configuring twin-instance elements, data sources, and related settings. |
| [dt-master](https://github.com/Open-Digital-Twin/dt-master) | Central service and API for the earlier Digital Twin architecture, backed by a database. |
| [dt-common](https://github.com/Open-Digital-Twin/dt-common) | Shared Rust modules reused by the earlier Digital Twin services. |
| [dt-sharedconfig](https://github.com/Open-Digital-Twin/dt-sharedconfig) | Shared database initialization and configuration scripts. |

## Federated Learning

| Repository | Purpose | Authors and people involved |
|---|---|---|
| [framework-fl-testing](https://github.com/Open-Digital-Twin/framework-fl-testing) | Python framework for testing Federated Learning algorithms in an edge-like environment, with client/server code, Docker and Kubernetes deployment, and experiment configuration. | [Felipe Machado Schwanck (@fschwanck)](https://github.com/fschwanck), [Juliano Araujo Wickboldt (@julianowick)](https://github.com/julianowick). |
| [article-analyzing-federated-learning-performance-in-distributed-edge-scenarios](https://github.com/Open-Digital-Twin/article-analyzing-federated-learning-performance-in-distributed-edge-scenarios) | Docker Swarm-based client/server experiments for Federated Learning, with container observation, metrics, and plotting utilities. | [@remde](https://github.com/remde), [Juliano Araujo Wickboldt (@julianowick)](https://github.com/julianowick). |
| [ml_data](https://github.com/Open-Digital-Twin/ml_data) | Experiment output and logs grouped by communication-manager and semantic-manager runs and client counts. | [Rafael Trevisan (@raTrevisan)](https://github.com/raTrevisan), [Juliano Araujo Wickboldt (@julianowick)](https://github.com/julianowick). |

## Research, data, and integration tests

| Repository | Purpose | Authors and people involved |
|---|---|---|
| [article-smart-home-use-cases](https://github.com/Open-Digital-Twin/article-smart-home-use-cases) | Proof-of-concept Smart Home Digital Twin study with two use cases and supporting academic materials. | [Laura Corssac (@lauracorssac)](https://github.com/lauracorssac), [Juliano Wickboldt (@julianowick)](https://github.com/julianowick). |
| [article-sdn-nfv-digital-twins](https://github.com/Open-Digital-Twin/article-sdn-nfv-digital-twins) | Portuguese-language research on Digital Twins in programmable networks, combining SDN, NFV, and a literature review. Includes the paper, slides, and research spreadsheet. | [Francisco Paiva Knebel (@FranciscoKnebel)](https://github.com/FranciscoKnebel). Advisors: [Juliano Araujo Wickboldt](https://github.com/julianowick) and [Alberto Egon Schaeffer Filho](https://www.inf.ufrgs.br/~alberto/). |
| [article-test-fog](https://github.com/Open-Digital-Twin/article-test-fog) | Scenarios, scripts, and parsers for testing the Digital Twin architecture in cloud and fog deployments for the “A Cloud-Fog Computing Architecture for Real Time Digital Twins” work. | [Francisco Paiva Knebel (@FranciscoKnebel)](https://github.com/FranciscoKnebel), [Juliano Araujo Wickboldt (@julianowick)](https://github.com/julianowick). |
| [article-test-kafka](https://github.com/Open-Digital-Twin/article-test-kafka) | Experiments with MQTT-to-Kafka data transmission, Kafka processing, and containerized test deployments. | [Andreo Barros](https://www.linkedin.com/in/andreo-barros),  [Juliano Araujo Wickboldt (@julianowick)](https://github.com/julianowick). |
| [article-test-emqx-cluster](https://github.com/Open-Digital-Twin/article-test-emqx-cluster) | Scripts, cluster configurations, and experiment outputs for EMQX cluster tests. | [Rafael Trevisan (@raTrevisan)](https://github.com/raTrevisan),  [Juliano Araujo Wickboldt (@julianowick)](https://github.com/julianowick). |
| [article-test-mqtt-sender](https://github.com/Open-Digital-Twin/article-test-mqtt-sender) | Rust MQTT publisher for generating messages with configurable payload size, count, broker, and QoS. | [Rafael Trevisan (@raTrevisan)](https://github.com/raTrevisan),  [Juliano Araujo Wickboldt (@julianowick)](https://github.com/julianowick). |
| [article-test-mqtt-receiver](https://github.com/Open-Digital-Twin/article-test-mqtt-receiver) | Rust MQTT subscriber used to receive and measure test messages. | [Rafael Trevisan (@raTrevisan)](https://github.com/raTrevisan),  [Juliano Araujo Wickboldt (@julianowick)](https://github.com/julianowick). |
| [test-kafka-emqx-cluster](https://github.com/Open-Digital-Twin/test-kafka-emqx-cluster) | Docker-based Kafka and EMQX integration test setup, with Node.js handlers, connector configurations, and log scripts. | [Francisco Paiva Knebel (@FranciscoKnebel)](https://github.com/FranciscoKnebel),  [Juliano Araujo Wickboldt (@julianowick)](https://github.com/julianowick). |
| [test-kafka-emqx-k8s](https://github.com/Open-Digital-Twin/test-kafka-emqx-k8s) | Kubernetes and Helm test deployment for a Digital Twin MQTT/Kafka setup, with infrastructure and experiment automation. | [Francisco Paiva Knebel (@FranciscoKnebel)](https://github.com/FranciscoKnebel), [Juliano Araujo Wickboldt (@julianowick)](https://github.com/julianowick). |

## Supporting, archived, and upstream repositories

| Repository | Purpose | Authors and people involved |
|---|---|---|
| [pole-service](https://github.com/Open-Digital-Twin/pole-service) (archived) | Archived Smart Cities pole-service prototype. It calculates air-quality metrics and emits events to the parent Neighborhood Twin; the repository also contains a device-service implementation. | [Alexandre Gustavo Wermann (@agwermann)](https://github.com/agwermann), [Juliano Araujo Wickboldt (@julianowick)](https://github.com/julianowick). |
| [device-service](https://github.com/Open-Digital-Twin/device-service) (archived) | Archived Smart Grids device-service prototype that notifies a Neighborhood Twin when a device reports a low battery level. | [Alexandre Gustavo Wermann (@agwermann)](https://github.com/agwermann), [Juliano Araujo Wickboldt (@julianowick)](https://github.com/julianowick). |
| [python-manager](https://github.com/Open-Digital-Twin/python-manager) | Python Kubernetes scaling manager that reads cluster/client metrics and scales according to queue or in-flight message thresholds. | [Rafael Trevisan (@raTrevisan)](https://github.com/raTrevisan),  [Juliano Araujo Wickboldt (@julianowick)](https://github.com/julianowick). |
| [scholar-fetch](https://github.com/Open-Digital-Twin/scholar-fetch) | Experimental Python utility for searching scholarly articles and syncing article records/files with Google Sheets. | [Francisco Paiva Knebel (@FranciscoKnebel)](https://github.com/FranciscoKnebel),  [Juliano Araujo Wickboldt (@julianowick)](https://github.com/julianowick). |
| [kube-prometheus](https://github.com/Open-Digital-Twin/kube-prometheus) | Prometheus Operator fork with Kubernetes monitoring manifests and a cluster branch used to track the installed cluster version. | Upstream project and community: [Prometheus Operator kube-prometheus](https://github.com/prometheus-operator/kube-prometheus). Upstream contributors remain credited by that project. |
| [mosquitto](https://github.com/Open-Digital-Twin/mosquitto) | Eclipse Mosquitto source tree for an MQTT broker and client utilities; its README points to the Eclipse project as the canonical source and issue tracker. | Upstream project: [Eclipse Mosquitto](https://github.com/eclipse-mosquitto/mosquitto). The history includes upstream contributors, local commits by [Francisco Paiva Knebel (@FranciscoKnebel)](https://github.com/FranciscoKnebel). |

## Licensing

Licensing is defined per repository. Check the individual repository's license and upstream notices before reusing code or models.
