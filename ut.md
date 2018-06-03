# UT




- [Variables](#variables)

- [Exceptions](#exceptions)

- [VERSION Function](#version)
- [SET_NLS Procedure](#set_nls)
- [RESET_NLS Procedure](#reset_nls)



## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
g_nls_date_format | <pre>g_nls_date_format varchar2(4000);</pre> | 
pragma | <pre>  pragma exception_init (e_package_invalidated, -04068);</pre> | 
raise | <pre>    raise e_package_invalidated;</pre> | 
end | <pre>  end if;</pre> | 
l_paths | <pre>  l_paths     ut_varchar2_list := ut_varchar2_list(sys_context('userenv', 'current_schema'));</pre> | 
l_lines | <pre>  l_lines     sys_refcursor;</pre> | 
l_line | <pre>  l_line      varchar2(4000);</pre> | 
loop | <pre>    loop<br />      fetch l_lines into l_line;</pre> | 
exit | <pre>      exit when l_lines%notfound;</pre> | 
pipe | <pre>      pipe row(l_line);</pre> | 
end | <pre>    end loop;</pre> | 
close | <pre>    close l_lines;</pre> | 
end | <pre>  end if;</pre> | 
l_paths | <pre>  l_paths     ut_varchar2_list := ut_varchar2_list(sys_context('userenv', 'current_schema'));</pre> | 
l_lines | <pre>  l_lines     sys_refcursor;</pre> | 
l_line | <pre>  l_line      varchar2(4000);</pre> | 
loop | <pre>    loop<br />      fetch l_lines into l_line;</pre> | 
exit | <pre>      exit when l_lines%notfound;</pre> | 
pipe | <pre>      pipe row(l_line);</pre> | 
end | <pre>    end loop;</pre> | 
close | <pre>    close l_lines;</pre> | 
end | <pre>  end if;</pre> | 
l_lines | <pre>  l_lines     sys_refcursor;</pre> | 
l_line | <pre>  l_line      varchar2(4000);</pre> | 
loop | <pre>    loop<br />      fetch l_lines into l_line;</pre> | 
exit | <pre>      exit when l_lines%notfound;</pre> | 
pipe | <pre>      pipe row(l_line);</pre> | 
end | <pre>    end loop;</pre> | 
close | <pre>    close l_lines;</pre> | 
end | <pre>  end if;</pre> | 
l_lines | <pre>  l_lines     sys_refcursor;</pre> | 
l_line | <pre>  l_line      varchar2(4000);</pre> | 
loop | <pre>    loop<br />      fetch l_lines into l_line;</pre> | 
exit | <pre>      exit when l_lines%notfound;</pre> | 
pipe | <pre>      pipe row(l_line);</pre> | 
end | <pre>    end loop;</pre> | 
close | <pre>    close l_lines;</pre> | 
end | <pre>  end if;</pre> | 
l_paths | <pre>  l_paths     ut_varchar2_list := ut_varchar2_list(coalesce(a_path, sys_context('userenv', 'current_schema')));</pre> | 
l_lines | <pre>  l_lines     sys_refcursor;</pre> | 
l_line | <pre>  l_line      varchar2(4000);</pre> | 
loop | <pre>    loop<br />      fetch l_lines into l_line;</pre> | 
exit | <pre>      exit when l_lines%notfound;</pre> | 
pipe | <pre>      pipe row(l_line);</pre> | 
end | <pre>    end loop;</pre> | 
close | <pre>    close l_lines;</pre> | 
end | <pre>  end if;</pre> | 
l_paths | <pre>  l_paths     ut_varchar2_list := ut_varchar2_list(coalesce(a_path, sys_context('userenv', 'current_schema')));</pre> | 
l_lines | <pre>  l_lines     sys_refcursor;</pre> | 
l_line | <pre>  l_line      varchar2(4000);</pre> | 
loop | <pre>    loop<br />      fetch l_lines into l_line;</pre> | 
exit | <pre>      exit when l_lines%notfound;</pre> | 
pipe | <pre>      pipe row(l_line);</pre> | 
end | <pre>    end loop;</pre> | 
close | <pre>    close l_lines;</pre> | 
end | <pre>  end if;</pre> | 
end | <pre>  end if;</pre> | 
end | <pre>  end if;</pre> | 
end | <pre>  end if;</pre> | 
execute | <pre>  execute immediate 'alter session set nls_date_format = '''||ut_utils.gc_date_format||'''';</pre> | 
end | <pre>  end if;</pre> | 
 | <pre>  g_nls_date_format := null;</pre> | 
end | <pre>end ut;</pre> | 



## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
g_nls_date_format | <pre>g_nls_date_format varchar2(4000);</pre> | 
pragma | <pre>  pragma exception_init (e_package_invalidated, -04068);</pre> | 
raise | <pre>    raise e_package_invalidated;</pre> | 
end | <pre>  end if;</pre> | 
l_paths | <pre>  l_paths     ut_varchar2_list := ut_varchar2_list(sys_context('userenv', 'current_schema'));</pre> | 
l_lines | <pre>  l_lines     sys_refcursor;</pre> | 
l_line | <pre>  l_line      varchar2(4000);</pre> | 
loop | <pre>    loop<br />      fetch l_lines into l_line;</pre> | 
exit | <pre>      exit when l_lines%notfound;</pre> | 
pipe | <pre>      pipe row(l_line);</pre> | 
end | <pre>    end loop;</pre> | 
close | <pre>    close l_lines;</pre> | 
end | <pre>  end if;</pre> | 
l_paths | <pre>  l_paths     ut_varchar2_list := ut_varchar2_list(sys_context('userenv', 'current_schema'));</pre> | 
l_lines | <pre>  l_lines     sys_refcursor;</pre> | 
l_line | <pre>  l_line      varchar2(4000);</pre> | 
loop | <pre>    loop<br />      fetch l_lines into l_line;</pre> | 
exit | <pre>      exit when l_lines%notfound;</pre> | 
pipe | <pre>      pipe row(l_line);</pre> | 
end | <pre>    end loop;</pre> | 
close | <pre>    close l_lines;</pre> | 
end | <pre>  end if;</pre> | 
l_lines | <pre>  l_lines     sys_refcursor;</pre> | 
l_line | <pre>  l_line      varchar2(4000);</pre> | 
loop | <pre>    loop<br />      fetch l_lines into l_line;</pre> | 
exit | <pre>      exit when l_lines%notfound;</pre> | 
pipe | <pre>      pipe row(l_line);</pre> | 
end | <pre>    end loop;</pre> | 
close | <pre>    close l_lines;</pre> | 
end | <pre>  end if;</pre> | 
l_lines | <pre>  l_lines     sys_refcursor;</pre> | 
l_line | <pre>  l_line      varchar2(4000);</pre> | 
loop | <pre>    loop<br />      fetch l_lines into l_line;</pre> | 
exit | <pre>      exit when l_lines%notfound;</pre> | 
pipe | <pre>      pipe row(l_line);</pre> | 
end | <pre>    end loop;</pre> | 
close | <pre>    close l_lines;</pre> | 
end | <pre>  end if;</pre> | 
l_paths | <pre>  l_paths     ut_varchar2_list := ut_varchar2_list(coalesce(a_path, sys_context('userenv', 'current_schema')));</pre> | 
l_lines | <pre>  l_lines     sys_refcursor;</pre> | 
l_line | <pre>  l_line      varchar2(4000);</pre> | 
loop | <pre>    loop<br />      fetch l_lines into l_line;</pre> | 
exit | <pre>      exit when l_lines%notfound;</pre> | 
pipe | <pre>      pipe row(l_line);</pre> | 
end | <pre>    end loop;</pre> | 
close | <pre>    close l_lines;</pre> | 
end | <pre>  end if;</pre> | 
l_paths | <pre>  l_paths     ut_varchar2_list := ut_varchar2_list(coalesce(a_path, sys_context('userenv', 'current_schema')));</pre> | 
l_lines | <pre>  l_lines     sys_refcursor;</pre> | 
l_line | <pre>  l_line      varchar2(4000);</pre> | 
loop | <pre>    loop<br />      fetch l_lines into l_line;</pre> | 
exit | <pre>      exit when l_lines%notfound;</pre> | 
pipe | <pre>      pipe row(l_line);</pre> | 
end | <pre>    end loop;</pre> | 
close | <pre>    close l_lines;</pre> | 
end | <pre>  end if;</pre> | 
end | <pre>  end if;</pre> | 
end | <pre>  end if;</pre> | 
end | <pre>  end if;</pre> | 
execute | <pre>  execute immediate 'alter session set nls_date_format = '''||ut_utils.gc_date_format||'''';</pre> | 
end | <pre>  end if;</pre> | 
 | <pre>  g_nls_date_format := null;</pre> | 
end | <pre>end ut;</pre> | 




 
## VERSION Function<a name="version"></a>


<p>
<p>Returns version of installed utPLSQL code</p>
</p>

### Syntax
```plsql
function version return varchar2
```

### Parameters
Name | Description
--- | ---
*return* | varchar2 VersionNumber: Version number installed in database
 
 


### Example
```plsql
select ut.version from dual;
```



 
## SET_NLS Procedure<a name="set_nls"></a>


<p>
<p>Helper procedure to set NLS session parameter for date processing in refcursor.<br />It needs to be called before refcursor is open in order to have DATE data type data in refcursor<br /> properly transformed into XML format as a date-time element.<br />If the function is not called before opening a cursor to be compared, the DATE data is compared using default NLS setting for date.</p>
</p>

### Syntax
```plsql
procedure set_nls
```

 





 
## RESET_NLS Procedure<a name="reset_nls"></a>


<p>
<p>Helper procedure to reset NLS session parameter to it&#39;s original state.<br />It needs to be called after refcursor is open in order restore the original session state and keep the NLS date setting at default.</p>
</p>

### Syntax
```plsql
procedure reset_nls
```

 





 
