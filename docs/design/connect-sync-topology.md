# Microsoft Entra Connect Sync – Deployment Topology

## 1. Architecture Decision

Goodgrove Bank will use an Active-Passive Microsoft Entra Connect Sync deployment.

The design consists of:

- One active Microsoft Entra Connect Sync server.
- One standby Microsoft Entra Connect Sync server in staging mode.
- One Active Directory forest containing three domains.
- One Microsoft Entra ID tenant.

## 2. Primary Sync Server

The primary server will:

- Connect to all three Active Directory domains.
- Import and synchronise directory objects.
- Export synchronised identity changes to Microsoft Entra ID.
- Perform Password Hash Synchronisation.

## 3. Standby Sync Server

The standby server will:

- Connect to all three Active Directory domains.
- Run in staging mode.
- Import and synchronise directory objects.
- Maintain an up-to-date synchronisation state.
- Remain ready for controlled failover.

While in staging mode, it will not perform exports or Password Hash Synchronisation.

## 4. High Availability

Only one server will operate in active mode at a time.

During a failure:

1. Investigate the primary server failure.
2. Ensure the primary server cannot resume exporting unexpectedly.
3. Verify the standby server configuration and synchronisation state.
4. Review pending exports.
5. Disable staging mode on the standby server.
6. Confirm that synchronisation and exports are operating correctly.

## 5. Configuration Management

Changes made to the primary server's synchronisation configuration must also be applied to the standby server.

Both servers must maintain consistent configuration and synchronisation scope.

## 6. Design Assumptions and Validation

The design assumes:

- All three domains are reachable from both sync servers.
- Appropriate Active Directory permissions are available.
- Both servers can communicate with Microsoft Entra ID.
- The standby server is monitored and regularly synchronised.
- Failover procedures are documented and tested.

These assumptions must be validated during implementation.

## 7. Microsoft Documentation

- https://learn.microsoft.com/en-us/entra/identity/hybrid/connect/plan-connect-topologies
- https://learn.microsoft.com/en-us/entra/identity/hybrid/connect/how-to-connect-sync-staging-server

## 8. Decision Status

Proposed architecture decision.

Production deployment and failover testing have not yet been performed.
