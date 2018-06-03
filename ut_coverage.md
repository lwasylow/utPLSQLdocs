# UT_COVERAGE



- [Constants](#constants)

- [Variables](#variables)

- [Exceptions](#exceptions)

- [COVERAGE_START Procedure](#coverage_start)
- [MOCK_COVERAGE_ID Procedure](#mock_coverage_id)



## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
g_coverage_id | <pre>g_coverage_id   tt_coverage_id_arr;</pre> | 
g_develop_mode | <pre>g_develop_mode  boolean not null := false;</pre> | 
g_is_started | <pre>g_is_started    boolean not null := false;</pre> | 
l_full_name | <pre>  l_full_name varchar2(100);</pre> | 
l_view_name | <pre>  l_view_name      varchar2(200) := ut_metadata.get_dba_view('dba_source');</pre> | 
else | <pre>  else<br />    l_full_name := 'lower(s.owner||''.''||s.name)';</pre> | 
end | <pre>  end if;</pre> | 
 | <pre>  l_result := l_result ||' from '||l_view_name||q'[ s]';</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 
l_skip_objects | <pre>  l_skip_objects  ut_object_names;</pre> | 
l_sql | <pre>  l_sql           varchar2(32767);</pre> | 
end | <pre>  end if;</pre> | 
 | <pre>  l_sql := a_sql;</pre> | 
else | <pre>  else<br />    open l_cursor for l_sql using a_coverage_options.schema_names, l_skip_objects;</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_cursor;</pre> | 
l_cov_sources_crsr | <pre>  l_cov_sources_crsr sys_refcursor;</pre> | 
l_cov_sources_data | <pre>  l_cov_sources_data ut_coverage_helper.t_coverage_sources_tmp_rows;</pre> | 
 | <pre>    l_cov_sources_crsr := get_cov_sources_cursor(a_coverage_options,a_sql);</pre> | 
loop | <pre>    loop<br />      fetch l_cov_sources_crsr bulk collect into l_cov_sources_data limit 1000;</pre> | 
exit | <pre>      exit when l_cov_sources_crsr%notfound;</pre> | 
end | <pre>    end loop;</pre> | 
close | <pre>    close l_cov_sources_crsr;</pre> | 
end | <pre>  end if;</pre> | 

## Constants<a name="constants"></a>

Name | Code | Description
--- | --- | ---
gc_proftab_coverage | <pre>gc_proftab_coverage    constant varchar2(32) := 'proftab';</pre> | 
gc_block_coverage | <pre>gc_block_coverage      constant varchar2(32) := 'block';</pre> | 
gc_extended_coverage | <pre>gc_extended_coverage   constant varchar2(32) := 'extended';</pre> | 

## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
g_coverage_id | <pre>g_coverage_id   tt_coverage_id_arr;</pre> | 
g_develop_mode | <pre>g_develop_mode  boolean not null := false;</pre> | 
g_is_started | <pre>g_is_started    boolean not null := false;</pre> | 
l_full_name | <pre>  l_full_name varchar2(100);</pre> | 
l_view_name | <pre>  l_view_name      varchar2(200) := ut_metadata.get_dba_view('dba_source');</pre> | 
else | <pre>  else<br />    l_full_name := 'lower(s.owner||''.''||s.name)';</pre> | 
end | <pre>  end if;</pre> | 
 | <pre>  l_result := l_result ||' from '||l_view_name||q'[ s]';</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 
l_skip_objects | <pre>  l_skip_objects  ut_object_names;</pre> | 
l_sql | <pre>  l_sql           varchar2(32767);</pre> | 
end | <pre>  end if;</pre> | 
 | <pre>  l_sql := a_sql;</pre> | 
else | <pre>  else<br />    open l_cursor for l_sql using a_coverage_options.schema_names, l_skip_objects;</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_cursor;</pre> | 
l_cov_sources_crsr | <pre>  l_cov_sources_crsr sys_refcursor;</pre> | 
l_cov_sources_data | <pre>  l_cov_sources_data ut_coverage_helper.t_coverage_sources_tmp_rows;</pre> | 
 | <pre>    l_cov_sources_crsr := get_cov_sources_cursor(a_coverage_options,a_sql);</pre> | 
loop | <pre>    loop<br />      fetch l_cov_sources_crsr bulk collect into l_cov_sources_data limit 1000;</pre> | 
exit | <pre>      exit when l_cov_sources_crsr%notfound;</pre> | 
end | <pre>    end loop;</pre> | 
close | <pre>    close l_cov_sources_crsr;</pre> | 
end | <pre>  end if;</pre> | 




 
## COVERAGE_START Procedure<a name="coverage_start"></a>


<p>
<p>Public functions</p>
</p>

### Syntax
```plsql
procedure coverage_start(a_coverage_options ut_coverage_options default null)
```

 





 
## MOCK_COVERAGE_ID Procedure<a name="mock_coverage_id"></a>


<p>
<p>*<br />Allows overwriting of private global variable g_coverage_id<br />Used internally, only for unit testing of the framework only</p>
</p>

### Syntax
```plsql
procedure mock_coverage_id(a_coverage_id integer,a_coverage_type in varchar2)
```

 





 
