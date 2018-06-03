# UT_COMPOUND_DATA_VALUE




- [Variables](#variables)

- [Exceptions](#exceptions)




## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
c_max_rows | <pre>  c_max_rows      constant integer := 20;</pre> | 
l_result | <pre>  l_result        clob;</pre> | 
l_result_string | <pre>  l_result_string varchar2(32767);</pre> | 
 | <pre>    l_result_string := ut_utils.to_string(l_result,null);</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result_string;</pre> | 
l_result_string | <pre>  l_result_string     varchar2(32767);</pre> | 
begin | <pre>begin<br />  l_result := get_data_diff(a_other, a_exclude_xpath, a_include_xpath, a_join_by_xpath,a_unordered);</pre> | 
 | <pre>  l_result_string := ut_utils.to_string(l_result,null);</pre> | 
return | <pre>  return l_result_string;</pre> | 
l_result | <pre>  l_result            clob;</pre> | 
l_results | <pre>  l_results           ut_utils.t_clob_tab := ut_utils.t_clob_tab();</pre> | 
l_message | <pre>  l_message           varchar2(32767);</pre> | 
l_ut_owner | <pre>  l_ut_owner          varchar2(250) := ut_utils.ut_owner;</pre> | 
l_diff_row_count | <pre>  l_diff_row_count    integer;</pre> | 
l_actual | <pre>  l_actual            ut_compound_data_value;</pre> | 
l_diff_id | <pre>  l_diff_id           ut_compound_data_helper.t_hash;</pre> | 
l_row_diffs | <pre>  l_row_diffs         ut_compound_data_helper.tt_row_diffs;</pre> | 
l_compare_type | <pre>  l_compare_type      varchar2(10);</pre> | 
end | <pre>      end if;</pre> | 
end | <pre>  end if;</pre> | 
 | <pre>  l_actual := treat(a_other as ut_compound_data_value);</pre> | 
 | <pre>  l_diff_id := ut_compound_data_helper.get_hash(self.data_id||l_actual.data_id);</pre> | 
end | <pre>    end loop;</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 
l_ut_owner | <pre>  l_ut_owner        varchar2(250) := ut_utils.ut_owner;</pre> | 
l_column_filter | <pre>  l_column_filter   varchar2(32767);</pre> | 
l_diff_id | <pre>  l_diff_id         ut_compound_data_helper.t_hash;</pre> | 
l_result | <pre>  l_result          integer;</pre> | 
end | <pre>  end if;</pre> | 
 | <pre>  l_other   := treat(a_other as ut_compound_data_value);</pre> | 
 | <pre>  l_diff_id := ut_compound_data_helper.get_hash(self.data_id||l_other.data_id);</pre> | 
 | <pre>  l_column_filter := ut_compound_data_helper.get_columns_filter(a_exclude_xpath, a_include_xpath);</pre> | 
else | <pre>else<br />  l_column := ':join_by_xpath pk_hash';</pre> | 
end | <pre>end if;</pre> | 
return | <pre>return l_column;</pre> | 
end | <pre>    end if;</pre> | 
 | <pre>    l_other   := treat(a_other as ut_compound_data_value);</pre> | 
 | <pre>    l_diff_id := ut_compound_data_helper.get_hash(self.data_id||l_other.data_id);</pre> | 
 | <pre>    l_column_filter := ut_compound_data_helper.get_columns_filter(a_exclude_xpath, a_include_xpath);</pre> | 
else | <pre>else<br />  l_result := 1;</pre> | 
end | <pre>end if;</pre> | 
return | <pre>return l_result;</pre> | 
is_data_null | <pre>is_data_null   integer,;</pre> | 
elements_count | <pre>elements_count  integer,;</pre> | 



## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
c_max_rows | <pre>  c_max_rows      constant integer := 20;</pre> | 
l_result | <pre>  l_result        clob;</pre> | 
l_result_string | <pre>  l_result_string varchar2(32767);</pre> | 
 | <pre>    l_result_string := ut_utils.to_string(l_result,null);</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result_string;</pre> | 
l_result_string | <pre>  l_result_string     varchar2(32767);</pre> | 
begin | <pre>begin<br />  l_result := get_data_diff(a_other, a_exclude_xpath, a_include_xpath, a_join_by_xpath,a_unordered);</pre> | 
 | <pre>  l_result_string := ut_utils.to_string(l_result,null);</pre> | 
return | <pre>  return l_result_string;</pre> | 
l_result | <pre>  l_result            clob;</pre> | 
l_results | <pre>  l_results           ut_utils.t_clob_tab := ut_utils.t_clob_tab();</pre> | 
l_message | <pre>  l_message           varchar2(32767);</pre> | 
l_ut_owner | <pre>  l_ut_owner          varchar2(250) := ut_utils.ut_owner;</pre> | 
l_diff_row_count | <pre>  l_diff_row_count    integer;</pre> | 
l_actual | <pre>  l_actual            ut_compound_data_value;</pre> | 
l_diff_id | <pre>  l_diff_id           ut_compound_data_helper.t_hash;</pre> | 
l_row_diffs | <pre>  l_row_diffs         ut_compound_data_helper.tt_row_diffs;</pre> | 
l_compare_type | <pre>  l_compare_type      varchar2(10);</pre> | 
end | <pre>      end if;</pre> | 
end | <pre>  end if;</pre> | 
 | <pre>  l_actual := treat(a_other as ut_compound_data_value);</pre> | 
 | <pre>  l_diff_id := ut_compound_data_helper.get_hash(self.data_id||l_actual.data_id);</pre> | 
end | <pre>    end loop;</pre> | 
end | <pre>  end if;</pre> | 
return | <pre>  return l_result;</pre> | 
l_ut_owner | <pre>  l_ut_owner        varchar2(250) := ut_utils.ut_owner;</pre> | 
l_column_filter | <pre>  l_column_filter   varchar2(32767);</pre> | 
l_diff_id | <pre>  l_diff_id         ut_compound_data_helper.t_hash;</pre> | 
l_result | <pre>  l_result          integer;</pre> | 
end | <pre>  end if;</pre> | 
 | <pre>  l_other   := treat(a_other as ut_compound_data_value);</pre> | 
 | <pre>  l_diff_id := ut_compound_data_helper.get_hash(self.data_id||l_other.data_id);</pre> | 
 | <pre>  l_column_filter := ut_compound_data_helper.get_columns_filter(a_exclude_xpath, a_include_xpath);</pre> | 
else | <pre>else<br />  l_column := ':join_by_xpath pk_hash';</pre> | 
end | <pre>end if;</pre> | 
return | <pre>return l_column;</pre> | 
end | <pre>    end if;</pre> | 
 | <pre>    l_other   := treat(a_other as ut_compound_data_value);</pre> | 
 | <pre>    l_diff_id := ut_compound_data_helper.get_hash(self.data_id||l_other.data_id);</pre> | 
 | <pre>    l_column_filter := ut_compound_data_helper.get_columns_filter(a_exclude_xpath, a_include_xpath);</pre> | 
else | <pre>else<br />  l_result := 1;</pre> | 
end | <pre>end if;</pre> | 
return | <pre>return l_result;</pre> | 
is_data_null | <pre>is_data_null   integer,;</pre> | 
elements_count | <pre>elements_count  integer,;</pre> | 




 
