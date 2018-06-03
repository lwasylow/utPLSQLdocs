# UT_CURR_USR_COMPOUND_HELPER




- [Variables](#variables)

- [Exceptions](#exceptions)




## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
end | <pre>end if;</pre> | 
return | <pre>return ut_key_anyval_pair(a_desc_rec.col_name,l_data);</pre> | 
end | <pre>end loop;</pre> | 
return | <pre>return l_result;</pre> | 
l_columns_count | <pre>    l_columns_count  pls_integer;</pre> | 
l_columns_desc | <pre>    l_columns_desc   dbms_sql.desc_tab3;</pre> | 
l_columns_tab | <pre>    l_columns_tab    ut_key_anyval_pairs;</pre> | 
end | <pre>    end if;</pre> | 
 | <pre>    l_cursor_number := dbms_sql.to_cursor_number( a_cursor );</pre> | 
 | <pre>    a_cursor := dbms_sql.to_refcursor( l_cursor_number );</pre> | 
 | <pre>    l_columns_tab := get_columns_info( l_columns_desc, l_columns_count,a_desc_user_types);</pre> | 
return | <pre>    return l_columns_tab;</pre> | 
l_columns_count | <pre>    l_columns_count  pls_integer;</pre> | 
l_columns_desc | <pre>    l_columns_desc   dbms_sql.desc_tab3;</pre> | 
 | <pre>  a_join_by_tab := null;</pre> | 
end | <pre>    end if;</pre> | 
 | <pre>    l_cursor_number := dbms_sql.to_cursor_number( a_cursor );</pre> | 
 | <pre>    a_cursor := dbms_sql.to_refcursor( l_cursor_number );</pre> | 
 | <pre>    a_columns_tab := get_columns_info( l_columns_desc, l_columns_count,false);</pre> | 
 | <pre>    a_join_by_tab := get_columns_info( l_columns_desc, l_columns_count,true);</pre> | 
l_join_by_info | <pre>    l_join_by_info         xmltype;</pre> | 
l_result_tmp | <pre>    l_result_tmp           xmltype;</pre> | 
l_columns_tab | <pre>    l_columns_tab          ut_key_anyval_pairs;</pre> | 
l_join_by_tab | <pre>    l_join_by_tab          ut_key_anyval_pairs;</pre> | 
begin | <pre>  begin<br />    <br />    get_descr_cursor(a_cursor,l_columns_tab,l_join_by_tab);</pre> | 
select | <pre>select xmlconcat(l_columns_info,l_result_tmp) into l_columns_info from dual;</pre> | 
end | <pre> <br />    end loop;</pre> | 
select | <pre>select xmlconcat(l_join_by_info,l_result_tmp) into l_join_by_info from dual;</pre> | 
end | <pre> <br />    end loop;</pre> | 
 | <pre>   <br />    a_contains_collection := ut_utils.boolean_to_int(g_is_collection);</pre> | 
l_result_tmp | <pre>    l_result_tmp     xmltype;</pre> | 
l_columns_tab | <pre>    l_columns_tab    ut_key_anyval_pairs;</pre> | 
begin | <pre>    begin<br />l_columns_tab := get_descr_cursor(a_cursor,a_desc_user_types);</pre> | 
select | <pre>  select xmlconcat(l_result,l_result_tmp) into l_result from dual;</pre> | 
end | <pre> <br />end loop;</pre> | 
return | <pre>return l_result;</pre> | 
l_schema_name | <pre>      l_schema_name              varchar2(32767);</pre> | 
l_version | <pre>      l_version                  varchar2(32767);</pre> | 
l_type_name | <pre>      l_type_name                varchar2(32767);</pre> | 
l_attributes | <pre>      l_attributes               pls_integer;</pre> | 
l_prec | <pre>      l_prec                     pls_integer;</pre> | 
l_scale | <pre> <br />      l_scale                    pls_integer;</pre> | 
l_len | <pre>      l_len                      pls_integer;</pre> | 
l_csid | <pre>      l_csid                     pls_integer;</pre> | 
l_csfrm | <pre>      l_csfrm                    pls_integer;</pre> | 
return | <pre>             <br />    return l_attributes;</pre> | 
l_attribute_typecode | <pre>    l_attribute_typecode pls_integer;</pre> | 
l_aname | <pre>    l_aname          varchar2(32767);</pre> | 
l_prec | <pre>    l_prec           pls_integer;</pre> | 
l_scale | <pre> <br />    l_scale          pls_integer;</pre> | 
l_len | <pre>    l_len            pls_integer;</pre> | 
l_csid | <pre>    l_csid           pls_integer;</pre> | 
l_csfrm | <pre>    l_csfrm          pls_integer;</pre> | 
l_attr_elt_type | <pre>    l_attr_elt_type  anytype;</pre> | 
end | <pre>     end if;</pre> | 
end | <pre>    end loop;</pre> | 
return | <pre>    return l_result;</pre> | 
l_anytype | <pre>    l_anytype anytype;</pre> | 
l_typecode | <pre>    l_typecode pls_integer;</pre> | 
l_result | <pre>    l_result xmltype;</pre> | 
l_columns_tab | <pre>    l_columns_tab ut_key_value_pairs := ut_key_value_pairs();</pre> | 
 | <pre>                 begin <br />                   :anydata := anydata.convertobject(l_v);</pre> | 
 | <pre>    <br />    l_typecode := l_anydata.gettype(l_anytype);</pre> | 
 | <pre>    l_columns_tab := get_anytype_attributes_info(l_anytype);</pre> | 
return | <pre>    <br />    return l_result;</pre> | 
begin | <pre>  <br />  begin<br />  g_anytype_name_map(dbms_types.typecode_date)             :=' DATE';</pre> | 



## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
end | <pre>end if;</pre> | 
return | <pre>return ut_key_anyval_pair(a_desc_rec.col_name,l_data);</pre> | 
end | <pre>end loop;</pre> | 
return | <pre>return l_result;</pre> | 
l_columns_count | <pre>    l_columns_count  pls_integer;</pre> | 
l_columns_desc | <pre>    l_columns_desc   dbms_sql.desc_tab3;</pre> | 
l_columns_tab | <pre>    l_columns_tab    ut_key_anyval_pairs;</pre> | 
end | <pre>    end if;</pre> | 
 | <pre>    l_cursor_number := dbms_sql.to_cursor_number( a_cursor );</pre> | 
 | <pre>    a_cursor := dbms_sql.to_refcursor( l_cursor_number );</pre> | 
 | <pre>    l_columns_tab := get_columns_info( l_columns_desc, l_columns_count,a_desc_user_types);</pre> | 
return | <pre>    return l_columns_tab;</pre> | 
l_columns_count | <pre>    l_columns_count  pls_integer;</pre> | 
l_columns_desc | <pre>    l_columns_desc   dbms_sql.desc_tab3;</pre> | 
 | <pre>  a_join_by_tab := null;</pre> | 
end | <pre>    end if;</pre> | 
 | <pre>    l_cursor_number := dbms_sql.to_cursor_number( a_cursor );</pre> | 
 | <pre>    a_cursor := dbms_sql.to_refcursor( l_cursor_number );</pre> | 
 | <pre>    a_columns_tab := get_columns_info( l_columns_desc, l_columns_count,false);</pre> | 
 | <pre>    a_join_by_tab := get_columns_info( l_columns_desc, l_columns_count,true);</pre> | 
l_join_by_info | <pre>    l_join_by_info         xmltype;</pre> | 
l_result_tmp | <pre>    l_result_tmp           xmltype;</pre> | 
l_columns_tab | <pre>    l_columns_tab          ut_key_anyval_pairs;</pre> | 
l_join_by_tab | <pre>    l_join_by_tab          ut_key_anyval_pairs;</pre> | 
begin | <pre>  begin<br />    <br />    get_descr_cursor(a_cursor,l_columns_tab,l_join_by_tab);</pre> | 
select | <pre>select xmlconcat(l_columns_info,l_result_tmp) into l_columns_info from dual;</pre> | 
end | <pre> <br />    end loop;</pre> | 
select | <pre>select xmlconcat(l_join_by_info,l_result_tmp) into l_join_by_info from dual;</pre> | 
end | <pre> <br />    end loop;</pre> | 
 | <pre>   <br />    a_contains_collection := ut_utils.boolean_to_int(g_is_collection);</pre> | 
l_result_tmp | <pre>    l_result_tmp     xmltype;</pre> | 
l_columns_tab | <pre>    l_columns_tab    ut_key_anyval_pairs;</pre> | 
begin | <pre>    begin<br />l_columns_tab := get_descr_cursor(a_cursor,a_desc_user_types);</pre> | 
select | <pre>  select xmlconcat(l_result,l_result_tmp) into l_result from dual;</pre> | 
end | <pre> <br />end loop;</pre> | 
return | <pre>return l_result;</pre> | 
l_schema_name | <pre>      l_schema_name              varchar2(32767);</pre> | 
l_version | <pre>      l_version                  varchar2(32767);</pre> | 
l_type_name | <pre>      l_type_name                varchar2(32767);</pre> | 
l_attributes | <pre>      l_attributes               pls_integer;</pre> | 
l_prec | <pre>      l_prec                     pls_integer;</pre> | 
l_scale | <pre> <br />      l_scale                    pls_integer;</pre> | 
l_len | <pre>      l_len                      pls_integer;</pre> | 
l_csid | <pre>      l_csid                     pls_integer;</pre> | 
l_csfrm | <pre>      l_csfrm                    pls_integer;</pre> | 
return | <pre>             <br />    return l_attributes;</pre> | 
l_attribute_typecode | <pre>    l_attribute_typecode pls_integer;</pre> | 
l_aname | <pre>    l_aname          varchar2(32767);</pre> | 
l_prec | <pre>    l_prec           pls_integer;</pre> | 
l_scale | <pre> <br />    l_scale          pls_integer;</pre> | 
l_len | <pre>    l_len            pls_integer;</pre> | 
l_csid | <pre>    l_csid           pls_integer;</pre> | 
l_csfrm | <pre>    l_csfrm          pls_integer;</pre> | 
l_attr_elt_type | <pre>    l_attr_elt_type  anytype;</pre> | 
end | <pre>     end if;</pre> | 
end | <pre>    end loop;</pre> | 
return | <pre>    return l_result;</pre> | 
l_anytype | <pre>    l_anytype anytype;</pre> | 
l_typecode | <pre>    l_typecode pls_integer;</pre> | 
l_result | <pre>    l_result xmltype;</pre> | 
l_columns_tab | <pre>    l_columns_tab ut_key_value_pairs := ut_key_value_pairs();</pre> | 
 | <pre>                 begin <br />                   :anydata := anydata.convertobject(l_v);</pre> | 
 | <pre>    <br />    l_typecode := l_anydata.gettype(l_anytype);</pre> | 
 | <pre>    l_columns_tab := get_anytype_attributes_info(l_anytype);</pre> | 
return | <pre>    <br />    return l_result;</pre> | 
begin | <pre>  <br />  begin<br />  g_anytype_name_map(dbms_types.typecode_date)             :=' DATE';</pre> | 




 
