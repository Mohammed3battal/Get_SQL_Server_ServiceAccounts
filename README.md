## Script: Get SQL Server Service Accounts

**Description**:
This script lists the Windows service accounts used by SQL Server components running on the current instance. It queries `sys.dm_server_services` to return service name and associated account information.

**Use Case**:
- Validate service accounts before configuring features like Always On, TDE, or Kerberos.
- Perform security audits to ensure least-privilege accounts are being used.
- Quickly identify misconfigured or unexpected service accounts.

**Output Includes**:
- `ServiceName`: Display name of the SQL Server service (e.g., SQL Server, SQL Server Agent)
- `ServiceAccount`: Windows account under which the service runs

**Requirements**:
- SQL Server 2008 R2 or later
- `VIEW SERVER STATE` permission
