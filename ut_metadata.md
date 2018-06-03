# UT_METADATA


- [Data Types](#types)


- [Variables](#variables)

- [Exceptions](#exceptions)

- [FORM_NAME Function](#form_name)
- [PACKAGE_VALID Function](#package_valid)
- [PROCEDURE_EXISTS Function](#procedure_exists)
- [DO_RESOLVE Procedure](#do_resolve)
- [DO_RESOLVE-1 Procedure](#do_resolve-1)
- [GET_SOURCE_DEFINITION_LINE Function](#get_source_definition_line)
- [RESET_SOURCE_DEFINITION_CACHE Procedure](#reset_source_definition_cache)
- [GET_DBA_VIEW Function](#get_dba_view)
- [PACKAGE_EXISTS_IN_CUR_SCHEMA Function](#package_exists_in_cur_schema)

## Types<a name="types"></a>

Name | Code | Description
--- | --- | ---
t_cache | <pre>type t_cache is table of all_source.text%type;</pre> | 

## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
end | <pre>    end if;</pre> | 
end | <pre>    end if;</pre> | 
return | <pre>    return l_line;</pre> | 
 | <pre>    g_cached_object := null;</pre> | 
l_result | <pre>    l_result              varchar2(128) := lower(a_dba_view_name);</pre> | 
pragma | <pre>    pragma exception_init(l_invalid_object_name,-44002);</pre> | 
begin | <pre>  begin<br />    l_result := dbms_assert.sql_object_name(l_result);</pre> | 
return | <pre>    return l_result;</pre> | 
c_current_schema | <pre>    c_current_schema constant all_tables.owner%type := sys_context('USERENV','CURRENT_SCHEMA');</pre> | 
return | <pre>    return l_cnt > 0;</pre> | 



## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
end | <pre>    end if;</pre> | 
end | <pre>    end if;</pre> | 
return | <pre>    return l_line;</pre> | 
 | <pre>    g_cached_object := null;</pre> | 
l_result | <pre>    l_result              varchar2(128) := lower(a_dba_view_name);</pre> | 
pragma | <pre>    pragma exception_init(l_invalid_object_name,-44002);</pre> | 
begin | <pre>  begin<br />    l_result := dbms_assert.sql_object_name(l_result);</pre> | 
return | <pre>    return l_result;</pre> | 
c_current_schema | <pre>    c_current_schema constant all_tables.owner%type := sys_context('USERENV','CURRENT_SCHEMA');</pre> | 
return | <pre>    return l_cnt > 0;</pre> | 




 
## FORM_NAME Function<a name="form_name"></a>


<p>
<p>Forms correct object/subprogram name to call as owner.object[.subprogram]</p>
</p>

### Syntax
```plsql
function form_name(a_owner_name varchar2, a_object varchar2, a_subprogram varchar2 default null) return varchar2
```

 





 
## PACKAGE_VALID Function<a name="package_valid"></a>


<p>
<p>Check if package exists and is in a VALID state</p>
</p>

### Syntax
```plsql
function package_valid(a_owner_name varchar2, a_package_name in varchar2) return boolean
```

 





 
## PROCEDURE_EXISTS Function<a name="procedure_exists"></a>


<p>
<p>Check if package exists and is VALID and contains the given procedure.</p>
</p>

### Syntax
```plsql
function procedure_exists(a_owner_name varchar2, a_package_name in varchar2, a_procedure_name in varchar2)
  return boolean
```

 





 
## DO_RESOLVE Procedure<a name="do_resolve"></a>


<p>
<p>Resolves [owner.]object using dbms_utility.name_resolve and returns resolved parts</p>
</p>

### Syntax
```plsql
procedure do_resolve(a_owner in out nocopy varchar2, a_object in out nocopy varchar2)
```

 





 
## DO_RESOLVE-1 Procedure<a name="do_resolve-1"></a>


<p>
<p>Resolves [owner.]object[.procedure] using dbms_utility.name_resolve and returns resolved parts</p>
</p>

### Syntax
```plsql
procedure do_resolve(a_owner in out nocopy varchar2, a_object in out nocopy varchar2, a_procedure_name in out nocopy varchar2)
```

 





 
## GET_SOURCE_DEFINITION_LINE Function<a name="get_source_definition_line"></a>


<p>
<p>Return the text of the source line for a given object (body). It excludes package spec and type spec</p>
</p>

### Syntax
```plsql
function get_source_definition_line(a_owner varchar2, a_object_name varchar2, a_line_no integer) return varchar2
```

 





 
## RESET_SOURCE_DEFINITION_CACHE Procedure<a name="reset_source_definition_cache"></a>


<p>
<p>Invalidates package-level cache for source.<br />Caching is used to improve performance of function get_source_definition_line</p>
</p>

### Syntax
```plsql
procedure reset_source_definition_cache
```

 





 
## GET_DBA_VIEW Function<a name="get_dba_view"></a>


<p>
<p>Returns dba_... view name if it is accessible, otherwise it returns all_xxx view</p>
</p>

### Syntax
```plsql
function get_dba_view(a_dba_view_name varchar2) return varchar2
```

### Parameters
Name | Description
--- | ---
`a_dba_view_name` | the name of dba view requested
 
 





 
## PACKAGE_EXISTS_IN_CUR_SCHEMA Function<a name="package_exists_in_cur_schema"></a>


<p>
<p>Returns true if given object is a package and it exists in current schema</p>
</p>

### Syntax
```plsql
function package_exists_in_cur_schema(a_object_name varchar2) return boolean
```

### Parameters
Name | Description
--- | ---
`a_object_name` | the name of the object to be checked
 
 





 
