# UT_RUN




- [Variables](#variables)

- [Exceptions](#exceptions)




## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
l_coverage_options | <pre>  l_coverage_options ut_coverage_options;</pre> | 
l_exclude_objects | <pre>  l_exclude_objects  ut_object_names;</pre> | 
begin | <pre>begin    <br />  self.run_paths := a_run_paths;</pre> | 
begin | <pre>begin<br />  ut_utils.debug_log('ut_run.execute');</pre> | 
end | <pre>  end loop;</pre> | 
return | <pre>  return l_completed_without_errors;</pre> | 
end | <pre>    end loop;</pre> | 
 | <pre>    l_result := self.results_count.result_status();</pre> | 
else | <pre>  else<br /><br />    l_result := ut_utils.gc_success;</pre> | 
end | <pre>  end if;</pre> | 
end | <pre>  end loop;</pre> | 



## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
l_coverage_options | <pre>  l_coverage_options ut_coverage_options;</pre> | 
l_exclude_objects | <pre>  l_exclude_objects  ut_object_names;</pre> | 
begin | <pre>begin    <br />  self.run_paths := a_run_paths;</pre> | 
begin | <pre>begin<br />  ut_utils.debug_log('ut_run.execute');</pre> | 
end | <pre>  end loop;</pre> | 
return | <pre>  return l_completed_without_errors;</pre> | 
end | <pre>    end loop;</pre> | 
 | <pre>    l_result := self.results_count.result_status();</pre> | 
else | <pre>  else<br /><br />    l_result := ut_utils.gc_success;</pre> | 
end | <pre>  end if;</pre> | 
end | <pre>  end loop;</pre> | 




 
