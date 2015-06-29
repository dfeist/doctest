# doctest

![Alt text](http://g.gravizo.com/g?
@startuml
skinparam componentStyle uml2
     [ConnectorRepository] --> ListConnectors
     [ConnectorRepository] --> GetConnectorConfigAttributes
     [ConnectionManager] --> CreateConnection
     [ConnectionManager] --> ValidateConnection
     [ConnectionManager] --> GetConnectorConfigAttributes2B
     [ConnectionManager] --> GetConnectorConfigAttributes3
     [ConnectionManager] --> GetConnectorConfigAttributes4B
     [ConnectionManager] ..> InstantiateConnection : use
     package "MuleRuntime" {
       [ConnectionInstance] --> InstantiateConnection
     }
User -> ConnectorRepository: Authentication Request
@enduml
)
