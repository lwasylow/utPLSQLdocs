# UT_COVERAGE_HELPER


- [Data Types](#types)





## Types<a name="types"></a>

Name | Code | Description
--- | --- | ---
t_proftab_row | <pre>type t_proftab_row is record (<br />    line  binary_integer,<br />    calls number(38,0)<br />  );</pre> | 
t_proftab_rows | <pre>  <br />type t_proftab_rows is table of t_proftab_row;</pre> | 
t_block_row | <pre>type t_block_row is record(<br />     line           binary_integer<br />    ,blocks         binary_integer<br />    ,covered_blocks binary_integer);</pre> | 
t_block_rows | <pre>type t_block_rows is table of t_block_row;</pre> | 










 
