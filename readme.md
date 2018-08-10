dynamic event reproducer
=======================

Subprocess start event
----------------------

event for all child of 110 does not work:

	curl -u donato:donato -X POST "http://localhost:8080/kie-server/services/rest/server/containers/dynamic-signal-reproducer_1.0.0/processes/instances/signal/stopChild:110" -H "accept: application/xml" -H "content-type: application/json" -d "{}"

event for a specific child of 110 works:

	curl -u donato:donato -X POST "http://localhost:8080/kie-server/services/rest/server/containers/dynamic-signal-reproducer_1.0.0/processes/instances/signal/stopChild:110?instanceId=113" -H "accept: application/xml" -H "content-type: application/json" -d "{}"

Intermediate catching event
---------------------------

event for all child of 114 works:

	curl -u donato:donato -X POST "http://localhost:8080/kie-server/services/rest/server/containers/dynamic-signal-reproducer_1.0.0/processes/instances/signal/contChild:114" -H "accept: application/xml" -H "content-type: application/json" -d "{}"


