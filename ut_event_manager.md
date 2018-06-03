# UT_EVENT_MANAGER


- [Data Types](#types)





## Types<a name="types"></a>

Name | Code | Description
--- | --- | ---
t_listeners | <pre>type t_listeners is table of ut_event_listener;</pre> | 
t_listener_number | <pre>subtype t_listener_number is binary_integer;</pre> | 
t_listener_numbers | <pre>type t_listener_numbers is table of boolean index by t_listener_number;</pre> | 
t_events_listeners | <pre>type t_events_listeners is table of t_listener_numbers index by t_event_name;</pre> | 
t_event_name | <pre>subtype t_event_name           is varchar2(250);</pre> | 










 
