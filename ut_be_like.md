# UT_BE_LIKE




- [Variables](#variables)

- [Exceptions](#exceptions)




## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
end | <pre>end ut_be_like;</pre> | 
l_result | <pre>  l_result boolean;</pre> | 
else | <pre>    else<br />      l_value := treat(a_actual as ut_data_value_clob).data_value;</pre> | 
end | <pre>    end if;</pre> | 
else | <pre>    else<br />      l_result := l_value like mask;</pre> | 
end | <pre>    end if;</pre> | 
else | <pre>  else<br />    l_result := (self as ut_matcher).run_matcher(a_actual);</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 
end | <pre>end run_matcher;</pre> | 
begin | <pre>begin<br />  l_result := (self as ut_matcher).failure_message(a_actual);</pre> | 
else | <pre>  else<br />    l_result := l_result || ': '|| ut_data_value_varchar2(self.mask).to_string_report(false, false);</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 
begin | <pre>begin<br />  l_result := (self as ut_matcher).failure_message_when_negated(a_actual);</pre> | 
else | <pre>  else<br />    l_result := l_result || ': '|| ut_data_value_varchar2(self.mask).to_string_report(false, false);</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 



## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
end | <pre>end ut_be_like;</pre> | 
l_result | <pre>  l_result boolean;</pre> | 
else | <pre>    else<br />      l_value := treat(a_actual as ut_data_value_clob).data_value;</pre> | 
end | <pre>    end if;</pre> | 
else | <pre>    else<br />      l_result := l_value like mask;</pre> | 
end | <pre>    end if;</pre> | 
else | <pre>  else<br />    l_result := (self as ut_matcher).run_matcher(a_actual);</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 
end | <pre>end run_matcher;</pre> | 
begin | <pre>begin<br />  l_result := (self as ut_matcher).failure_message(a_actual);</pre> | 
else | <pre>  else<br />    l_result := l_result || ': '|| ut_data_value_varchar2(self.mask).to_string_report(false, false);</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 
begin | <pre>begin<br />  l_result := (self as ut_matcher).failure_message_when_negated(a_actual);</pre> | 
else | <pre>  else<br />    l_result := l_result || ': '|| ut_data_value_varchar2(self.mask).to_string_report(false, false);</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 




 
