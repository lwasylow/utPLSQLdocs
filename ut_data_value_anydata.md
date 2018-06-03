# UT_DATA_VALUE_ANYDATA




- [Variables](#variables)

- [Exceptions](#exceptions)




## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
l_ctx | <pre>  l_ctx      number;</pre> | 
l_ut_owner | <pre>  l_ut_owner varchar2(250) := ut_utils.ut_owner;</pre> | 
begin | <pre>begin<br />  self.data_type  := case when a_value is not null then lower(a_value.gettypename) else 'undefined' end;</pre> | 
l_value | <pre>        l_value anydata := :a_value;</pre> | 
l_status | <pre>        l_status integer;</pre> | 
begin | <pre>      begin<br />        l_status := l_value.get'||a_data_object_type||'(l_data);</pre> | 
else | <pre>  else<br />    self.is_data_null := 1;</pre> | 
end | <pre>  end if;</pre> | 
open | <pre>    open l_query for select a_value val from dual;</pre> | 
 | <pre>    l_ctx := sys.dbms_xmlgen.newcontext( l_query );</pre> | 
end | <pre>  end if;</pre> | 
l_type | <pre>  l_type      anytype;</pre> | 
l_type_code | <pre>  l_type_code integer;</pre> | 
else | <pre>      else<br />        l_result := ut_data_value_collection(a_data_value);</pre> | 
end | <pre>      end if;</pre> | 
else | <pre>    else<br />      raise_application_error(-20000, 'Data type '||a_data_value.gettypename||' in ANYDATA is not supported by utPLSQL');</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 



## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
l_ctx | <pre>  l_ctx      number;</pre> | 
l_ut_owner | <pre>  l_ut_owner varchar2(250) := ut_utils.ut_owner;</pre> | 
begin | <pre>begin<br />  self.data_type  := case when a_value is not null then lower(a_value.gettypename) else 'undefined' end;</pre> | 
l_value | <pre>        l_value anydata := :a_value;</pre> | 
l_status | <pre>        l_status integer;</pre> | 
begin | <pre>      begin<br />        l_status := l_value.get'||a_data_object_type||'(l_data);</pre> | 
else | <pre>  else<br />    self.is_data_null := 1;</pre> | 
end | <pre>  end if;</pre> | 
open | <pre>    open l_query for select a_value val from dual;</pre> | 
 | <pre>    l_ctx := sys.dbms_xmlgen.newcontext( l_query );</pre> | 
end | <pre>  end if;</pre> | 
l_type | <pre>  l_type      anytype;</pre> | 
l_type_code | <pre>  l_type_code integer;</pre> | 
else | <pre>      else<br />        l_result := ut_data_value_collection(a_data_value);</pre> | 
end | <pre>      end if;</pre> | 
else | <pre>    else<br />      raise_application_error(-20000, 'Data type '||a_data_value.gettypename||' in ANYDATA is not supported by utPLSQL');</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 




 
