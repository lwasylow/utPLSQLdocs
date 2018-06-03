# UT_COVERAGE_HTML_REPORTER




- [Variables](#variables)

- [Exceptions](#exceptions)




## Variables<a name="variables"></a>

Name | Code | Description
--- | --- | ---
 | <pre>  assets_path := nvl(a_html_report_assets_path, ut_coverage_report_html_helper.get_default_html_assets_path());</pre> | 
l_coverage_data | <pre>  l_coverage_data ut_coverage.t_coverage;</pre> | 
begin | <pre>begin<br />  ut_coverage.coverage_stop();</pre> | 
 | <pre>  l_coverage_data := ut_coverage.get_coverage_data(a_run.coverage_options);</pre> | 



## Exceptions<a name="exceptions"></a>

Name | Code | Description
--- | --- | ---
 | <pre>  assets_path := nvl(a_html_report_assets_path, ut_coverage_report_html_helper.get_default_html_assets_path());</pre> | 
l_coverage_data | <pre>  l_coverage_data ut_coverage.t_coverage;</pre> | 
begin | <pre>begin<br />  ut_coverage.coverage_stop();</pre> | 
 | <pre>  l_coverage_data := ut_coverage.get_coverage_data(a_run.coverage_options);</pre> | 




 
