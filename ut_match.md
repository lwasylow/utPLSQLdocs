# UT_MATCH




- [Variables](#variables)

- [Exceptions](#exceptions)




## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
else | <pre>  else<br />    l_result := (self as ut_matcher).run_matcher(a_actual);</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 
begin | <pre>begin<br />  l_result := (self as ut_matcher).failure_message(a_actual);</pre> | 
else | <pre>  else<br />    l_result := l_result || ': '|| ut_data_value_varchar2(self.pattern).to_string_report(false, false);</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 
begin | <pre>begin<br />  l_result := (self as ut_matcher).failure_message_when_negated(a_actual);</pre> | 
else | <pre>  else<br />    l_result := l_result || ': '|| ut_data_value_varchar2(self.pattern).to_string_report(false, false);</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 



## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
else | <pre>  else<br />    l_result := (self as ut_matcher).run_matcher(a_actual);</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 
begin | <pre>begin<br />  l_result := (self as ut_matcher).failure_message(a_actual);</pre> | 
else | <pre>  else<br />    l_result := l_result || ': '|| ut_data_value_varchar2(self.pattern).to_string_report(false, false);</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 
begin | <pre>begin<br />  l_result := (self as ut_matcher).failure_message_when_negated(a_actual);</pre> | 
else | <pre>  else<br />    l_result := l_result || ': '|| ut_data_value_varchar2(self.pattern).to_string_report(false, false);</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 




 
