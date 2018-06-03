# UT_ANNOTATION_CACHE_MANAGER






- [UPDATE_CACHE Procedure](#update_cache)
- [GET_ANNOTATIONS_FOR_OBJECTS Function](#get_annotations_for_objects)
- [CLEANUP_CACHE Procedure](#cleanup_cache)
- [PURGE_CACHE Procedure](#purge_cache)












 
## UPDATE_CACHE Procedure<a name="update_cache"></a>


<p>
<p>utPLSQL - Version 3<br />  Copyright 2016 - 2017 utPLSQL Project</p><p>  Licensed under the Apache License, Version 2.0 (the &quot;License&quot;):<br />  you may not use this file except in compliance with the License.<br />  You may obtain a copy of the License at</p><pre><code>  http://www.apache.org/licenses/LICENSE-2.0</code></pre><p>  Unless required by applicable law or agreed to in writing, software<br />  distributed under the License is distributed on an &quot;AS IS&quot; BASIS,<br />  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.<br />  See the License for the specific language governing permissions and<br />  limitations under the License.</p>
</p>

### Syntax
```plsql
procedure update_cache(a_object ut_annotated_object)
```

 





 
## GET_ANNOTATIONS_FOR_OBJECTS Function<a name="get_annotations_for_objects"></a>


<p>
<p>Returns a ref_cursor containing <code>ut_annotated_object</code> as result<br />Range of data returned is limited by the input collection o cache object info</p>
</p>

### Syntax
```plsql
function get_annotations_for_objects(a_cached_objects ut_annotation_objs_cache_info) return sys_refcursor
```

### Parameters
Name | Description
--- | ---
`a_cached_objects` | a <code>ut_annotation_objs_cache_info</code> list with information about objects to get from cache
 
 





 
## CLEANUP_CACHE Procedure<a name="cleanup_cache"></a>


<p>
<p>Removes cached information about annotations for objects on the list and updates parse_time in cache info table.</p>
</p>

### Syntax
```plsql
procedure cleanup_cache(a_objects ut_annotation_objs_cache_info)
```

### Parameters
Name | Description
--- | ---
`a_objects` | a <code>ut_annotation_objs_cache_info</code> list with information about objects to remove from cache
 
 





 
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
 
 





 
