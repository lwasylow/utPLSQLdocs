# UT_UTILS


- [Data Types](#types)

- [Constants](#constants)



- [SURROUND_WITH Function](#surround_with)
- [VALIDATE_ROLLBACK_TYPE Procedure](#validate_rollback_type)
- [TEST_RESULT_TO_CHAR Function](#test_result_to_char)
- [GEN_SAVEPOINT_NAME Function](#gen_savepoint_name)
- [STRING_TO_TABLE Function](#string_to_table)
- [CLOB_TO_TABLE Function](#clob_to_table)
- [TIME_DIFF Function](#time_diff)
- [INDENT_LINES Function](#indent_lines)
- [GET_UTPLSQL_OBJECTS_LIST Function](#get_utplsql_objects_list)
- [APPEND_TO_LIST Procedure](#append_to_list)
- [SET_ACTION Procedure](#set_action)
- [SET_CLIENT_INFO Procedure](#set_client_info)
- [TO_VERSION Function](#to_version)
- [SAVE_DBMS_OUTPUT_TO_CACHE Procedure](#save_dbms_output_to_cache)
- [READ_CACHE_TO_DBMS_OUTPUT Procedure](#read_cache_to_dbms_output)
- [UT_OWNER Function](#ut_owner)
- [SCALE_CARDINALITY Function](#scale_cardinality)
- [TO_XML_NUMBER_FORMAT Function](#to_xml_number_format)
- [TRIM_LIST_ELEMENTS Function](#trim_list_elements)
- [FILTER_LIST Function](#filter_list)
- [REPLACE_MULTILINE_COMMENTS Function](#replace_multiline_comments)

## Types<a name="types"></a>

Name | Code | Description
--- | --- | ---
t_event_name | <pre>subtype t_event_name           is varchar2(30);</pre> | 
t_executable_type | <pre>subtype t_executable_type      is varchar2(30);</pre> | 
t_test_result | <pre>subtype t_test_result   is binary_integer range 0 .. 3;</pre> | 
t_rollback_type | <pre>subtype t_rollback_type is binary_integer range 0 .. 1;</pre> | 
t_version | <pre>type t_version is record(<br />  major  natural,<br />  minor  natural,<br />  bugfix natural,<br />  build  natural<br />);</pre> | 
t_clob_tab | <pre>type t_clob_tab is table of clob;</pre> | 



## Constants<a name="constants"></a>

Name | Code | Description
--- | --- | ---
gc_version | <pre>gc_version                 constant varchar2(50) := 'v3.1.2.1964-develop';</pre> | 






 
## SURROUND_WITH Function<a name="surround_with"></a>


<p>
<p>utPLSQL - Version 3<br />  Copyright 2016 - 2017 utPLSQL Project</p><p>  Licensed under the Apache License, Version 2.0 (the &quot;License&quot;):<br />  you may not use this file except in compliance with the License.<br />  You may obtain a copy of the License at</p><pre><code>  http://www.apache.org/licenses/LICENSE-2.0</code></pre><p>  Unless required by applicable law or agreed to in writing, software<br />  distributed under the License is distributed on an &quot;AS IS&quot; BASIS,<br />  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.<br />  See the License for the specific language governing permissions and<br />  limitations under the License.</p>
</p>

### Syntax
```plsql
function surround_with(a_value varchar2, a_quote_char varchar2) return varchar2
```

 





 
## VALIDATE_ROLLBACK_TYPE Procedure<a name="validate_rollback_type"></a>


<p>
<p>Procedure: validate_rollback_type</p><p>   Validates passed value against supported rollback types</p>
</p>

### Syntax
```plsql
procedure validate_rollback_type(a_rollback_type number)
```

 





 
## TEST_RESULT_TO_CHAR Function<a name="test_result_to_char"></a>


<p>
<p>Converts test results into strings</p>
</p>

### Syntax
```plsql
function test_result_to_char(a_test_result integer) return varchar2
```

### Parameters
Name | Description
--- | ---
`a_test_result` | numeric representation of test result
*return* | a string representation of a test_result.
 
 





 
## GEN_SAVEPOINT_NAME Function<a name="gen_savepoint_name"></a>


<p>
<p>Generates a unique name for a savepoint<br />Uses sys_guid, as timestamp gives only miliseconds on Windows and is not unique<br />Issue: #506 for details on the implementation approach</p>
</p>

### Syntax
```plsql
function gen_savepoint_name return varchar2
```

 





 
## STRING_TO_TABLE Function<a name="string_to_table"></a>


<p>
<p>Splits a given string into table of string by delimiter.<br />The delimiter gets removed.<br />If null passed as any of the parameters, empty table is returned.<br />If no occurence of a_delimiter found in a_text then text is returned as a single row of the table.<br />If no text between delimiters found then an empty row is returned, example:<br />  string_to_table( &#39;a,,b&#39;, &#39;,&#39; ) gives table ut_varchar2_list( &#39;a&#39;, null, &#39;b&#39; );</p>
</p>

### Syntax
```plsql
function string_to_table(a_string varchar2, a_delimiter varchar2:= chr(10), a_skip_leading_delimiter varchar2 := 'N') return ut_varchar2_list
```

### Parameters
Name | Description
--- | ---
`a_string` | the text to be split.
`a_delimiter` | the delimiter character or string
`a_skip_leading_delimiter` | determines if the leading delimiter should be ignored, used by clob_to_table
*return* | table of varchar2 values
 
 





 
## CLOB_TO_TABLE Function<a name="clob_to_table"></a>


<p>
<p>Splits a given string into table of string by delimiter.<br />Default value of a_max_amount is 8191 because of code can contains multibyte character.<br />The delimiter gets removed.<br />If null passed as any of the parameters, empty table is returned.<br />If split text is longer than a_max_amount it gets split into pieces of a_max_amount.<br />If no text between delimiters found then an empty row is returned, example:<br />  string_to_table( &#39;a,,b&#39;, &#39;,&#39; ) gives table ut_varchar2_list( &#39;a&#39;, null, &#39;b&#39; );</p>
</p>

### Syntax
```plsql
function clob_to_table(a_clob clob, a_max_amount integer := 8191, a_delimiter varchar2:= chr(10)) return ut_varchar2_list
```

### Parameters
Name | Description
--- | ---
`a_clob` | the text to be split.
`a_delimiter` | the delimiter character or string (default chr(10) )
`a_max_amount` | the maximum length of returned string (default 8191)
*return* | table of varchar2 values
 
 





 
## TIME_DIFF Function<a name="time_diff"></a>


<p>
<p>Returns time difference in seconds (with miliseconds) between given timestamps</p>
</p>

### Syntax
```plsql
function time_diff(a_start_time timestamp with time zone, a_end_time timestamp with time zone) return number
```

 





 
## INDENT_LINES Function<a name="indent_lines"></a>


<p>
<p>Returns a text indented with spaces except the first line.</p>
</p>

### Syntax
```plsql
function indent_lines(a_text varchar2, a_indent_size integer := 4, a_include_first_line boolean := false) return varchar2
```

 





 
## GET_UTPLSQL_OBJECTS_LIST Function<a name="get_utplsql_objects_list"></a>


<p>
<p>Returns a list of object that are part of utPLSQL framework</p>
</p>

### Syntax
```plsql
function get_utplsql_objects_list return ut_object_names
```

 





 
## APPEND_TO_LIST Procedure<a name="append_to_list"></a>


<p>
<p>Append a item to the end of ut_varchar2_list</p>
</p>

### Syntax
```plsql
procedure append_to_list(a_list in out nocopy ut_varchar2_list, a_item varchar2)
```

 





 
## SET_ACTION Procedure<a name="set_action"></a>


<p>
<p>Set session&#39;s action and module using dbms_application_info</p>
</p>

### Syntax
```plsql
procedure set_action(a_text in varchar2)
```

 





 
## SET_CLIENT_INFO Procedure<a name="set_client_info"></a>


<p>
<p>Set session&#39;s client info using dbms_application_info</p>
</p>

### Syntax
```plsql
procedure set_client_info(a_text in varchar2)
```

 





 
## TO_VERSION Function<a name="to_version"></a>


<p>
<p>Converts version string into version record</p>
</p>

### Syntax
```plsql
function to_version(a_version_no varchar2) return t_version
```

### Parameters
Name | Description
--- | ---
`a_version_no` | string representation of version in format vX.X.X.X where X is a positive integer
*return* | t_version    record with up to four positive numbers containing version
 
 



### Thrown exceptions
*throws* 20214 if passed version string is not matching version pattern


 
## SAVE_DBMS_OUTPUT_TO_CACHE Procedure<a name="save_dbms_output_to_cache"></a>


<p>
<p>Saves data from dbms_output buffer into a global temporary table (cache)<br />  used to store dbms_output buffer captured before the run</p>
</p>

### Syntax
```plsql
procedure save_dbms_output_to_cache
```

 





 
## READ_CACHE_TO_DBMS_OUTPUT Procedure<a name="read_cache_to_dbms_output"></a>


<p>
<p>Reads data from global temporary table (cache) abd puts it back into dbms_output<br />  used to recover dbms_output buffer data after a run is complete</p>
</p>

### Syntax
```plsql
procedure read_cache_to_dbms_output
```

 





 
## UT_OWNER Function<a name="ut_owner"></a>


<p>
<p>Function is used to reference to utPLSQL owned objects in dynamic sql statements executed from packages with invoker rights</p>
</p>

### Syntax
```plsql
function ut_owner return varchar2
```

### Parameters
Name | Description
--- | ---
*return* | the name of the utPSQL schema owner
 
 





 
## SCALE_CARDINALITY Function<a name="scale_cardinality"></a>


<p>
<p>Used in dynamic sql select statements to maintain balance between<br />  number of hard-parses and optimiser accurancy for cardinality of collections</p>
</p>

### Syntax
```plsql
function scale_cardinality(a_cardinality natural) return natural
```

### Parameters
Name | Description
--- | ---
*return* | 3, for inputs of: 1-9; 33 for input of 10 - 99; 333 for (100 - 999)
 
 





 
## TO_XML_NUMBER_FORMAT Function<a name="to_xml_number_format"></a>


<p>
<p>Returns number as string. The value is represented as decimal according to XML standard:<br /><a href="https://www.w3.org/TR/xmlschema-2/#decimal">https://www.w3.org/TR/xmlschema-2/#decimal</a></p>
</p>

### Syntax
```plsql
function to_xml_number_format(a_value number) return varchar2
```

 





 
## TRIM_LIST_ELEMENTS Function<a name="trim_list_elements"></a>


<p>
<p>It takes a collection of type ut_varchar2_list and it trims the characters passed as arguments for every element</p>
</p>

### Syntax
```plsql
function trim_list_elements(a_list IN ut_varchar2_list, a_regexp_to_trim in varchar2 default '[:space:]') return ut_varchar2_list
```

 





 
## FILTER_LIST Function<a name="filter_list"></a>


<p>
<p>It takes a collection of type ut_varchar2_list and it only returns the elements which meets the regular expression</p>
</p>

### Syntax
```plsql
function filter_list(a_list IN ut_varchar2_list, a_regexp_filter in varchar2) return ut_varchar2_list
```

 





 
## REPLACE_MULTILINE_COMMENTS Function<a name="replace_multiline_comments"></a>


<p>
<p>Replaces multi-line comments in given source-code with empty lines</p>
</p>

### Syntax
```plsql
function replace_multiline_comments(a_source clob) return clob
```

 





 
