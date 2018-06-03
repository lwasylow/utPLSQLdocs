# UT_TEAMCITY_REPORTER_HELPER


- [Data Types](#types)




- [TEST_SUITE_STARTED Function](#test_suite_started)

## Types<a name="types"></a>

Name | Code | Description
--- | --- | ---
t_prop_index | <pre>subtype t_prop_index is varchar2(2000 char);</pre> | 
t_props | <pre>type t_props is table of varchar2(32767) index by t_prop_index;</pre> | 










 
## TEST_SUITE_STARTED Function<a name="test_suite_started"></a>


<p>
<p>utPLSQL - Version 3<br />  Copyright 2016 - 2017 utPLSQL Project</p><p>  Licensed under the Apache License, Version 2.0 (the &quot;License&quot;):<br />  you may not use this file except in compliance with the License.<br />  You may obtain a copy of the License at</p><pre><code>  http://www.apache.org/licenses/LICENSE-2.0</code></pre><p>  Unless required by applicable law or agreed to in writing, software<br />  distributed under the License is distributed on an &quot;AS IS&quot; BASIS,<br />  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.<br />  See the License for the specific language governing permissions and<br />  limitations under the License.</p>
</p>

### Syntax
```plsql
function test_suite_started(a_suite_name varchar2, a_flow_id varchar2 default null) return varchar2
```

 





 
