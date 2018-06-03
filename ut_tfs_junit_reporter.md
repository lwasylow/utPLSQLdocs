# UT_TFS_JUNIT_REPORTER




- [Variables](#variables)

- [Exceptions](#exceptions)




## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
l_output | <pre>    l_output clob;</pre> | 
end | <pre>    end loop;</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>end if;</pre> | 
l_suite | <pre>l_suite       ut_suite;</pre> | 
l_outputs | <pre>l_outputs     clob;</pre> | 
l_errors | <pre>l_errors      ut_varchar2_list;</pre> | 
end | <pre>  end if;</pre> | 
end | <pre>end loop;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>  end loop;</pre> | 
 | <pre>  l_suite := treat(a_suite as ut_suite);</pre> | 
 | <pre>  l_outputs := l_suite.get_serveroutputs();</pre> | 
else | <pre>  else <br />    self.print_text('<system-out/>');</pre> | 
end | <pre>  end if;</pre> | 
 | <pre>  l_errors := l_suite.get_error_stack_traces();</pre> | 
else | <pre>  else<br />    self.print_text('<system-err/>');</pre> | 
end | <pre>  end if;</pre> | 
end | <pre>end if;</pre> | 
begin | <pre> <br /><br />  begin<br />    l_suite_id := 0;</pre> | 
end | <pre>    end loop;</pre> | 



## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
l_output | <pre>    l_output clob;</pre> | 
end | <pre>    end loop;</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>end if;</pre> | 
l_suite | <pre>l_suite       ut_suite;</pre> | 
l_outputs | <pre>l_outputs     clob;</pre> | 
l_errors | <pre>l_errors      ut_varchar2_list;</pre> | 
end | <pre>  end if;</pre> | 
end | <pre>end loop;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>  end loop;</pre> | 
 | <pre>  l_suite := treat(a_suite as ut_suite);</pre> | 
 | <pre>  l_outputs := l_suite.get_serveroutputs();</pre> | 
else | <pre>  else <br />    self.print_text('<system-out/>');</pre> | 
end | <pre>  end if;</pre> | 
 | <pre>  l_errors := l_suite.get_error_stack_traces();</pre> | 
else | <pre>  else<br />    self.print_text('<system-err/>');</pre> | 
end | <pre>  end if;</pre> | 
end | <pre>end if;</pre> | 
begin | <pre> <br /><br />  begin<br />    l_suite_id := 0;</pre> | 
end | <pre>    end loop;</pre> | 




 
