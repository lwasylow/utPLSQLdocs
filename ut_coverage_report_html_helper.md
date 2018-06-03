# UT_COVERAGE_REPORT_HTML_HELPER



- [Constants](#constants)



- [GET_INDEX Function](#get_index)
- [GET_DEFAULT_HTML_ASSETS_PATH Function](#get_default_html_assets_path)





## Constants<a name="constants"></a>

Name | Code | Description
--- | --- | ---
gc_green_coverage_pct | <pre>gc_green_coverage_pct  constant integer := 90;</pre> | 
gc_yellow_coverage_pct | <pre>gc_yellow_coverage_pct constant integer := 80;</pre> | 
gc_green_css | <pre>gc_green_css  constant varchar2(10) := 'green';</pre> | 
gc_yellow_css | <pre>gc_yellow_css constant varchar2(10) := 'yellow';</pre> | 
gc_red_css | <pre>gc_red_css    constant varchar2(10) := 'red';</pre> | 
gc_missed | <pre>gc_missed      constant varchar2(7) := 'missed';</pre> | 
gc_skipped | <pre>gc_skipped     constant varchar2(7) := 'skipped';</pre> | 
gc_disabled | <pre>gc_disabled    constant varchar2(7) := 'never';</pre> | 
gc_covered | <pre>gc_covered     constant varchar2(7) := 'covered';</pre> | 
gc_partcovered | <pre>gc_partcovered constant varchar2(7) := 'partcov';</pre> | 






 
## GET_INDEX Function<a name="get_index"></a>


<p>
<p>public definitions</p>
</p>

### Syntax
```plsql
function get_index(a_coverage_data ut_coverage.t_coverage, a_assets_path varchar2, a_project_name varchar2 := null, a_command_line varchar2 := null)
  return clob
```

 





 
## GET_DEFAULT_HTML_ASSETS_PATH Function<a name="get_default_html_assets_path"></a>


<p>
<p>utPLSQL - Version 3<br />  Copyright 2016 - 2017 utPLSQL Project</p><p>  Licensed under the Apache License, Version 2.0 (the &quot;License&quot;):<br />  you may not use this file except in compliance with the License.<br />  You may obtain a copy of the License at</p><pre><code>  http://www.apache.org/licenses/LICENSE-2.0</code></pre><p>  Unless required by applicable law or agreed to in writing, software<br />  distributed under the License is distributed on an &quot;AS IS&quot; BASIS,<br />  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.<br />  See the License for the specific language governing permissions and<br />  limitations under the License.</p>
</p>

### Syntax
```plsql
function get_default_html_assets_path return varchar2 deterministic
```

 





 
