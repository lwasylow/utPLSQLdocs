# UT_COVERAGE_COBERTURA_REPORTER




- [Variables](#variables)

- [Exceptions](#exceptions)




## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
l_coverage_data | <pre>  l_coverage_data ut_coverage.t_coverage;</pre> | 
l_result | <pre>    l_result       clob;</pre> | 
l_line_no | <pre>    l_line_no      binary_integer;</pre> | 
l_pct | <pre>    l_pct          integer;</pre> | 
begin | <pre>  begin<br />    dbms_lob.createtemporary(l_result, true);</pre> | 
 | <pre>    l_line_no := a_unit_coverage.lines.first;</pre> | 
end | <pre>      end loop;</pre> | 
else | <pre>        else<br />          l_file_part := '<line number="'||l_line_no||'" hits="'||a_unit_coverage.lines(l_line_no).executions||'"';</pre> | 
 | <pre>            l_pct := (a_unit_coverage.lines(l_line_no).covered_blocks/a_unit_coverage.lines(l_line_no).no_blocks)*100;</pre> | 
 | <pre>            l_file_part := l_file_part || ' condition-coverage="'||l_pct||'%';</pre> | 
 | <pre>            l_file_part := l_file_part || ' ('||a_unit_coverage.lines(l_line_no).covered_blocks||'/'||a_unit_coverage.lines(l_line_no).no_blocks||')"';</pre> | 
else | <pre>          else<br />            l_file_part := l_file_part || ' branch="false"';</pre> | 
end | <pre>          end if;</pre> | 
 | <pre>          l_file_part := l_file_part ||'/>'||chr(10);</pre> | 
end | <pre>        end if;</pre> | 
 | <pre>        l_line_no := a_unit_coverage.lines.next(l_line_no);</pre> | 
end | <pre>      end loop;</pre> | 
end | <pre>    end if;</pre> | 
return | <pre>    return l_result;</pre> | 
l_result | <pre>    l_result               clob;</pre> | 
l_unit | <pre>    l_unit                 ut_coverage.t_full_name;</pre> | 
l_obj_name | <pre>    l_obj_name             ut_coverage.t_object_name;</pre> | 
c_coverage_def | <pre>    c_coverage_def constant varchar2(200) := '<?xml version="1.0"?>'||CHR(10)||'<!DOCTYPE coverage SYSTEM "http://cobertura.sourceforge.net/xml/coverage-04.dtd">'||chr(10);</pre> | 
c_file_footer | <pre>    c_file_footer     constant varchar2(30) := '</file>'||chr(10);</pre> | 
c_coverage_footer | <pre>    c_coverage_footer constant varchar2(30) := '</coverage>';</pre> | 
c_sources_footer | <pre>    c_sources_footer  constant varchar2(30) := '</sources>'||chr(10);</pre> | 
c_packages_footer | <pre>    c_packages_footer  constant varchar2(30) := '</packages>'||chr(10);</pre> | 
c_package_footer | <pre>    c_package_footer  constant varchar2(30) := '</package>'||chr(10);</pre> | 
c_class_footer | <pre>    c_class_footer  constant varchar2(30) := '</class>'||chr(10);</pre> | 
c_lines_footer | <pre>    c_lines_footer  constant varchar2(30) := '</lines>'||chr(10);</pre> | 
l_epoch | <pre>    l_epoch         varchar2(50) := (sysdate - to_date('01-01-1970 00:00:00', 'dd-mm-yyyy hh24:mi:ss')) * 24 * 60 * 60;</pre> | 
begin | <pre>    begin<br /> <br />    dbms_lob.createtemporary(l_result,true);</pre> | 
 | <pre>    l_unit := a_coverage_data.objects.first;</pre> | 
 | <pre>    l_file_part := '<sources>'||CHR(10);</pre> | 
 | <pre>      l_unit := a_coverage_data.objects.next(l_unit);</pre> | 
end | <pre>    end loop;</pre> | 
 | <pre>    l_unit := a_coverage_data.objects.first;</pre> | 
 | <pre>    l_file_part := '<packages>'||CHR(10);</pre> | 
 | <pre>      l_file_part := '<package name="'||dbms_xmlgen.convert(l_obj_name)||'" line-rate="0.0" branch-rate="0.0" complexity="0.0">'||CHR(10);</pre> | 
 | <pre>      <br />      l_file_part := '<class name="'||dbms_xmlgen.convert(l_obj_name)||'" filename="'||dbms_xmlgen.convert(l_unit)||'" line-rate="0.0" branch-rate="0.0" complexity="0.0">'||CHR(10);</pre> | 
 | <pre>      <br />      l_file_part := '<lines>'||CHR(10);</pre> | 
 | <pre>     <br />      l_unit := a_coverage_data.objects.next(l_unit);</pre> | 
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
l_pct | <pre>    l_pct          integer;</pre> | 
begin | <pre>  begin<br />    dbms_lob.createtemporary(l_result, true);</pre> | 
 | <pre>    l_line_no := a_unit_coverage.lines.first;</pre> | 
end | <pre>      end loop;</pre> | 
else | <pre>        else<br />          l_file_part := '<line number="'||l_line_no||'" hits="'||a_unit_coverage.lines(l_line_no).executions||'"';</pre> | 
 | <pre>            l_pct := (a_unit_coverage.lines(l_line_no).covered_blocks/a_unit_coverage.lines(l_line_no).no_blocks)*100;</pre> | 
 | <pre>            l_file_part := l_file_part || ' condition-coverage="'||l_pct||'%';</pre> | 
 | <pre>            l_file_part := l_file_part || ' ('||a_unit_coverage.lines(l_line_no).covered_blocks||'/'||a_unit_coverage.lines(l_line_no).no_blocks||')"';</pre> | 
else | <pre>          else<br />            l_file_part := l_file_part || ' branch="false"';</pre> | 
end | <pre>          end if;</pre> | 
 | <pre>          l_file_part := l_file_part ||'/>'||chr(10);</pre> | 
end | <pre>        end if;</pre> | 
 | <pre>        l_line_no := a_unit_coverage.lines.next(l_line_no);</pre> | 
end | <pre>      end loop;</pre> | 
end | <pre>    end if;</pre> | 
return | <pre>    return l_result;</pre> | 
l_result | <pre>    l_result               clob;</pre> | 
l_unit | <pre>    l_unit                 ut_coverage.t_full_name;</pre> | 
l_obj_name | <pre>    l_obj_name             ut_coverage.t_object_name;</pre> | 
c_coverage_def | <pre>    c_coverage_def constant varchar2(200) := '<?xml version="1.0"?>'||CHR(10)||'<!DOCTYPE coverage SYSTEM "http://cobertura.sourceforge.net/xml/coverage-04.dtd">'||chr(10);</pre> | 
c_file_footer | <pre>    c_file_footer     constant varchar2(30) := '</file>'||chr(10);</pre> | 
c_coverage_footer | <pre>    c_coverage_footer constant varchar2(30) := '</coverage>';</pre> | 
c_sources_footer | <pre>    c_sources_footer  constant varchar2(30) := '</sources>'||chr(10);</pre> | 
c_packages_footer | <pre>    c_packages_footer  constant varchar2(30) := '</packages>'||chr(10);</pre> | 
c_package_footer | <pre>    c_package_footer  constant varchar2(30) := '</package>'||chr(10);</pre> | 
c_class_footer | <pre>    c_class_footer  constant varchar2(30) := '</class>'||chr(10);</pre> | 
c_lines_footer | <pre>    c_lines_footer  constant varchar2(30) := '</lines>'||chr(10);</pre> | 
l_epoch | <pre>    l_epoch         varchar2(50) := (sysdate - to_date('01-01-1970 00:00:00', 'dd-mm-yyyy hh24:mi:ss')) * 24 * 60 * 60;</pre> | 
begin | <pre>    begin<br /> <br />    dbms_lob.createtemporary(l_result,true);</pre> | 
 | <pre>    l_unit := a_coverage_data.objects.first;</pre> | 
 | <pre>    l_file_part := '<sources>'||CHR(10);</pre> | 
 | <pre>      l_unit := a_coverage_data.objects.next(l_unit);</pre> | 
end | <pre>    end loop;</pre> | 
 | <pre>    l_unit := a_coverage_data.objects.first;</pre> | 
 | <pre>    l_file_part := '<packages>'||CHR(10);</pre> | 
 | <pre>      l_file_part := '<package name="'||dbms_xmlgen.convert(l_obj_name)||'" line-rate="0.0" branch-rate="0.0" complexity="0.0">'||CHR(10);</pre> | 
 | <pre>      <br />      l_file_part := '<class name="'||dbms_xmlgen.convert(l_obj_name)||'" filename="'||dbms_xmlgen.convert(l_unit)||'" line-rate="0.0" branch-rate="0.0" complexity="0.0">'||CHR(10);</pre> | 
 | <pre>      <br />      l_file_part := '<lines>'||CHR(10);</pre> | 
 | <pre>     <br />      l_unit := a_coverage_data.objects.next(l_unit);</pre> | 
end | <pre>    end loop;</pre> | 
return | <pre>    return l_result;</pre> | 
begin | <pre>begin<br />  ut_coverage.coverage_stop();</pre> | 
 | <pre>  l_coverage_data := ut_coverage.get_coverage_data(a_run.coverage_options);</pre> | 




 
