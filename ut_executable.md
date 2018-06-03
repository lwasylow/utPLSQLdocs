# UT_EXECUTABLE




- [Variables](#variables)

- [Exceptions](#exceptions)




## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
l_message_part | <pre>  l_message_part varchar2(4000) := 'Call params for ' || self.associated_event_name || ' are not valid: ';</pre> | 
else | <pre>  else<br />    l_result := true;</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 
end | <pre>end is_defined;</pre> | 
l_message_part | <pre>  l_message_part varchar2(4000) := 'Call params for ' || self.associated_event_name || ' are not valid: ';</pre> | 
else | <pre>  else<br />    l_result := false;</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 
end | <pre>end is_invalid;</pre> | 
begin | <pre>begin<br />  l_completed_without_errors := self.do_execute(a_item);</pre> | 
end | <pre>end do_execute;</pre> | 
l_status | <pre>  l_status                   number;</pre> | 
l_cursor_number | <pre>  l_cursor_number            number;</pre> | 
l_completed_without_errors | <pre>  l_completed_without_errors boolean := true;</pre> | 
l_failed_with_invalid_pck | <pre>  l_failed_with_invalid_pck  boolean := true;</pre> | 
l_start_transaction_id | <pre>  l_start_transaction_id     varchar2(250);</pre> | 
l_end_transaction_id | <pre>  l_end_transaction_id     varchar2(250);</pre> | 
l_line | <pre>    l_line varchar2(32767);</pre> | 
begin | <pre>  begin<br />    dbms_lob.createtemporary(self.serveroutput, true, dur => dbms_lob.session);</pre> | 
loop | <pre>    loop<br />      dbms_output.get_line(line => l_line, status => l_status);</pre> | 
exit | <pre>      exit when l_status = 1;</pre> | 
end | <pre>      end if;</pre> | 
end | <pre>    end loop;</pre> | 
end | <pre>  end save_dbms_output;</pre> | 
begin | <pre>begin<br />  l_start_transaction_id := dbms_transaction.local_transaction_id(true);</pre> | 
 | <pre>  l_completed_without_errors := self.is_defined();</pre> | 
 | <pre>    l_cursor_number := dbms_sql.open_cursor;</pre> | 
begin | <pre>begin<br />  dbms_sql.parse(l_cursor_number, statement => l_statement, language_flag => dbms_sql.native);</pre> | 
 | <pre>  l_status := dbms_sql.execute(l_cursor_number);</pre> | 
end | <pre>    end if;</pre> | 
 | <pre>l_completed_without_errors := (self.error_stack||self.error_backtrace) is null;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>    end if;</pre> | 
 | <pre>    l_end_transaction_id := dbms_transaction.local_transaction_id();</pre> | 
end | <pre>    end if;</pre> | 
return | <pre>    return l_completed_without_errors;</pre> | 
end | <pre>    <br />  end do_execute;</pre> | 



## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
l_message_part | <pre>  l_message_part varchar2(4000) := 'Call params for ' || self.associated_event_name || ' are not valid: ';</pre> | 
else | <pre>  else<br />    l_result := true;</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 
end | <pre>end is_defined;</pre> | 
l_message_part | <pre>  l_message_part varchar2(4000) := 'Call params for ' || self.associated_event_name || ' are not valid: ';</pre> | 
else | <pre>  else<br />    l_result := false;</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 
end | <pre>end is_invalid;</pre> | 
begin | <pre>begin<br />  l_completed_without_errors := self.do_execute(a_item);</pre> | 
end | <pre>end do_execute;</pre> | 
l_status | <pre>  l_status                   number;</pre> | 
l_cursor_number | <pre>  l_cursor_number            number;</pre> | 
l_completed_without_errors | <pre>  l_completed_without_errors boolean := true;</pre> | 
l_failed_with_invalid_pck | <pre>  l_failed_with_invalid_pck  boolean := true;</pre> | 
l_start_transaction_id | <pre>  l_start_transaction_id     varchar2(250);</pre> | 
l_end_transaction_id | <pre>  l_end_transaction_id     varchar2(250);</pre> | 
l_line | <pre>    l_line varchar2(32767);</pre> | 
begin | <pre>  begin<br />    dbms_lob.createtemporary(self.serveroutput, true, dur => dbms_lob.session);</pre> | 
loop | <pre>    loop<br />      dbms_output.get_line(line => l_line, status => l_status);</pre> | 
exit | <pre>      exit when l_status = 1;</pre> | 
end | <pre>      end if;</pre> | 
end | <pre>    end loop;</pre> | 
end | <pre>  end save_dbms_output;</pre> | 
begin | <pre>begin<br />  l_start_transaction_id := dbms_transaction.local_transaction_id(true);</pre> | 
 | <pre>  l_completed_without_errors := self.is_defined();</pre> | 
 | <pre>    l_cursor_number := dbms_sql.open_cursor;</pre> | 
begin | <pre>begin<br />  dbms_sql.parse(l_cursor_number, statement => l_statement, language_flag => dbms_sql.native);</pre> | 
 | <pre>  l_status := dbms_sql.execute(l_cursor_number);</pre> | 
end | <pre>    end if;</pre> | 
 | <pre>l_completed_without_errors := (self.error_stack||self.error_backtrace) is null;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>    end if;</pre> | 
 | <pre>    l_end_transaction_id := dbms_transaction.local_transaction_id();</pre> | 
end | <pre>    end if;</pre> | 
return | <pre>    return l_completed_without_errors;</pre> | 
end | <pre>    <br />  end do_execute;</pre> | 




 
