# UT_JUNIT_REPORTER




- [Variables](#variables)

- [Exceptions](#exceptions)




## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
c_cddata_tag_end | <pre>  c_cddata_tag_end   constant varchar2(10) := ']]>';</pre> | 
l_suite_id | <pre>  l_suite_id    integer := 0;</pre> | 
l_output | <pre>    l_output clob;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>        end loop;</pre> | 
end | <pre>      end loop;</pre> | 
end | <pre>    end if;</pre> | 
 | <pre>    l_output := a_test.get_serveroutputs();</pre> | 
else | <pre>    else<br />      self.print_text('<system-out/>');</pre> | 
end | <pre>    end if;</pre> | 
l_suite | <pre>    l_suite       ut_suite;</pre> | 
l_tests | <pre>    l_tests       ut_suite_items := ut_suite_items();</pre> | 
l_data | <pre>    l_data        clob;</pre> | 
l_errors | <pre>    l_errors      ut_varchar2_list;</pre> | 
begin | <pre>  begin<br />    a_suite_id := a_suite_id + 1;</pre> | 
end | <pre>      end if;</pre> | 
end | <pre>    end loop;</pre> | 
end | <pre>    end loop;</pre> | 
 | <pre>      l_data := l_suite.get_serveroutputs();</pre> | 
else | <pre>      else<br />        self.print_text('<system-out/>');</pre> | 
end | <pre>      end if;</pre> | 
 | <pre>      l_errors := l_suite.get_error_stack_traces();</pre> | 
else | <pre>      else<br />        self.print_text('<system-err/>');</pre> | 
end | <pre>      end if;</pre> | 
end | <pre>    end if;</pre> | 
begin | <pre>begin<br />  l_suite_id := 0;</pre> | 
end | <pre>  end loop;</pre> | 



## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
c_cddata_tag_end | <pre>  c_cddata_tag_end   constant varchar2(10) := ']]>';</pre> | 
l_suite_id | <pre>  l_suite_id    integer := 0;</pre> | 
l_output | <pre>    l_output clob;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>        end loop;</pre> | 
end | <pre>      end loop;</pre> | 
end | <pre>    end if;</pre> | 
 | <pre>    l_output := a_test.get_serveroutputs();</pre> | 
else | <pre>    else<br />      self.print_text('<system-out/>');</pre> | 
end | <pre>    end if;</pre> | 
l_suite | <pre>    l_suite       ut_suite;</pre> | 
l_tests | <pre>    l_tests       ut_suite_items := ut_suite_items();</pre> | 
l_data | <pre>    l_data        clob;</pre> | 
l_errors | <pre>    l_errors      ut_varchar2_list;</pre> | 
begin | <pre>  begin<br />    a_suite_id := a_suite_id + 1;</pre> | 
end | <pre>      end if;</pre> | 
end | <pre>    end loop;</pre> | 
end | <pre>    end loop;</pre> | 
 | <pre>      l_data := l_suite.get_serveroutputs();</pre> | 
else | <pre>      else<br />        self.print_text('<system-out/>');</pre> | 
end | <pre>      end if;</pre> | 
 | <pre>      l_errors := l_suite.get_error_stack_traces();</pre> | 
else | <pre>      else<br />        self.print_text('<system-err/>');</pre> | 
end | <pre>      end if;</pre> | 
end | <pre>    end if;</pre> | 
begin | <pre>begin<br />  l_suite_id := 0;</pre> | 
end | <pre>  end loop;</pre> | 




 
