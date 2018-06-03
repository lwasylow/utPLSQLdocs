# UT_FILE_MAPPER


- [Data Types](#types)

- [Constants](#constants)



- [TO_HASH_TABLE Function](#to_hash_table)
- [DEFAULT_FILE_TO_OBJ_TYPE_MAP Function](#default_file_to_obj_type_map)

## Types<a name="types"></a>

Name | Code | Description
--- | --- | ---
tt_key_values | <pre>type tt_key_values is table of varchar2(4000) index by varchar2(4000);</pre> | 



## Constants<a name="constants"></a>

Name | Code | Description
--- | --- | ---
gc_file_mapping_regex | <pre>gc_file_mapping_regex        constant varchar2(100) := '/((\w+)\.)?(\w+)\.(\w{3})$';</pre> | 
gc_regex_owner_subexpression | <pre>gc_regex_owner_subexpression constant positive := 2;</pre> | 
gc_regex_name_subexpression | <pre>gc_regex_name_subexpression  constant positive := 3;</pre> | 
gc_regex_type_subexpression | <pre>gc_regex_type_subexpression  constant positive := 4;</pre> | 






 
## TO_HASH_TABLE Function<a name="to_hash_table"></a>


<p>
<p>Private functions</p>
</p>

### Syntax
```plsql
function to_hash_table(a_key_value_tab ut_key_value_pairs) return tt_key_values
```

 





 
## DEFAULT_FILE_TO_OBJ_TYPE_MAP Function<a name="default_file_to_obj_type_map"></a>


<p>
<p>Public functions</p>
</p>

### Syntax
```plsql
function default_file_to_obj_type_map return ut_key_value_pairs
```

 





 
