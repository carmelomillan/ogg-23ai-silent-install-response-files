# oggcore_rsp

Oracle GoldenGate 23ai – Core Silent Install Response Files (runInstaller)

This directory contains response files used to perform silent installations of the Oracle GoldenGate 23ai core binaries using the Oracle Universal Installer (runInstaller).

Each file corresponds to a specific GoldenGate technology type and defines the minimal required parameters:

INSTALL_OPTION
SOFTWARE_LOCATION
INVENTORY_LOCATION
UNIX_GROUP_NAME

These templates help automate and standardize GoldenGate 23ai installations across multiple platforms and environments.

Included Response Files

| Technology                             | Filename                     | INSTALL_OPTION |
| -------------------------------------- | ---------------------------- | -------------- |
| Oracle Database                        | `oggcore23ai_oracledb.rsp`   | `ORA23ai`      |
| Distributed App & Analytics (Big Data) | `oggcore23ai_bigdata.rsp`    | `Generic`      |
| MySQL                                  | `oggcore23ai_mysql.rsp`      | `MySQL`        |
| PostgreSQL                             | `oggcore23ai_postgresql.rsp` | `PostgreSQL`   |
| Microsoft SQL Server                   | `oggcore23ai_mssql.rsp`      | `MSSQL`        |
| Db2 z/OS                               | `oggcore23ai_db2zos.rsp`     | `DB2ZOS`       |
| Db2 LUW                                | `oggcore23ai_db2luw.rsp`     | `DB2LUW`       |
| Db2 for i (iSeries / AS400)            | `oggcore23ai_db2400.rsp`     | `DB2400`       |
| Teradata                               | `oggcore23ai_teradata.rsp`   | `Teradata`     |
| TimesTen                               | `oggcore23ai_timesten.rsp`   | `TimesTen`     |
| Sybase                                 | `oggcore23ai_sybase.rsp`     | `Sybase`       |

How to Use

Run the Oracle Universal Installer in silent mode:

./runInstaller -silent -nowait -responseFile /path/to/oggcore_rsp/<file>.rsp


Make sure to execute the required root scripts afterwards:

sudo /u01/app/oraInventory/orainstRoot.sh

Directory Structure Convention



You can adapt this structure to match your company standards.

Official Documentation

Oracle GoldenGate 23ai Installation Guide (silent install & response files):
https://docs.oracle.com/en/middleware/goldengate/core/23/coredoc/install-understanding-and-obtaining-oracle-goldengate-distribution.html

Disclaimer

These files are provided as examples and should be reviewed and customized for:

filesystem paths
inventory and user/group settings
security requirements
OS-specific prerequisites
before being used in production environments.

