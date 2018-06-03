# UT_SUITE_BUILDER


- [Data Types](#types)


- [Variables](#variables)

- [Exceptions](#exceptions)

- [BUILD_SCHEMA_SUITES Function](#build_schema_suites)
- [BUILD_SUITES Function](#build_suites)

## Types<a name="types"></a>

Name | Code | Description
--- | --- | ---
t_annotation_text | <pre>subtype t_annotation_text     is varchar2(4000);</pre> | 
t_annotation_name | <pre>subtype t_annotation_name     is varchar2(4000);</pre> | 
t_object_name | <pre>subtype t_object_name         is varchar2(500);</pre> | 
t_annotation_position | <pre>subtype t_annotation_position is binary_integer;</pre> | 
tt_procedure_annotations | <pre>type tt_procedure_annotations is table of tt_annotation_texts index by t_annotation_name;</pre> | 

## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
 | <pre>l_throws_list := ut_utils.trim_list_elements(ut_utils.string_to_table(a_annotation_text, ',', 'Y'));</pre> | 
else | <pre>else<br />  l_throws_list(i) := l_throws_list(i);</pre> | 
end | <pre>end if;</pre> | 
end | <pre>    end loop;</pre> | 
 | <pre>    <br />    l_throws_list := ut_utils.filter_list( ut_utils.trim_list_elements(l_throws_list), l_regexp_for_excep_nums);</pre> | 
end | <pre>    end loop;</pre> | 
return | <pre>    return l_exception_number_list;</pre> | 
begin | <pre>  begin<br />    a_list := ut_integer_list();</pre> | 
 | <pre>    l_annotation_pos := a_throws_ann_text.first;</pre> | 
 | <pre>l_annotation_pos := a_throws_ann_text.next(l_annotation_pos);</pre> | 
end | <pre>    end loop;</pre> | 
end | <pre>end if;</pre> | 
begin | <pre>    begin<br />l_annotation_pos := a_annotation_texts.first;</pre> | 
 | <pre>  l_annotation_pos := a_annotation_texts.next( l_annotation_pos);</pre> | 
end | <pre>end loop;</pre> | 
l_line_no | <pre>    l_line_no           binary_integer;</pre> | 
 | <pre>    l_line_no := a_annotations(a_for_annotation).next( l_line_no );</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>    end if;</pre> | 
l_line_no | <pre>    l_line_no           binary_integer;</pre> | 
 | <pre>      l_line_no := a_annotations(a_for_annotation).next( l_line_no );</pre> | 
end | <pre>    end loop;</pre> | 
end | <pre>  end if;</pre> | 
end | <pre>end if;</pre> | 
l_warning | <pre>    l_warning         varchar2(32767);</pre> | 
l_line_no | <pre>    l_line_no           binary_integer;</pre> | 
begin | <pre>  begin<br />    l_annotation_name := a_proc_annotations.first;</pre> | 
 | <pre>    l_line_no := a_proc_annotations(l_annotation_name).next(l_line_no);</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>end if;</pre> | 
 | <pre>l_annotation_name := a_proc_annotations.next(l_annotation_name);</pre> | 
end | <pre>    end loop;</pre> | 
l_annotation_texts | <pre>    l_annotation_texts tt_annotation_texts;</pre> | 
l_annotation_pos | <pre>    l_annotation_pos   binary_integer;</pre> | 
begin | <pre>  begin<br />    l_test := ut_test(a_suite.object_owner, a_suite.object_name, a_procedure_name);</pre> | 
else | <pre>    else<br />l_test.description := a_annotations(gc_test)(a_annotations(gc_test).first);</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>    end if;</pre> | 
l_context | <pre>    l_context   ut_logical_suite;</pre> | 
end | <pre>  end if;</pre> | 
end | <pre>end loop;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>    end if;</pre> | 
begin | <pre>  begin<br />    a_before_each_list := ut_executables();</pre> | 
 | <pre>    a_after_each_list := ut_executables();</pre> | 
 | <pre>    l_position := a_annotations.first;</pre> | 
end | <pre>end if;</pre> | 
 | <pre>l_position := a_annotations.next( l_position);</pre> | 
end | <pre>    end loop;</pre> | 
l_after_each_list | <pre>    l_after_each_list    ut_executables;</pre> | 
l_rollback_type | <pre>    l_rollback_type      ut_utils.t_rollback_type;</pre> | 
l_annotation_text | <pre>    l_annotation_text    varchar2(32767);</pre> | 
l_object_name | <pre>    l_object_name        t_object_name;</pre> | 
else | <pre>    else<br />l_object_name := a_suite.object_name;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>  end if;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>    end if;</pre> | 
l_end_context_pos | <pre>    l_end_context_pos    t_annotation_position;</pre> | 
l_package_ann_index | <pre>    l_package_ann_index  tt_annotations_index;</pre> | 
l_annotations | <pre>    l_annotations        tt_package_annotations;</pre> | 
l_suite | <pre>    l_suite              ut_suite;</pre> | 
l_context_no | <pre>    l_context_no         binary_integer := 1;</pre> | 
 | <pre>    l_result := a_package_ann_index(gc_endcontext).next(l_result);</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>end if;</pre> | 
return | <pre>return l_result;</pre> | 
l_position | <pre>l_position           t_annotation_position;</pre> | 
begin | <pre>    begin<br />l_position := a_context_pos;</pre> | 
 | <pre>  l_position := a_annotations.next(l_position);</pre> | 
end | <pre>end loop;</pre> | 
return | <pre>return l_annotations;</pre> | 
end | <pre>    end if;</pre> | 
 | <pre>    l_context_pos := a_package_ann_index(gc_context).first;</pre> | 
end | <pre>end if;</pre> | 
 | <pre>l_annotations       := get_annotations_in_context(a_annotations, l_context_pos, l_end_context_pos);</pre> | 
 | <pre>l_package_ann_index := build_annotation_index(l_annotations);</pre> | 
 | <pre>l_suite := ut_suite(a_suite.object_owner, a_suite.object_name, gc_context||'_'||l_context_no);</pre> | 
else | <pre>else<br />  l_context_pos := null;</pre> | 
end | <pre>end if;</pre> | 
 | <pre>l_context_no := l_context_no + 1;</pre> | 
end | <pre>    end loop;</pre> | 
 | <pre>    l_annotation_pos := a_package_ann_index(gc_context).next(l_annotation_pos);</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>end if;</pre> | 
 | <pre>    l_annotation_pos := a_package_ann_index(gc_endcontext).next(l_annotation_pos);</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>end if;</pre> | 
l_package_ann_index | <pre>    l_package_ann_index tt_annotations_index;</pre> | 
l_suite | <pre>    l_suite              ut_suite;</pre> | 
begin | <pre>  begin<br />    l_package_ann_index   := build_annotation_index(l_annotations);</pre> | 
end | <pre>    end if;</pre> | 
return | <pre>    return l_suite;</pre> | 
end | <pre>  end create_suite;</pre> | 
l_suite_path | <pre>    l_suite_path        varchar2(4000 char);</pre> | 
l_parent_path | <pre>    l_parent_path       varchar2(4000 char);</pre> | 
l_name | <pre>    l_name              varchar2(4000 char);</pre> | 
l_suites_by_path | <pre>    l_suites_by_path    tt_schema_suites;</pre> | 
begin | <pre>  begin<br />    l_suites_by_path := a_suites_by_path;</pre> | 
 | <pre>    l_suite_path  := l_suites_by_path.last;</pre> | 
else | <pre>  else<br />    ut_utils.debug_log('  Parent suite "'||l_parent_path||'" found in list of suites');</pre> | 
end | <pre>  end if;</pre> | 
end | <pre>end if;</pre> | 
 | <pre>l_suite_path := l_suites_by_path.prior(l_suite_path);</pre> | 
end | <pre>    end loop;</pre> | 
return | <pre>    return l_result;</pre> | 
l_annotated_objects | <pre>    l_annotated_objects ut_annotated_objects;</pre> | 
l_all_suites | <pre>    l_all_suites        tt_schema_suites;</pre> | 
l_result | <pre>    l_result            t_schema_suites_info;</pre> | 
begin | <pre>  begin<br />    fetch a_annotated_objects bulk collect into l_annotated_objects;</pre> | 
close | <pre>    close a_annotated_objects;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>    end loop;</pre> | 
return | <pre>    return l_result;</pre> | 
return | <pre>    return build_suites(l_annotations_cursor);</pre> | 
end | <pre>end ut_suite_builder;</pre> | 



## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
 | <pre>l_throws_list := ut_utils.trim_list_elements(ut_utils.string_to_table(a_annotation_text, ',', 'Y'));</pre> | 
else | <pre>else<br />  l_throws_list(i) := l_throws_list(i);</pre> | 
end | <pre>end if;</pre> | 
end | <pre>    end loop;</pre> | 
 | <pre>    <br />    l_throws_list := ut_utils.filter_list( ut_utils.trim_list_elements(l_throws_list), l_regexp_for_excep_nums);</pre> | 
end | <pre>    end loop;</pre> | 
return | <pre>    return l_exception_number_list;</pre> | 
begin | <pre>  begin<br />    a_list := ut_integer_list();</pre> | 
 | <pre>    l_annotation_pos := a_throws_ann_text.first;</pre> | 
 | <pre>l_annotation_pos := a_throws_ann_text.next(l_annotation_pos);</pre> | 
end | <pre>    end loop;</pre> | 
end | <pre>end if;</pre> | 
begin | <pre>    begin<br />l_annotation_pos := a_annotation_texts.first;</pre> | 
 | <pre>  l_annotation_pos := a_annotation_texts.next( l_annotation_pos);</pre> | 
end | <pre>end loop;</pre> | 
l_line_no | <pre>    l_line_no           binary_integer;</pre> | 
 | <pre>    l_line_no := a_annotations(a_for_annotation).next( l_line_no );</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>    end if;</pre> | 
l_line_no | <pre>    l_line_no           binary_integer;</pre> | 
 | <pre>      l_line_no := a_annotations(a_for_annotation).next( l_line_no );</pre> | 
end | <pre>    end loop;</pre> | 
end | <pre>  end if;</pre> | 
end | <pre>end if;</pre> | 
l_warning | <pre>    l_warning         varchar2(32767);</pre> | 
l_line_no | <pre>    l_line_no           binary_integer;</pre> | 
begin | <pre>  begin<br />    l_annotation_name := a_proc_annotations.first;</pre> | 
 | <pre>    l_line_no := a_proc_annotations(l_annotation_name).next(l_line_no);</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>end if;</pre> | 
 | <pre>l_annotation_name := a_proc_annotations.next(l_annotation_name);</pre> | 
end | <pre>    end loop;</pre> | 
l_annotation_texts | <pre>    l_annotation_texts tt_annotation_texts;</pre> | 
l_annotation_pos | <pre>    l_annotation_pos   binary_integer;</pre> | 
begin | <pre>  begin<br />    l_test := ut_test(a_suite.object_owner, a_suite.object_name, a_procedure_name);</pre> | 
else | <pre>    else<br />l_test.description := a_annotations(gc_test)(a_annotations(gc_test).first);</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>    end if;</pre> | 
l_context | <pre>    l_context   ut_logical_suite;</pre> | 
end | <pre>  end if;</pre> | 
end | <pre>end loop;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>    end if;</pre> | 
begin | <pre>  begin<br />    a_before_each_list := ut_executables();</pre> | 
 | <pre>    a_after_each_list := ut_executables();</pre> | 
 | <pre>    l_position := a_annotations.first;</pre> | 
end | <pre>end if;</pre> | 
 | <pre>l_position := a_annotations.next( l_position);</pre> | 
end | <pre>    end loop;</pre> | 
l_after_each_list | <pre>    l_after_each_list    ut_executables;</pre> | 
l_rollback_type | <pre>    l_rollback_type      ut_utils.t_rollback_type;</pre> | 
l_annotation_text | <pre>    l_annotation_text    varchar2(32767);</pre> | 
l_object_name | <pre>    l_object_name        t_object_name;</pre> | 
else | <pre>    else<br />l_object_name := a_suite.object_name;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>  end if;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>    end if;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>    end if;</pre> | 
l_end_context_pos | <pre>    l_end_context_pos    t_annotation_position;</pre> | 
l_package_ann_index | <pre>    l_package_ann_index  tt_annotations_index;</pre> | 
l_annotations | <pre>    l_annotations        tt_package_annotations;</pre> | 
l_suite | <pre>    l_suite              ut_suite;</pre> | 
l_context_no | <pre>    l_context_no         binary_integer := 1;</pre> | 
 | <pre>    l_result := a_package_ann_index(gc_endcontext).next(l_result);</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>end if;</pre> | 
return | <pre>return l_result;</pre> | 
l_position | <pre>l_position           t_annotation_position;</pre> | 
begin | <pre>    begin<br />l_position := a_context_pos;</pre> | 
 | <pre>  l_position := a_annotations.next(l_position);</pre> | 
end | <pre>end loop;</pre> | 
return | <pre>return l_annotations;</pre> | 
end | <pre>    end if;</pre> | 
 | <pre>    l_context_pos := a_package_ann_index(gc_context).first;</pre> | 
end | <pre>end if;</pre> | 
 | <pre>l_annotations       := get_annotations_in_context(a_annotations, l_context_pos, l_end_context_pos);</pre> | 
 | <pre>l_package_ann_index := build_annotation_index(l_annotations);</pre> | 
 | <pre>l_suite := ut_suite(a_suite.object_owner, a_suite.object_name, gc_context||'_'||l_context_no);</pre> | 
else | <pre>else<br />  l_context_pos := null;</pre> | 
end | <pre>end if;</pre> | 
 | <pre>l_context_no := l_context_no + 1;</pre> | 
end | <pre>    end loop;</pre> | 
 | <pre>    l_annotation_pos := a_package_ann_index(gc_context).next(l_annotation_pos);</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>end if;</pre> | 
 | <pre>    l_annotation_pos := a_package_ann_index(gc_endcontext).next(l_annotation_pos);</pre> | 
end | <pre>  end loop;</pre> | 
end | <pre>end if;</pre> | 
l_package_ann_index | <pre>    l_package_ann_index tt_annotations_index;</pre> | 
l_suite | <pre>    l_suite              ut_suite;</pre> | 
begin | <pre>  begin<br />    l_package_ann_index   := build_annotation_index(l_annotations);</pre> | 
end | <pre>    end if;</pre> | 
return | <pre>    return l_suite;</pre> | 
end | <pre>  end create_suite;</pre> | 
l_suite_path | <pre>    l_suite_path        varchar2(4000 char);</pre> | 
l_parent_path | <pre>    l_parent_path       varchar2(4000 char);</pre> | 
l_name | <pre>    l_name              varchar2(4000 char);</pre> | 
l_suites_by_path | <pre>    l_suites_by_path    tt_schema_suites;</pre> | 
begin | <pre>  begin<br />    l_suites_by_path := a_suites_by_path;</pre> | 
 | <pre>    l_suite_path  := l_suites_by_path.last;</pre> | 
else | <pre>  else<br />    ut_utils.debug_log('  Parent suite "'||l_parent_path||'" found in list of suites');</pre> | 
end | <pre>  end if;</pre> | 
end | <pre>end if;</pre> | 
 | <pre>l_suite_path := l_suites_by_path.prior(l_suite_path);</pre> | 
end | <pre>    end loop;</pre> | 
return | <pre>    return l_result;</pre> | 
l_annotated_objects | <pre>    l_annotated_objects ut_annotated_objects;</pre> | 
l_all_suites | <pre>    l_all_suites        tt_schema_suites;</pre> | 
l_result | <pre>    l_result            t_schema_suites_info;</pre> | 
begin | <pre>  begin<br />    fetch a_annotated_objects bulk collect into l_annotated_objects;</pre> | 
close | <pre>    close a_annotated_objects;</pre> | 
end | <pre>end if;</pre> | 
end | <pre>    end loop;</pre> | 
return | <pre>    return l_result;</pre> | 
return | <pre>    return build_suites(l_annotations_cursor);</pre> | 
end | <pre>end ut_suite_builder;</pre> | 




 
## BUILD_SCHEMA_SUITES Function<a name="build_schema_suites"></a>


<p>
<p>Builds set of hierarchical suites for a given schema</p>
</p>

### Syntax
```plsql
function build_schema_suites(a_owner_name varchar2) return t_schema_suites_info
```

### Parameters
Name | Description
--- | ---
`a_owner_name` | name of the schema to builds suites for
*return* | list of suites organized into hierarchy
 
 





 
## BUILD_SUITES Function<a name="build_suites"></a>


<p>
<p>Builds set of hierarchical suites for given annotations</p>
</p>

### Syntax
```plsql
function build_suites(a_annotated_objects sys_refcursor) return t_schema_suites_info
```

### Parameters
Name | Description
--- | ---
`a_annotated_objects` | cursor returning ut_annotated_object type
*return* | list of suites organized into hierarchy
 
 





 
