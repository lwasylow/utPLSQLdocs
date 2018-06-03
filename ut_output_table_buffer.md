# UT_OUTPUT_TABLE_BUFFER




- [Variables](#variables)

- [Exceptions](#exceptions)




## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
l_exists | <pre>  l_exists int;</pre> | 
begin | <pre>begin<br />  select count(*) into l_exists from ut_output_buffer_info_tmp where output_id = self.output_id;</pre> | 
else | <pre>  else<br />    insert into ut_output_buffer_info_tmp(output_id, start_date) values (self.output_id, self.start_date);</pre> | 
end | <pre>  end if;</pre> | 
pragma | <pre>  pragma autonomous_transaction;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>  end if;</pre> | 
l_already_waited_for | <pre>  l_already_waited_for number(10,2) := 0;</pre> | 
l_finished | <pre>  l_finished           boolean := false;</pre> | 
lc_init_wait_sec | <pre>  lc_init_wait_sec     constant naturaln := coalesce(a_initial_timeout, 60 * 60 * 4 );</pre> | 
lc_short_sleep_time | <pre>  lc_short_sleep_time  constant number(1,1) := 0.1;</pre> | 
pragma | <pre>    pragma autonomous_transaction;</pre> | 
return | <pre>    return l_results;</pre> | 
 | <pre>      l_already_waited_for := l_already_waited_for + l_sleep_time;</pre> | 
end | <pre>      end if;</pre> | 
else | <pre>    else<br /><br /><br />      l_wait_for := lc_max_wait_sec;</pre> | 
 | <pre>      l_already_waited_for := 0;</pre> | 
 | <pre>      l_sleep_time := lc_short_sleep_time;</pre> | 
else | <pre>        else<br />          l_finished := true;</pre> | 
end | <pre>        end if;</pre> | 
end | <pre>      end loop;</pre> | 
end | <pre>    end if;</pre> | 
exit | <pre>    exit when l_already_waited_for >= l_wait_for or l_finished;</pre> | 
end | <pre>  end loop;</pre> | 
return | <pre>  return l_lines;</pre> | 
l_line | <pre>  l_line varchar2(32767);</pre> | 
begin | <pre>begin<br />  l_lines := self.get_lines_cursor(a_initial_timeout, a_timeout_sec);</pre> | 
loop | <pre>  loop<br />    fetch l_lines into l_line;</pre> | 
exit | <pre>    exit when l_lines%notfound;</pre> | 
end | <pre>  end loop;</pre> | 
close | <pre>  close l_lines;</pre> | 
l_max_retention_date | <pre>  l_max_retention_date     date := sysdate - l_retention_days;</pre> | 
pragma | <pre>  pragma autonomous_transaction;</pre> | 
delete | <pre>  delete from ut_output_buffer_info_tmp i where i.start_date <= l_max_retention_date;</pre> | 



## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
l_exists | <pre>  l_exists int;</pre> | 
begin | <pre>begin<br />  select count(*) into l_exists from ut_output_buffer_info_tmp where output_id = self.output_id;</pre> | 
else | <pre>  else<br />    insert into ut_output_buffer_info_tmp(output_id, start_date) values (self.output_id, self.start_date);</pre> | 
end | <pre>  end if;</pre> | 
pragma | <pre>  pragma autonomous_transaction;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>  end if;</pre> | 
l_already_waited_for | <pre>  l_already_waited_for number(10,2) := 0;</pre> | 
l_finished | <pre>  l_finished           boolean := false;</pre> | 
lc_init_wait_sec | <pre>  lc_init_wait_sec     constant naturaln := coalesce(a_initial_timeout, 60 * 60 * 4 );</pre> | 
lc_short_sleep_time | <pre>  lc_short_sleep_time  constant number(1,1) := 0.1;</pre> | 
pragma | <pre>    pragma autonomous_transaction;</pre> | 
return | <pre>    return l_results;</pre> | 
 | <pre>      l_already_waited_for := l_already_waited_for + l_sleep_time;</pre> | 
end | <pre>      end if;</pre> | 
else | <pre>    else<br /><br /><br />      l_wait_for := lc_max_wait_sec;</pre> | 
 | <pre>      l_already_waited_for := 0;</pre> | 
 | <pre>      l_sleep_time := lc_short_sleep_time;</pre> | 
else | <pre>        else<br />          l_finished := true;</pre> | 
end | <pre>        end if;</pre> | 
end | <pre>      end loop;</pre> | 
end | <pre>    end if;</pre> | 
exit | <pre>    exit when l_already_waited_for >= l_wait_for or l_finished;</pre> | 
end | <pre>  end loop;</pre> | 
return | <pre>  return l_lines;</pre> | 
l_line | <pre>  l_line varchar2(32767);</pre> | 
begin | <pre>begin<br />  l_lines := self.get_lines_cursor(a_initial_timeout, a_timeout_sec);</pre> | 
loop | <pre>  loop<br />    fetch l_lines into l_line;</pre> | 
exit | <pre>    exit when l_lines%notfound;</pre> | 
end | <pre>  end loop;</pre> | 
close | <pre>  close l_lines;</pre> | 
l_max_retention_date | <pre>  l_max_retention_date     date := sysdate - l_retention_days;</pre> | 
pragma | <pre>  pragma autonomous_transaction;</pre> | 
delete | <pre>  delete from ut_output_buffer_info_tmp i where i.start_date <= l_max_retention_date;</pre> | 




 
