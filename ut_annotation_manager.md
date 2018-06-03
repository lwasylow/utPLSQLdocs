# UT_ANNOTATION_MANAGER






- [GET_ANNOTATED_OBJECTS Function](#get_annotated_objects)
- [REBUILD_ANNOTATION_CACHE Procedure](#rebuild_annotation_cache)
- [PURGE_CACHE Procedure](#purge_cache)












 
## GET_ANNOTATED_OBJECTS Function<a name="get_annotated_objects"></a>


<p>
<p>Gets annotations for all objects of a specified type for database schema.<br />Annotations that are stale or missing are parsed and placed in persistent cache.<br />After placing in cache, annotation data is returned as pipelined table data.</p>
</p>

### Syntax
```plsql
function get_annotated_objects(a_object_owner varchar2, a_object_type varchar2) return ut_annotated_objects pipelined
```

### Parameters
Name | Description
--- | ---
`a_object_owner` | owner of objects to get annotations for
`a_object_type` | type of objects to get annotations for
*return* | array containing annotated objects along with annotations for each object (nested)
 
 





 
## REBUILD_ANNOTATION_CACHE Procedure<a name="rebuild_annotation_cache"></a>


<p>
<p>Rebuilds annotation cache for a specified schema and object type.<br /> The procedure is called internally by <code>get_annotated_objects</code> function.<br /> It can be used to speedup initial execution of utPLSQL on a given schema<br />  if it is executed before any call is made to <code>ut.run</code> or <code>ut_runner.run</code> procedure.</p>
</p>

### Syntax
```plsql
procedure rebuild_annotation_cache(a_object_owner varchar2, a_object_type varchar2)
```

### Parameters
Name | Description
--- | ---
`a_object_owner` | owner of objects to get annotations for
`a_object_type` | type of objects to get annotations for
 
 





 
## PURGE_CACHE Procedure<a name="purge_cache"></a>


<p>
<p>Removes cached information about annotations for objects of specified type and specified owner</p>
</p>

### Syntax
```plsql
procedure purge_cache(a_object_owner varchar2, a_object_type varchar2)
```

### Parameters
Name | Description
--- | ---
`a_object_owner` | owner of objects to purge annotations for
`a_object_type` | type of objects to purge annotations for
 
 





 
