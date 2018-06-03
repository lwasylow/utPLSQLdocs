# UT_COVERALLS_REPORTER




- [Variables](#variables)

- [Exceptions](#exceptions)




## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
l_coverage_data | <pre>  l_coverage_data ut_coverage.t_coverage;</pre> | 
l_result | <pre>    l_result          clob;</pre> | 
l_last_line_no | <pre>    l_last_line_no    binary_integer;</pre> | 
c_coverage_header | <pre>    c_coverage_header constant varchar2(30) := '"coverage": [';</pre> | 
c_null | <pre>    c_null            constant varchar2(4) := 'null';</pre> | 
begin | <pre>  begin<br />    dbms_lob.createtemporary(l_result, true);</pre> | 
 | <pre>    l_last_line_no := a_unit_coverage.lines.last;</pre> | 
end | <pre>      end loop;</pre> | 
else | <pre>            else<br />          l_file_part := c_null;</pre> | 
end | <pre>        end if;</pre> | 
end | <pre>        end if;</pre> | 
end | <pre>      end loop;</pre> | 
end | <pre>    end if;</pre> | 
return | <pre>    return l_result;</pre> | 
l_result | <pre>    l_result               clob;</pre> | 
l_unit | <pre>    l_unit                 ut_coverage.t_full_name;</pre> | 
c_coverage_header | <pre>    c_coverage_header constant varchar2(30) := '{"source_files":['||chr(10);</pre> | 
c_coverage_footer | <pre>    c_coverage_footer constant varchar2(30) := ']}'||chr(10)||chr(10)||chr(10)||chr(10)||' ';</pre> | 
begin | <pre>    begin<br />    dbms_lob.createtemporary(l_result,true);</pre> | 
 | <pre>    l_unit := a_coverage_data.objects.first;</pre> | 
 | <pre>      l_unit := a_coverage_data.objects.next(l_unit);</pre> | 
end | <pre>      end if;</pre> | 
end | <pre>    end loop;</pre> | 
return | <pre>    return l_result;</pre> | 
begin | <pre>begin<br />  ut_coverage.coverage_stop();</pre> | 
 | <pre>  l_coverage_data := ut_coverage.get_coverage_data(a_run.coverage_options);</pre> | 



## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
l_coverage_data | <pre>  l_coverage_data ut_coverage.t_coverage;</pre> | 
l_result | <pre>    l_result          clob;</pre> | 
l_last_line_no | <pre>    l_last_line_no    binary_integer;</pre> | 
c_coverage_header | <pre>    c_coverage_header constant varchar2(30) := '"coverage": [';</pre> | 
c_null | <pre>    c_null            constant varchar2(4) := 'null';</pre> | 
begin | <pre>  begin<br />    dbms_lob.createtemporary(l_result, true);</pre> | 
 | <pre>    l_last_line_no := a_unit_coverage.lines.last;</pre> | 
end | <pre>      end loop;</pre> | 
else | <pre>            else<br />          l_file_part := c_null;</pre> | 
end | <pre>        end if;</pre> | 
end | <pre>        end if;</pre> | 
end | <pre>      end loop;</pre> | 
end | <pre>    end if;</pre> | 
return | <pre>    return l_result;</pre> | 
l_result | <pre>    l_result               clob;</pre> | 
l_unit | <pre>    l_unit                 ut_coverage.t_full_name;</pre> | 
c_coverage_header | <pre>    c_coverage_header constant varchar2(30) := '{"source_files":['||chr(10);</pre> | 
c_coverage_footer | <pre>    c_coverage_footer constant varchar2(30) := ']}'||chr(10)||chr(10)||chr(10)||chr(10)||' ';</pre> | 
begin | <pre>    begin<br />    dbms_lob.createtemporary(l_result,true);</pre> | 
 | <pre>    l_unit := a_coverage_data.objects.first;</pre> | 
 | <pre>      l_unit := a_coverage_data.objects.next(l_unit);</pre> | 
end | <pre>      end if;</pre> | 
end | <pre>    end loop;</pre> | 
return | <pre>    return l_result;</pre> | 
begin | <pre>begin<br />  ut_coverage.coverage_stop();</pre> | 
 | <pre>  l_coverage_data := ut_coverage.get_coverage_data(a_run.coverage_options);</pre> | 




 
