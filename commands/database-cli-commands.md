# Database CLI

> **Section:** 28  
> **Source** = transcribed from the supplied Word screenshots. **Added** = recommended expansion for a practical engineering command compendium.

> [!CAUTION]
> Commands that modify systems, permissions, storage, firewalls, infrastructure, or data can be destructive. Review targets and test in a safe environment before production use.

| Command / Example | Purpose | Origin | Notes |
|---|---|---|---|
| `psql -h HOST -U USER -d DATABASE` | Connect to PostgreSQL. | Added |  |
| `psql -c "SELECT version();"` | Run a PostgreSQL query from the shell. | Added |  |
| `psql -f script.sql` | Execute SQL from a file. | Added |  |
| `\l` | List PostgreSQL databases inside psql. | Added |  |
| `\dt` | List tables inside psql. | Added |  |
| `\d TABLE` | Describe a PostgreSQL table inside psql. | Added |  |
| `\q` | Quit psql. | Added |  |
| `mysql -h HOST -u USER -p` | Connect to MySQL/MariaDB and prompt for a password. | Added |  |
| `mysql -u USER -p DATABASE < script.sql` | Execute a SQL script in MySQL/MariaDB. | Added |  |
| `SHOW DATABASES;` | List databases inside MySQL/MariaDB. | Added |  |
| `SHOW TABLES;` | List tables in the active database. | Added |  |
| `DESCRIBE TABLE;` | Describe a table. | Added |  |
| `sqlite3 database.db` | Open a SQLite database. | Added |  |
| `.tables` | List tables in sqlite3. | Added |  |
| `.schema TABLE` | Show a table schema in sqlite3. | Added |  |
| `.headers on` | Show column headers in sqlite3 output. | Added |  |
| `.mode column` | Use aligned column output in sqlite3. | Added |  |
| `.quit` | Quit sqlite3. | Added |  |
| `redis-cli ping` | Test a Redis server connection. | Added |  |
| `redis-cli INFO` | Show Redis server information. | Added |  |
| `redis-cli --scan` | Iterate keys using SCAN rather than blocking KEYS *. | Added |  |

## Quick help

```bash
# Most Unix/Linux commands support one or more of these:
COMMAND --help
man COMMAND
info COMMAND
```
