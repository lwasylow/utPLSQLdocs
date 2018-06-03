# UT_SUITE




- [Variables](#variables)

- [Exceptions](#exceptions)




## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
 | <pre>  before_all_list := ut_executables();</pre> | 
 | <pre>  after_all_list  := ut_executables();</pre> | 
l_no_errors | <pre>  l_no_errors boolean;</pre> | 
end | <pre>    end loop;</pre> | 
begin | <pre>begin<br />  ut_utils.debug_log('ut_suite.execute');</pre> | 
else | <pre>  else<br />    ut_event_manager.trigger_event(ut_utils.gc_before_suite, self);</pre> | 
 | <pre>    l_suite_savepoint := self.create_savepoint_if_needed();</pre> | 
 | <pre>    l_no_errors := true;</pre> | 
end | <pre>      end if;</pre> | 
end | <pre>    end loop;</pre> | 
end | <pre>      end loop;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>      end if;</pre> | 
end | <pre>    end loop;</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_no_errors;</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>  end loop;</pre> | 
return | <pre>  return l_stack_traces;</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>  end loop;</pre> | 
return | <pre>  return l_outputs;</pre> | 
before_all_list | <pre>before_all_list ut_executables,;</pre> | 



## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
 | <pre>  before_all_list := ut_executables();</pre> | 
 | <pre>  after_all_list  := ut_executables();</pre> | 
l_no_errors | <pre>  l_no_errors boolean;</pre> | 
end | <pre>    end loop;</pre> | 
begin | <pre>begin<br />  ut_utils.debug_log('ut_suite.execute');</pre> | 
else | <pre>  else<br />    ut_event_manager.trigger_event(ut_utils.gc_before_suite, self);</pre> | 
 | <pre>    l_suite_savepoint := self.create_savepoint_if_needed();</pre> | 
 | <pre>    l_no_errors := true;</pre> | 
end | <pre>      end if;</pre> | 
end | <pre>    end loop;</pre> | 
end | <pre>      end loop;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>      end if;</pre> | 
end | <pre>    end loop;</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_no_errors;</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>  end loop;</pre> | 
return | <pre>  return l_stack_traces;</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>  end loop;</pre> | 
return | <pre>  return l_outputs;</pre> | 
before_all_list | <pre>before_all_list ut_executables,;</pre> | 




 
