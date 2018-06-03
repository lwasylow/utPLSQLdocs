# UT_RUNNER






- [TO_UT_OBJECT_LIST Function](#to_ut_object_list)
- [VERSION Function](#version)
- [VERSION_COMPATIBILITY_CHECK Function](#version_compatibility_check)
- [RUN Procedure](#run)
- [REBUILD_ANNOTATION_CACHE Procedure](#rebuild_annotation_cache)
- [PURGE_CACHE Procedure](#purge_cache)
- [GET_UNIT_TEST_INFO Function](#get_unit_test_info)
- [GET_REPORTERS_LIST Function](#get_reporters_list)












 
## TO_UT_OBJECT_LIST Function<a name="to_ut_object_list"></a>


<p>
<p>Private functions</p>
</p>

### Syntax
```plsql
function to_ut_object_list(a_names ut_varchar2_list, a_schema_names ut_varchar2_rows) return ut_object_names
```

 





 
## VERSION Function<a name="version"></a>


<p>
<p>Public functions</p>
</p>

### Syntax
```plsql
function version return varchar2
```

 





 
## VERSION_COMPATIBILITY_CHECK Function<a name="version_compatibility_check"></a>


<p>
<p>Check if version is compatible with another version (by default the current framework version)<br />Version is compatible if:<br />  a_current.major = a_requested.major<br />  a_requested.minor &lt; a_current.minor or a_requested.minor = a_current.minor and a_requested.bugfix &lt;= a_current.bugfix</p>
</p>

### Syntax
```plsql
function version_compatibility_check( a_requested varchar2, a_current varchar2 := null ) return integer
```

### Parameters
Name | Description
--- | ---
`a_requested` | requested utPLSQL version string
`a_current` | current utPLSQL version string, if null is passed, defaults to current framework version
*return* | 1/0         1-true, 0-false
 
 





 
## RUN Procedure<a name="run"></a>


<p>
<p>Execute specified suites/tests by paths</p>
</p>

### Syntax
```plsql
procedure run(
  a_paths ut_varchar2_list, a_reporters ut_reporters, a_color_console boolean := false,
  a_coverage_schemes ut_varchar2_list := null, a_source_file_mappings ut_file_mappings := null, a_test_file_mappings ut_file_mappings := null,
  a_include_objects ut_varchar2_list := null, a_exclude_objects ut_varchar2_list := null, 
  a_fail_on_errors boolean default false
)
```

### Parameters
Name | Description
--- | ---
`a_paths` | list of schemes, packages, procedures or suite-paths to execute
`a_reporters` | list of reporter objects (formats) to use for reporting
`a_color_console` | true/false - should the console format reporters use ANSI color tags
`a_coverage_schemes` | list of database schemes to include in coverage
`a_source_file_mappings` | list of project source files mapped to DB objects that coverage should be reported on
`a_test_file_mappings` | list of project test files mapped to DB objects that test results should be reported on
`a_include_objects` | list of database objects (in format &#39;owner.name&#39;) that coverage should be reported on
`a_exclude_objects` | list of database objects (in format &#39;owner.name&#39;) that coverage should be skipped for
`a_fail_on_errors` | true/false - should an exception be thrown when tests are completed with failures/errors
 
 


### Example
```plsql
Parameter `a_paths` accepts values of the following formats:
  schema - executes all suites in the schema
  schema:suite1[.suite2] - executes all items of suite1 (suite2) in the schema.
                         suite1.suite2 is a suitepath variable
  schema:suite1[.suite2][.test1] - executes test1 in suite suite1.suite2
  schema.suite1 - executes the suite package suite1 in the schema "schema"
                all the parent suites in the hiearcy setups/teardown procedures as also executed
                all chile items are executed
  schema.suite1.test2 - executes test2 procedure of suite1 suite with execution of all parent setup/teardown procedures
```



 
## REBUILD_ANNOTATION_CACHE Procedure<a name="rebuild_annotation_cache"></a>


<p>
<p>Rebuilds annotation cache for a specified schema and object type.<br /> It can be used to speedup execution of utPLSQL on a given schema<br />  if it is executed before initial call made to <code>ut.run</code> or <code>ut_runner.run</code> procedure.</p>
</p>

### Syntax
```plsql
procedure rebuild_annotation_cache(a_object_owner varchar2, a_object_type varchar2 := null)
```

### Parameters
Name | Description
--- | ---
`a_object_owner` | owner of objects to get annotations for
`a_object_type` | optional type of objects to get annotations for (defaults to &#39;PACKAGE&#39;)
 
 





 
## PURGE_CACHE Procedure<a name="purge_cache"></a>


<p>
<p>Removes cached information about annotations for objects of specified type and specified owner</p>
</p>

### Syntax
```plsql
procedure purge_cache(a_object_owner varchar2 := null, a_object_type varchar2 := null)
```

### Parameters
Name | Description
--- | ---
`a_object_owner` | optional - owner of objects to purge annotations for. If null (default) then all schemas are purged
`a_object_type` | optional - type of objects to purge annotations for. If null (default) then cache for all object types is purged
 
 





 
## GET_UNIT_TEST_INFO Function<a name="get_unit_test_info"></a>


<p>
<p>Returns a pipelined collection containing information about unit tests package/packages for a given owner</p>
</p>

### Syntax
```plsql
function get_unit_test_info(a_owner varchar2, a_package_name varchar2 := null) return tt_annotations pipelined
```

### Parameters
Name | Description
--- | ---
`a_owner` | owner of unit tests to retrieve
`a_package_name` | optional name of unit test package to retrieve, if NULLm all unit test packages are returned
*return* | tt_annotations table of records
 
 





 
## GET_REPORTERS_LIST Function<a name="get_reporters_list"></a>


<p>
<p>Returns a list of available reporters. Gives information about whether a reporter is an output reporter or not</p>
</p>

### Syntax
```plsql
function get_reporters_list return tt_reporters_info pipelined
```

### Parameters
Name | Description
--- | ---
*return* | tt_reporters_info
 
 





 
