Telescope-SQL
Overview
Telescope-SQL enables authorized users to query and explore telescope observational data stored in an SQL database. It leverages a structured pipeline of scripts that initialize, shape, and manage data access through a set of pre-defined SQL files.
Repository Contents

README.txt: Original instructions and execution sequence
SQL scripts:
clear.sql – cleans or resets existing data structures
tables.sql – defines the core database schema (tables)
views.sql – creates convenient views or aggregations for querying
user.sql – sets up user roles, permissions, or access controls
inventory.sql – populates data inventory (e.g., instruments, filters, datasets)
order.sql – inserts or organizes observation orders or sequences
morestock.sql – supplements or updates additional data
Example Expanded README (README.md)
# Telescope-SQL

## 1. About  
Telescope-SQL is a lightweight framework of SQL scripts designed to provision, reset, and manage telescope observation data within an SQL database. It streamlines setup by enforcing a clear, repeatable script execution order, helping to maintain consistent data structures and access policies.

## 2. Why Use It?  
- **Orderly Setup**: Scripts are designed to run in a specific sequence for safety and predictability.  
- **Clean Initialization**: `clear.sql` ensures a clean starting state before schema changes.  
- **Layered Approach**: Build foundational tables, then derived views, followed by data and permissions.  
- **Access Control**: `user.sql` enables user provisioning—ideal for environments with restricted access.  
- **Incremental Data Loading**: Support phased or batch data imports (`inventory.sql`, `order.sql`, `morestock.sql`).

## 3. Script Order & Purpose  
| Order | Script           | Description |
|-------|------------------|-------------|
| 1     | `clear.sql`      | Drops or resets existing tables/views—start fresh. |
| 2     | `tables.sql`     | Creates the core tables for storing telescope data. |
| 3     | `views.sql`      | Defines views or calculated fields for easier querying. |
| 4     | `user.sql`       | Creates database users/roles and assigns permissions. |
| 5     | `inventory.sql`  | Populates inventory-type data (like instruments or targets). |
| 6     | `order.sql`      | Loads observational or process ordering data. |
| 7     | `morestock.sql`  | Adds supplementary data updates or extensions. |
