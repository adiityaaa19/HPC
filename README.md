# Translation Memory Commands

---

| Function                | Description                               |
|------------------------|-------------------------------------------|
| `list_memories`       | List saved translation memories           |
| `create_memory`       | Create a new translation memory           |
| `update_memory`       | Update a memory’s name                    |
| `delete_memory`       | Delete a translation memory               |
| `add_translation`     | Add a translation unit to a memory        |
| `delete_translation`  | Remove a translation unit from a memory   |
| `import_tmx`          | Import a TMX file into a memory           |
| `check_import_status` | Check TMX import status                   |

---









## SQL MCP Server 1.2.0
| 🟢 Tools (32) | <span style="opacity:0.6">🔴 Prompts</span> | <span style="opacity:0.6">🔴 Resources</span> | <span style="opacity:0.6">🔴 Logging</span> | <span style="opacity:0.6">🔴 Experimental</span> |
| --- | --- | --- | --- | --- |
## 🛠️ Tools (32)

<table style="text-align: left;">
<thead>
    <tr>
        <th style="width: auto;"></th>
        <th style="width: auto;">Tool Name</th>
        <th style="width: auto;">Description</th>
        <th style="width: auto;">Inputs</th>
    </tr>
</thead>
<tbody style="vertical-align: top;">
        <tr>
            <td>1.</td>
            <td>
                <code><b>alterTable</b></code>
            </td>
            <td>Alter an existing table structure</td>
            <td>
                <ul>
                    <li> <code>operations</code> : {column : {check : string, default : string, name : string, nullable : boolean, type : string}, type : ADD_COLUMN} | {columnName : string, type : DROP_COLUMN} | {columnName : string, newType : string, nullable : boolean, type : ALTER_COLUMN} | {constraint : {columns : string [ ], name : string, type : PRIMARY_KEY} | {columns : string [ ], name : string, type : UNIQUE} | {columns : string [ ], name : string, onDelete : NO ACTION|CASCADE|SET NULL|SET DEFAULT, onUpdate : NO ACTION|CASCADE|SET NULL|SET DEFAULT, referencedColumns : string [ ], referencedTable : string, type : FOREIGN_KEY} | {expression : string, name : string, type : CHECK} | {columnName : string, expression : string, type : DEFAULT}, type : ADD_CONSTRAINT} | {constraintName : string, type : DROP_CONSTRAINT} [ ]<br /></li>
                    <li> <code>table</code> : string<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>2.</td>
            <td>
                <code><b>beginTransaction</b></code>
            </td>
            <td>Begin a new transaction and return a transaction ID</td>
            <td>
                <ul>
                    <li> <code>isolationLevel</code> : READ_UNCOMMITTED|READ_COMMITTED|REPEATABLE_READ|SERIALIZABLE|SNAPSHOT<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>3.</td>
            <td>
                <code><b>bulkDelete</b></code>
            </td>
            <td>Delete multiple rows efficiently</td>
            <td>
                <ul>
                    <li> <code>batchSize</code> : number<br /></li>
                    <li> <code>keys</code> : unknown<br /></li>
                    <li> <code>table</code> : string<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>4.</td>
            <td>
                <code><b>bulkInsert</b></code>
            </td>
            <td>Insert multiple rows efficiently</td>
            <td>
                <ul>
                    <li> <code>batchSize</code> : number<br /></li>
                    <li> <code>returnInserted</code> : boolean<br /></li>
                    <li> <code>rows</code> : unknown<br /></li>
                    <li> <code>table</code> : string<br /></li>
                    <li> <code>validateSchema</code> : boolean<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>5.</td>
            <td>
                <code><b>bulkUpdate</b></code>
            </td>
            <td>Update multiple rows efficiently</td>
            <td>
                <ul>
                    <li> <code>batchSize</code> : number<br /></li>
                    <li> <code>table</code> : string<br /></li>
                    <li> <code>updates</code> : unknown<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>6.</td>
            <td>
                <code><b>bulkUpsert</b></code>
            </td>
            <td>Insert or update multiple rows using MERGE</td>
            <td>
                <ul>
                    <li> <code>batchSize</code> : number<br /></li>
                    <li> <code>keyColumns</code> : string [ ]<br /></li>
                    <li> <code>rows</code> : unknown<br /></li>
                    <li> <code>table</code> : string<br /></li>
                    <li> <code>updateColumns</code> : string [ ]<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>7.</td>
            <td>
                <code><b>commitTransaction</b></code>
            </td>
            <td>Commit an active transaction</td>
            <td>
                <ul>
                    <li> <code>transactionId</code> : string<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>8.</td>
            <td>
                <code><b>createIndex</b></code>
            </td>
            <td>Create an index on a table</td>
            <td>
                <ul>
                    <li> <code>clustered</code> : boolean<br /></li>
                    <li> <code>columns</code> : {direction : ASC|DESC, name : string} [ ]<br /></li>
                    <li> <code>fillFactor</code> : number<br /></li>
                    <li> <code>include</code> : string [ ]<br /></li>
                    <li> <code>indexName</code> : string<br /></li>
                    <li> <code>online</code> : boolean<br /></li>
                    <li> <code>table</code> : string<br /></li>
                    <li> <code>unique</code> : boolean<br /></li>
                    <li> <code>where</code> : string<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>9.</td>
            <td>
                <code><b>createRow</b></code>
            </td>
            <td>Create a new row</td>
            <td>
                <ul>
                    <li> <code>row</code> : unknown<br /></li>
                    <li> <code>table</code> : string<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>10.</td>
            <td>
                <code><b>createTable</b></code>
            </td>
            <td>Create a new table with columns and constraints</td>
            <td>
                <ul>
                    <li> <code>columns</code> : {check : string, computed : string, default : string, identity : {increment : number, seed : number}, name : string, nullable : boolean, primaryKey : boolean, references : {column : string, onDelete : NO ACTION|CASCADE|SET NULL|SET DEFAULT, onUpdate : NO ACTION|CASCADE|SET NULL|SET DEFAULT, table : string}, type : string, unique : boolean} [ ]<br /></li>
                    <li> <code>constraints</code> : {checks : {expression : string, name : string} [ ], foreignKeys : {columns : string [ ], name : string, onDelete : NO ACTION|CASCADE|SET NULL|SET DEFAULT, onUpdate : NO ACTION|CASCADE|SET NULL|SET DEFAULT, referencedColumns : string [ ], referencedTable : string} [ ], primaryKey : {columns : string [ ], name : string}, uniqueKeys : {columns : string [ ], name : string} [ ]}<br /></li>
                    <li> <code>table</code> : string<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>11.</td>
            <td>
                <code><b>deleteRow</b></code>
            </td>
            <td>Delete a row</td>
            <td>
                <ul>
                    <li> <code>key</code> : unknown<br /></li>
                    <li> <code>table</code> : string<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>12.</td>
            <td>
                <code><b>dropIndex</b></code>
            </td>
            <td>Drop an index from a table</td>
            <td>
                <ul>
                    <li> <code>ifExists</code> : boolean<br /></li>
                    <li> <code>indexName</code> : string<br /></li>
                    <li> <code>table</code> : string<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>13.</td>
            <td>
                <code><b>dropTable</b></code>
            </td>
            <td>Drop an existing table</td>
            <td>
                <ul>
                    <li> <code>ifExists</code> : boolean<br /></li>
                    <li> <code>table</code> : string<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>14.</td>
            <td>
                <code><b>executeQuery</b></code>
            </td>
            <td>Execute a custom SQL query with optional parameters</td>
            <td>
                <ul>
                    <li> <code>parameters</code> : unknown<br /></li>
                    <li> <code>query</code> : string<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>15.</td>
            <td>
                <code><b>executeSqlBatch</b></code>
            </td>
            <td>Execute multiple SQL statements in sequence, optionally wrapped in a transaction</td>
            <td>
                <ul>
                    <li> <code>isolationLevel</code> : READ_UNCOMMITTED|READ_COMMITTED|REPEATABLE_READ|SERIALIZABLE|SNAPSHOT<br /></li>
                    <li> <code>statements</code> : unknown<br /></li>
                    <li> <code>stopOnError</code> : boolean<br /></li>
                    <li> <code>useTransaction</code> : boolean<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>16.</td>
            <td>
                <code><b>executeStoredProcedure</b></code>
            </td>
            <td>Execute a stored procedure with parameters</td>
            <td>
                <ul>
                    <li> <code>outputParameters</code> : {name : string, size : number, type : varchar|nvarchar|int|bigint|decimal|float|bit|date|datetime|uniqueidentifier} [ ]<br /></li>
                    <li> <code>parameters</code> : unknown<br /></li>
                    <li> <code>procedure</code> : string<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>17.</td>
            <td>
                <code><b>executeTransaction</b></code>
            </td>
            <td>Execute multiple operations in a transaction</td>
            <td>
                <ul>
                    <li> <code>isolationLevel</code> : READ_UNCOMMITTED|READ_COMMITTED|REPEATABLE_READ|SERIALIZABLE|SNAPSHOT<br /></li>
                    <li> <code>operations</code> : unknown<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>18.</td>
            <td>
                <code><b>getStoredProcedureInfo</b></code>
            </td>
            <td>Get detailed information about a stored procedure including parameters</td>
            <td>
                <ul>
                    <li> <code>procedure</code> : string<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>19.</td>
            <td>
                <code><b>getTableSchema</b></code>
            </td>
            <td>Get detailed schema/structure information for a specific table</td>
            <td>
                <ul>
                    <li> <code>table</code> : string<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>20.</td>
            <td>
                <code><b>listConstraints</b></code>
            </td>
            <td>List all constraints for a table or schema</td>
            <td>
                <ul>
                    <li> <code>schema</code> : string<br /></li>
                    <li> <code>table</code> : string<br /></li>
                    <li> <code>type</code> : PRIMARY KEY|FOREIGN KEY|CHECK|UNIQUE|DEFAULT|ALL<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>21.</td>
            <td>
                <code><b>listFunctions</b></code>
            </td>
            <td>List all user-defined functions in the database</td>
            <td>
                <ul>
                    <li> <code>pattern</code> : string<br /></li>
                    <li> <code>schema</code> : string<br /></li>
                    <li> <code>type</code> : SCALAR|TABLE|ALL<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>22.</td>
            <td>
                <code><b>listIndexes</b></code>
            </td>
            <td>List all indexes for a specific table</td>
            <td>
                <ul>
                    <li> <code>includeColumns</code> : boolean<br /></li>
                    <li> <code>table</code> : string<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>23.</td>
            <td>
                <code><b>listSchemas</b></code>
            </td>
            <td>Lists all available schemas in the database</td>
            <td>
                <ul>
                </ul>
            </td>
        </tr>
        <tr>
            <td>24.</td>
            <td>
                <code><b>listStoredProcedures</b></code>
            </td>
            <td>List available stored procedures</td>
            <td>
                <ul>
                    <li> <code>pattern</code> : string<br /></li>
                    <li> <code>schema</code> : string<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>25.</td>
            <td>
                <code><b>listTables</b></code>
            </td>
            <td>List all tables in the database with metadata</td>
            <td>
                <ul>
                    <li> <code>pattern</code> : string<br /></li>
                    <li> <code>schema</code> : string<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>26.</td>
            <td>
                <code><b>listTriggers</b></code>
            </td>
            <td>List all triggers in the database</td>
            <td>
                <ul>
                    <li> <code>pattern</code> : string<br /></li>
                    <li> <code>schema</code> : string<br /></li>
                    <li> <code>table</code> : string<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>27.</td>
            <td>
                <code><b>listViews</b></code>
            </td>
            <td>List all views in the database</td>
            <td>
                <ul>
                    <li> <code>pattern</code> : string<br /></li>
                    <li> <code>schema</code> : string<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>28.</td>
            <td>
                <code><b>queryBuilder</b></code>
            </td>
            <td>Build and execute complex SQL queries</td>
            <td>
                <ul>
                    <li> <code>from</code> : string | {alias : string, table : string}<br /></li>
                    <li> <code>groupBy</code> : string [ ]<br /></li>
                    <li> <code>having</code> : string<br /></li>
                    <li> <code>joins</code> : {on : string | {left : string, right : string}, table : string, type : INNER|LEFT|RIGHT|FULL} [ ]<br /></li>
                    <li> <code>limit</code> : number<br /></li>
                    <li> <code>offset</code> : number<br /></li>
                    <li> <code>orderBy</code> : {column : string, direction : ASC|DESC} [ ]<br /></li>
                    <li> <code>select</code> : string [ ] | *<br /></li>
                    <li> <code>where</code> : unknown<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>29.</td>
            <td>
                <code><b>readRows</b></code>
            </td>
            <td>Read rows from a table</td>
            <td>
                <ul>
                    <li> <code>filter</code> : unknown<br /></li>
                    <li> <code>limit</code> : number<br /></li>
                    <li> <code>table</code> : string<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>30.</td>
            <td>
                <code><b>readSchema</b></code>
            </td>
            <td>Read Schema Information</td>
            <td>
                <ul>
                    <li> <code>schema</code> : string<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>31.</td>
            <td>
                <code><b>rollbackTransaction</b></code>
            </td>
            <td>Rollback an active transaction</td>
            <td>
                <ul>
                    <li> <code>transactionId</code> : string<br /></li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>32.</td>
            <td>
                <code><b>updateRow</b></code>
            </td>
            <td>Update an existing row</td>
            <td>
                <ul>
                    <li> <code>changes</code> : unknown<br /></li>
                    <li> <code>key</code> : unknown<br /></li>
                    <li> <code>table</code> : string<br /></li>
                </ul>
            </td>
        </tr>
</tbody>
</table>




<sup>◾ generated by [mcp-discovery](https://github.com/rust-mcp-stack/mcp-discovery)</sup>

