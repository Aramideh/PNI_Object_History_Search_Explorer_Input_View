# PNI_Object_History_Search_Explorer_Input_View

## Exploer Input View To Search Object History In PNI Application


### Introduction


In PNI Application's Object Editors, there is a action button named "Object History", which shows the history of the object currently in the editor manager. This modules helps you search for objects manipulated in the design manager environment.

![](https://github.com/Aramideh/PNI_Object_History_Search_Explorer_Input_View/blob/main/resources/Object_History_Search.png.png)




### Getting Started


* 1: Add below code to the explorer_model_config.xml of the Application
```
		<plugin name="pni_explorer_search_history_model"  class_name="pni_explorer_search_history_model" />
```
	
	
* 2: Add below code to the pni_explorer_config.xml of the Application
```	

	<plugin name="explorer_search_history_input" class_name="pni_explorer_search_history_input_view">
	   <properties>
			<property name="pni_explorer_search_history_model" value="pni_explorer_search_history_model"/>
			<property name="group_by_date?" value="false"/>
			<property name="group_by_users?" value="false"/>
        </properties>
	</plugin>	

     <plugin name="explorer_input_plugin"  class_name="explorer_input_plugin">
       <plugin_data>
          <handle plugin_name="explorer_search_input"/>
          <handle plugin_name="explorer_navigation_input" default="yes"/>
			<!-- Change Started -->
		   <handle plugin_name="explorer_search_history_input"/>
		   <!-- Change Ended -->			  
       </plugin_data>
     </plugin>

```
 Please query your application's config.xml file for more information on the explorer plugin configuration file locations

* 3: Load the module
* 4: Start the application


### Author Notes

 * This modules is tested on Smallworld 4.3 and 5.1.9 

### Authors
* [**Sadeq Aramideh**](https://github.com/Aramideh)


