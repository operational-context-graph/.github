# Operational Context Graph

The **Operational Context Graph (OCG)** is the central store of operational knowledge for the [Autonomous Operations Platform](https://github.com/autonomous-operations-platform). It implements the Record principle of the React-Record-Reason architecture: external systems write telemetry, actions, and insights, and the OCG derives and versions a semantic network over that data.

The OCG represents a data center as a graph of entities and relationships, built on seven stores: a semantic network, telemetry, insights, recorded actions, secrets, an audit log, and an infrastructure knowledge base. It applies no business logic, consuming systems make all operational decisions. The OCG stores and versions operational knowledge but never acts on it. All operational decisions are made by the systems that consume it.

---

[Documentation](https://operational-context-graph.dev) · [Contributing](../CONTRIBUTING.md) · [Backlog](https://github.com/operational-context-graph/backlog)

## Additional Resources

> ApeiroRA is the EU-funded reference architecture that Operational Context Graph is built on.

- [Apeiro Reference Architecture](https://apeirora.eu)
- [ApeiroRA Github Organization](https://github.com/apeirora)

<p align="center">
  <img alt="Bundesministerium für Wirtschaft und Energie (BMWE)-EU funding logo" src="https://apeirora.eu/assets/img/BMWK-EU.png" width="400"/>
</p>
