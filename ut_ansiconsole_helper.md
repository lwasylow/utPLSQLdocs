# UT_ANSICONSOLE_HELPER



- [Constants](#constants)



- [COLOR_ENABLED Procedure](#color_enabled)





## Constants<a name="constants"></a>

Name | Code | Description
--- | --- | ---
gc_red | <pre>gc_red     constant varchar2(7) := chr(27) || '[31m';</pre> | 
gc_green | <pre>gc_green   constant varchar2(7) := chr(27) || '[32m';</pre> | 
gc_yellow | <pre>gc_yellow  constant varchar2(7) := chr(27) || '[33m';</pre> | 
gc_blue | <pre>gc_blue    constant varchar2(7) := chr(27) || '[34m';</pre> | 
gc_magenta | <pre>gc_magenta constant varchar2(7) := chr(27) || '[35m';</pre> | 
gc_cyan | <pre>gc_cyan    constant varchar2(7) := chr(27) || '[36m';</pre> | 
gc_reset | <pre>gc_reset   constant varchar2(7) := chr(27) || '[0m';</pre> | 






 
## COLOR_ENABLED Procedure<a name="color_enabled"></a>


<p>
<p>utPLSQL - Version 3<br />  Copyright 2016 - 2017 utPLSQL Project</p><p>  Licensed under the Apache License, Version 2.0 (the &quot;License&quot;):<br />  you may not use this file except in compliance with the License.<br />  You may obtain a copy of the License at</p><pre><code>  http://www.apache.org/licenses/LICENSE-2.0</code></pre><p>  Unless required by applicable law or agreed to in writing, software<br />  distributed under the License is distributed on an &quot;AS IS&quot; BASIS,<br />  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.<br />  See the License for the specific language governing permissions and<br />  limitations under the License.</p>
</p>

### Syntax
```plsql
procedure color_enabled(a_enabled boolean)
```

 





 
