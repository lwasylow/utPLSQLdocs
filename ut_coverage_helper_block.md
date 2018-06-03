# UT_COVERAGE_HELPER_BLOCK


- [Data Types](#types)




- [COVERAGE_START Procedure](#coverage_start)

## Types<a name="types"></a>

Name | Code | Description
--- | --- | ---
t_proftab_row | <pre>type t_proftab_row is record (<br />    line  binary_integer,<br />    calls number(38,0)<br />  );</pre> | 
t_proftab_rows | <pre>  <br />type t_proftab_rows is table of t_proftab_row;</pre> | 
t_block_row | <pre>type t_block_row is record(<br />     line           binary_integer<br />    ,blocks         binary_integer<br />    ,covered_blocks binary_integer);</pre> | 
t_block_rows | <pre>type t_block_rows is table of t_block_row;</pre> | 










 
## COVERAGE_START Procedure<a name="coverage_start"></a>


<p>
<p>utPLSQL - Version 3<br />  Copyright 2016 - 2017 utPLSQL Project</p><p>  Licensed under the Apache License, Version 2.0 (the &quot;License&quot;):<br />  you may not use this file except in compliance with the License.<br />  You may obtain a copy of the License at</p><pre><code>  http://www.apache.org/licenses/LICENSE-2.0</code></pre><p>  Unless required by applicable law or agreed to in writing, software<br />  distributed under the License is distributed on an &quot;AS IS&quot; BASIS,<br />  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.<br />  See the License for the specific language governing permissions and<br />  limitations under the License.</p>
</p>

### Syntax
```plsql
procedure coverage_start(a_run_comment in varchar2,a_coverage_id out integer)
```

 





 
