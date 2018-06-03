# UT_COMPOUND_DATA_HELPER



- [Constants](#constants)

- [Variables](#variables)

- [Exceptions](#exceptions)

- [GET_COLUMNS_ROW_FILTER Function](#get_columns_row_filter)



## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
g_user_defined_type | <pre>g_user_defined_type pls_integer := dbms_sql.user_defined_type;</pre> | 
l_res | <pre>  l_res xmltype;</pre> | 
l_data | <pre>  l_data ut_data_value := a_column_details.value;</pre> | 
l_key | <pre>  l_key varchar2(4000) := ut_utils.xmlgen_escaped_string(a_column_details.KEY);</pre> | 
begin | <pre>begin<br />  l_result := '<'||l_key||' xml_valid_name="'||l_key||'">';</pre> | 
else | <pre>  else<br />    l_result := l_result || ut_utils.xmlgen_escaped_string((treat(l_data as ut_data_value_varchar2).data_value));</pre> | 
end | <pre>  end if;</pre> | 
 | <pre>  <br />  l_result := l_result ||'</'||l_key||'>';</pre> | 
return | <pre>  <br />  return xmltype(l_result);</pre> | 
l_source_column | <pre>  l_source_column varchar2(500) := a_table_alias||'.'||a_column_alias;</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_filter;</pre> | 

## Constants<a name="constants"></a>

Name | Code | Description
--- | --- | ---
gc_compare_join_by | <pre>gc_compare_join_by   constant varchar2(10):='join_by';</pre> | 
gc_compare_unordered | <pre>gc_compare_unordered constant varchar2(10):='unordered';</pre> | 
gc_compare_normal | <pre>gc_compare_normal    constant varchar2(10):='normal';</pre> | 

## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
g_user_defined_type | <pre>g_user_defined_type pls_integer := dbms_sql.user_defined_type;</pre> | 
l_res | <pre>  l_res xmltype;</pre> | 
l_data | <pre>  l_data ut_data_value := a_column_details.value;</pre> | 
l_key | <pre>  l_key varchar2(4000) := ut_utils.xmlgen_escaped_string(a_column_details.KEY);</pre> | 
begin | <pre>begin<br />  l_result := '<'||l_key||' xml_valid_name="'||l_key||'">';</pre> | 
else | <pre>  else<br />    l_result := l_result || ut_utils.xmlgen_escaped_string((treat(l_data as ut_data_value_varchar2).data_value));</pre> | 
end | <pre>  end if;</pre> | 
 | <pre>  <br />  l_result := l_result ||'</'||l_key||'>';</pre> | 
return | <pre>  <br />  return xmltype(l_result);</pre> | 
l_source_column | <pre>  l_source_column varchar2(500) := a_table_alias||'.'||a_column_alias;</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_filter;</pre> | 




 
## GET_COLUMNS_ROW_FILTER Function<a name="get_columns_row_filter"></a>


<p>
<p>Current get column filter shaving off ROW tag during extract, this not working well with include and XMLTABLE option<br />so when there is extract we artificially inject removed tag</p>
</p>

### Syntax
```plsql
function get_columns_row_filter(
  a_exclude_xpath varchar2, a_include_xpath varchar2,
  a_table_alias varchar2 := 'ucd', a_column_alias varchar2 := 'item_data'
) return varchar2
```

 





 
