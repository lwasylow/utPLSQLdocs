# UT_ANNOTATION_PARSER






- [PARSE_OBJECT_ANNOTATIONS Function](#parse_object_annotations)
- [PARSE_OBJECT_ANNOTATIONS-1 Function](#parse_object_annotations-1)












 
## PARSE_OBJECT_ANNOTATIONS Function<a name="parse_object_annotations"></a>


<p>
<p>Runs the source lines through dbms_preprocessor to remove lines that were not compiled (conditional compilation)<br />Parses the processed source code and converts it to annotations</p>
</p>

### Syntax
```plsql
function parse_object_annotations(a_source_lines dbms_preprocessor.source_lines_t) return ut_annotations
```

### Parameters
Name | Description
--- | ---
`a_source_lines` | ordered lines of source code to be parsed
*return* | array containing annotations
 
 





 
