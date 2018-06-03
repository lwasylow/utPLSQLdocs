# UT_SUITE_MANAGER


- [Data Types](#types)




- [GET_SCHEMA_UT_PACKAGES Function](#get_schema_ut_packages)
- [CONFIGURE_EXECUTION_BY_PATH Function](#configure_execution_by_path)
- [GET_SCHEMA_NAMES Function](#get_schema_names)

## Types<a name="types"></a>

Name | Code | Description
--- | --- | ---
tt_schema_suites | <pre>subtype tt_schema_suites is ut_suite_builder.tt_schema_suites;</pre> | 
t_object_suite_path | <pre>subtype t_object_suite_path is ut_suite_builder.t_object_suite_path;</pre> | 
t_schema_suites_info | <pre>subtype t_schema_suites_info is ut_suite_builder.t_schema_suites_info;</pre> | 
t_schema_info | <pre>type t_schema_info is record (changed_at date, obj_cnt integer);</pre> | 
t_schema_cache | <pre>type t_schema_cache is record(<br />   schema_suites tt_schema_suites<br />  ,changed_at    date<br />  ,obj_cnt       integer<br />  ,suite_paths   t_object_suite_path<br />);</pre> | 
tt_schema_suites_list | <pre>type tt_schema_suites_list is table of t_schema_cache index by varchar2(128 char);</pre> | 
t_schema_paths | <pre>type t_schema_paths is table of ut_varchar2_list index by varchar2(4000 char);</pre> | 










 
## CONFIGURE_EXECUTION_BY_PATH Function<a name="configure_execution_by_path"></a>


<p>
<p>Builds a hierarchical suites based on given suite-paths</p>
</p>

### Syntax
```plsql
function configure_execution_by_path(a_paths in ut_varchar2_list) return ut_suite_items
```

### Parameters
Name | Description
--- | ---
`a_paths` | list of suite-paths or procedure names or package names or schema names
*return* | array containing root suites-ready to be executed
 
 





 
## GET_SCHEMA_NAMES Function<a name="get_schema_names"></a>


<p>
<p>Cleanup paths by removing leading/trailing whitespace and making paths lowercase<br />Get list of schema names from execution paths.</p>
</p>

### Syntax
```plsql
function get_schema_names(a_paths ut_varchar2_list) return ut_varchar2_rows
```

 





 
