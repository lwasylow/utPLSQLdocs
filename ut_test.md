# UT_TEST




- [Variables](#variables)

- [Exceptions](#exceptions)




## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
l_savepoint | <pre>  l_savepoint varchar2(30);</pre> | 
begin | <pre>begin<br /><br />  ut_utils.debug_log('ut_test.execute');</pre> | 
else | <pre>  else<br />    ut_event_manager.trigger_event(ut_utils.gc_before_test, self);</pre> | 
 | <pre>    l_savepoint := self.create_savepoint_if_needed();</pre> | 
 | <pre>    l_no_errors := true;</pre> | 
exit | <pre>      exit when not l_no_errors;</pre> | 
end | <pre>    end loop;</pre> | 
exit | <pre>        exit when not l_no_errors;</pre> | 
end | <pre>      end loop;</pre> | 
end | <pre>      end if;</pre> | 
end | <pre>      end loop;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>    end loop;</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_no_errors;</pre> | 
else | <pre>  else<br />    self.result := ut_utils.gc_error;</pre> | 
end | <pre>  end if;</pre> | 
 | <pre>  l_warnings := coalesce( ut_expectation_processor.get_warnings(), ut_varchar2_list() );</pre> | 
begin | <pre>begin<br />  ut_utils.append_to_list(l_stack_traces, self.parent_error_stack_trace);</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>  end loop;</pre> | 
return | <pre>  return l_stack_traces;</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>  end loop;</pre> | 
return | <pre>  return l_outputs;</pre> | 
before_each_list | <pre>before_each_list ut_executables,;</pre> | 
before_test_list | <pre>before_test_list ut_executables,;</pre> | 
item | <pre>item        ut_executable_test,;</pre> | 
after_test_list | <pre>after_test_list  ut_executables,;</pre> | 
after_each_list | <pre>after_each_list ut_executables,;</pre> | 
all_expectations | <pre>all_expectations    ut_expectation_results,;</pre> | 
failed_expectations | <pre>failed_expectations ut_expectation_results,;</pre> | 
parent_error_stack_trace | <pre>parent_error_stack_trace varchar2(4000),;</pre> | 



## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
l_savepoint | <pre>  l_savepoint varchar2(30);</pre> | 
begin | <pre>begin<br /><br />  ut_utils.debug_log('ut_test.execute');</pre> | 
else | <pre>  else<br />    ut_event_manager.trigger_event(ut_utils.gc_before_test, self);</pre> | 
 | <pre>    l_savepoint := self.create_savepoint_if_needed();</pre> | 
 | <pre>    l_no_errors := true;</pre> | 
exit | <pre>      exit when not l_no_errors;</pre> | 
end | <pre>    end loop;</pre> | 
exit | <pre>        exit when not l_no_errors;</pre> | 
end | <pre>      end loop;</pre> | 
end | <pre>      end if;</pre> | 
end | <pre>      end loop;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>    end loop;</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_no_errors;</pre> | 
else | <pre>  else<br />    self.result := ut_utils.gc_error;</pre> | 
end | <pre>  end if;</pre> | 
 | <pre>  l_warnings := coalesce( ut_expectation_processor.get_warnings(), ut_varchar2_list() );</pre> | 
begin | <pre>begin<br />  ut_utils.append_to_list(l_stack_traces, self.parent_error_stack_trace);</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>  end loop;</pre> | 
return | <pre>  return l_stack_traces;</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>  end loop;</pre> | 
return | <pre>  return l_outputs;</pre> | 
before_each_list | <pre>before_each_list ut_executables,;</pre> | 
before_test_list | <pre>before_test_list ut_executables,;</pre> | 
item | <pre>item        ut_executable_test,;</pre> | 
after_test_list | <pre>after_test_list  ut_executables,;</pre> | 
after_each_list | <pre>after_each_list ut_executables,;</pre> | 
all_expectations | <pre>all_expectations    ut_expectation_results,;</pre> | 
failed_expectations | <pre>failed_expectations ut_expectation_results,;</pre> | 
parent_error_stack_trace | <pre>parent_error_stack_trace varchar2(4000),;</pre> | 




 
