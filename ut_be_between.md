# UT_BE_BETWEEN




- [Variables](#variables)

- [Exceptions](#exceptions)




## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
l_upper_result | <pre>  l_upper_result boolean;</pre> | 
l_result | <pre>  l_result boolean;</pre> | 
 | <pre>    l_upper_result := a_actual <= self.upper_bound;</pre> | 
end | <pre>    end if;</pre> | 
else | <pre>  else<br />    l_result := (self as ut_matcher).run_matcher(a_actual);</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 



## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
l_upper_result | <pre>  l_upper_result boolean;</pre> | 
l_result | <pre>  l_result boolean;</pre> | 
 | <pre>    l_upper_result := a_actual <= self.upper_bound;</pre> | 
end | <pre>    end if;</pre> | 
else | <pre>  else<br />    l_result := (self as ut_matcher).run_matcher(a_actual);</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 




 
