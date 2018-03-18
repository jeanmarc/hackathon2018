# hackathon2018

## Sandbox details


Neo4j Browser: https://10-0-1-251-33369.neo4jsandbox.com/

Direct Neo4j HTTP: http://34.201.164.142:33369/browser/

Username: neo4j
Password: ***

IP Address: 34.201.164.142
HTTP Port: 33369
Bolt Port: 33368


## connecting with CLI

```
$ neo4j-client -u hackathon -P bolt://34.201.164.142:33368
The authenticity of host '34.201.164.142:33368' could not be established.
TLS certificate fingerprint is 5ac491094964cf61d9f61be39f610468a39fdd845b7b0381e78346a584d6572cac297755e0f27055b0d776d30b9e2bc1c0fd11312344a4e52f9f2385510f20f0.
Would you like to trust this host (NO/yes/once)? yes
Password: 
neo4j-client 1.2.1.
Enter `:help` for usage hints.
Connected to 'neo4j://hackathon@34.201.164.142:33368'
neo4j> MATCH (n1)-[r]->(n2) RETURN r, n1, n2 LIMIT 25                                                                                                                                                                                                                                                                                                                                                                                                                             ;
+----------------------------------------------------------------------------+----------------------------------------------------------------------------+----------------------------------------------------------------------------+
| r                                                                          | n1                                                                         | n2                                                                         |
+----------------------------------------------------------------------------+----------------------------------------------------------------------------+----------------------------------------------------------------------------+
| [:CONTAINS{}]                                                              | (:DataCenter{name:"DC1",location:"Iceland, Rekjavik"})                     | (:Egress:Router{name:"DC1-RE"})                                            |
| [:ROUTES{}]                                                                | (:Egress:Router{name:"DC1-RE"})                                            | (:Interface{ip:"10.0.0.254"})                                              |
| [:CONTAINS{}]                                                              | (:DataCenter{name:"DC1",location:"Iceland, Rekjavik"})                     | (:Rack{name:"DC1-RCK-1-1",zone:1,rack:1})                                  |
| [:HOLDS{}]                                                                 | (:Rack{name:"DC1-RCK-1-1",zone:1,rack:1})                                  | (:Switch{rack:1,ip:"10.1.1"})                                              |
| [:ROUTES{}]                                                                | (:Switch{rack:1,ip:"10.1.1"})                                              | (:Interface{ip:"10.1.1.254"})                                              |
| [:ROUTES{}]                                                                | (:Network:Zone{size:16,zone:1,ip:"10.1"})                                  | (:Interface{ip:"10.1.1.254"})                                              |
| [:CONNECTS{}]                                                              | (:Interface{ip:"10.1.1.196"})                                              | (:Interface{ip:"10.1.1.254"})                                              |
| [:CONNECTS{}]                                                              | (:Interface{ip:"10.1.1.195"})                                              | (:Interface{ip:"10.1.1.254"})                                              |
| [:CONNECTS{}]                                                              | (:Interface{ip:"10.1.1.198"})                                              | (:Interface{ip:"10.1.1.254"})                                              |
| [:CONNECTS{}]                                                              | (:Interface{ip:"10.1.1.197"})                                              | (:Interface{ip:"10.1.1.254"})                                              |
| [:CONNECTS{}]                                                              | (:Interface{ip:"10.1.1.200"})                                              | (:Interface{ip:"10.1.1.254"})                                              |
| [:CONNECTS{}]                                                              | (:Interface{ip:"10.1.1.199"})                                              | (:Interface{ip:"10.1.1.254"})                                              |
| [:CONNECTS{}]                                                              | (:Interface{ip:"10.1.1.179"})                                              | (:Interface{ip:"10.1.1.254"})                                              |
| [:CONNECTS{}]                                                              | (:Interface{ip:"10.1.1.180"})                                              | (:Interface{ip:"10.1.1.254"})                                              |
| [:CONNECTS{}]                                                              | (:Interface{ip:"10.1.1.181"})                                              | (:Interface{ip:"10.1.1.254"})                                              |
| [:CONNECTS{}]                                                              | (:Interface{ip:"10.1.1.182"})                                              | (:Interface{ip:"10.1.1.254"})                                              |
| [:CONNECTS{}]                                                              | (:Interface{ip:"10.1.1.183"})                                              | (:Interface{ip:"10.1.1.254"})                                              |
| [:CONNECTS{}]                                                              | (:Interface{ip:"10.1.1.184"})                                              | (:Interface{ip:"10.1.1.254"})                                              |
| [:CONNECTS{}]                                                              | (:Interface{ip:"10.1.1.185"})                                              | (:Interface{ip:"10.1.1.254"})                                              |
| [:CONNECTS{}]                                                              | (:Interface{ip:"10.1.1.186"})                                              | (:Interface{ip:"10.1.1.254"})                                              |
| [:CONNECTS{}]                                                              | (:Interface{ip:"10.1.1.187"})                                              | (:Interface{ip:"10.1.1.254"})                                              |
| [:CONNECTS{}]                                                              | (:Interface{ip:"10.1.1.188"})                                              | (:Interface{ip:"10.1.1.254"})                                              |
| [:CONNECTS{}]                                                              | (:Interface{ip:"10.1.1.189"})                                              | (:Interface{ip:"10.1.1.254"})                                              |
| [:CONNECTS{}]                                                              | (:Interface{ip:"10.1.1.190"})                                              | (:Interface{ip:"10.1.1.254"})                                              |
| [:CONNECTS{}]                                                              | (:Interface{ip:"10.1.1.191"})                                              | (:Interface{ip:"10.1.1.254"})                                              |
+----------------------------------------------------------------------------+----------------------------------------------------------------------------+----------------------------------------------------------------------------+
neo4j> 
```