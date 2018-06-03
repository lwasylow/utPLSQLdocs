# UT_EQUAL




- [Variables](#variables)

- [Exceptions](#exceptions)




## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
 | <pre>  return ( a_assert_result or ( self.expected.is_null() and a_actual.is_null() and ut_utils.int_to_boolean( nulls_are_equal_flag ) ) );</pre> | 
 | <pre>  exclude_list := ut_varchar2_list(a_exclude);</pre> | 
 | <pre>  exclude_list := coalesce(a_exclude, ut_varchar2_list());</pre> | 
 | <pre>  exclude_list := ut_varchar2_list(a_exclude);</pre> | 
 | <pre>  exclude_list := coalesce(a_exclude, ut_varchar2_list());</pre> | 
begin | <pre>begin<br />  ut_utils.append_to_list(l_result.include_list, a_items);</pre> | 
return | <pre>  return l_result;</pre> | 
begin | <pre>begin<br />  l_result.include_list := l_result.include_list multiset union all coalesce(a_items,ut_varchar2_list());</pre> | 
return | <pre>  return l_result;</pre> | 
begin | <pre>begin<br />  ut_utils.append_to_list(l_result.exclude_list, a_items);</pre> | 
return | <pre>  return l_result;</pre> | 
begin | <pre>begin<br />  l_result.exclude_list := l_result.exclude_list multiset union all coalesce(a_items,ut_varchar2_list());</pre> | 
return | <pre>  return l_result;</pre> | 
begin | <pre>begin<br />  l_result.is_unordered := ut_utils.boolean_to_int(true);</pre> | 
return | <pre>  return l_result;</pre> | 
begin | <pre>begin<br />  l_result.is_unordered := ut_utils.boolean_to_int(true);</pre> | 
return | <pre>  return l_result;</pre> | 
begin | <pre>begin<br />  l_result.is_unordered := ut_utils.boolean_to_int(true);</pre> | 
return | <pre>  return l_result;</pre> | 
else | <pre>    else<br />      l_result := equal_with_nulls((self.expected = a_actual), a_actual);</pre> | 
end | <pre>    end if;</pre> | 
 | <pre>    l_result := equal_with_nulls( l_result, a_actual );</pre> | 
else | <pre>  else<br />    l_result := (self as ut_matcher).run_matcher(a_actual);</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 
else | <pre>  else<br />    l_result := (self as ut_matcher).failure_message(a_actual) || ': '|| self.expected.to_string_report();</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 
begin | <pre>begin<br />  return (self as ut_matcher).failure_message_when_negated(a_actual) || ': '|| expected.to_string_report();</pre> | 
nulls_are_equal_flag | <pre>nulls_are_equal_flag number(1,0),;</pre> | 
exclude_list | <pre>exclude_list   ut_varchar2_list,;</pre> | 
include_list | <pre>include_list   ut_varchar2_list,;</pre> | 
is_unordered | <pre>is_unordered   number(1,0),;</pre> | 



## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
 | <pre>  return ( a_assert_result or ( self.expected.is_null() and a_actual.is_null() and ut_utils.int_to_boolean( nulls_are_equal_flag ) ) );</pre> | 
 | <pre>  exclude_list := ut_varchar2_list(a_exclude);</pre> | 
 | <pre>  exclude_list := coalesce(a_exclude, ut_varchar2_list());</pre> | 
 | <pre>  exclude_list := ut_varchar2_list(a_exclude);</pre> | 
 | <pre>  exclude_list := coalesce(a_exclude, ut_varchar2_list());</pre> | 
begin | <pre>begin<br />  ut_utils.append_to_list(l_result.include_list, a_items);</pre> | 
return | <pre>  return l_result;</pre> | 
begin | <pre>begin<br />  l_result.include_list := l_result.include_list multiset union all coalesce(a_items,ut_varchar2_list());</pre> | 
return | <pre>  return l_result;</pre> | 
begin | <pre>begin<br />  ut_utils.append_to_list(l_result.exclude_list, a_items);</pre> | 
return | <pre>  return l_result;</pre> | 
begin | <pre>begin<br />  l_result.exclude_list := l_result.exclude_list multiset union all coalesce(a_items,ut_varchar2_list());</pre> | 
return | <pre>  return l_result;</pre> | 
begin | <pre>begin<br />  l_result.is_unordered := ut_utils.boolean_to_int(true);</pre> | 
return | <pre>  return l_result;</pre> | 
begin | <pre>begin<br />  l_result.is_unordered := ut_utils.boolean_to_int(true);</pre> | 
return | <pre>  return l_result;</pre> | 
begin | <pre>begin<br />  l_result.is_unordered := ut_utils.boolean_to_int(true);</pre> | 
return | <pre>  return l_result;</pre> | 
else | <pre>    else<br />      l_result := equal_with_nulls((self.expected = a_actual), a_actual);</pre> | 
end | <pre>    end if;</pre> | 
 | <pre>    l_result := equal_with_nulls( l_result, a_actual );</pre> | 
else | <pre>  else<br />    l_result := (self as ut_matcher).run_matcher(a_actual);</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 
else | <pre>  else<br />    l_result := (self as ut_matcher).failure_message(a_actual) || ': '|| self.expected.to_string_report();</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 
begin | <pre>begin<br />  return (self as ut_matcher).failure_message_when_negated(a_actual) || ': '|| expected.to_string_report();</pre> | 
nulls_are_equal_flag | <pre>nulls_are_equal_flag number(1,0),;</pre> | 
exclude_list | <pre>exclude_list   ut_varchar2_list,;</pre> | 
include_list | <pre>include_list   ut_varchar2_list,;</pre> | 
is_unordered | <pre>is_unordered   number(1,0),;</pre> | 




 
