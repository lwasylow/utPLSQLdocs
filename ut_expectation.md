# UT_EXPECTATION




- [Variables](#variables)

- [Exceptions](#exceptions)




## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
l_matcher | <pre>  l_matcher       ut_matcher := a_matcher;</pre> | 
l_message | <pre>  l_message       varchar2(32767);</pre> | 
begin | <pre>begin<br />  <br />  l_expectation_result := l_matcher.run_matcher( self.actual_data );</pre> | 
 | <pre>  l_expectation_result := coalesce(l_expectation_result,false);</pre> | 
 | <pre>  l_message := coalesce( l_matcher.error_message( self.actual_data ), l_matcher.failure_message( self.actual_data ) );</pre> | 
l_matcher | <pre>  l_matcher       ut_matcher := a_matcher;</pre> | 
l_message | <pre>  l_message       varchar2(32767);</pre> | 
begin | <pre>begin<br />  <br />  l_expectation_result := l_matcher.run_matcher_negated( self.actual_data );</pre> | 
 | <pre>  l_expectation_result := coalesce(l_expectation_result,false);</pre> | 
 | <pre>  l_message := coalesce( l_matcher.error_message( self.actual_data ), l_matcher.failure_message_when_negated( self.actual_data ) );</pre> | 



## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
l_matcher | <pre>  l_matcher       ut_matcher := a_matcher;</pre> | 
l_message | <pre>  l_message       varchar2(32767);</pre> | 
begin | <pre>begin<br />  <br />  l_expectation_result := l_matcher.run_matcher( self.actual_data );</pre> | 
 | <pre>  l_expectation_result := coalesce(l_expectation_result,false);</pre> | 
 | <pre>  l_message := coalesce( l_matcher.error_message( self.actual_data ), l_matcher.failure_message( self.actual_data ) );</pre> | 
l_matcher | <pre>  l_matcher       ut_matcher := a_matcher;</pre> | 
l_message | <pre>  l_message       varchar2(32767);</pre> | 
begin | <pre>begin<br />  <br />  l_expectation_result := l_matcher.run_matcher_negated( self.actual_data );</pre> | 
 | <pre>  l_expectation_result := coalesce(l_expectation_result,false);</pre> | 
 | <pre>  l_message := coalesce( l_matcher.error_message( self.actual_data ), l_matcher.failure_message_when_negated( self.actual_data ) );</pre> | 




 
