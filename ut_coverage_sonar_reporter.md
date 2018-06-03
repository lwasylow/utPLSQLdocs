# UT_COVERAGE_SONAR_REPORTER




- [Variables](#variables)

- [Exceptions](#exceptions)




## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
l_coverage_data | <pre>  l_coverage_data ut_coverage.t_coverage;</pre> | 
l_result | <pre>    l_result       clob;</pre> | 
l_line_no | <pre>    l_line_no      binary_integer;</pre> | 
begin | <pre>  begin<br />    dbms_lob.createtemporary(l_result, true);</pre> | 
 | <pre>    l_line_no := a_unit_coverage.lines.first;</pre> | 
end | <pre>      end loop;</pre> | 
else | <pre>        else<br />          l_file_part := '<lineToCover lineNumber="'||l_line_no||'" covered="true"';</pre> | 
 | <pre>            l_file_part := l_file_part || ' coveredBranches="'||a_unit_coverage.lines(l_line_no).covered_blocks||'"';</pre> | 
end | <pre>          end if;</pre> | 
 | <pre>          l_file_part := l_file_part ||'/>'||chr(10);</pre> | 
end | <pre>        end if;</pre> | 
 | <pre>        l_line_no := a_unit_coverage.lines.next(l_line_no);</pre> | 
end | <pre>      end loop;</pre> | 
end | <pre>    end if;</pre> | 
return | <pre>    return l_result;</pre> | 
l_result | <pre>    l_result               clob;</pre> | 
l_unit | <pre>    l_unit                 ut_coverage.t_full_name;</pre> | 
c_coverage_header | <pre>    c_coverage_header constant varchar2(30) := '<coverage version="1">'||chr(10);</pre> | 
c_file_footer | <pre>    c_file_footer     constant varchar2(30) := '</file>'||chr(10);</pre> | 
c_coverage_footer | <pre>    c_coverage_footer constant varchar2(30) := '</coverage>';</pre> | 
begin | <pre>    begin<br />    dbms_lob.createtemporary(l_result,true);</pre> | 
 | <pre>    l_unit := a_coverage_data.objects.first;</pre> | 
 | <pre>      l_unit := a_coverage_data.objects.next(l_unit);</pre> | 
end | <pre>    end loop;</pre> | 
return | <pre>    return l_result;</pre> | 
begin | <pre>begin<br />  ut_coverage.coverage_stop();</pre> | 
 | <pre>  l_coverage_data := ut_coverage.get_coverage_data(a_run.coverage_options);</pre> | 



## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
l_coverage_data | <pre>  l_coverage_data ut_coverage.t_coverage;</pre> | 
l_result | <pre>    l_result       clob;</pre> | 
l_line_no | <pre>    l_line_no      binary_integer;</pre> | 
begin | <pre>  begin<br />    dbms_lob.createtemporary(l_result, true);</pre> | 
 | <pre>    l_line_no := a_unit_coverage.lines.first;</pre> | 
end | <pre>      end loop;</pre> | 
else | <pre>        else<br />          l_file_part := '<lineToCover lineNumber="'||l_line_no||'" covered="true"';</pre> | 
 | <pre>            l_file_part := l_file_part || ' coveredBranches="'||a_unit_coverage.lines(l_line_no).covered_blocks||'"';</pre> | 
end | <pre>          end if;</pre> | 
 | <pre>          l_file_part := l_file_part ||'/>'||chr(10);</pre> | 
end | <pre>        end if;</pre> | 
 | <pre>        l_line_no := a_unit_coverage.lines.next(l_line_no);</pre> | 
end | <pre>      end loop;</pre> | 
end | <pre>    end if;</pre> | 
return | <pre>    return l_result;</pre> | 
l_result | <pre>    l_result               clob;</pre> | 
l_unit | <pre>    l_unit                 ut_coverage.t_full_name;</pre> | 
c_coverage_header | <pre>    c_coverage_header constant varchar2(30) := '<coverage version="1">'||chr(10);</pre> | 
c_file_footer | <pre>    c_file_footer     constant varchar2(30) := '</file>'||chr(10);</pre> | 
c_coverage_footer | <pre>    c_coverage_footer constant varchar2(30) := '</coverage>';</pre> | 
begin | <pre>    begin<br />    dbms_lob.createtemporary(l_result,true);</pre> | 
 | <pre>    l_unit := a_coverage_data.objects.first;</pre> | 
 | <pre>      l_unit := a_coverage_data.objects.next(l_unit);</pre> | 
end | <pre>    end loop;</pre> | 
return | <pre>    return l_result;</pre> | 
begin | <pre>begin<br />  ut_coverage.coverage_stop();</pre> | 
 | <pre>  l_coverage_data := ut_coverage.get_coverage_data(a_run.coverage_options);</pre> | 




 
